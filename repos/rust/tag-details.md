<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `rust`

-	[`rust:1`](#rust1)
-	[`rust:1-alpine`](#rust1-alpine)
-	[`rust:1-alpine3.18`](#rust1-alpine318)
-	[`rust:1-alpine3.19`](#rust1-alpine319)
-	[`rust:1-bookworm`](#rust1-bookworm)
-	[`rust:1-bullseye`](#rust1-bullseye)
-	[`rust:1-buster`](#rust1-buster)
-	[`rust:1-slim`](#rust1-slim)
-	[`rust:1-slim-bookworm`](#rust1-slim-bookworm)
-	[`rust:1-slim-bullseye`](#rust1-slim-bullseye)
-	[`rust:1-slim-buster`](#rust1-slim-buster)
-	[`rust:1.77`](#rust177)
-	[`rust:1.77-alpine`](#rust177-alpine)
-	[`rust:1.77-alpine3.18`](#rust177-alpine318)
-	[`rust:1.77-alpine3.19`](#rust177-alpine319)
-	[`rust:1.77-bookworm`](#rust177-bookworm)
-	[`rust:1.77-bullseye`](#rust177-bullseye)
-	[`rust:1.77-buster`](#rust177-buster)
-	[`rust:1.77-slim`](#rust177-slim)
-	[`rust:1.77-slim-bookworm`](#rust177-slim-bookworm)
-	[`rust:1.77-slim-bullseye`](#rust177-slim-bullseye)
-	[`rust:1.77-slim-buster`](#rust177-slim-buster)
-	[`rust:1.77.2`](#rust1772)
-	[`rust:1.77.2-alpine`](#rust1772-alpine)
-	[`rust:1.77.2-alpine3.18`](#rust1772-alpine318)
-	[`rust:1.77.2-alpine3.19`](#rust1772-alpine319)
-	[`rust:1.77.2-bookworm`](#rust1772-bookworm)
-	[`rust:1.77.2-bullseye`](#rust1772-bullseye)
-	[`rust:1.77.2-buster`](#rust1772-buster)
-	[`rust:1.77.2-slim`](#rust1772-slim)
-	[`rust:1.77.2-slim-bookworm`](#rust1772-slim-bookworm)
-	[`rust:1.77.2-slim-bullseye`](#rust1772-slim-bullseye)
-	[`rust:1.77.2-slim-buster`](#rust1772-slim-buster)
-	[`rust:alpine`](#rustalpine)
-	[`rust:alpine3.18`](#rustalpine318)
-	[`rust:alpine3.19`](#rustalpine319)
-	[`rust:bookworm`](#rustbookworm)
-	[`rust:bullseye`](#rustbullseye)
-	[`rust:buster`](#rustbuster)
-	[`rust:latest`](#rustlatest)
-	[`rust:slim`](#rustslim)
-	[`rust:slim-bookworm`](#rustslim-bookworm)
-	[`rust:slim-bullseye`](#rustslim-bullseye)
-	[`rust:slim-buster`](#rustslim-buster)

## `rust:1`

```console
$ docker pull rust@sha256:8824f00d57259b0b833257532b2a4ec94132d1bf00e4b36e87a56266aff3a40c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1` - linux; amd64

```console
$ docker pull rust@sha256:c5000325cce93b58cb94ed7a77c85fa8a35520e6119b10a0d3a0ccc95960cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521828909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bb4f02fb0e8300d16b98188d95219c00741eeaf7deb9be498dcd44a5076f6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c40c3e3cdf945721f480e1d939aac857876fdb5c33b8fbfcf655c63b0b9428`  
		Last Modified: Wed, 24 Apr 2024 04:21:09 GMT  
		Size: 64.1 MB (64142118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05cc1123d7e335d59b0f465c23b7ad2ad27f4875b6c3eab41c65a9b50efa382`  
		Last Modified: Wed, 24 Apr 2024 04:21:45 GMT  
		Size: 211.2 MB (211175606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803b1968af78ef789730661c289a7ec4f7df4e634c9bee1c4837346ca3f4ef27`  
		Last Modified: Wed, 24 Apr 2024 05:12:18 GMT  
		Size: 172.9 MB (172884762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:8ea2ab75a2c2b231008469686581ab02e095b9fe922c119ade3d1479d3a3cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a288afbc55e2553d0168a7df78f087461c3e1f16288ca208348ce7cc956d6732`

```dockerfile
```

-	Layers:
	-	`sha256:51b060ea2235773d7512609d22d18dc74debf609f249989b35d729c12f6aab34`  
		Last Modified: Wed, 24 Apr 2024 05:12:16 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf815ddf8eb88dfd476d46a5029e837216ec0c685187027d0aefdf4d2eafcab6`  
		Last Modified: Wed, 24 Apr 2024 05:12:15 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:02f414fb213df08e9b7333e1bc6b6197034057b124e931a621fad867f8421ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510038334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef39effc782b510f66eab7f223bcc443fe6b080f53b290010473d523bdf9f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0525f0e8022d3b0295c1e79a86a4f89704f111e1b222a81c92bc1cd11e968380`  
		Last Modified: Fri, 12 Apr 2024 10:10:51 GMT  
		Size: 208.6 MB (208612483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:bf7d1b36a17124b80128713cf3d086d5796c86dc372c6282cf498daf6c1395eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1beec69f650b1aebc630728883823a22b7d6678dd70d219c8e0a42fa58672ce`

```dockerfile
```

-	Layers:
	-	`sha256:703cb3fa1a3d5fecd4a490acbbca87494b9e3a268f01c0fcf9d5e3680d83130e`  
		Last Modified: Fri, 12 Apr 2024 10:10:47 GMT  
		Size: 15.2 MB (15176005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9869ff78ed8192003451c3741439e311265dc77f2e68f7449112268e7789237`  
		Last Modified: Fri, 12 Apr 2024 10:10:45 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3160cca3c6dda6fe0ab864a99ac7c140053d5d1eb607de1149d8ddf283291f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581324975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f4049f68d66356001e70d6436c367cca3844efe78889fcc32dc84b7c30c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03d269bebeec78b201e8b34ead41bf134d4d60a7a9487567cdf8c35741b6e6`  
		Last Modified: Thu, 11 Apr 2024 09:06:37 GMT  
		Size: 241.6 MB (241616470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:c60bcda0982aaadca0e716b39a6374a61127c1a6de578325b4dd1a522cb7ae9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb01e6329c5de88d432e822441857852f9ab3a22ddb8644d6e833d6c705ee0`

```dockerfile
```

-	Layers:
	-	`sha256:ce8cf433ca365e2b10c8bd5a4abea406fa4f9e3ac157ea49fc5512e07028b8bd`  
		Last Modified: Thu, 11 Apr 2024 09:06:32 GMT  
		Size: 15.4 MB (15398644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3621a57d1464a572d892b6cf38eb44c3744f32365aa7308fb2da4a2e713ffa1`  
		Last Modified: Thu, 11 Apr 2024 09:06:31 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:890ff0201af78ee848b18a52a4f4531488b4e59578aaceb80267d92a5a5b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538602380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dcdd8241e4fbe59faf26d535c41d723ac8d9bc7a5ffc066ce3cc3d6bcd9976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c7b4c0568972903287c2ba295779f478db7fc45d1844ec5d10e22332f4cd1d84`  
		Last Modified: Wed, 24 Apr 2024 03:43:10 GMT  
		Size: 50.6 MB (50602565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba4056eb3a537ebb74fd333c27daceac5385bc3101b6029e706a51de775f00`  
		Last Modified: Wed, 24 Apr 2024 04:41:08 GMT  
		Size: 24.9 MB (24888940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0583cb1d092e1ca2b9a9e9ad274c286cbda7804622a36572a00c3440b4d88`  
		Last Modified: Wed, 24 Apr 2024 04:41:36 GMT  
		Size: 66.0 MB (65989175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4346162f795b064031764e3d351299d91568e9a1cb9ff0ae23d323d99339d1`  
		Last Modified: Wed, 24 Apr 2024 04:42:27 GMT  
		Size: 210.1 MB (210101062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ac1055cd771ed58d7865a880ab6bdb9b418503c9c767d13f68c437558fa46b`  
		Last Modified: Wed, 24 Apr 2024 05:12:29 GMT  
		Size: 187.0 MB (187020638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:97a7f910b863aa2ed9321369136bc22e1676fa469a92973958256b086366154c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08a98dfd4d629087d8353ef923ae123298df4a8a02235b5ed9609d9911589c`

```dockerfile
```

-	Layers:
	-	`sha256:be07c0f3fc84146f8b856092f446a575df879c8175d38ad9587726f5548f7dce`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76565694008f6464d1b540c738ca7df8e8974bac84071148aef50fcdfba095c4`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 13.2 KB (13177 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:3e03cf7b5c139593ad629b57e55624da795a4e789e4826ae88a0ef68a9feed27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551593932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62106ad4d5b838965cd23e3c23325d159f7ba16e3c4a5f525a573b48831d1e4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bf47934b0700489c27f4b1918c464037353ebec2ebc12585ceea997c9a34c71c`  
		Last Modified: Wed, 24 Apr 2024 03:25:57 GMT  
		Size: 53.6 MB (53580168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677be8677970cb6c89d034144a91a8695625d82f32553778be503e17ab5f55b3`  
		Last Modified: Wed, 24 Apr 2024 04:22:57 GMT  
		Size: 25.7 MB (25699777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48162777bb1b177bfa77ee29ba9552a6c899119f959faa64ef54f0a5aab3116`  
		Last Modified: Wed, 24 Apr 2024 04:23:19 GMT  
		Size: 69.6 MB (69584472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e881f9e7d456fa7b2b9e91f26b48776888d7ca1975413e2554119bfef1024`  
		Last Modified: Wed, 24 Apr 2024 04:23:59 GMT  
		Size: 214.2 MB (214213767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1dbcd760ee8f07bc74473682877cfe356c1743a81028d53592a9a203cbfe1d`  
		Last Modified: Thu, 25 Apr 2024 09:37:45 GMT  
		Size: 188.5 MB (188515748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:55139c979bd14dda211e51a3877d62232d3d44423d7a50eccb13987f2a8fc4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028f773eef818abb6e7c12c5785e8f0bc2100c507b72b5a932ab4e3db8b15eb2`

```dockerfile
```

-	Layers:
	-	`sha256:370f05a65fe56210232e2a29f47c225fa190152fce2f2fd2173f04fd6eebe017`  
		Last Modified: Thu, 25 Apr 2024 09:37:40 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c82a7840b4a0f54d7ee75413d11f713e9e9abf3e2ac8616c18bd4b2245f37e1`  
		Last Modified: Thu, 25 Apr 2024 09:37:39 GMT  
		Size: 12.6 KB (12625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:9b74675247503eb0c3e3831dfdf10985c254b3ba9aa9a36eac8917f912a134eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:dc037af6f82e10c9862879cfe7dcbeb883b23092013b3a1df295512a4ade5d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272492183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d9a62b548d2deef025a80cbb517fcdaab56526b8cfc88d0ef4ab90b8dab39d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f170ecb6344abd22a40dfedc95278fed4a73a9409a285b6a31c6994b8097ab`  
		Last Modified: Tue, 09 Apr 2024 23:50:39 GMT  
		Size: 55.3 MB (55346790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150084451e7317de7972997b74d7d7b3a6947e9e01a1a3cd1a3b799e8348208`  
		Last Modified: Tue, 09 Apr 2024 23:50:42 GMT  
		Size: 213.7 MB (213736664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:65412a414e6e29d6f1c17de3346d8babf260891f011363110e2ef9d34763d2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e244aa001a61ab57db8fdbd3135b351cc3c55962ee776136e5af23d4b0a303ee`

```dockerfile
```

-	Layers:
	-	`sha256:4e63ddf0710f8dcc924c71396e2f3b39819922b0db63df53204e50c9b9c396a6`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 710.6 KB (710617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4861d7790f28e1d13f2037ee5c69a885431a65a224621e3a0915312ccd1038`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 11.8 KB (11792 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d30747064955669d4e48ece7dc69776bf05abe2ffa4eb866314bc842f9231936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278817954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd976a496d7d864344a2b39dad2155dbb9ef5d526f06ac412d4a3e2a37cb0be1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651ca114e522c42e6bb17953edf4a18bba82fe2287f93e32f6b3957ff901c2`  
		Last Modified: Sat, 16 Mar 2024 17:12:47 GMT  
		Size: 53.0 MB (52970287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157aaa1f3fa9784926886cafbadb1c30dcd160078deb54be2c6a6b7452ba670`  
		Last Modified: Wed, 10 Apr 2024 00:03:58 GMT  
		Size: 222.5 MB (222499952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:07fcac075e46cdcd0b7ad2a6c17d6d167910b8b9e827ccef0d73092dd6f12499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.2 KB (753242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f9b404804f7716cd3fce2e04dae7f19c8620b407f12a708e1f3f9cd944f9e`

```dockerfile
```

-	Layers:
	-	`sha256:4c6e25bf8fa604c97f277fd247f3614d3c6a8a1844f4cb78b3c466115463a60c`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 741.6 KB (741598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233de60c24dbdbc3fdcb9f32aba1af2eea5604c7ded084a880fb98dabaa39275`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 11.6 KB (11644 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.18`

```console
$ docker pull rust@sha256:b8f4f707c6460f4228deecdcc4acdfc50045fa7396f8aec732dc4ea322a41066
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:f5762f07bc2d9d6699afb162b7f35dfa48e5945cf4395b4f9b9d6826cb1d3c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268673214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d5e3a7dd699641a0c6368e65fad736d7c583359096663c1e4bf5e98b85d5a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f914773acc6db8be08970614a0ed0f5fce71828723bfcb6e6cf1d97a26c284eb`  
		Last Modified: Tue, 09 Apr 2024 23:50:41 GMT  
		Size: 51.5 MB (51534043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0af00c163854d8ec5ea9d8a150960293bfd4aa34804a7a160ef80f44ce71d`  
		Last Modified: Tue, 09 Apr 2024 23:50:44 GMT  
		Size: 213.7 MB (213736629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:9bfd12461323300ebd4c975ebc91a40d5949fa914272a2abe34315cac6c58c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49a20d1e055b2d8dcd9f1dc20fe467a5b977e5e797847f63adebc0d7732c718`

```dockerfile
```

-	Layers:
	-	`sha256:d549196acdb3131a3a009a32ec149198450da016167ecb17316ed5105a440284`  
		Last Modified: Tue, 09 Apr 2024 23:50:40 GMT  
		Size: 701.9 KB (701886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff0d60c39141b47c8ebf94551e1235d461f65e03b68df4a8ae19688754cc60b`  
		Last Modified: Tue, 09 Apr 2024 23:50:40 GMT  
		Size: 10.6 KB (10588 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3a178840b556deece46aeea0e6f3029a9bf525530b5eba1f6037531c098947a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271899543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78a508d74d054080dc4bcea6dc7bd9819bd806d6bfd06910138e6c94e384e19`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b1cd0d662b55abd28904427ae8befdb37b765cf7ff19dc4a587c51429117c7`  
		Last Modified: Sat, 16 Mar 2024 17:11:39 GMT  
		Size: 46.1 MB (46066359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a88ea76700e9b87c7238a55b12f22030ed622804d3c18cd00497bbf3d9760d`  
		Last Modified: Wed, 10 Apr 2024 00:02:53 GMT  
		Size: 222.5 MB (222499823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:bf2d6cdc43bc8c6f6942a7e2a4eec7dd93b4f8a2e51b5cdee8f402c636b252d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.2 KB (747167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd7d1515764e16148a0a685fa2c88831a6e8bae26f370009e24a37eb15c52f1`

```dockerfile
```

-	Layers:
	-	`sha256:817ff20e322fc42973b1489c74c9d5e24420023ac7706158646e0c8187ea53d9`  
		Last Modified: Wed, 10 Apr 2024 00:02:48 GMT  
		Size: 736.7 KB (736735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff708420c480e2a3ada601eacf662d093335bbf3c2b624e814c55dd24d3d368`  
		Last Modified: Wed, 10 Apr 2024 00:02:48 GMT  
		Size: 10.4 KB (10432 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:9b74675247503eb0c3e3831dfdf10985c254b3ba9aa9a36eac8917f912a134eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:dc037af6f82e10c9862879cfe7dcbeb883b23092013b3a1df295512a4ade5d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272492183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d9a62b548d2deef025a80cbb517fcdaab56526b8cfc88d0ef4ab90b8dab39d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f170ecb6344abd22a40dfedc95278fed4a73a9409a285b6a31c6994b8097ab`  
		Last Modified: Tue, 09 Apr 2024 23:50:39 GMT  
		Size: 55.3 MB (55346790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150084451e7317de7972997b74d7d7b3a6947e9e01a1a3cd1a3b799e8348208`  
		Last Modified: Tue, 09 Apr 2024 23:50:42 GMT  
		Size: 213.7 MB (213736664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:65412a414e6e29d6f1c17de3346d8babf260891f011363110e2ef9d34763d2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e244aa001a61ab57db8fdbd3135b351cc3c55962ee776136e5af23d4b0a303ee`

```dockerfile
```

-	Layers:
	-	`sha256:4e63ddf0710f8dcc924c71396e2f3b39819922b0db63df53204e50c9b9c396a6`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 710.6 KB (710617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4861d7790f28e1d13f2037ee5c69a885431a65a224621e3a0915312ccd1038`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 11.8 KB (11792 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d30747064955669d4e48ece7dc69776bf05abe2ffa4eb866314bc842f9231936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278817954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd976a496d7d864344a2b39dad2155dbb9ef5d526f06ac412d4a3e2a37cb0be1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651ca114e522c42e6bb17953edf4a18bba82fe2287f93e32f6b3957ff901c2`  
		Last Modified: Sat, 16 Mar 2024 17:12:47 GMT  
		Size: 53.0 MB (52970287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157aaa1f3fa9784926886cafbadb1c30dcd160078deb54be2c6a6b7452ba670`  
		Last Modified: Wed, 10 Apr 2024 00:03:58 GMT  
		Size: 222.5 MB (222499952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:07fcac075e46cdcd0b7ad2a6c17d6d167910b8b9e827ccef0d73092dd6f12499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.2 KB (753242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f9b404804f7716cd3fce2e04dae7f19c8620b407f12a708e1f3f9cd944f9e`

```dockerfile
```

-	Layers:
	-	`sha256:4c6e25bf8fa604c97f277fd247f3614d3c6a8a1844f4cb78b3c466115463a60c`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 741.6 KB (741598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233de60c24dbdbc3fdcb9f32aba1af2eea5604c7ded084a880fb98dabaa39275`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 11.6 KB (11644 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:8824f00d57259b0b833257532b2a4ec94132d1bf00e4b36e87a56266aff3a40c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:c5000325cce93b58cb94ed7a77c85fa8a35520e6119b10a0d3a0ccc95960cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521828909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bb4f02fb0e8300d16b98188d95219c00741eeaf7deb9be498dcd44a5076f6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c40c3e3cdf945721f480e1d939aac857876fdb5c33b8fbfcf655c63b0b9428`  
		Last Modified: Wed, 24 Apr 2024 04:21:09 GMT  
		Size: 64.1 MB (64142118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05cc1123d7e335d59b0f465c23b7ad2ad27f4875b6c3eab41c65a9b50efa382`  
		Last Modified: Wed, 24 Apr 2024 04:21:45 GMT  
		Size: 211.2 MB (211175606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803b1968af78ef789730661c289a7ec4f7df4e634c9bee1c4837346ca3f4ef27`  
		Last Modified: Wed, 24 Apr 2024 05:12:18 GMT  
		Size: 172.9 MB (172884762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ea2ab75a2c2b231008469686581ab02e095b9fe922c119ade3d1479d3a3cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a288afbc55e2553d0168a7df78f087461c3e1f16288ca208348ce7cc956d6732`

```dockerfile
```

-	Layers:
	-	`sha256:51b060ea2235773d7512609d22d18dc74debf609f249989b35d729c12f6aab34`  
		Last Modified: Wed, 24 Apr 2024 05:12:16 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf815ddf8eb88dfd476d46a5029e837216ec0c685187027d0aefdf4d2eafcab6`  
		Last Modified: Wed, 24 Apr 2024 05:12:15 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:02f414fb213df08e9b7333e1bc6b6197034057b124e931a621fad867f8421ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510038334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef39effc782b510f66eab7f223bcc443fe6b080f53b290010473d523bdf9f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0525f0e8022d3b0295c1e79a86a4f89704f111e1b222a81c92bc1cd11e968380`  
		Last Modified: Fri, 12 Apr 2024 10:10:51 GMT  
		Size: 208.6 MB (208612483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bf7d1b36a17124b80128713cf3d086d5796c86dc372c6282cf498daf6c1395eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1beec69f650b1aebc630728883823a22b7d6678dd70d219c8e0a42fa58672ce`

```dockerfile
```

-	Layers:
	-	`sha256:703cb3fa1a3d5fecd4a490acbbca87494b9e3a268f01c0fcf9d5e3680d83130e`  
		Last Modified: Fri, 12 Apr 2024 10:10:47 GMT  
		Size: 15.2 MB (15176005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9869ff78ed8192003451c3741439e311265dc77f2e68f7449112268e7789237`  
		Last Modified: Fri, 12 Apr 2024 10:10:45 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3160cca3c6dda6fe0ab864a99ac7c140053d5d1eb607de1149d8ddf283291f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581324975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f4049f68d66356001e70d6436c367cca3844efe78889fcc32dc84b7c30c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03d269bebeec78b201e8b34ead41bf134d4d60a7a9487567cdf8c35741b6e6`  
		Last Modified: Thu, 11 Apr 2024 09:06:37 GMT  
		Size: 241.6 MB (241616470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c60bcda0982aaadca0e716b39a6374a61127c1a6de578325b4dd1a522cb7ae9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb01e6329c5de88d432e822441857852f9ab3a22ddb8644d6e833d6c705ee0`

```dockerfile
```

-	Layers:
	-	`sha256:ce8cf433ca365e2b10c8bd5a4abea406fa4f9e3ac157ea49fc5512e07028b8bd`  
		Last Modified: Thu, 11 Apr 2024 09:06:32 GMT  
		Size: 15.4 MB (15398644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3621a57d1464a572d892b6cf38eb44c3744f32365aa7308fb2da4a2e713ffa1`  
		Last Modified: Thu, 11 Apr 2024 09:06:31 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:890ff0201af78ee848b18a52a4f4531488b4e59578aaceb80267d92a5a5b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538602380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dcdd8241e4fbe59faf26d535c41d723ac8d9bc7a5ffc066ce3cc3d6bcd9976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c7b4c0568972903287c2ba295779f478db7fc45d1844ec5d10e22332f4cd1d84`  
		Last Modified: Wed, 24 Apr 2024 03:43:10 GMT  
		Size: 50.6 MB (50602565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba4056eb3a537ebb74fd333c27daceac5385bc3101b6029e706a51de775f00`  
		Last Modified: Wed, 24 Apr 2024 04:41:08 GMT  
		Size: 24.9 MB (24888940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0583cb1d092e1ca2b9a9e9ad274c286cbda7804622a36572a00c3440b4d88`  
		Last Modified: Wed, 24 Apr 2024 04:41:36 GMT  
		Size: 66.0 MB (65989175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4346162f795b064031764e3d351299d91568e9a1cb9ff0ae23d323d99339d1`  
		Last Modified: Wed, 24 Apr 2024 04:42:27 GMT  
		Size: 210.1 MB (210101062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ac1055cd771ed58d7865a880ab6bdb9b418503c9c767d13f68c437558fa46b`  
		Last Modified: Wed, 24 Apr 2024 05:12:29 GMT  
		Size: 187.0 MB (187020638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:97a7f910b863aa2ed9321369136bc22e1676fa469a92973958256b086366154c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08a98dfd4d629087d8353ef923ae123298df4a8a02235b5ed9609d9911589c`

```dockerfile
```

-	Layers:
	-	`sha256:be07c0f3fc84146f8b856092f446a575df879c8175d38ad9587726f5548f7dce`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76565694008f6464d1b540c738ca7df8e8974bac84071148aef50fcdfba095c4`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 13.2 KB (13177 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:3e03cf7b5c139593ad629b57e55624da795a4e789e4826ae88a0ef68a9feed27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551593932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62106ad4d5b838965cd23e3c23325d159f7ba16e3c4a5f525a573b48831d1e4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bf47934b0700489c27f4b1918c464037353ebec2ebc12585ceea997c9a34c71c`  
		Last Modified: Wed, 24 Apr 2024 03:25:57 GMT  
		Size: 53.6 MB (53580168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677be8677970cb6c89d034144a91a8695625d82f32553778be503e17ab5f55b3`  
		Last Modified: Wed, 24 Apr 2024 04:22:57 GMT  
		Size: 25.7 MB (25699777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48162777bb1b177bfa77ee29ba9552a6c899119f959faa64ef54f0a5aab3116`  
		Last Modified: Wed, 24 Apr 2024 04:23:19 GMT  
		Size: 69.6 MB (69584472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e881f9e7d456fa7b2b9e91f26b48776888d7ca1975413e2554119bfef1024`  
		Last Modified: Wed, 24 Apr 2024 04:23:59 GMT  
		Size: 214.2 MB (214213767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1dbcd760ee8f07bc74473682877cfe356c1743a81028d53592a9a203cbfe1d`  
		Last Modified: Thu, 25 Apr 2024 09:37:45 GMT  
		Size: 188.5 MB (188515748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:55139c979bd14dda211e51a3877d62232d3d44423d7a50eccb13987f2a8fc4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028f773eef818abb6e7c12c5785e8f0bc2100c507b72b5a932ab4e3db8b15eb2`

```dockerfile
```

-	Layers:
	-	`sha256:370f05a65fe56210232e2a29f47c225fa190152fce2f2fd2173f04fd6eebe017`  
		Last Modified: Thu, 25 Apr 2024 09:37:40 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c82a7840b4a0f54d7ee75413d11f713e9e9abf3e2ac8616c18bd4b2245f37e1`  
		Last Modified: Thu, 25 Apr 2024 09:37:39 GMT  
		Size: 12.6 KB (12625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:d651343e195b96bd4304dc33066bddf01f5a173b400df3c917b867a6d1f373d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:ccdf877ab59edf47e838cb586e8b37fd680a49a0a47d76ec4812142f8ab53f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 MB (495324610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce2473fbb694edc3adf51a56951e6455e2f655a776a865bf3d50385554989e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbeb8ef1d906919c518d52a9eb71cedf1ee5c3247b6ea106571a6252d5a4f05`  
		Last Modified: Wed, 24 Apr 2024 04:22:13 GMT  
		Size: 54.6 MB (54589380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e29bc91fb60d9860548fd0c66a11e7a14b5e9417059fd06a35fb120d542ee0`  
		Last Modified: Wed, 24 Apr 2024 04:22:47 GMT  
		Size: 197.0 MB (196986464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e74378906d6fcccfb1da6ff001463c333214d1c0961407017b0d92af11e99c`  
		Last Modified: Wed, 24 Apr 2024 05:12:06 GMT  
		Size: 172.9 MB (172884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:36cae1d27d3ffbeb7555c6e06ed91e6a6918856ccadacace444c64fb29ce5848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14987008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5475ef900d52d6d072e8823424349abe8270e19b3c105e4786bba417fa3f04f2`

```dockerfile
```

-	Layers:
	-	`sha256:e387fd514acb6becdc86178a7dbcd8e2de771419ac6ea9fe70fbadd665d114b2`  
		Last Modified: Wed, 24 Apr 2024 05:12:03 GMT  
		Size: 15.0 MB (14974944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f594e55497c4d0d325d1ac218e2aa59c03166f2e40597564a2214fc39079c6`  
		Last Modified: Wed, 24 Apr 2024 05:12:02 GMT  
		Size: 12.1 KB (12064 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:df9cd31df4d327523202f35516a11da6137aaeda2a08adc293e833a621f32dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491537963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc193a8f3c4651a63b0d0686148c39f44211822b8951a59661f1f806d4ba4d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:eb53aade3ed19f72413045948cad3084902fe630cc20789d2c2b5bc334679575 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23ca580217f1a6b17dba868e7ec34ae7fff221e07640fca532510daca8ed46f6`  
		Last Modified: Wed, 10 Apr 2024 01:04:48 GMT  
		Size: 50.2 MB (50246481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89b030e474718221560707f98fb967bd582bc0f355ca5caf120fc5f25b2d58`  
		Last Modified: Wed, 10 Apr 2024 07:01:21 GMT  
		Size: 14.9 MB (14879245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef8c5cdb2957e3cc1b26c037acafd549c7286845f8007127da85b383702cee3`  
		Last Modified: Wed, 10 Apr 2024 07:01:40 GMT  
		Size: 50.4 MB (50357907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c48f55e50a2918f423e3f80c787998eca4a47eec492d7e81553c5a738f095b`  
		Last Modified: Wed, 10 Apr 2024 07:02:17 GMT  
		Size: 167.4 MB (167441750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d040ff95e5e69aef50846a70d877773fcac32ff0f9d06253de2ae1af716e5734`  
		Last Modified: Fri, 12 Apr 2024 10:08:54 GMT  
		Size: 208.6 MB (208612580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:27e0a1d5194760cbf075370163165605974c9c995ea10b77865e58f93297b83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14787748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af251232f279d9d3d121b812683d85782f17d1bba6e318f2eb262560b385b1f`

```dockerfile
```

-	Layers:
	-	`sha256:b589bde1ab79c3fb90f18abb53e64717165bb517252d9cc4aa98393250dcd3d5`  
		Last Modified: Fri, 12 Apr 2024 10:08:48 GMT  
		Size: 14.8 MB (14776282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c521898116f82ca4982d8062c10f81c24a776f01ecadfc5280e29d90c17d9e03`  
		Last Modified: Fri, 12 Apr 2024 10:08:48 GMT  
		Size: 11.5 KB (11466 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1a3393a2d46c70be9b5f94dbbdad036e81cd4f53d22093a2c5a1b787778ebbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.7 MB (555703379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a93805309b544762c6959305d7a87882f3e00dde2cce0002faf220d1458abd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3f4a530684a6d51e431d14164bdf20c7ad515e8948ddbfbf5f9c2c3680727`  
		Last Modified: Wed, 10 Apr 2024 04:33:00 GMT  
		Size: 15.7 MB (15749239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27317b8832e116e0457de89bfb9097cbcd3165d6079c38230f3728894dfb3af1`  
		Last Modified: Wed, 10 Apr 2024 04:33:14 GMT  
		Size: 54.7 MB (54694342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dceb3c5772a800dd46b1b628a79e2167bd6bb0e9844a04e9ffc8a550a182b`  
		Last Modified: Wed, 10 Apr 2024 04:33:40 GMT  
		Size: 189.9 MB (189914112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f2acf4f3dce2c3a2795f5dca30272ad70e7ee1791a9408f571c2ef4cba93e7`  
		Last Modified: Thu, 11 Apr 2024 09:05:00 GMT  
		Size: 241.6 MB (241616510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c55d4e3706c53b607de807dfe5b67c0a41dfbf3050aeb10e1466a6d6d57794fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14988253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7715d50b671577b7d31dd38c33ffcba338f92fe0787f979fda4ae5eb9cdd792a`

```dockerfile
```

-	Layers:
	-	`sha256:b88b1950f542b58e6a5e7e351442969a5cbc11b8b9addc4ffc305dcf4770bd41`  
		Last Modified: Thu, 11 Apr 2024 09:04:54 GMT  
		Size: 15.0 MB (14976847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90dc2dba9d291701a8e356d68176d87b7608fe5f13cd0bb213154866267432f5`  
		Last Modified: Thu, 11 Apr 2024 09:04:53 GMT  
		Size: 11.4 KB (11406 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:99e80cd2bda0ca76de778c4bc0ba34c74e3de3956965791a351350aa2d53a7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.2 MB (515187676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964c90dd4b2891f01a4fbf7d61d46b5d47d2984449fdb31abed3fb4244ba9810`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:531ff4ee4f75fb0b1990fd185259fbec17670ebea9c3011de30a27e2de08c387`  
		Last Modified: Wed, 24 Apr 2024 03:43:58 GMT  
		Size: 56.1 MB (56076550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76062ffe019e6bfc91f0fe0510211f961184446e120461504dd7066278dbfb88`  
		Last Modified: Wed, 24 Apr 2024 04:42:41 GMT  
		Size: 16.3 MB (16269075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41af9e34185ddf73f8ecb610526409cc80e34f0aab2c2078a0effbe14be251`  
		Last Modified: Wed, 24 Apr 2024 04:43:06 GMT  
		Size: 55.9 MB (55929331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c343ec37d7971f52aa446a2e4bdf1947c24ac26c712f8d041bbde1de773ac`  
		Last Modified: Wed, 24 Apr 2024 04:43:51 GMT  
		Size: 199.9 MB (199892179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb203619e4b4cf64618cfa2c19ee1d65659b90ebdb6c6ee85de5f4da9c02e44c`  
		Last Modified: Wed, 24 Apr 2024 05:59:24 GMT  
		Size: 187.0 MB (187020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8c5065810bf725f4d006d056e2ecb13ca43faa90846226938e6ad83cbe5079ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14975802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07523a23b3c8e37e88a7e8e8a58a73eab78fd2627b3335433f824e07ba2d958`

```dockerfile
```

-	Layers:
	-	`sha256:62a66bf05356563138f65afc0e39dceefd84c1f7aca3fabaf5ecbca321bd679d`  
		Last Modified: Wed, 24 Apr 2024 05:59:20 GMT  
		Size: 15.0 MB (14963767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723a356feef7c199377ac324d03af4e1a42605c331083af3da8610fb9fc106b8`  
		Last Modified: Wed, 24 Apr 2024 05:59:19 GMT  
		Size: 12.0 KB (12035 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:29323ef01bbc112f2626a112df6540115e6815ef07ad2ec4e88aff3821006aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.5 MB (519468840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2151423f0c0c0cae1cc3858001cf459a34880c3542d1dd1ac89df8bb42db01c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:aac3759e46343ae5d9b035355707bd07abf04ff80e3d29e689ea89cc78633190`  
		Last Modified: Wed, 24 Apr 2024 03:27:06 GMT  
		Size: 59.0 MB (58968197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc915aadd544630a28ea807628347805a6b8bc6f250feae34a46f66ac5228d3`  
		Last Modified: Wed, 24 Apr 2024 04:24:14 GMT  
		Size: 16.8 MB (16767223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87809a577847ee55cd1298464ee16a72985d1700dcf4e546db6fca794086d7c7`  
		Last Modified: Wed, 24 Apr 2024 04:24:32 GMT  
		Size: 58.9 MB (58873993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b19380d6722f8bacf55a08edef5ab2bef7d748909aa0109770daf96177909f5`  
		Last Modified: Wed, 24 Apr 2024 04:25:08 GMT  
		Size: 196.3 MB (196343705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628886dc5a2cba117f1a160da40f7cdba890a9661d5b7ebf648b56daa9650bd1`  
		Last Modified: Thu, 25 Apr 2024 09:33:54 GMT  
		Size: 188.5 MB (188515722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:26e50deba46d7e0e49b0734934c375a1505b03dd640bef54ef6e5d182854a987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14953986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f593beaf1e613e4b46c5c999914c44bbcc87f30d78b21507d25d9a6047305dd4`

```dockerfile
```

-	Layers:
	-	`sha256:2e7e2d41aaffd5046784b0118f36fedbbbd9a80fa0e503d16067cade6134667c`  
		Last Modified: Thu, 25 Apr 2024 09:33:50 GMT  
		Size: 14.9 MB (14942547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a42423e593b1e4032328bd8df2924f0976804ba727dd0ae7fb996d9374e10b`  
		Last Modified: Thu, 25 Apr 2024 09:33:49 GMT  
		Size: 11.4 KB (11439 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-buster`

```console
$ docker pull rust@sha256:67afb05ae84c379fd1ef6c2af5a5988ae3a1402f5770b1c433716c3c8dcb2fe7
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

### `rust:1-buster` - linux; amd64

```console
$ docker pull rust@sha256:fd9265894ebb1726c08256cb3aacec8f4cb885d1060679f38aea5b912e24294e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.0 MB (484968446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783350f1d2be0610e2730df688417194ca785d80410ffbd196e066bf18264960`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
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
	-	`sha256:191249de5b7ca0b4a8a5b5d8c19f5e94207c98ac4748bbe000d55d4a9c36deaf`  
		Last Modified: Wed, 24 Apr 2024 05:10:48 GMT  
		Size: 172.9 MB (172884715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:0122d3cb2d238112d8ddf6530059ba7d3c5418e5fe10b6ce6f7bea70c24d5c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15978514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ddd78af473b781391d26953e04b4d00a22822fb134c6f3b616e239638d6039`

```dockerfile
```

-	Layers:
	-	`sha256:21e5e906506b573f52865ef471c93575cacb3df811f226d258e83d35df54893f`  
		Last Modified: Wed, 24 Apr 2024 05:10:43 GMT  
		Size: 16.0 MB (15966858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd656bc775aa85ed1d157d20989d1d938ef91e8ebaacdb1f059dd629824719f7`  
		Last Modified: Wed, 24 Apr 2024 05:10:42 GMT  
		Size: 11.7 KB (11656 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:d2a8509b3be550586f457a19b228cdc2de0b78ab062e7bf4ec198a8745cc21ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486339195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b65f67846b1f7ac4de8b0e6c3b61a864f968b815796c9bd1137d547800904d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:56eb0c1e9a01d2e3320b2f3d897736bfe09ccb53ef1ae8bfea2b9d4099bc1d6b in / 
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
	-	`sha256:300908ef79221077165ff78ff105758d14dd67c42610c4e0aafdd731a920a871`  
		Last Modified: Wed, 10 Apr 2024 01:05:35 GMT  
		Size: 46.0 MB (45962444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a28291d070880fd3bc1d1083c0a3dfd62197b6f8f9b8f0222bebfb7abc3998c`  
		Last Modified: Wed, 10 Apr 2024 07:02:28 GMT  
		Size: 16.2 MB (16217560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df332bea5b985c1c2dd5d35090367d1eeb17f766d81c69c6484a9dbdfb6a2a19`  
		Last Modified: Wed, 10 Apr 2024 07:02:46 GMT  
		Size: 47.4 MB (47411064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c429ea890a21b115686f06bcd8e64b77317af15fee22637d21494c7f7e8763`  
		Last Modified: Wed, 10 Apr 2024 07:03:24 GMT  
		Size: 168.1 MB (168135545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a8d87914e90936da310261b7cf6db3b8d4cd941ac36d01a329b6a539b8532d`  
		Last Modified: Fri, 12 Apr 2024 10:07:00 GMT  
		Size: 208.6 MB (208612582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:8d3df22872c5331a3b7dbd9ef6776ffeeed758d67b5577d16a3e9b04a5d2ac9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15423342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8934156cede7d8af64415e272e84c840fb7ae69b9a7fd35fa465ab349febf8`

```dockerfile
```

-	Layers:
	-	`sha256:7211e52e2624ee2d88410d49e28e0f8c9429402417cdc964037fc456623a6a1c`  
		Last Modified: Fri, 12 Apr 2024 10:06:55 GMT  
		Size: 15.4 MB (15412281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4bf7ecccbc2c3b7f1330ab90fab736d6467f54ca700dd24fb2e920cbdcb0fc`  
		Last Modified: Fri, 12 Apr 2024 10:06:54 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3f1b8288a64eaa661ef9d21d57965a6ce3af9c7fe1d4cf6eace903500c4d82e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544120500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c11826c12adf7e8e962ae839db1d4ea5e82b9df9958790153e5ac1b78711a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
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
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91b3908edaca8722a607f2265f615c82feb05f6440b5b8deab683e5f1338bfa`  
		Last Modified: Thu, 11 Apr 2024 09:03:31 GMT  
		Size: 241.6 MB (241616460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:1c1f949dcf2838a090f86a1847cac48ad01397a9edb0dff68e89d7193b0f9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15611975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ea129f23fc50bb965c6144abce71a0e69eccaf6989544d846c1ace9998e5a7`

```dockerfile
```

-	Layers:
	-	`sha256:df58017d086478c7376b7b37cf7f31b66e6987fa8f4fb639435f3daf7f77fe3f`  
		Last Modified: Thu, 11 Apr 2024 09:03:26 GMT  
		Size: 15.6 MB (15600976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174e8feb82f898148915b77b182fc9e1913079b6a09d883054bedac9a05eda6f`  
		Last Modified: Thu, 11 Apr 2024 09:03:26 GMT  
		Size: 11.0 KB (10999 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; 386

```console
$ docker pull rust@sha256:505bfca6bd398b4f00fce2ca2f2557b66aee0f09794144211116711a68f26b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.5 MB (508529720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe99a8ac5417c69838900906c1c7e30fbb0e60dfee7d690412859cdc78e7c42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:5f943bcdbbb65accdf0b3bc452a1d4fafd2c64a9c6f6b3010b2a7ca20bedef36 in / 
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
	-	`sha256:1b3962c4dea2d1d71b72cea574044d31a38d535a42183f4cd4993e6868c8de0d`  
		Last Modified: Wed, 24 Apr 2024 05:59:21 GMT  
		Size: 187.0 MB (187020738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:14cc95a3b98a58a84c3b868c33797396615d28771f00ae4f18b86a4442ffe7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15984068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb23ba590670f34ed24d660fea07e3e81a4b7efc98779effadb10adcebae634`

```dockerfile
```

-	Layers:
	-	`sha256:4400aa22d51411366132ed581c0eceaf6d4506634547b51715e0a2e460edda3e`  
		Last Modified: Wed, 24 Apr 2024 05:59:15 GMT  
		Size: 16.0 MB (15972439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6736ab863825c83fd0375286ca8c26322fa3921013d3db8f900b976c99982a4`  
		Last Modified: Wed, 24 Apr 2024 05:59:15 GMT  
		Size: 11.6 KB (11629 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:a8f04112cc1892451320b241b0fe7c074d506de026ad7d96162c8482f9b8ce1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1-slim` - linux; amd64

```console
$ docker pull rust@sha256:638e3590f320c70f5edbfe1842d42ae385624f8c6071f91037d465e7bf7178f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272626407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226d76b23659549e4748842478c0207ab5f79656c520fcb856f4eb235de0bfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12808888e0a2157cb0269632bdee49433c9f8556ccda1464afb6f94479129ead`  
		Last Modified: Wed, 24 Apr 2024 05:13:05 GMT  
		Size: 243.5 MB (243475928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5040f97f4a64566983b901b8fb9eae5ed9a1d4da8aa370cdff68de72249c4cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b52883aa5b9709eca3de616ddcc0c58126a33c1e0528ef6ff5f9a703697301c`

```dockerfile
```

-	Layers:
	-	`sha256:40a7699dc460633d2771085a3dc0e3d6f9aeb38030c5cd7a573799fae19a1fe4`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd14237218530973d0aee254a672a5a6fff80aab1f6eec85a9333d25355e634`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:8cfe44ff0e1d69b947a70df0359e48b4b7e1057d7c8849788ac4ef4da4f26a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd61a2122260688f839cbd2b8f940fd85eb6213d9be0561bc99d9d127dbbda89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd18c5ddc627e06a0ca56860a2c399710c2100cb5c189b0fabbe66dfb32f175`  
		Last Modified: Thu, 25 Apr 2024 00:16:57 GMT  
		Size: 256.2 MB (256248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:9fb4006e0666af50e2d9d516f1ee5bd14c6e8ee24e685e8f6c1066a72baf6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cc6bf9290ed472822b7c279a1146749b547500ed2b17cf92162d46ee0be09b`

```dockerfile
```

-	Layers:
	-	`sha256:7b7c864d459efcb9dcd68176e945b29238d18677fbf26fc97e155f5372e39a80`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65818ca85b37143c261fa4ff5bc754b1d6efb29dd4fa5a388c8c41cf9ef1b2d6`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 12.8 KB (12752 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fe4252019e0facdc82bd032d22eb0d1c4ca58f5c3540356840ea3f9a15b79c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336641733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738a4a3e15b336c497f51dd0341cebd130f98fc5e6ea5546d50463e3985f0f70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014c3ccaea43ce9fd3e3c56ffefc4fcc50ba52d2cac23c5776e1533bb9e7f634`  
		Last Modified: Wed, 10 Apr 2024 21:20:56 GMT  
		Size: 307.5 MB (307479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4bd8788f5359ae12cb9bc1acc434ae90d51e6f7cd825268f70daa6bf97d2325d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003752c0fbdb6817f01a5ce924bea0fc77facd03291bd1bcd89b48034b53a37e`

```dockerfile
```

-	Layers:
	-	`sha256:a43e77b376b0764e2dd70d8f2bb3d33a1e3e3ed5dc88c771d83fa0525ca92868`  
		Last Modified: Wed, 10 Apr 2024 21:20:49 GMT  
		Size: 3.9 MB (3941346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bcfee754885be41d14895386082b6d75a7631863a2b3174b1fb4e7ea77225d`  
		Last Modified: Wed, 10 Apr 2024 21:20:48 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:08523c621a2f1d85417842ce00b1b9a42cae8216c42f87e18bdc421c713f7aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284576083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4981314b33e7ff1620efe817f2d72fc26a1c68c6a8a0c469c3bea63aa9b7a03c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad09fde316fe0e55a14718d6a0e81c083b2f8db66b02507b77a68117757c57a`  
		Last Modified: Wed, 24 Apr 2024 05:12:53 GMT  
		Size: 254.4 MB (254412900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:99ae02c25a1e078ad005a0fb13a480de4139db49eac3e367c19f9a19b1042c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a8378609675925b2f4b4b20f668ce4dc84d34f24b2cb8a26d32ce28a92535`

```dockerfile
```

-	Layers:
	-	`sha256:38704fffa432b9b8793aae63e4759b2f6b2f6e2bedf5dcd36d4c4fe39829037a`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da465366a30fda81b5c80fb19fa525c3093aa9fa32f0046ab820b871c201439f`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 12.8 KB (12769 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:189bd571f7eda5c3a23b70cbc343ed2cf7a24f72403e602fb71217cf569c94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290203818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31abbd30af48b3f5e0705a87cc896e94c40e7105e2d56fc679a29fefe8d8f9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27733677c7e7ffa3ae36f75ea55eca558d3b1535be93b58e60e358a3fa368deb`  
		Last Modified: Thu, 25 Apr 2024 09:39:52 GMT  
		Size: 257.1 MB (257062617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:850f59e79459f30440637f4f653d198d566176041d523a4ae01cb0498e12a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da07cd9aab3aa522fedda7cf41f03250557c862c629dc3a085cca69325b9aa`

```dockerfile
```

-	Layers:
	-	`sha256:aa0002bfc1a0d55e006eb61a57f2ec44a70a0758f0e5b78d46e00d75476b9ec6`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068a9188948e8d6cc2034275e59e9515d1cb420e57eda3a7f9a3600fb6039d21`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:a8f04112cc1892451320b241b0fe7c074d506de026ad7d96162c8482f9b8ce1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:638e3590f320c70f5edbfe1842d42ae385624f8c6071f91037d465e7bf7178f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272626407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226d76b23659549e4748842478c0207ab5f79656c520fcb856f4eb235de0bfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12808888e0a2157cb0269632bdee49433c9f8556ccda1464afb6f94479129ead`  
		Last Modified: Wed, 24 Apr 2024 05:13:05 GMT  
		Size: 243.5 MB (243475928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5040f97f4a64566983b901b8fb9eae5ed9a1d4da8aa370cdff68de72249c4cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b52883aa5b9709eca3de616ddcc0c58126a33c1e0528ef6ff5f9a703697301c`

```dockerfile
```

-	Layers:
	-	`sha256:40a7699dc460633d2771085a3dc0e3d6f9aeb38030c5cd7a573799fae19a1fe4`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd14237218530973d0aee254a672a5a6fff80aab1f6eec85a9333d25355e634`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:8cfe44ff0e1d69b947a70df0359e48b4b7e1057d7c8849788ac4ef4da4f26a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd61a2122260688f839cbd2b8f940fd85eb6213d9be0561bc99d9d127dbbda89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd18c5ddc627e06a0ca56860a2c399710c2100cb5c189b0fabbe66dfb32f175`  
		Last Modified: Thu, 25 Apr 2024 00:16:57 GMT  
		Size: 256.2 MB (256248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9fb4006e0666af50e2d9d516f1ee5bd14c6e8ee24e685e8f6c1066a72baf6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cc6bf9290ed472822b7c279a1146749b547500ed2b17cf92162d46ee0be09b`

```dockerfile
```

-	Layers:
	-	`sha256:7b7c864d459efcb9dcd68176e945b29238d18677fbf26fc97e155f5372e39a80`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65818ca85b37143c261fa4ff5bc754b1d6efb29dd4fa5a388c8c41cf9ef1b2d6`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 12.8 KB (12752 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fe4252019e0facdc82bd032d22eb0d1c4ca58f5c3540356840ea3f9a15b79c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336641733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738a4a3e15b336c497f51dd0341cebd130f98fc5e6ea5546d50463e3985f0f70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014c3ccaea43ce9fd3e3c56ffefc4fcc50ba52d2cac23c5776e1533bb9e7f634`  
		Last Modified: Wed, 10 Apr 2024 21:20:56 GMT  
		Size: 307.5 MB (307479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4bd8788f5359ae12cb9bc1acc434ae90d51e6f7cd825268f70daa6bf97d2325d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003752c0fbdb6817f01a5ce924bea0fc77facd03291bd1bcd89b48034b53a37e`

```dockerfile
```

-	Layers:
	-	`sha256:a43e77b376b0764e2dd70d8f2bb3d33a1e3e3ed5dc88c771d83fa0525ca92868`  
		Last Modified: Wed, 10 Apr 2024 21:20:49 GMT  
		Size: 3.9 MB (3941346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bcfee754885be41d14895386082b6d75a7631863a2b3174b1fb4e7ea77225d`  
		Last Modified: Wed, 10 Apr 2024 21:20:48 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:08523c621a2f1d85417842ce00b1b9a42cae8216c42f87e18bdc421c713f7aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284576083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4981314b33e7ff1620efe817f2d72fc26a1c68c6a8a0c469c3bea63aa9b7a03c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad09fde316fe0e55a14718d6a0e81c083b2f8db66b02507b77a68117757c57a`  
		Last Modified: Wed, 24 Apr 2024 05:12:53 GMT  
		Size: 254.4 MB (254412900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:99ae02c25a1e078ad005a0fb13a480de4139db49eac3e367c19f9a19b1042c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a8378609675925b2f4b4b20f668ce4dc84d34f24b2cb8a26d32ce28a92535`

```dockerfile
```

-	Layers:
	-	`sha256:38704fffa432b9b8793aae63e4759b2f6b2f6e2bedf5dcd36d4c4fe39829037a`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da465366a30fda81b5c80fb19fa525c3093aa9fa32f0046ab820b871c201439f`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 12.8 KB (12769 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:189bd571f7eda5c3a23b70cbc343ed2cf7a24f72403e602fb71217cf569c94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290203818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31abbd30af48b3f5e0705a87cc896e94c40e7105e2d56fc679a29fefe8d8f9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27733677c7e7ffa3ae36f75ea55eca558d3b1535be93b58e60e358a3fa368deb`  
		Last Modified: Thu, 25 Apr 2024 09:39:52 GMT  
		Size: 257.1 MB (257062617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:850f59e79459f30440637f4f653d198d566176041d523a4ae01cb0498e12a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da07cd9aab3aa522fedda7cf41f03250557c862c629dc3a085cca69325b9aa`

```dockerfile
```

-	Layers:
	-	`sha256:aa0002bfc1a0d55e006eb61a57f2ec44a70a0758f0e5b78d46e00d75476b9ec6`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068a9188948e8d6cc2034275e59e9515d1cb420e57eda3a7f9a3600fb6039d21`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:caca164937940b63e2ae6292b2507fe6c2feec7fc17fe958f182eab8af018b84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:43ea72d42d2c038ea843c9b41316622f86f5374dc6dfb82a037587761a04b849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264265732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9e28bbeb4bfd6d136fe79aa0822e42176d77fd24f75c05e8458b105546c898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c309d2cedf4817a559551782149cdca9318d0a6c23018b97523a0fe91857f`  
		Last Modified: Wed, 24 Apr 2024 05:11:46 GMT  
		Size: 232.8 MB (232831469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8b95d9eb6aa93d0dc9fb69ff759960ed6ca6dffc91099527b5f001a00f624d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053dac136f29cad1cf8460c926ae37b678819959d2a4d6f351e2d57c76b04680`

```dockerfile
```

-	Layers:
	-	`sha256:3bf84e83a418f557d6b1f21933fed9e3f861d44845045ea89e0dbcb27c9bc330`  
		Last Modified: Wed, 24 Apr 2024 05:11:41 GMT  
		Size: 4.1 MB (4139833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf51e74c2bf86d87b3bd5677d94c687071178480fd648aa0c64a816c4ed6e0a`  
		Last Modified: Wed, 24 Apr 2024 05:11:41 GMT  
		Size: 11.6 KB (11630 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d87bd027a2ec897941ff0f691413f27f6ab798f47ffd1c6954fd687bf58928f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277276352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c859469ac3ba60ce123589a9d56e54f17c194a61ee18931acfd7e3133b2aec9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d54685378a8d57ac36e4ff6a2c342ac52809f585a7d4c8fb662229230e65ce`  
		Last Modified: Thu, 25 Apr 2024 00:15:07 GMT  
		Size: 250.7 MB (250681610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3ceebf9c5462589e2d813246b8a8b6852d230b823549fe33fbab50984fca842e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8625ff2e32464e91cc3d770313871c50321ca890b2a17a4e0a2092840860cd`

```dockerfile
```

-	Layers:
	-	`sha256:f5d89aa7dc719b61e8b5071c3b29c385557d01a1d8ded536e3e3559ebf05078e`  
		Last Modified: Thu, 25 Apr 2024 00:15:01 GMT  
		Size: 3.9 MB (3949756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9151d79ca50c92149bee7df68a8e9b97ed397aedf889f6cbd71f43a42f9f1d6`  
		Last Modified: Thu, 25 Apr 2024 00:15:01 GMT  
		Size: 11.5 KB (11533 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4c5434f97e2e831215a9c5ed5abdf21894ad3c1e7f85f3661cc20c4f1d5fdcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327435048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3e88fc0ee536589d8ff9f84db749baeb19f637ca9d3ca26f872061af6ab348`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ffe28413ff737e9319fc6b161f92951752ebcccd38ff443b7b7a1bf7c46ec`  
		Last Modified: Wed, 10 Apr 2024 21:19:30 GMT  
		Size: 297.4 MB (297358742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:07546376e3d6ff97ef9245f0ddf9c23c2343abfcfc0d612ecd603355351e4fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b9a0d3926f551a4aa8aa4b4aa20168cbead544a81f98131d46e0b3d74339b3`

```dockerfile
```

-	Layers:
	-	`sha256:80783504581f38a49f386edba09b9cd5153392c5ad0174015ef551f090f4452b`  
		Last Modified: Wed, 10 Apr 2024 21:19:23 GMT  
		Size: 4.1 MB (4136557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:333d3575ff26376a87ab3ee97463a3424ff3ef7b03e78b7c28d8433a6e4586b9`  
		Last Modified: Wed, 10 Apr 2024 21:19:23 GMT  
		Size: 11.5 KB (11469 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:9d5d2ddfdd6a58b18bb7f0b8e5f8f37047f9ea8f1e2aa50dbcd4977bab58cd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280018615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbfbb115c7bc121e9f0e8a7827e251c41349a8bd1984a1e769d5c0374d67939`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37221a01bece8cf821897f51b65bd44350746155d325214a918695731a66d3f`  
		Last Modified: Wed, 24 Apr 2024 05:12:24 GMT  
		Size: 247.6 MB (247593842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:790c11b457e330245a08ee08368b80c4f9ba2376cd04a83d8c1281b66b8c95ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31aebfaf8b74b4087da8d50d05aab6f15d452168841659b66338f8cdefa27db2`

```dockerfile
```

-	Layers:
	-	`sha256:7ded81c8554c4a76e11a1920802c6a674e41a6c19c84a7a708cb38fde0d159c8`  
		Last Modified: Wed, 24 Apr 2024 05:12:19 GMT  
		Size: 4.1 MB (4131887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86498619bcaaa39fefc2150c322446a6fcf7367d267078da6811a589fe3d3977`  
		Last Modified: Wed, 24 Apr 2024 05:12:19 GMT  
		Size: 11.6 KB (11601 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:d1fbaf1eb7c480f19373691dee46b7333091e312a0067cfff60e4f88125b1a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278620161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0eb2329b60e7b7a4c321b3eb186e7e8291157920a4c927c5b1239dcd290362`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1effd22b3d858125536254bd2d670cd1a720ea963a5f5b9a6295f1cf04c849f2`  
		Last Modified: Thu, 25 Apr 2024 09:35:52 GMT  
		Size: 243.3 MB (243308436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6c908c45ab479e9a650293593a45d8210151cc0acedb0d2b98bd1874afc7b2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ca374cdff5e57bddc8583419f72f992120d629a52de5d00744829a915b1da9`

```dockerfile
```

-	Layers:
	-	`sha256:409c6f41b6182bd1869c433f7aab4744d5fc0538822f779fc042144d994129ad`  
		Last Modified: Thu, 25 Apr 2024 09:35:46 GMT  
		Size: 4.1 MB (4100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020f597651f5972b28de5ed540ee23e227c15cab9910914b31894c8c48ed893f`  
		Last Modified: Thu, 25 Apr 2024 09:35:46 GMT  
		Size: 11.5 KB (11500 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-buster`

```console
$ docker pull rust@sha256:c52682b3c2455ba53083c61fc7d888d9e5c05af0e9f1720cedfcccf9681fa1f5
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

### `rust:1-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:e07c7817a1f8c56703b7c838c9a1d935ff5564981ab688fa9e5fe8a90e281234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245641279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fede2e811700e9b934388f903e43604d03cb4b02baa1b22f9e413087e23b6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b134fdd9ab24eec74b1973bea2fd971ba7966b53832863f2203aab5b1d6f89d`  
		Last Modified: Wed, 24 Apr 2024 05:10:28 GMT  
		Size: 218.3 MB (218303704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e5f87c411463e875b33cd48735d0289a9f7360541f0a7e32517cdd0a524b74c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45862094e4737de29467a79fec0a29be59819e15e997285078a0863166b3f96f`

```dockerfile
```

-	Layers:
	-	`sha256:d67cbeec45f86edc9afc54108da384643c40148c2fcf4dfc1693ed69d478a260`  
		Last Modified: Wed, 24 Apr 2024 05:10:24 GMT  
		Size: 3.9 MB (3941693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6058ee49cb0823ba46e949353f949deae7132061fb1b1b6c1a08016edfff47f`  
		Last Modified: Wed, 24 Apr 2024 05:10:24 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:06c1a08af5dabc4454b1cc105c607d4d06c9b0814db93873ff926a1ee1ef7b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264467965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4b9e3843b862fb3d9313d353d263101bf53a6b5d8b5e5fc90bf323760a9189`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f904fd6bf6b41f2fa9b506f896ebdbe821cd028a693fdf7968eacbc7b23da79f`  
		Last Modified: Thu, 25 Apr 2024 00:13:15 GMT  
		Size: 241.5 MB (241522901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e89bf36198f7184854a7500fc86b2d9017d6dec89f9311e71ecc44493f5ea944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492e0ecf007f0e2320b0b6564175d11a3d1f73d3402844e54236f518ce9eee78`

```dockerfile
```

-	Layers:
	-	`sha256:34f4a9c71e486a6edc1e06711c9c2d0e0a73aac8cc3987e71e5a681711ebaada`  
		Last Modified: Thu, 25 Apr 2024 00:13:09 GMT  
		Size: 3.7 MB (3749343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fa92b499139c82ddeb20b2d912bdeb136fcb250880b3abb0507ed48c61ef2b`  
		Last Modified: Thu, 25 Apr 2024 00:13:09 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3d47794cfa590e602f949345fc56267448530e64cf207ba79a4a8ebb82dd5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307822239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b58e4d35c7954b401373ee5f917c051f71d431fa6428121ce81b12148ab192`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81eb727fb6d6e4fe3e3a1ca3b615eb88245d64c5376a62e8bf275616c3c6cbb`  
		Last Modified: Wed, 10 Apr 2024 21:18:05 GMT  
		Size: 281.9 MB (281858778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:2628255e922502afd4e4aa0c4e30f4a26a1866d57111adb0984f7099d6b6549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1ff19d2b3c12e6fa257c298f2817debf02d8779e528210e136f9067dea6452`

```dockerfile
```

-	Layers:
	-	`sha256:152b56576a1f9f73de903d5f06d63ced13edd3b6f90bbb2d7ed9e780766cbae4`  
		Last Modified: Wed, 10 Apr 2024 21:17:59 GMT  
		Size: 3.6 MB (3574733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ce6be4574a6a214b953ebd2d8aa8c578da1ee01ca9ee50a67e6c3e5064b46c`  
		Last Modified: Wed, 10 Apr 2024 21:17:58 GMT  
		Size: 11.1 KB (11063 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:03a4f59dd317b964c56e75b84763dc831da494e3ec21fd36ae34348eecbcbd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265011000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8693b85bfe42d16b6f845d8e99d4a830f075c232156916f63ad424ad023a5ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:32f0f06baa0e4f10bff55aaa215b511838432ecc5fe547373d9ac99494556801 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:204b51fc41806ed93b4ccb6ce8272fa49b5f0b099ba6e3b5a940a9e7cd3ce202`  
		Last Modified: Wed, 24 Apr 2024 03:45:03 GMT  
		Size: 28.0 MB (27994678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bbd5edd24ae790e1053c99262c3c1062e6a89592bd6cccc53fef0b1e87e5a0`  
		Last Modified: Wed, 24 Apr 2024 05:10:57 GMT  
		Size: 237.0 MB (237016322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e45b1cd901a13a4ce4276a8780227951cd768d74e51877fec136f5906be660cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883ed62f0760eff19d06298c55f6a6eb27a6b79873ea0a37ccbe2f0b6defd196`

```dockerfile
```

-	Layers:
	-	`sha256:cda5f4adc3ed394903a5491d8b6ca36016e55f666a851196b374d2075686d8a9`  
		Last Modified: Wed, 24 Apr 2024 05:10:52 GMT  
		Size: 3.9 MB (3948318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4b9dd3825cdc912de170e8e5e11c701ebb88ea3e6ff82af59b8053cdd2b527`  
		Last Modified: Wed, 24 Apr 2024 05:10:51 GMT  
		Size: 11.2 KB (11195 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77`

```console
$ docker pull rust@sha256:8824f00d57259b0b833257532b2a4ec94132d1bf00e4b36e87a56266aff3a40c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77` - linux; amd64

```console
$ docker pull rust@sha256:c5000325cce93b58cb94ed7a77c85fa8a35520e6119b10a0d3a0ccc95960cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521828909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bb4f02fb0e8300d16b98188d95219c00741eeaf7deb9be498dcd44a5076f6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c40c3e3cdf945721f480e1d939aac857876fdb5c33b8fbfcf655c63b0b9428`  
		Last Modified: Wed, 24 Apr 2024 04:21:09 GMT  
		Size: 64.1 MB (64142118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05cc1123d7e335d59b0f465c23b7ad2ad27f4875b6c3eab41c65a9b50efa382`  
		Last Modified: Wed, 24 Apr 2024 04:21:45 GMT  
		Size: 211.2 MB (211175606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803b1968af78ef789730661c289a7ec4f7df4e634c9bee1c4837346ca3f4ef27`  
		Last Modified: Wed, 24 Apr 2024 05:12:18 GMT  
		Size: 172.9 MB (172884762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77` - unknown; unknown

```console
$ docker pull rust@sha256:8ea2ab75a2c2b231008469686581ab02e095b9fe922c119ade3d1479d3a3cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a288afbc55e2553d0168a7df78f087461c3e1f16288ca208348ce7cc956d6732`

```dockerfile
```

-	Layers:
	-	`sha256:51b060ea2235773d7512609d22d18dc74debf609f249989b35d729c12f6aab34`  
		Last Modified: Wed, 24 Apr 2024 05:12:16 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf815ddf8eb88dfd476d46a5029e837216ec0c685187027d0aefdf4d2eafcab6`  
		Last Modified: Wed, 24 Apr 2024 05:12:15 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77` - linux; arm variant v7

```console
$ docker pull rust@sha256:02f414fb213df08e9b7333e1bc6b6197034057b124e931a621fad867f8421ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510038334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef39effc782b510f66eab7f223bcc443fe6b080f53b290010473d523bdf9f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0525f0e8022d3b0295c1e79a86a4f89704f111e1b222a81c92bc1cd11e968380`  
		Last Modified: Fri, 12 Apr 2024 10:10:51 GMT  
		Size: 208.6 MB (208612483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77` - unknown; unknown

```console
$ docker pull rust@sha256:bf7d1b36a17124b80128713cf3d086d5796c86dc372c6282cf498daf6c1395eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1beec69f650b1aebc630728883823a22b7d6678dd70d219c8e0a42fa58672ce`

```dockerfile
```

-	Layers:
	-	`sha256:703cb3fa1a3d5fecd4a490acbbca87494b9e3a268f01c0fcf9d5e3680d83130e`  
		Last Modified: Fri, 12 Apr 2024 10:10:47 GMT  
		Size: 15.2 MB (15176005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9869ff78ed8192003451c3741439e311265dc77f2e68f7449112268e7789237`  
		Last Modified: Fri, 12 Apr 2024 10:10:45 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3160cca3c6dda6fe0ab864a99ac7c140053d5d1eb607de1149d8ddf283291f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581324975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f4049f68d66356001e70d6436c367cca3844efe78889fcc32dc84b7c30c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03d269bebeec78b201e8b34ead41bf134d4d60a7a9487567cdf8c35741b6e6`  
		Last Modified: Thu, 11 Apr 2024 09:06:37 GMT  
		Size: 241.6 MB (241616470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77` - unknown; unknown

```console
$ docker pull rust@sha256:c60bcda0982aaadca0e716b39a6374a61127c1a6de578325b4dd1a522cb7ae9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb01e6329c5de88d432e822441857852f9ab3a22ddb8644d6e833d6c705ee0`

```dockerfile
```

-	Layers:
	-	`sha256:ce8cf433ca365e2b10c8bd5a4abea406fa4f9e3ac157ea49fc5512e07028b8bd`  
		Last Modified: Thu, 11 Apr 2024 09:06:32 GMT  
		Size: 15.4 MB (15398644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3621a57d1464a572d892b6cf38eb44c3744f32365aa7308fb2da4a2e713ffa1`  
		Last Modified: Thu, 11 Apr 2024 09:06:31 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77` - linux; 386

```console
$ docker pull rust@sha256:890ff0201af78ee848b18a52a4f4531488b4e59578aaceb80267d92a5a5b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538602380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dcdd8241e4fbe59faf26d535c41d723ac8d9bc7a5ffc066ce3cc3d6bcd9976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c7b4c0568972903287c2ba295779f478db7fc45d1844ec5d10e22332f4cd1d84`  
		Last Modified: Wed, 24 Apr 2024 03:43:10 GMT  
		Size: 50.6 MB (50602565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba4056eb3a537ebb74fd333c27daceac5385bc3101b6029e706a51de775f00`  
		Last Modified: Wed, 24 Apr 2024 04:41:08 GMT  
		Size: 24.9 MB (24888940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0583cb1d092e1ca2b9a9e9ad274c286cbda7804622a36572a00c3440b4d88`  
		Last Modified: Wed, 24 Apr 2024 04:41:36 GMT  
		Size: 66.0 MB (65989175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4346162f795b064031764e3d351299d91568e9a1cb9ff0ae23d323d99339d1`  
		Last Modified: Wed, 24 Apr 2024 04:42:27 GMT  
		Size: 210.1 MB (210101062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ac1055cd771ed58d7865a880ab6bdb9b418503c9c767d13f68c437558fa46b`  
		Last Modified: Wed, 24 Apr 2024 05:12:29 GMT  
		Size: 187.0 MB (187020638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77` - unknown; unknown

```console
$ docker pull rust@sha256:97a7f910b863aa2ed9321369136bc22e1676fa469a92973958256b086366154c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08a98dfd4d629087d8353ef923ae123298df4a8a02235b5ed9609d9911589c`

```dockerfile
```

-	Layers:
	-	`sha256:be07c0f3fc84146f8b856092f446a575df879c8175d38ad9587726f5548f7dce`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76565694008f6464d1b540c738ca7df8e8974bac84071148aef50fcdfba095c4`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 13.2 KB (13177 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77` - linux; ppc64le

```console
$ docker pull rust@sha256:3e03cf7b5c139593ad629b57e55624da795a4e789e4826ae88a0ef68a9feed27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551593932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62106ad4d5b838965cd23e3c23325d159f7ba16e3c4a5f525a573b48831d1e4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bf47934b0700489c27f4b1918c464037353ebec2ebc12585ceea997c9a34c71c`  
		Last Modified: Wed, 24 Apr 2024 03:25:57 GMT  
		Size: 53.6 MB (53580168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677be8677970cb6c89d034144a91a8695625d82f32553778be503e17ab5f55b3`  
		Last Modified: Wed, 24 Apr 2024 04:22:57 GMT  
		Size: 25.7 MB (25699777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48162777bb1b177bfa77ee29ba9552a6c899119f959faa64ef54f0a5aab3116`  
		Last Modified: Wed, 24 Apr 2024 04:23:19 GMT  
		Size: 69.6 MB (69584472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e881f9e7d456fa7b2b9e91f26b48776888d7ca1975413e2554119bfef1024`  
		Last Modified: Wed, 24 Apr 2024 04:23:59 GMT  
		Size: 214.2 MB (214213767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1dbcd760ee8f07bc74473682877cfe356c1743a81028d53592a9a203cbfe1d`  
		Last Modified: Thu, 25 Apr 2024 09:37:45 GMT  
		Size: 188.5 MB (188515748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77` - unknown; unknown

```console
$ docker pull rust@sha256:55139c979bd14dda211e51a3877d62232d3d44423d7a50eccb13987f2a8fc4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028f773eef818abb6e7c12c5785e8f0bc2100c507b72b5a932ab4e3db8b15eb2`

```dockerfile
```

-	Layers:
	-	`sha256:370f05a65fe56210232e2a29f47c225fa190152fce2f2fd2173f04fd6eebe017`  
		Last Modified: Thu, 25 Apr 2024 09:37:40 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c82a7840b4a0f54d7ee75413d11f713e9e9abf3e2ac8616c18bd4b2245f37e1`  
		Last Modified: Thu, 25 Apr 2024 09:37:39 GMT  
		Size: 12.6 KB (12625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-alpine`

```console
$ docker pull rust@sha256:9b74675247503eb0c3e3831dfdf10985c254b3ba9aa9a36eac8917f912a134eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.77-alpine` - linux; amd64

```console
$ docker pull rust@sha256:dc037af6f82e10c9862879cfe7dcbeb883b23092013b3a1df295512a4ade5d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272492183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d9a62b548d2deef025a80cbb517fcdaab56526b8cfc88d0ef4ab90b8dab39d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f170ecb6344abd22a40dfedc95278fed4a73a9409a285b6a31c6994b8097ab`  
		Last Modified: Tue, 09 Apr 2024 23:50:39 GMT  
		Size: 55.3 MB (55346790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150084451e7317de7972997b74d7d7b3a6947e9e01a1a3cd1a3b799e8348208`  
		Last Modified: Tue, 09 Apr 2024 23:50:42 GMT  
		Size: 213.7 MB (213736664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:65412a414e6e29d6f1c17de3346d8babf260891f011363110e2ef9d34763d2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e244aa001a61ab57db8fdbd3135b351cc3c55962ee776136e5af23d4b0a303ee`

```dockerfile
```

-	Layers:
	-	`sha256:4e63ddf0710f8dcc924c71396e2f3b39819922b0db63df53204e50c9b9c396a6`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 710.6 KB (710617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4861d7790f28e1d13f2037ee5c69a885431a65a224621e3a0915312ccd1038`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 11.8 KB (11792 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d30747064955669d4e48ece7dc69776bf05abe2ffa4eb866314bc842f9231936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278817954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd976a496d7d864344a2b39dad2155dbb9ef5d526f06ac412d4a3e2a37cb0be1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651ca114e522c42e6bb17953edf4a18bba82fe2287f93e32f6b3957ff901c2`  
		Last Modified: Sat, 16 Mar 2024 17:12:47 GMT  
		Size: 53.0 MB (52970287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157aaa1f3fa9784926886cafbadb1c30dcd160078deb54be2c6a6b7452ba670`  
		Last Modified: Wed, 10 Apr 2024 00:03:58 GMT  
		Size: 222.5 MB (222499952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:07fcac075e46cdcd0b7ad2a6c17d6d167910b8b9e827ccef0d73092dd6f12499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.2 KB (753242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f9b404804f7716cd3fce2e04dae7f19c8620b407f12a708e1f3f9cd944f9e`

```dockerfile
```

-	Layers:
	-	`sha256:4c6e25bf8fa604c97f277fd247f3614d3c6a8a1844f4cb78b3c466115463a60c`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 741.6 KB (741598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233de60c24dbdbc3fdcb9f32aba1af2eea5604c7ded084a880fb98dabaa39275`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 11.6 KB (11644 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-alpine3.18`

```console
$ docker pull rust@sha256:b8f4f707c6460f4228deecdcc4acdfc50045fa7396f8aec732dc4ea322a41066
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.77-alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:f5762f07bc2d9d6699afb162b7f35dfa48e5945cf4395b4f9b9d6826cb1d3c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268673214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d5e3a7dd699641a0c6368e65fad736d7c583359096663c1e4bf5e98b85d5a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f914773acc6db8be08970614a0ed0f5fce71828723bfcb6e6cf1d97a26c284eb`  
		Last Modified: Tue, 09 Apr 2024 23:50:41 GMT  
		Size: 51.5 MB (51534043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0af00c163854d8ec5ea9d8a150960293bfd4aa34804a7a160ef80f44ce71d`  
		Last Modified: Tue, 09 Apr 2024 23:50:44 GMT  
		Size: 213.7 MB (213736629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:9bfd12461323300ebd4c975ebc91a40d5949fa914272a2abe34315cac6c58c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49a20d1e055b2d8dcd9f1dc20fe467a5b977e5e797847f63adebc0d7732c718`

```dockerfile
```

-	Layers:
	-	`sha256:d549196acdb3131a3a009a32ec149198450da016167ecb17316ed5105a440284`  
		Last Modified: Tue, 09 Apr 2024 23:50:40 GMT  
		Size: 701.9 KB (701886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff0d60c39141b47c8ebf94551e1235d461f65e03b68df4a8ae19688754cc60b`  
		Last Modified: Tue, 09 Apr 2024 23:50:40 GMT  
		Size: 10.6 KB (10588 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3a178840b556deece46aeea0e6f3029a9bf525530b5eba1f6037531c098947a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271899543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78a508d74d054080dc4bcea6dc7bd9819bd806d6bfd06910138e6c94e384e19`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b1cd0d662b55abd28904427ae8befdb37b765cf7ff19dc4a587c51429117c7`  
		Last Modified: Sat, 16 Mar 2024 17:11:39 GMT  
		Size: 46.1 MB (46066359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a88ea76700e9b87c7238a55b12f22030ed622804d3c18cd00497bbf3d9760d`  
		Last Modified: Wed, 10 Apr 2024 00:02:53 GMT  
		Size: 222.5 MB (222499823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:bf2d6cdc43bc8c6f6942a7e2a4eec7dd93b4f8a2e51b5cdee8f402c636b252d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.2 KB (747167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd7d1515764e16148a0a685fa2c88831a6e8bae26f370009e24a37eb15c52f1`

```dockerfile
```

-	Layers:
	-	`sha256:817ff20e322fc42973b1489c74c9d5e24420023ac7706158646e0c8187ea53d9`  
		Last Modified: Wed, 10 Apr 2024 00:02:48 GMT  
		Size: 736.7 KB (736735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff708420c480e2a3ada601eacf662d093335bbf3c2b624e814c55dd24d3d368`  
		Last Modified: Wed, 10 Apr 2024 00:02:48 GMT  
		Size: 10.4 KB (10432 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-alpine3.19`

```console
$ docker pull rust@sha256:9b74675247503eb0c3e3831dfdf10985c254b3ba9aa9a36eac8917f912a134eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.77-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:dc037af6f82e10c9862879cfe7dcbeb883b23092013b3a1df295512a4ade5d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272492183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d9a62b548d2deef025a80cbb517fcdaab56526b8cfc88d0ef4ab90b8dab39d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f170ecb6344abd22a40dfedc95278fed4a73a9409a285b6a31c6994b8097ab`  
		Last Modified: Tue, 09 Apr 2024 23:50:39 GMT  
		Size: 55.3 MB (55346790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150084451e7317de7972997b74d7d7b3a6947e9e01a1a3cd1a3b799e8348208`  
		Last Modified: Tue, 09 Apr 2024 23:50:42 GMT  
		Size: 213.7 MB (213736664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:65412a414e6e29d6f1c17de3346d8babf260891f011363110e2ef9d34763d2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e244aa001a61ab57db8fdbd3135b351cc3c55962ee776136e5af23d4b0a303ee`

```dockerfile
```

-	Layers:
	-	`sha256:4e63ddf0710f8dcc924c71396e2f3b39819922b0db63df53204e50c9b9c396a6`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 710.6 KB (710617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4861d7790f28e1d13f2037ee5c69a885431a65a224621e3a0915312ccd1038`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 11.8 KB (11792 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d30747064955669d4e48ece7dc69776bf05abe2ffa4eb866314bc842f9231936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278817954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd976a496d7d864344a2b39dad2155dbb9ef5d526f06ac412d4a3e2a37cb0be1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651ca114e522c42e6bb17953edf4a18bba82fe2287f93e32f6b3957ff901c2`  
		Last Modified: Sat, 16 Mar 2024 17:12:47 GMT  
		Size: 53.0 MB (52970287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157aaa1f3fa9784926886cafbadb1c30dcd160078deb54be2c6a6b7452ba670`  
		Last Modified: Wed, 10 Apr 2024 00:03:58 GMT  
		Size: 222.5 MB (222499952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:07fcac075e46cdcd0b7ad2a6c17d6d167910b8b9e827ccef0d73092dd6f12499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.2 KB (753242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f9b404804f7716cd3fce2e04dae7f19c8620b407f12a708e1f3f9cd944f9e`

```dockerfile
```

-	Layers:
	-	`sha256:4c6e25bf8fa604c97f277fd247f3614d3c6a8a1844f4cb78b3c466115463a60c`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 741.6 KB (741598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233de60c24dbdbc3fdcb9f32aba1af2eea5604c7ded084a880fb98dabaa39275`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 11.6 KB (11644 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-bookworm`

```console
$ docker pull rust@sha256:8824f00d57259b0b833257532b2a4ec94132d1bf00e4b36e87a56266aff3a40c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:c5000325cce93b58cb94ed7a77c85fa8a35520e6119b10a0d3a0ccc95960cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521828909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bb4f02fb0e8300d16b98188d95219c00741eeaf7deb9be498dcd44a5076f6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c40c3e3cdf945721f480e1d939aac857876fdb5c33b8fbfcf655c63b0b9428`  
		Last Modified: Wed, 24 Apr 2024 04:21:09 GMT  
		Size: 64.1 MB (64142118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05cc1123d7e335d59b0f465c23b7ad2ad27f4875b6c3eab41c65a9b50efa382`  
		Last Modified: Wed, 24 Apr 2024 04:21:45 GMT  
		Size: 211.2 MB (211175606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803b1968af78ef789730661c289a7ec4f7df4e634c9bee1c4837346ca3f4ef27`  
		Last Modified: Wed, 24 Apr 2024 05:12:18 GMT  
		Size: 172.9 MB (172884762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ea2ab75a2c2b231008469686581ab02e095b9fe922c119ade3d1479d3a3cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a288afbc55e2553d0168a7df78f087461c3e1f16288ca208348ce7cc956d6732`

```dockerfile
```

-	Layers:
	-	`sha256:51b060ea2235773d7512609d22d18dc74debf609f249989b35d729c12f6aab34`  
		Last Modified: Wed, 24 Apr 2024 05:12:16 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf815ddf8eb88dfd476d46a5029e837216ec0c685187027d0aefdf4d2eafcab6`  
		Last Modified: Wed, 24 Apr 2024 05:12:15 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:02f414fb213df08e9b7333e1bc6b6197034057b124e931a621fad867f8421ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510038334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef39effc782b510f66eab7f223bcc443fe6b080f53b290010473d523bdf9f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0525f0e8022d3b0295c1e79a86a4f89704f111e1b222a81c92bc1cd11e968380`  
		Last Modified: Fri, 12 Apr 2024 10:10:51 GMT  
		Size: 208.6 MB (208612483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bf7d1b36a17124b80128713cf3d086d5796c86dc372c6282cf498daf6c1395eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1beec69f650b1aebc630728883823a22b7d6678dd70d219c8e0a42fa58672ce`

```dockerfile
```

-	Layers:
	-	`sha256:703cb3fa1a3d5fecd4a490acbbca87494b9e3a268f01c0fcf9d5e3680d83130e`  
		Last Modified: Fri, 12 Apr 2024 10:10:47 GMT  
		Size: 15.2 MB (15176005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9869ff78ed8192003451c3741439e311265dc77f2e68f7449112268e7789237`  
		Last Modified: Fri, 12 Apr 2024 10:10:45 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3160cca3c6dda6fe0ab864a99ac7c140053d5d1eb607de1149d8ddf283291f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581324975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f4049f68d66356001e70d6436c367cca3844efe78889fcc32dc84b7c30c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03d269bebeec78b201e8b34ead41bf134d4d60a7a9487567cdf8c35741b6e6`  
		Last Modified: Thu, 11 Apr 2024 09:06:37 GMT  
		Size: 241.6 MB (241616470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c60bcda0982aaadca0e716b39a6374a61127c1a6de578325b4dd1a522cb7ae9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb01e6329c5de88d432e822441857852f9ab3a22ddb8644d6e833d6c705ee0`

```dockerfile
```

-	Layers:
	-	`sha256:ce8cf433ca365e2b10c8bd5a4abea406fa4f9e3ac157ea49fc5512e07028b8bd`  
		Last Modified: Thu, 11 Apr 2024 09:06:32 GMT  
		Size: 15.4 MB (15398644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3621a57d1464a572d892b6cf38eb44c3744f32365aa7308fb2da4a2e713ffa1`  
		Last Modified: Thu, 11 Apr 2024 09:06:31 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bookworm` - linux; 386

```console
$ docker pull rust@sha256:890ff0201af78ee848b18a52a4f4531488b4e59578aaceb80267d92a5a5b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538602380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dcdd8241e4fbe59faf26d535c41d723ac8d9bc7a5ffc066ce3cc3d6bcd9976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c7b4c0568972903287c2ba295779f478db7fc45d1844ec5d10e22332f4cd1d84`  
		Last Modified: Wed, 24 Apr 2024 03:43:10 GMT  
		Size: 50.6 MB (50602565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba4056eb3a537ebb74fd333c27daceac5385bc3101b6029e706a51de775f00`  
		Last Modified: Wed, 24 Apr 2024 04:41:08 GMT  
		Size: 24.9 MB (24888940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0583cb1d092e1ca2b9a9e9ad274c286cbda7804622a36572a00c3440b4d88`  
		Last Modified: Wed, 24 Apr 2024 04:41:36 GMT  
		Size: 66.0 MB (65989175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4346162f795b064031764e3d351299d91568e9a1cb9ff0ae23d323d99339d1`  
		Last Modified: Wed, 24 Apr 2024 04:42:27 GMT  
		Size: 210.1 MB (210101062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ac1055cd771ed58d7865a880ab6bdb9b418503c9c767d13f68c437558fa46b`  
		Last Modified: Wed, 24 Apr 2024 05:12:29 GMT  
		Size: 187.0 MB (187020638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:97a7f910b863aa2ed9321369136bc22e1676fa469a92973958256b086366154c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08a98dfd4d629087d8353ef923ae123298df4a8a02235b5ed9609d9911589c`

```dockerfile
```

-	Layers:
	-	`sha256:be07c0f3fc84146f8b856092f446a575df879c8175d38ad9587726f5548f7dce`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76565694008f6464d1b540c738ca7df8e8974bac84071148aef50fcdfba095c4`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 13.2 KB (13177 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:3e03cf7b5c139593ad629b57e55624da795a4e789e4826ae88a0ef68a9feed27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551593932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62106ad4d5b838965cd23e3c23325d159f7ba16e3c4a5f525a573b48831d1e4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bf47934b0700489c27f4b1918c464037353ebec2ebc12585ceea997c9a34c71c`  
		Last Modified: Wed, 24 Apr 2024 03:25:57 GMT  
		Size: 53.6 MB (53580168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677be8677970cb6c89d034144a91a8695625d82f32553778be503e17ab5f55b3`  
		Last Modified: Wed, 24 Apr 2024 04:22:57 GMT  
		Size: 25.7 MB (25699777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48162777bb1b177bfa77ee29ba9552a6c899119f959faa64ef54f0a5aab3116`  
		Last Modified: Wed, 24 Apr 2024 04:23:19 GMT  
		Size: 69.6 MB (69584472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e881f9e7d456fa7b2b9e91f26b48776888d7ca1975413e2554119bfef1024`  
		Last Modified: Wed, 24 Apr 2024 04:23:59 GMT  
		Size: 214.2 MB (214213767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1dbcd760ee8f07bc74473682877cfe356c1743a81028d53592a9a203cbfe1d`  
		Last Modified: Thu, 25 Apr 2024 09:37:45 GMT  
		Size: 188.5 MB (188515748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:55139c979bd14dda211e51a3877d62232d3d44423d7a50eccb13987f2a8fc4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028f773eef818abb6e7c12c5785e8f0bc2100c507b72b5a932ab4e3db8b15eb2`

```dockerfile
```

-	Layers:
	-	`sha256:370f05a65fe56210232e2a29f47c225fa190152fce2f2fd2173f04fd6eebe017`  
		Last Modified: Thu, 25 Apr 2024 09:37:40 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c82a7840b4a0f54d7ee75413d11f713e9e9abf3e2ac8616c18bd4b2245f37e1`  
		Last Modified: Thu, 25 Apr 2024 09:37:39 GMT  
		Size: 12.6 KB (12625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-bullseye`

```console
$ docker pull rust@sha256:d651343e195b96bd4304dc33066bddf01f5a173b400df3c917b867a6d1f373d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:ccdf877ab59edf47e838cb586e8b37fd680a49a0a47d76ec4812142f8ab53f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 MB (495324610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce2473fbb694edc3adf51a56951e6455e2f655a776a865bf3d50385554989e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbeb8ef1d906919c518d52a9eb71cedf1ee5c3247b6ea106571a6252d5a4f05`  
		Last Modified: Wed, 24 Apr 2024 04:22:13 GMT  
		Size: 54.6 MB (54589380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e29bc91fb60d9860548fd0c66a11e7a14b5e9417059fd06a35fb120d542ee0`  
		Last Modified: Wed, 24 Apr 2024 04:22:47 GMT  
		Size: 197.0 MB (196986464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e74378906d6fcccfb1da6ff001463c333214d1c0961407017b0d92af11e99c`  
		Last Modified: Wed, 24 Apr 2024 05:12:06 GMT  
		Size: 172.9 MB (172884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:36cae1d27d3ffbeb7555c6e06ed91e6a6918856ccadacace444c64fb29ce5848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14987008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5475ef900d52d6d072e8823424349abe8270e19b3c105e4786bba417fa3f04f2`

```dockerfile
```

-	Layers:
	-	`sha256:e387fd514acb6becdc86178a7dbcd8e2de771419ac6ea9fe70fbadd665d114b2`  
		Last Modified: Wed, 24 Apr 2024 05:12:03 GMT  
		Size: 15.0 MB (14974944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f594e55497c4d0d325d1ac218e2aa59c03166f2e40597564a2214fc39079c6`  
		Last Modified: Wed, 24 Apr 2024 05:12:02 GMT  
		Size: 12.1 KB (12064 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:df9cd31df4d327523202f35516a11da6137aaeda2a08adc293e833a621f32dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491537963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc193a8f3c4651a63b0d0686148c39f44211822b8951a59661f1f806d4ba4d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:eb53aade3ed19f72413045948cad3084902fe630cc20789d2c2b5bc334679575 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23ca580217f1a6b17dba868e7ec34ae7fff221e07640fca532510daca8ed46f6`  
		Last Modified: Wed, 10 Apr 2024 01:04:48 GMT  
		Size: 50.2 MB (50246481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89b030e474718221560707f98fb967bd582bc0f355ca5caf120fc5f25b2d58`  
		Last Modified: Wed, 10 Apr 2024 07:01:21 GMT  
		Size: 14.9 MB (14879245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef8c5cdb2957e3cc1b26c037acafd549c7286845f8007127da85b383702cee3`  
		Last Modified: Wed, 10 Apr 2024 07:01:40 GMT  
		Size: 50.4 MB (50357907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c48f55e50a2918f423e3f80c787998eca4a47eec492d7e81553c5a738f095b`  
		Last Modified: Wed, 10 Apr 2024 07:02:17 GMT  
		Size: 167.4 MB (167441750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d040ff95e5e69aef50846a70d877773fcac32ff0f9d06253de2ae1af716e5734`  
		Last Modified: Fri, 12 Apr 2024 10:08:54 GMT  
		Size: 208.6 MB (208612580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:27e0a1d5194760cbf075370163165605974c9c995ea10b77865e58f93297b83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14787748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af251232f279d9d3d121b812683d85782f17d1bba6e318f2eb262560b385b1f`

```dockerfile
```

-	Layers:
	-	`sha256:b589bde1ab79c3fb90f18abb53e64717165bb517252d9cc4aa98393250dcd3d5`  
		Last Modified: Fri, 12 Apr 2024 10:08:48 GMT  
		Size: 14.8 MB (14776282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c521898116f82ca4982d8062c10f81c24a776f01ecadfc5280e29d90c17d9e03`  
		Last Modified: Fri, 12 Apr 2024 10:08:48 GMT  
		Size: 11.5 KB (11466 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1a3393a2d46c70be9b5f94dbbdad036e81cd4f53d22093a2c5a1b787778ebbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.7 MB (555703379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a93805309b544762c6959305d7a87882f3e00dde2cce0002faf220d1458abd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3f4a530684a6d51e431d14164bdf20c7ad515e8948ddbfbf5f9c2c3680727`  
		Last Modified: Wed, 10 Apr 2024 04:33:00 GMT  
		Size: 15.7 MB (15749239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27317b8832e116e0457de89bfb9097cbcd3165d6079c38230f3728894dfb3af1`  
		Last Modified: Wed, 10 Apr 2024 04:33:14 GMT  
		Size: 54.7 MB (54694342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dceb3c5772a800dd46b1b628a79e2167bd6bb0e9844a04e9ffc8a550a182b`  
		Last Modified: Wed, 10 Apr 2024 04:33:40 GMT  
		Size: 189.9 MB (189914112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f2acf4f3dce2c3a2795f5dca30272ad70e7ee1791a9408f571c2ef4cba93e7`  
		Last Modified: Thu, 11 Apr 2024 09:05:00 GMT  
		Size: 241.6 MB (241616510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c55d4e3706c53b607de807dfe5b67c0a41dfbf3050aeb10e1466a6d6d57794fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14988253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7715d50b671577b7d31dd38c33ffcba338f92fe0787f979fda4ae5eb9cdd792a`

```dockerfile
```

-	Layers:
	-	`sha256:b88b1950f542b58e6a5e7e351442969a5cbc11b8b9addc4ffc305dcf4770bd41`  
		Last Modified: Thu, 11 Apr 2024 09:04:54 GMT  
		Size: 15.0 MB (14976847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90dc2dba9d291701a8e356d68176d87b7608fe5f13cd0bb213154866267432f5`  
		Last Modified: Thu, 11 Apr 2024 09:04:53 GMT  
		Size: 11.4 KB (11406 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bullseye` - linux; 386

```console
$ docker pull rust@sha256:99e80cd2bda0ca76de778c4bc0ba34c74e3de3956965791a351350aa2d53a7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.2 MB (515187676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964c90dd4b2891f01a4fbf7d61d46b5d47d2984449fdb31abed3fb4244ba9810`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:531ff4ee4f75fb0b1990fd185259fbec17670ebea9c3011de30a27e2de08c387`  
		Last Modified: Wed, 24 Apr 2024 03:43:58 GMT  
		Size: 56.1 MB (56076550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76062ffe019e6bfc91f0fe0510211f961184446e120461504dd7066278dbfb88`  
		Last Modified: Wed, 24 Apr 2024 04:42:41 GMT  
		Size: 16.3 MB (16269075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41af9e34185ddf73f8ecb610526409cc80e34f0aab2c2078a0effbe14be251`  
		Last Modified: Wed, 24 Apr 2024 04:43:06 GMT  
		Size: 55.9 MB (55929331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c343ec37d7971f52aa446a2e4bdf1947c24ac26c712f8d041bbde1de773ac`  
		Last Modified: Wed, 24 Apr 2024 04:43:51 GMT  
		Size: 199.9 MB (199892179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb203619e4b4cf64618cfa2c19ee1d65659b90ebdb6c6ee85de5f4da9c02e44c`  
		Last Modified: Wed, 24 Apr 2024 05:59:24 GMT  
		Size: 187.0 MB (187020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8c5065810bf725f4d006d056e2ecb13ca43faa90846226938e6ad83cbe5079ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14975802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07523a23b3c8e37e88a7e8e8a58a73eab78fd2627b3335433f824e07ba2d958`

```dockerfile
```

-	Layers:
	-	`sha256:62a66bf05356563138f65afc0e39dceefd84c1f7aca3fabaf5ecbca321bd679d`  
		Last Modified: Wed, 24 Apr 2024 05:59:20 GMT  
		Size: 15.0 MB (14963767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723a356feef7c199377ac324d03af4e1a42605c331083af3da8610fb9fc106b8`  
		Last Modified: Wed, 24 Apr 2024 05:59:19 GMT  
		Size: 12.0 KB (12035 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:29323ef01bbc112f2626a112df6540115e6815ef07ad2ec4e88aff3821006aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.5 MB (519468840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2151423f0c0c0cae1cc3858001cf459a34880c3542d1dd1ac89df8bb42db01c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:aac3759e46343ae5d9b035355707bd07abf04ff80e3d29e689ea89cc78633190`  
		Last Modified: Wed, 24 Apr 2024 03:27:06 GMT  
		Size: 59.0 MB (58968197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc915aadd544630a28ea807628347805a6b8bc6f250feae34a46f66ac5228d3`  
		Last Modified: Wed, 24 Apr 2024 04:24:14 GMT  
		Size: 16.8 MB (16767223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87809a577847ee55cd1298464ee16a72985d1700dcf4e546db6fca794086d7c7`  
		Last Modified: Wed, 24 Apr 2024 04:24:32 GMT  
		Size: 58.9 MB (58873993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b19380d6722f8bacf55a08edef5ab2bef7d748909aa0109770daf96177909f5`  
		Last Modified: Wed, 24 Apr 2024 04:25:08 GMT  
		Size: 196.3 MB (196343705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628886dc5a2cba117f1a160da40f7cdba890a9661d5b7ebf648b56daa9650bd1`  
		Last Modified: Thu, 25 Apr 2024 09:33:54 GMT  
		Size: 188.5 MB (188515722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:26e50deba46d7e0e49b0734934c375a1505b03dd640bef54ef6e5d182854a987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14953986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f593beaf1e613e4b46c5c999914c44bbcc87f30d78b21507d25d9a6047305dd4`

```dockerfile
```

-	Layers:
	-	`sha256:2e7e2d41aaffd5046784b0118f36fedbbbd9a80fa0e503d16067cade6134667c`  
		Last Modified: Thu, 25 Apr 2024 09:33:50 GMT  
		Size: 14.9 MB (14942547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a42423e593b1e4032328bd8df2924f0976804ba727dd0ae7fb996d9374e10b`  
		Last Modified: Thu, 25 Apr 2024 09:33:49 GMT  
		Size: 11.4 KB (11439 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-buster`

```console
$ docker pull rust@sha256:67afb05ae84c379fd1ef6c2af5a5988ae3a1402f5770b1c433716c3c8dcb2fe7
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

### `rust:1.77-buster` - linux; amd64

```console
$ docker pull rust@sha256:fd9265894ebb1726c08256cb3aacec8f4cb885d1060679f38aea5b912e24294e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.0 MB (484968446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783350f1d2be0610e2730df688417194ca785d80410ffbd196e066bf18264960`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
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
	-	`sha256:191249de5b7ca0b4a8a5b5d8c19f5e94207c98ac4748bbe000d55d4a9c36deaf`  
		Last Modified: Wed, 24 Apr 2024 05:10:48 GMT  
		Size: 172.9 MB (172884715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-buster` - unknown; unknown

```console
$ docker pull rust@sha256:0122d3cb2d238112d8ddf6530059ba7d3c5418e5fe10b6ce6f7bea70c24d5c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15978514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ddd78af473b781391d26953e04b4d00a22822fb134c6f3b616e239638d6039`

```dockerfile
```

-	Layers:
	-	`sha256:21e5e906506b573f52865ef471c93575cacb3df811f226d258e83d35df54893f`  
		Last Modified: Wed, 24 Apr 2024 05:10:43 GMT  
		Size: 16.0 MB (15966858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd656bc775aa85ed1d157d20989d1d938ef91e8ebaacdb1f059dd629824719f7`  
		Last Modified: Wed, 24 Apr 2024 05:10:42 GMT  
		Size: 11.7 KB (11656 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:d2a8509b3be550586f457a19b228cdc2de0b78ab062e7bf4ec198a8745cc21ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486339195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b65f67846b1f7ac4de8b0e6c3b61a864f968b815796c9bd1137d547800904d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:56eb0c1e9a01d2e3320b2f3d897736bfe09ccb53ef1ae8bfea2b9d4099bc1d6b in / 
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
	-	`sha256:300908ef79221077165ff78ff105758d14dd67c42610c4e0aafdd731a920a871`  
		Last Modified: Wed, 10 Apr 2024 01:05:35 GMT  
		Size: 46.0 MB (45962444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a28291d070880fd3bc1d1083c0a3dfd62197b6f8f9b8f0222bebfb7abc3998c`  
		Last Modified: Wed, 10 Apr 2024 07:02:28 GMT  
		Size: 16.2 MB (16217560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df332bea5b985c1c2dd5d35090367d1eeb17f766d81c69c6484a9dbdfb6a2a19`  
		Last Modified: Wed, 10 Apr 2024 07:02:46 GMT  
		Size: 47.4 MB (47411064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c429ea890a21b115686f06bcd8e64b77317af15fee22637d21494c7f7e8763`  
		Last Modified: Wed, 10 Apr 2024 07:03:24 GMT  
		Size: 168.1 MB (168135545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a8d87914e90936da310261b7cf6db3b8d4cd941ac36d01a329b6a539b8532d`  
		Last Modified: Fri, 12 Apr 2024 10:07:00 GMT  
		Size: 208.6 MB (208612582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-buster` - unknown; unknown

```console
$ docker pull rust@sha256:8d3df22872c5331a3b7dbd9ef6776ffeeed758d67b5577d16a3e9b04a5d2ac9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15423342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8934156cede7d8af64415e272e84c840fb7ae69b9a7fd35fa465ab349febf8`

```dockerfile
```

-	Layers:
	-	`sha256:7211e52e2624ee2d88410d49e28e0f8c9429402417cdc964037fc456623a6a1c`  
		Last Modified: Fri, 12 Apr 2024 10:06:55 GMT  
		Size: 15.4 MB (15412281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4bf7ecccbc2c3b7f1330ab90fab736d6467f54ca700dd24fb2e920cbdcb0fc`  
		Last Modified: Fri, 12 Apr 2024 10:06:54 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3f1b8288a64eaa661ef9d21d57965a6ce3af9c7fe1d4cf6eace903500c4d82e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544120500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c11826c12adf7e8e962ae839db1d4ea5e82b9df9958790153e5ac1b78711a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
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
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91b3908edaca8722a607f2265f615c82feb05f6440b5b8deab683e5f1338bfa`  
		Last Modified: Thu, 11 Apr 2024 09:03:31 GMT  
		Size: 241.6 MB (241616460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-buster` - unknown; unknown

```console
$ docker pull rust@sha256:1c1f949dcf2838a090f86a1847cac48ad01397a9edb0dff68e89d7193b0f9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15611975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ea129f23fc50bb965c6144abce71a0e69eccaf6989544d846c1ace9998e5a7`

```dockerfile
```

-	Layers:
	-	`sha256:df58017d086478c7376b7b37cf7f31b66e6987fa8f4fb639435f3daf7f77fe3f`  
		Last Modified: Thu, 11 Apr 2024 09:03:26 GMT  
		Size: 15.6 MB (15600976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174e8feb82f898148915b77b182fc9e1913079b6a09d883054bedac9a05eda6f`  
		Last Modified: Thu, 11 Apr 2024 09:03:26 GMT  
		Size: 11.0 KB (10999 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-buster` - linux; 386

```console
$ docker pull rust@sha256:505bfca6bd398b4f00fce2ca2f2557b66aee0f09794144211116711a68f26b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.5 MB (508529720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe99a8ac5417c69838900906c1c7e30fbb0e60dfee7d690412859cdc78e7c42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:5f943bcdbbb65accdf0b3bc452a1d4fafd2c64a9c6f6b3010b2a7ca20bedef36 in / 
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
	-	`sha256:1b3962c4dea2d1d71b72cea574044d31a38d535a42183f4cd4993e6868c8de0d`  
		Last Modified: Wed, 24 Apr 2024 05:59:21 GMT  
		Size: 187.0 MB (187020738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-buster` - unknown; unknown

```console
$ docker pull rust@sha256:14cc95a3b98a58a84c3b868c33797396615d28771f00ae4f18b86a4442ffe7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15984068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb23ba590670f34ed24d660fea07e3e81a4b7efc98779effadb10adcebae634`

```dockerfile
```

-	Layers:
	-	`sha256:4400aa22d51411366132ed581c0eceaf6d4506634547b51715e0a2e460edda3e`  
		Last Modified: Wed, 24 Apr 2024 05:59:15 GMT  
		Size: 16.0 MB (15972439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6736ab863825c83fd0375286ca8c26322fa3921013d3db8f900b976c99982a4`  
		Last Modified: Wed, 24 Apr 2024 05:59:15 GMT  
		Size: 11.6 KB (11629 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-slim`

```console
$ docker pull rust@sha256:a8f04112cc1892451320b241b0fe7c074d506de026ad7d96162c8482f9b8ce1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77-slim` - linux; amd64

```console
$ docker pull rust@sha256:638e3590f320c70f5edbfe1842d42ae385624f8c6071f91037d465e7bf7178f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272626407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226d76b23659549e4748842478c0207ab5f79656c520fcb856f4eb235de0bfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12808888e0a2157cb0269632bdee49433c9f8556ccda1464afb6f94479129ead`  
		Last Modified: Wed, 24 Apr 2024 05:13:05 GMT  
		Size: 243.5 MB (243475928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5040f97f4a64566983b901b8fb9eae5ed9a1d4da8aa370cdff68de72249c4cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b52883aa5b9709eca3de616ddcc0c58126a33c1e0528ef6ff5f9a703697301c`

```dockerfile
```

-	Layers:
	-	`sha256:40a7699dc460633d2771085a3dc0e3d6f9aeb38030c5cd7a573799fae19a1fe4`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd14237218530973d0aee254a672a5a6fff80aab1f6eec85a9333d25355e634`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:8cfe44ff0e1d69b947a70df0359e48b4b7e1057d7c8849788ac4ef4da4f26a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd61a2122260688f839cbd2b8f940fd85eb6213d9be0561bc99d9d127dbbda89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd18c5ddc627e06a0ca56860a2c399710c2100cb5c189b0fabbe66dfb32f175`  
		Last Modified: Thu, 25 Apr 2024 00:16:57 GMT  
		Size: 256.2 MB (256248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim` - unknown; unknown

```console
$ docker pull rust@sha256:9fb4006e0666af50e2d9d516f1ee5bd14c6e8ee24e685e8f6c1066a72baf6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cc6bf9290ed472822b7c279a1146749b547500ed2b17cf92162d46ee0be09b`

```dockerfile
```

-	Layers:
	-	`sha256:7b7c864d459efcb9dcd68176e945b29238d18677fbf26fc97e155f5372e39a80`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65818ca85b37143c261fa4ff5bc754b1d6efb29dd4fa5a388c8c41cf9ef1b2d6`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 12.8 KB (12752 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fe4252019e0facdc82bd032d22eb0d1c4ca58f5c3540356840ea3f9a15b79c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336641733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738a4a3e15b336c497f51dd0341cebd130f98fc5e6ea5546d50463e3985f0f70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014c3ccaea43ce9fd3e3c56ffefc4fcc50ba52d2cac23c5776e1533bb9e7f634`  
		Last Modified: Wed, 10 Apr 2024 21:20:56 GMT  
		Size: 307.5 MB (307479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4bd8788f5359ae12cb9bc1acc434ae90d51e6f7cd825268f70daa6bf97d2325d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003752c0fbdb6817f01a5ce924bea0fc77facd03291bd1bcd89b48034b53a37e`

```dockerfile
```

-	Layers:
	-	`sha256:a43e77b376b0764e2dd70d8f2bb3d33a1e3e3ed5dc88c771d83fa0525ca92868`  
		Last Modified: Wed, 10 Apr 2024 21:20:49 GMT  
		Size: 3.9 MB (3941346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bcfee754885be41d14895386082b6d75a7631863a2b3174b1fb4e7ea77225d`  
		Last Modified: Wed, 10 Apr 2024 21:20:48 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim` - linux; 386

```console
$ docker pull rust@sha256:08523c621a2f1d85417842ce00b1b9a42cae8216c42f87e18bdc421c713f7aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284576083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4981314b33e7ff1620efe817f2d72fc26a1c68c6a8a0c469c3bea63aa9b7a03c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad09fde316fe0e55a14718d6a0e81c083b2f8db66b02507b77a68117757c57a`  
		Last Modified: Wed, 24 Apr 2024 05:12:53 GMT  
		Size: 254.4 MB (254412900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim` - unknown; unknown

```console
$ docker pull rust@sha256:99ae02c25a1e078ad005a0fb13a480de4139db49eac3e367c19f9a19b1042c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a8378609675925b2f4b4b20f668ce4dc84d34f24b2cb8a26d32ce28a92535`

```dockerfile
```

-	Layers:
	-	`sha256:38704fffa432b9b8793aae63e4759b2f6b2f6e2bedf5dcd36d4c4fe39829037a`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da465366a30fda81b5c80fb19fa525c3093aa9fa32f0046ab820b871c201439f`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 12.8 KB (12769 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:189bd571f7eda5c3a23b70cbc343ed2cf7a24f72403e602fb71217cf569c94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290203818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31abbd30af48b3f5e0705a87cc896e94c40e7105e2d56fc679a29fefe8d8f9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27733677c7e7ffa3ae36f75ea55eca558d3b1535be93b58e60e358a3fa368deb`  
		Last Modified: Thu, 25 Apr 2024 09:39:52 GMT  
		Size: 257.1 MB (257062617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim` - unknown; unknown

```console
$ docker pull rust@sha256:850f59e79459f30440637f4f653d198d566176041d523a4ae01cb0498e12a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da07cd9aab3aa522fedda7cf41f03250557c862c629dc3a085cca69325b9aa`

```dockerfile
```

-	Layers:
	-	`sha256:aa0002bfc1a0d55e006eb61a57f2ec44a70a0758f0e5b78d46e00d75476b9ec6`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068a9188948e8d6cc2034275e59e9515d1cb420e57eda3a7f9a3600fb6039d21`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-slim-bookworm`

```console
$ docker pull rust@sha256:a8f04112cc1892451320b241b0fe7c074d506de026ad7d96162c8482f9b8ce1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:638e3590f320c70f5edbfe1842d42ae385624f8c6071f91037d465e7bf7178f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272626407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226d76b23659549e4748842478c0207ab5f79656c520fcb856f4eb235de0bfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12808888e0a2157cb0269632bdee49433c9f8556ccda1464afb6f94479129ead`  
		Last Modified: Wed, 24 Apr 2024 05:13:05 GMT  
		Size: 243.5 MB (243475928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5040f97f4a64566983b901b8fb9eae5ed9a1d4da8aa370cdff68de72249c4cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b52883aa5b9709eca3de616ddcc0c58126a33c1e0528ef6ff5f9a703697301c`

```dockerfile
```

-	Layers:
	-	`sha256:40a7699dc460633d2771085a3dc0e3d6f9aeb38030c5cd7a573799fae19a1fe4`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd14237218530973d0aee254a672a5a6fff80aab1f6eec85a9333d25355e634`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:8cfe44ff0e1d69b947a70df0359e48b4b7e1057d7c8849788ac4ef4da4f26a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd61a2122260688f839cbd2b8f940fd85eb6213d9be0561bc99d9d127dbbda89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd18c5ddc627e06a0ca56860a2c399710c2100cb5c189b0fabbe66dfb32f175`  
		Last Modified: Thu, 25 Apr 2024 00:16:57 GMT  
		Size: 256.2 MB (256248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9fb4006e0666af50e2d9d516f1ee5bd14c6e8ee24e685e8f6c1066a72baf6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cc6bf9290ed472822b7c279a1146749b547500ed2b17cf92162d46ee0be09b`

```dockerfile
```

-	Layers:
	-	`sha256:7b7c864d459efcb9dcd68176e945b29238d18677fbf26fc97e155f5372e39a80`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65818ca85b37143c261fa4ff5bc754b1d6efb29dd4fa5a388c8c41cf9ef1b2d6`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 12.8 KB (12752 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fe4252019e0facdc82bd032d22eb0d1c4ca58f5c3540356840ea3f9a15b79c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336641733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738a4a3e15b336c497f51dd0341cebd130f98fc5e6ea5546d50463e3985f0f70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014c3ccaea43ce9fd3e3c56ffefc4fcc50ba52d2cac23c5776e1533bb9e7f634`  
		Last Modified: Wed, 10 Apr 2024 21:20:56 GMT  
		Size: 307.5 MB (307479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4bd8788f5359ae12cb9bc1acc434ae90d51e6f7cd825268f70daa6bf97d2325d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003752c0fbdb6817f01a5ce924bea0fc77facd03291bd1bcd89b48034b53a37e`

```dockerfile
```

-	Layers:
	-	`sha256:a43e77b376b0764e2dd70d8f2bb3d33a1e3e3ed5dc88c771d83fa0525ca92868`  
		Last Modified: Wed, 10 Apr 2024 21:20:49 GMT  
		Size: 3.9 MB (3941346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bcfee754885be41d14895386082b6d75a7631863a2b3174b1fb4e7ea77225d`  
		Last Modified: Wed, 10 Apr 2024 21:20:48 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:08523c621a2f1d85417842ce00b1b9a42cae8216c42f87e18bdc421c713f7aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284576083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4981314b33e7ff1620efe817f2d72fc26a1c68c6a8a0c469c3bea63aa9b7a03c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad09fde316fe0e55a14718d6a0e81c083b2f8db66b02507b77a68117757c57a`  
		Last Modified: Wed, 24 Apr 2024 05:12:53 GMT  
		Size: 254.4 MB (254412900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:99ae02c25a1e078ad005a0fb13a480de4139db49eac3e367c19f9a19b1042c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a8378609675925b2f4b4b20f668ce4dc84d34f24b2cb8a26d32ce28a92535`

```dockerfile
```

-	Layers:
	-	`sha256:38704fffa432b9b8793aae63e4759b2f6b2f6e2bedf5dcd36d4c4fe39829037a`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da465366a30fda81b5c80fb19fa525c3093aa9fa32f0046ab820b871c201439f`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 12.8 KB (12769 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:189bd571f7eda5c3a23b70cbc343ed2cf7a24f72403e602fb71217cf569c94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290203818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31abbd30af48b3f5e0705a87cc896e94c40e7105e2d56fc679a29fefe8d8f9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27733677c7e7ffa3ae36f75ea55eca558d3b1535be93b58e60e358a3fa368deb`  
		Last Modified: Thu, 25 Apr 2024 09:39:52 GMT  
		Size: 257.1 MB (257062617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:850f59e79459f30440637f4f653d198d566176041d523a4ae01cb0498e12a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da07cd9aab3aa522fedda7cf41f03250557c862c629dc3a085cca69325b9aa`

```dockerfile
```

-	Layers:
	-	`sha256:aa0002bfc1a0d55e006eb61a57f2ec44a70a0758f0e5b78d46e00d75476b9ec6`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068a9188948e8d6cc2034275e59e9515d1cb420e57eda3a7f9a3600fb6039d21`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-slim-bullseye`

```console
$ docker pull rust@sha256:caca164937940b63e2ae6292b2507fe6c2feec7fc17fe958f182eab8af018b84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:43ea72d42d2c038ea843c9b41316622f86f5374dc6dfb82a037587761a04b849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264265732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9e28bbeb4bfd6d136fe79aa0822e42176d77fd24f75c05e8458b105546c898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c309d2cedf4817a559551782149cdca9318d0a6c23018b97523a0fe91857f`  
		Last Modified: Wed, 24 Apr 2024 05:11:46 GMT  
		Size: 232.8 MB (232831469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8b95d9eb6aa93d0dc9fb69ff759960ed6ca6dffc91099527b5f001a00f624d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053dac136f29cad1cf8460c926ae37b678819959d2a4d6f351e2d57c76b04680`

```dockerfile
```

-	Layers:
	-	`sha256:3bf84e83a418f557d6b1f21933fed9e3f861d44845045ea89e0dbcb27c9bc330`  
		Last Modified: Wed, 24 Apr 2024 05:11:41 GMT  
		Size: 4.1 MB (4139833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf51e74c2bf86d87b3bd5677d94c687071178480fd648aa0c64a816c4ed6e0a`  
		Last Modified: Wed, 24 Apr 2024 05:11:41 GMT  
		Size: 11.6 KB (11630 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d87bd027a2ec897941ff0f691413f27f6ab798f47ffd1c6954fd687bf58928f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277276352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c859469ac3ba60ce123589a9d56e54f17c194a61ee18931acfd7e3133b2aec9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d54685378a8d57ac36e4ff6a2c342ac52809f585a7d4c8fb662229230e65ce`  
		Last Modified: Thu, 25 Apr 2024 00:15:07 GMT  
		Size: 250.7 MB (250681610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3ceebf9c5462589e2d813246b8a8b6852d230b823549fe33fbab50984fca842e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8625ff2e32464e91cc3d770313871c50321ca890b2a17a4e0a2092840860cd`

```dockerfile
```

-	Layers:
	-	`sha256:f5d89aa7dc719b61e8b5071c3b29c385557d01a1d8ded536e3e3559ebf05078e`  
		Last Modified: Thu, 25 Apr 2024 00:15:01 GMT  
		Size: 3.9 MB (3949756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9151d79ca50c92149bee7df68a8e9b97ed397aedf889f6cbd71f43a42f9f1d6`  
		Last Modified: Thu, 25 Apr 2024 00:15:01 GMT  
		Size: 11.5 KB (11533 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4c5434f97e2e831215a9c5ed5abdf21894ad3c1e7f85f3661cc20c4f1d5fdcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327435048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3e88fc0ee536589d8ff9f84db749baeb19f637ca9d3ca26f872061af6ab348`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ffe28413ff737e9319fc6b161f92951752ebcccd38ff443b7b7a1bf7c46ec`  
		Last Modified: Wed, 10 Apr 2024 21:19:30 GMT  
		Size: 297.4 MB (297358742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:07546376e3d6ff97ef9245f0ddf9c23c2343abfcfc0d612ecd603355351e4fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b9a0d3926f551a4aa8aa4b4aa20168cbead544a81f98131d46e0b3d74339b3`

```dockerfile
```

-	Layers:
	-	`sha256:80783504581f38a49f386edba09b9cd5153392c5ad0174015ef551f090f4452b`  
		Last Modified: Wed, 10 Apr 2024 21:19:23 GMT  
		Size: 4.1 MB (4136557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:333d3575ff26376a87ab3ee97463a3424ff3ef7b03e78b7c28d8433a6e4586b9`  
		Last Modified: Wed, 10 Apr 2024 21:19:23 GMT  
		Size: 11.5 KB (11469 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:9d5d2ddfdd6a58b18bb7f0b8e5f8f37047f9ea8f1e2aa50dbcd4977bab58cd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280018615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbfbb115c7bc121e9f0e8a7827e251c41349a8bd1984a1e769d5c0374d67939`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37221a01bece8cf821897f51b65bd44350746155d325214a918695731a66d3f`  
		Last Modified: Wed, 24 Apr 2024 05:12:24 GMT  
		Size: 247.6 MB (247593842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:790c11b457e330245a08ee08368b80c4f9ba2376cd04a83d8c1281b66b8c95ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31aebfaf8b74b4087da8d50d05aab6f15d452168841659b66338f8cdefa27db2`

```dockerfile
```

-	Layers:
	-	`sha256:7ded81c8554c4a76e11a1920802c6a674e41a6c19c84a7a708cb38fde0d159c8`  
		Last Modified: Wed, 24 Apr 2024 05:12:19 GMT  
		Size: 4.1 MB (4131887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86498619bcaaa39fefc2150c322446a6fcf7367d267078da6811a589fe3d3977`  
		Last Modified: Wed, 24 Apr 2024 05:12:19 GMT  
		Size: 11.6 KB (11601 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:d1fbaf1eb7c480f19373691dee46b7333091e312a0067cfff60e4f88125b1a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278620161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0eb2329b60e7b7a4c321b3eb186e7e8291157920a4c927c5b1239dcd290362`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1effd22b3d858125536254bd2d670cd1a720ea963a5f5b9a6295f1cf04c849f2`  
		Last Modified: Thu, 25 Apr 2024 09:35:52 GMT  
		Size: 243.3 MB (243308436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6c908c45ab479e9a650293593a45d8210151cc0acedb0d2b98bd1874afc7b2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ca374cdff5e57bddc8583419f72f992120d629a52de5d00744829a915b1da9`

```dockerfile
```

-	Layers:
	-	`sha256:409c6f41b6182bd1869c433f7aab4744d5fc0538822f779fc042144d994129ad`  
		Last Modified: Thu, 25 Apr 2024 09:35:46 GMT  
		Size: 4.1 MB (4100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020f597651f5972b28de5ed540ee23e227c15cab9910914b31894c8c48ed893f`  
		Last Modified: Thu, 25 Apr 2024 09:35:46 GMT  
		Size: 11.5 KB (11500 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-slim-buster`

```console
$ docker pull rust@sha256:c52682b3c2455ba53083c61fc7d888d9e5c05af0e9f1720cedfcccf9681fa1f5
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

### `rust:1.77-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:e07c7817a1f8c56703b7c838c9a1d935ff5564981ab688fa9e5fe8a90e281234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245641279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fede2e811700e9b934388f903e43604d03cb4b02baa1b22f9e413087e23b6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b134fdd9ab24eec74b1973bea2fd971ba7966b53832863f2203aab5b1d6f89d`  
		Last Modified: Wed, 24 Apr 2024 05:10:28 GMT  
		Size: 218.3 MB (218303704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e5f87c411463e875b33cd48735d0289a9f7360541f0a7e32517cdd0a524b74c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45862094e4737de29467a79fec0a29be59819e15e997285078a0863166b3f96f`

```dockerfile
```

-	Layers:
	-	`sha256:d67cbeec45f86edc9afc54108da384643c40148c2fcf4dfc1693ed69d478a260`  
		Last Modified: Wed, 24 Apr 2024 05:10:24 GMT  
		Size: 3.9 MB (3941693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6058ee49cb0823ba46e949353f949deae7132061fb1b1b6c1a08016edfff47f`  
		Last Modified: Wed, 24 Apr 2024 05:10:24 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:06c1a08af5dabc4454b1cc105c607d4d06c9b0814db93873ff926a1ee1ef7b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264467965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4b9e3843b862fb3d9313d353d263101bf53a6b5d8b5e5fc90bf323760a9189`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f904fd6bf6b41f2fa9b506f896ebdbe821cd028a693fdf7968eacbc7b23da79f`  
		Last Modified: Thu, 25 Apr 2024 00:13:15 GMT  
		Size: 241.5 MB (241522901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e89bf36198f7184854a7500fc86b2d9017d6dec89f9311e71ecc44493f5ea944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492e0ecf007f0e2320b0b6564175d11a3d1f73d3402844e54236f518ce9eee78`

```dockerfile
```

-	Layers:
	-	`sha256:34f4a9c71e486a6edc1e06711c9c2d0e0a73aac8cc3987e71e5a681711ebaada`  
		Last Modified: Thu, 25 Apr 2024 00:13:09 GMT  
		Size: 3.7 MB (3749343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fa92b499139c82ddeb20b2d912bdeb136fcb250880b3abb0507ed48c61ef2b`  
		Last Modified: Thu, 25 Apr 2024 00:13:09 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3d47794cfa590e602f949345fc56267448530e64cf207ba79a4a8ebb82dd5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307822239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b58e4d35c7954b401373ee5f917c051f71d431fa6428121ce81b12148ab192`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81eb727fb6d6e4fe3e3a1ca3b615eb88245d64c5376a62e8bf275616c3c6cbb`  
		Last Modified: Wed, 10 Apr 2024 21:18:05 GMT  
		Size: 281.9 MB (281858778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:2628255e922502afd4e4aa0c4e30f4a26a1866d57111adb0984f7099d6b6549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1ff19d2b3c12e6fa257c298f2817debf02d8779e528210e136f9067dea6452`

```dockerfile
```

-	Layers:
	-	`sha256:152b56576a1f9f73de903d5f06d63ced13edd3b6f90bbb2d7ed9e780766cbae4`  
		Last Modified: Wed, 10 Apr 2024 21:17:59 GMT  
		Size: 3.6 MB (3574733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ce6be4574a6a214b953ebd2d8aa8c578da1ee01ca9ee50a67e6c3e5064b46c`  
		Last Modified: Wed, 10 Apr 2024 21:17:58 GMT  
		Size: 11.1 KB (11063 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:03a4f59dd317b964c56e75b84763dc831da494e3ec21fd36ae34348eecbcbd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265011000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8693b85bfe42d16b6f845d8e99d4a830f075c232156916f63ad424ad023a5ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:32f0f06baa0e4f10bff55aaa215b511838432ecc5fe547373d9ac99494556801 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:204b51fc41806ed93b4ccb6ce8272fa49b5f0b099ba6e3b5a940a9e7cd3ce202`  
		Last Modified: Wed, 24 Apr 2024 03:45:03 GMT  
		Size: 28.0 MB (27994678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bbd5edd24ae790e1053c99262c3c1062e6a89592bd6cccc53fef0b1e87e5a0`  
		Last Modified: Wed, 24 Apr 2024 05:10:57 GMT  
		Size: 237.0 MB (237016322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e45b1cd901a13a4ce4276a8780227951cd768d74e51877fec136f5906be660cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883ed62f0760eff19d06298c55f6a6eb27a6b79873ea0a37ccbe2f0b6defd196`

```dockerfile
```

-	Layers:
	-	`sha256:cda5f4adc3ed394903a5491d8b6ca36016e55f666a851196b374d2075686d8a9`  
		Last Modified: Wed, 24 Apr 2024 05:10:52 GMT  
		Size: 3.9 MB (3948318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4b9dd3825cdc912de170e8e5e11c701ebb88ea3e6ff82af59b8053cdd2b527`  
		Last Modified: Wed, 24 Apr 2024 05:10:51 GMT  
		Size: 11.2 KB (11195 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2`

```console
$ docker pull rust@sha256:8824f00d57259b0b833257532b2a4ec94132d1bf00e4b36e87a56266aff3a40c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77.2` - linux; amd64

```console
$ docker pull rust@sha256:c5000325cce93b58cb94ed7a77c85fa8a35520e6119b10a0d3a0ccc95960cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521828909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bb4f02fb0e8300d16b98188d95219c00741eeaf7deb9be498dcd44a5076f6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c40c3e3cdf945721f480e1d939aac857876fdb5c33b8fbfcf655c63b0b9428`  
		Last Modified: Wed, 24 Apr 2024 04:21:09 GMT  
		Size: 64.1 MB (64142118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05cc1123d7e335d59b0f465c23b7ad2ad27f4875b6c3eab41c65a9b50efa382`  
		Last Modified: Wed, 24 Apr 2024 04:21:45 GMT  
		Size: 211.2 MB (211175606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803b1968af78ef789730661c289a7ec4f7df4e634c9bee1c4837346ca3f4ef27`  
		Last Modified: Wed, 24 Apr 2024 05:12:18 GMT  
		Size: 172.9 MB (172884762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2` - unknown; unknown

```console
$ docker pull rust@sha256:8ea2ab75a2c2b231008469686581ab02e095b9fe922c119ade3d1479d3a3cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a288afbc55e2553d0168a7df78f087461c3e1f16288ca208348ce7cc956d6732`

```dockerfile
```

-	Layers:
	-	`sha256:51b060ea2235773d7512609d22d18dc74debf609f249989b35d729c12f6aab34`  
		Last Modified: Wed, 24 Apr 2024 05:12:16 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf815ddf8eb88dfd476d46a5029e837216ec0c685187027d0aefdf4d2eafcab6`  
		Last Modified: Wed, 24 Apr 2024 05:12:15 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2` - linux; arm variant v7

```console
$ docker pull rust@sha256:02f414fb213df08e9b7333e1bc6b6197034057b124e931a621fad867f8421ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510038334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef39effc782b510f66eab7f223bcc443fe6b080f53b290010473d523bdf9f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0525f0e8022d3b0295c1e79a86a4f89704f111e1b222a81c92bc1cd11e968380`  
		Last Modified: Fri, 12 Apr 2024 10:10:51 GMT  
		Size: 208.6 MB (208612483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2` - unknown; unknown

```console
$ docker pull rust@sha256:bf7d1b36a17124b80128713cf3d086d5796c86dc372c6282cf498daf6c1395eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1beec69f650b1aebc630728883823a22b7d6678dd70d219c8e0a42fa58672ce`

```dockerfile
```

-	Layers:
	-	`sha256:703cb3fa1a3d5fecd4a490acbbca87494b9e3a268f01c0fcf9d5e3680d83130e`  
		Last Modified: Fri, 12 Apr 2024 10:10:47 GMT  
		Size: 15.2 MB (15176005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9869ff78ed8192003451c3741439e311265dc77f2e68f7449112268e7789237`  
		Last Modified: Fri, 12 Apr 2024 10:10:45 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3160cca3c6dda6fe0ab864a99ac7c140053d5d1eb607de1149d8ddf283291f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581324975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f4049f68d66356001e70d6436c367cca3844efe78889fcc32dc84b7c30c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03d269bebeec78b201e8b34ead41bf134d4d60a7a9487567cdf8c35741b6e6`  
		Last Modified: Thu, 11 Apr 2024 09:06:37 GMT  
		Size: 241.6 MB (241616470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2` - unknown; unknown

```console
$ docker pull rust@sha256:c60bcda0982aaadca0e716b39a6374a61127c1a6de578325b4dd1a522cb7ae9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb01e6329c5de88d432e822441857852f9ab3a22ddb8644d6e833d6c705ee0`

```dockerfile
```

-	Layers:
	-	`sha256:ce8cf433ca365e2b10c8bd5a4abea406fa4f9e3ac157ea49fc5512e07028b8bd`  
		Last Modified: Thu, 11 Apr 2024 09:06:32 GMT  
		Size: 15.4 MB (15398644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3621a57d1464a572d892b6cf38eb44c3744f32365aa7308fb2da4a2e713ffa1`  
		Last Modified: Thu, 11 Apr 2024 09:06:31 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2` - linux; 386

```console
$ docker pull rust@sha256:890ff0201af78ee848b18a52a4f4531488b4e59578aaceb80267d92a5a5b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538602380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dcdd8241e4fbe59faf26d535c41d723ac8d9bc7a5ffc066ce3cc3d6bcd9976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c7b4c0568972903287c2ba295779f478db7fc45d1844ec5d10e22332f4cd1d84`  
		Last Modified: Wed, 24 Apr 2024 03:43:10 GMT  
		Size: 50.6 MB (50602565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba4056eb3a537ebb74fd333c27daceac5385bc3101b6029e706a51de775f00`  
		Last Modified: Wed, 24 Apr 2024 04:41:08 GMT  
		Size: 24.9 MB (24888940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0583cb1d092e1ca2b9a9e9ad274c286cbda7804622a36572a00c3440b4d88`  
		Last Modified: Wed, 24 Apr 2024 04:41:36 GMT  
		Size: 66.0 MB (65989175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4346162f795b064031764e3d351299d91568e9a1cb9ff0ae23d323d99339d1`  
		Last Modified: Wed, 24 Apr 2024 04:42:27 GMT  
		Size: 210.1 MB (210101062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ac1055cd771ed58d7865a880ab6bdb9b418503c9c767d13f68c437558fa46b`  
		Last Modified: Wed, 24 Apr 2024 05:12:29 GMT  
		Size: 187.0 MB (187020638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2` - unknown; unknown

```console
$ docker pull rust@sha256:97a7f910b863aa2ed9321369136bc22e1676fa469a92973958256b086366154c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08a98dfd4d629087d8353ef923ae123298df4a8a02235b5ed9609d9911589c`

```dockerfile
```

-	Layers:
	-	`sha256:be07c0f3fc84146f8b856092f446a575df879c8175d38ad9587726f5548f7dce`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76565694008f6464d1b540c738ca7df8e8974bac84071148aef50fcdfba095c4`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 13.2 KB (13177 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2` - linux; ppc64le

```console
$ docker pull rust@sha256:3e03cf7b5c139593ad629b57e55624da795a4e789e4826ae88a0ef68a9feed27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551593932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62106ad4d5b838965cd23e3c23325d159f7ba16e3c4a5f525a573b48831d1e4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bf47934b0700489c27f4b1918c464037353ebec2ebc12585ceea997c9a34c71c`  
		Last Modified: Wed, 24 Apr 2024 03:25:57 GMT  
		Size: 53.6 MB (53580168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677be8677970cb6c89d034144a91a8695625d82f32553778be503e17ab5f55b3`  
		Last Modified: Wed, 24 Apr 2024 04:22:57 GMT  
		Size: 25.7 MB (25699777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48162777bb1b177bfa77ee29ba9552a6c899119f959faa64ef54f0a5aab3116`  
		Last Modified: Wed, 24 Apr 2024 04:23:19 GMT  
		Size: 69.6 MB (69584472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e881f9e7d456fa7b2b9e91f26b48776888d7ca1975413e2554119bfef1024`  
		Last Modified: Wed, 24 Apr 2024 04:23:59 GMT  
		Size: 214.2 MB (214213767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1dbcd760ee8f07bc74473682877cfe356c1743a81028d53592a9a203cbfe1d`  
		Last Modified: Thu, 25 Apr 2024 09:37:45 GMT  
		Size: 188.5 MB (188515748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2` - unknown; unknown

```console
$ docker pull rust@sha256:55139c979bd14dda211e51a3877d62232d3d44423d7a50eccb13987f2a8fc4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028f773eef818abb6e7c12c5785e8f0bc2100c507b72b5a932ab4e3db8b15eb2`

```dockerfile
```

-	Layers:
	-	`sha256:370f05a65fe56210232e2a29f47c225fa190152fce2f2fd2173f04fd6eebe017`  
		Last Modified: Thu, 25 Apr 2024 09:37:40 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c82a7840b4a0f54d7ee75413d11f713e9e9abf3e2ac8616c18bd4b2245f37e1`  
		Last Modified: Thu, 25 Apr 2024 09:37:39 GMT  
		Size: 12.6 KB (12625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-alpine`

```console
$ docker pull rust@sha256:9b74675247503eb0c3e3831dfdf10985c254b3ba9aa9a36eac8917f912a134eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.77.2-alpine` - linux; amd64

```console
$ docker pull rust@sha256:dc037af6f82e10c9862879cfe7dcbeb883b23092013b3a1df295512a4ade5d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272492183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d9a62b548d2deef025a80cbb517fcdaab56526b8cfc88d0ef4ab90b8dab39d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f170ecb6344abd22a40dfedc95278fed4a73a9409a285b6a31c6994b8097ab`  
		Last Modified: Tue, 09 Apr 2024 23:50:39 GMT  
		Size: 55.3 MB (55346790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150084451e7317de7972997b74d7d7b3a6947e9e01a1a3cd1a3b799e8348208`  
		Last Modified: Tue, 09 Apr 2024 23:50:42 GMT  
		Size: 213.7 MB (213736664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:65412a414e6e29d6f1c17de3346d8babf260891f011363110e2ef9d34763d2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e244aa001a61ab57db8fdbd3135b351cc3c55962ee776136e5af23d4b0a303ee`

```dockerfile
```

-	Layers:
	-	`sha256:4e63ddf0710f8dcc924c71396e2f3b39819922b0db63df53204e50c9b9c396a6`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 710.6 KB (710617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4861d7790f28e1d13f2037ee5c69a885431a65a224621e3a0915312ccd1038`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 11.8 KB (11792 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d30747064955669d4e48ece7dc69776bf05abe2ffa4eb866314bc842f9231936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278817954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd976a496d7d864344a2b39dad2155dbb9ef5d526f06ac412d4a3e2a37cb0be1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651ca114e522c42e6bb17953edf4a18bba82fe2287f93e32f6b3957ff901c2`  
		Last Modified: Sat, 16 Mar 2024 17:12:47 GMT  
		Size: 53.0 MB (52970287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157aaa1f3fa9784926886cafbadb1c30dcd160078deb54be2c6a6b7452ba670`  
		Last Modified: Wed, 10 Apr 2024 00:03:58 GMT  
		Size: 222.5 MB (222499952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:07fcac075e46cdcd0b7ad2a6c17d6d167910b8b9e827ccef0d73092dd6f12499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.2 KB (753242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f9b404804f7716cd3fce2e04dae7f19c8620b407f12a708e1f3f9cd944f9e`

```dockerfile
```

-	Layers:
	-	`sha256:4c6e25bf8fa604c97f277fd247f3614d3c6a8a1844f4cb78b3c466115463a60c`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 741.6 KB (741598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233de60c24dbdbc3fdcb9f32aba1af2eea5604c7ded084a880fb98dabaa39275`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 11.6 KB (11644 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-alpine3.18`

```console
$ docker pull rust@sha256:b8f4f707c6460f4228deecdcc4acdfc50045fa7396f8aec732dc4ea322a41066
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.77.2-alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:f5762f07bc2d9d6699afb162b7f35dfa48e5945cf4395b4f9b9d6826cb1d3c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268673214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d5e3a7dd699641a0c6368e65fad736d7c583359096663c1e4bf5e98b85d5a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f914773acc6db8be08970614a0ed0f5fce71828723bfcb6e6cf1d97a26c284eb`  
		Last Modified: Tue, 09 Apr 2024 23:50:41 GMT  
		Size: 51.5 MB (51534043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0af00c163854d8ec5ea9d8a150960293bfd4aa34804a7a160ef80f44ce71d`  
		Last Modified: Tue, 09 Apr 2024 23:50:44 GMT  
		Size: 213.7 MB (213736629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:9bfd12461323300ebd4c975ebc91a40d5949fa914272a2abe34315cac6c58c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49a20d1e055b2d8dcd9f1dc20fe467a5b977e5e797847f63adebc0d7732c718`

```dockerfile
```

-	Layers:
	-	`sha256:d549196acdb3131a3a009a32ec149198450da016167ecb17316ed5105a440284`  
		Last Modified: Tue, 09 Apr 2024 23:50:40 GMT  
		Size: 701.9 KB (701886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff0d60c39141b47c8ebf94551e1235d461f65e03b68df4a8ae19688754cc60b`  
		Last Modified: Tue, 09 Apr 2024 23:50:40 GMT  
		Size: 10.6 KB (10588 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3a178840b556deece46aeea0e6f3029a9bf525530b5eba1f6037531c098947a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271899543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78a508d74d054080dc4bcea6dc7bd9819bd806d6bfd06910138e6c94e384e19`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b1cd0d662b55abd28904427ae8befdb37b765cf7ff19dc4a587c51429117c7`  
		Last Modified: Sat, 16 Mar 2024 17:11:39 GMT  
		Size: 46.1 MB (46066359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a88ea76700e9b87c7238a55b12f22030ed622804d3c18cd00497bbf3d9760d`  
		Last Modified: Wed, 10 Apr 2024 00:02:53 GMT  
		Size: 222.5 MB (222499823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:bf2d6cdc43bc8c6f6942a7e2a4eec7dd93b4f8a2e51b5cdee8f402c636b252d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.2 KB (747167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd7d1515764e16148a0a685fa2c88831a6e8bae26f370009e24a37eb15c52f1`

```dockerfile
```

-	Layers:
	-	`sha256:817ff20e322fc42973b1489c74c9d5e24420023ac7706158646e0c8187ea53d9`  
		Last Modified: Wed, 10 Apr 2024 00:02:48 GMT  
		Size: 736.7 KB (736735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff708420c480e2a3ada601eacf662d093335bbf3c2b624e814c55dd24d3d368`  
		Last Modified: Wed, 10 Apr 2024 00:02:48 GMT  
		Size: 10.4 KB (10432 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-alpine3.19`

```console
$ docker pull rust@sha256:9b74675247503eb0c3e3831dfdf10985c254b3ba9aa9a36eac8917f912a134eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.77.2-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:dc037af6f82e10c9862879cfe7dcbeb883b23092013b3a1df295512a4ade5d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272492183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d9a62b548d2deef025a80cbb517fcdaab56526b8cfc88d0ef4ab90b8dab39d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f170ecb6344abd22a40dfedc95278fed4a73a9409a285b6a31c6994b8097ab`  
		Last Modified: Tue, 09 Apr 2024 23:50:39 GMT  
		Size: 55.3 MB (55346790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150084451e7317de7972997b74d7d7b3a6947e9e01a1a3cd1a3b799e8348208`  
		Last Modified: Tue, 09 Apr 2024 23:50:42 GMT  
		Size: 213.7 MB (213736664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:65412a414e6e29d6f1c17de3346d8babf260891f011363110e2ef9d34763d2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e244aa001a61ab57db8fdbd3135b351cc3c55962ee776136e5af23d4b0a303ee`

```dockerfile
```

-	Layers:
	-	`sha256:4e63ddf0710f8dcc924c71396e2f3b39819922b0db63df53204e50c9b9c396a6`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 710.6 KB (710617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4861d7790f28e1d13f2037ee5c69a885431a65a224621e3a0915312ccd1038`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 11.8 KB (11792 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d30747064955669d4e48ece7dc69776bf05abe2ffa4eb866314bc842f9231936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278817954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd976a496d7d864344a2b39dad2155dbb9ef5d526f06ac412d4a3e2a37cb0be1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651ca114e522c42e6bb17953edf4a18bba82fe2287f93e32f6b3957ff901c2`  
		Last Modified: Sat, 16 Mar 2024 17:12:47 GMT  
		Size: 53.0 MB (52970287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157aaa1f3fa9784926886cafbadb1c30dcd160078deb54be2c6a6b7452ba670`  
		Last Modified: Wed, 10 Apr 2024 00:03:58 GMT  
		Size: 222.5 MB (222499952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:07fcac075e46cdcd0b7ad2a6c17d6d167910b8b9e827ccef0d73092dd6f12499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.2 KB (753242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f9b404804f7716cd3fce2e04dae7f19c8620b407f12a708e1f3f9cd944f9e`

```dockerfile
```

-	Layers:
	-	`sha256:4c6e25bf8fa604c97f277fd247f3614d3c6a8a1844f4cb78b3c466115463a60c`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 741.6 KB (741598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233de60c24dbdbc3fdcb9f32aba1af2eea5604c7ded084a880fb98dabaa39275`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 11.6 KB (11644 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-bookworm`

```console
$ docker pull rust@sha256:8824f00d57259b0b833257532b2a4ec94132d1bf00e4b36e87a56266aff3a40c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77.2-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:c5000325cce93b58cb94ed7a77c85fa8a35520e6119b10a0d3a0ccc95960cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521828909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bb4f02fb0e8300d16b98188d95219c00741eeaf7deb9be498dcd44a5076f6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c40c3e3cdf945721f480e1d939aac857876fdb5c33b8fbfcf655c63b0b9428`  
		Last Modified: Wed, 24 Apr 2024 04:21:09 GMT  
		Size: 64.1 MB (64142118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05cc1123d7e335d59b0f465c23b7ad2ad27f4875b6c3eab41c65a9b50efa382`  
		Last Modified: Wed, 24 Apr 2024 04:21:45 GMT  
		Size: 211.2 MB (211175606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803b1968af78ef789730661c289a7ec4f7df4e634c9bee1c4837346ca3f4ef27`  
		Last Modified: Wed, 24 Apr 2024 05:12:18 GMT  
		Size: 172.9 MB (172884762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ea2ab75a2c2b231008469686581ab02e095b9fe922c119ade3d1479d3a3cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a288afbc55e2553d0168a7df78f087461c3e1f16288ca208348ce7cc956d6732`

```dockerfile
```

-	Layers:
	-	`sha256:51b060ea2235773d7512609d22d18dc74debf609f249989b35d729c12f6aab34`  
		Last Modified: Wed, 24 Apr 2024 05:12:16 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf815ddf8eb88dfd476d46a5029e837216ec0c685187027d0aefdf4d2eafcab6`  
		Last Modified: Wed, 24 Apr 2024 05:12:15 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:02f414fb213df08e9b7333e1bc6b6197034057b124e931a621fad867f8421ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510038334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef39effc782b510f66eab7f223bcc443fe6b080f53b290010473d523bdf9f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0525f0e8022d3b0295c1e79a86a4f89704f111e1b222a81c92bc1cd11e968380`  
		Last Modified: Fri, 12 Apr 2024 10:10:51 GMT  
		Size: 208.6 MB (208612483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bf7d1b36a17124b80128713cf3d086d5796c86dc372c6282cf498daf6c1395eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1beec69f650b1aebc630728883823a22b7d6678dd70d219c8e0a42fa58672ce`

```dockerfile
```

-	Layers:
	-	`sha256:703cb3fa1a3d5fecd4a490acbbca87494b9e3a268f01c0fcf9d5e3680d83130e`  
		Last Modified: Fri, 12 Apr 2024 10:10:47 GMT  
		Size: 15.2 MB (15176005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9869ff78ed8192003451c3741439e311265dc77f2e68f7449112268e7789237`  
		Last Modified: Fri, 12 Apr 2024 10:10:45 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3160cca3c6dda6fe0ab864a99ac7c140053d5d1eb607de1149d8ddf283291f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581324975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f4049f68d66356001e70d6436c367cca3844efe78889fcc32dc84b7c30c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03d269bebeec78b201e8b34ead41bf134d4d60a7a9487567cdf8c35741b6e6`  
		Last Modified: Thu, 11 Apr 2024 09:06:37 GMT  
		Size: 241.6 MB (241616470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c60bcda0982aaadca0e716b39a6374a61127c1a6de578325b4dd1a522cb7ae9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb01e6329c5de88d432e822441857852f9ab3a22ddb8644d6e833d6c705ee0`

```dockerfile
```

-	Layers:
	-	`sha256:ce8cf433ca365e2b10c8bd5a4abea406fa4f9e3ac157ea49fc5512e07028b8bd`  
		Last Modified: Thu, 11 Apr 2024 09:06:32 GMT  
		Size: 15.4 MB (15398644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3621a57d1464a572d892b6cf38eb44c3744f32365aa7308fb2da4a2e713ffa1`  
		Last Modified: Thu, 11 Apr 2024 09:06:31 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bookworm` - linux; 386

```console
$ docker pull rust@sha256:890ff0201af78ee848b18a52a4f4531488b4e59578aaceb80267d92a5a5b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538602380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dcdd8241e4fbe59faf26d535c41d723ac8d9bc7a5ffc066ce3cc3d6bcd9976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c7b4c0568972903287c2ba295779f478db7fc45d1844ec5d10e22332f4cd1d84`  
		Last Modified: Wed, 24 Apr 2024 03:43:10 GMT  
		Size: 50.6 MB (50602565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba4056eb3a537ebb74fd333c27daceac5385bc3101b6029e706a51de775f00`  
		Last Modified: Wed, 24 Apr 2024 04:41:08 GMT  
		Size: 24.9 MB (24888940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0583cb1d092e1ca2b9a9e9ad274c286cbda7804622a36572a00c3440b4d88`  
		Last Modified: Wed, 24 Apr 2024 04:41:36 GMT  
		Size: 66.0 MB (65989175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4346162f795b064031764e3d351299d91568e9a1cb9ff0ae23d323d99339d1`  
		Last Modified: Wed, 24 Apr 2024 04:42:27 GMT  
		Size: 210.1 MB (210101062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ac1055cd771ed58d7865a880ab6bdb9b418503c9c767d13f68c437558fa46b`  
		Last Modified: Wed, 24 Apr 2024 05:12:29 GMT  
		Size: 187.0 MB (187020638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:97a7f910b863aa2ed9321369136bc22e1676fa469a92973958256b086366154c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08a98dfd4d629087d8353ef923ae123298df4a8a02235b5ed9609d9911589c`

```dockerfile
```

-	Layers:
	-	`sha256:be07c0f3fc84146f8b856092f446a575df879c8175d38ad9587726f5548f7dce`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76565694008f6464d1b540c738ca7df8e8974bac84071148aef50fcdfba095c4`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 13.2 KB (13177 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:3e03cf7b5c139593ad629b57e55624da795a4e789e4826ae88a0ef68a9feed27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551593932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62106ad4d5b838965cd23e3c23325d159f7ba16e3c4a5f525a573b48831d1e4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bf47934b0700489c27f4b1918c464037353ebec2ebc12585ceea997c9a34c71c`  
		Last Modified: Wed, 24 Apr 2024 03:25:57 GMT  
		Size: 53.6 MB (53580168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677be8677970cb6c89d034144a91a8695625d82f32553778be503e17ab5f55b3`  
		Last Modified: Wed, 24 Apr 2024 04:22:57 GMT  
		Size: 25.7 MB (25699777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48162777bb1b177bfa77ee29ba9552a6c899119f959faa64ef54f0a5aab3116`  
		Last Modified: Wed, 24 Apr 2024 04:23:19 GMT  
		Size: 69.6 MB (69584472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e881f9e7d456fa7b2b9e91f26b48776888d7ca1975413e2554119bfef1024`  
		Last Modified: Wed, 24 Apr 2024 04:23:59 GMT  
		Size: 214.2 MB (214213767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1dbcd760ee8f07bc74473682877cfe356c1743a81028d53592a9a203cbfe1d`  
		Last Modified: Thu, 25 Apr 2024 09:37:45 GMT  
		Size: 188.5 MB (188515748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:55139c979bd14dda211e51a3877d62232d3d44423d7a50eccb13987f2a8fc4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028f773eef818abb6e7c12c5785e8f0bc2100c507b72b5a932ab4e3db8b15eb2`

```dockerfile
```

-	Layers:
	-	`sha256:370f05a65fe56210232e2a29f47c225fa190152fce2f2fd2173f04fd6eebe017`  
		Last Modified: Thu, 25 Apr 2024 09:37:40 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c82a7840b4a0f54d7ee75413d11f713e9e9abf3e2ac8616c18bd4b2245f37e1`  
		Last Modified: Thu, 25 Apr 2024 09:37:39 GMT  
		Size: 12.6 KB (12625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-bullseye`

```console
$ docker pull rust@sha256:d651343e195b96bd4304dc33066bddf01f5a173b400df3c917b867a6d1f373d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77.2-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:ccdf877ab59edf47e838cb586e8b37fd680a49a0a47d76ec4812142f8ab53f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 MB (495324610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce2473fbb694edc3adf51a56951e6455e2f655a776a865bf3d50385554989e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbeb8ef1d906919c518d52a9eb71cedf1ee5c3247b6ea106571a6252d5a4f05`  
		Last Modified: Wed, 24 Apr 2024 04:22:13 GMT  
		Size: 54.6 MB (54589380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e29bc91fb60d9860548fd0c66a11e7a14b5e9417059fd06a35fb120d542ee0`  
		Last Modified: Wed, 24 Apr 2024 04:22:47 GMT  
		Size: 197.0 MB (196986464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e74378906d6fcccfb1da6ff001463c333214d1c0961407017b0d92af11e99c`  
		Last Modified: Wed, 24 Apr 2024 05:12:06 GMT  
		Size: 172.9 MB (172884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:36cae1d27d3ffbeb7555c6e06ed91e6a6918856ccadacace444c64fb29ce5848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14987008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5475ef900d52d6d072e8823424349abe8270e19b3c105e4786bba417fa3f04f2`

```dockerfile
```

-	Layers:
	-	`sha256:e387fd514acb6becdc86178a7dbcd8e2de771419ac6ea9fe70fbadd665d114b2`  
		Last Modified: Wed, 24 Apr 2024 05:12:03 GMT  
		Size: 15.0 MB (14974944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f594e55497c4d0d325d1ac218e2aa59c03166f2e40597564a2214fc39079c6`  
		Last Modified: Wed, 24 Apr 2024 05:12:02 GMT  
		Size: 12.1 KB (12064 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:df9cd31df4d327523202f35516a11da6137aaeda2a08adc293e833a621f32dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491537963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc193a8f3c4651a63b0d0686148c39f44211822b8951a59661f1f806d4ba4d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:eb53aade3ed19f72413045948cad3084902fe630cc20789d2c2b5bc334679575 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23ca580217f1a6b17dba868e7ec34ae7fff221e07640fca532510daca8ed46f6`  
		Last Modified: Wed, 10 Apr 2024 01:04:48 GMT  
		Size: 50.2 MB (50246481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89b030e474718221560707f98fb967bd582bc0f355ca5caf120fc5f25b2d58`  
		Last Modified: Wed, 10 Apr 2024 07:01:21 GMT  
		Size: 14.9 MB (14879245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef8c5cdb2957e3cc1b26c037acafd549c7286845f8007127da85b383702cee3`  
		Last Modified: Wed, 10 Apr 2024 07:01:40 GMT  
		Size: 50.4 MB (50357907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c48f55e50a2918f423e3f80c787998eca4a47eec492d7e81553c5a738f095b`  
		Last Modified: Wed, 10 Apr 2024 07:02:17 GMT  
		Size: 167.4 MB (167441750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d040ff95e5e69aef50846a70d877773fcac32ff0f9d06253de2ae1af716e5734`  
		Last Modified: Fri, 12 Apr 2024 10:08:54 GMT  
		Size: 208.6 MB (208612580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:27e0a1d5194760cbf075370163165605974c9c995ea10b77865e58f93297b83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14787748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af251232f279d9d3d121b812683d85782f17d1bba6e318f2eb262560b385b1f`

```dockerfile
```

-	Layers:
	-	`sha256:b589bde1ab79c3fb90f18abb53e64717165bb517252d9cc4aa98393250dcd3d5`  
		Last Modified: Fri, 12 Apr 2024 10:08:48 GMT  
		Size: 14.8 MB (14776282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c521898116f82ca4982d8062c10f81c24a776f01ecadfc5280e29d90c17d9e03`  
		Last Modified: Fri, 12 Apr 2024 10:08:48 GMT  
		Size: 11.5 KB (11466 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1a3393a2d46c70be9b5f94dbbdad036e81cd4f53d22093a2c5a1b787778ebbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.7 MB (555703379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a93805309b544762c6959305d7a87882f3e00dde2cce0002faf220d1458abd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3f4a530684a6d51e431d14164bdf20c7ad515e8948ddbfbf5f9c2c3680727`  
		Last Modified: Wed, 10 Apr 2024 04:33:00 GMT  
		Size: 15.7 MB (15749239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27317b8832e116e0457de89bfb9097cbcd3165d6079c38230f3728894dfb3af1`  
		Last Modified: Wed, 10 Apr 2024 04:33:14 GMT  
		Size: 54.7 MB (54694342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dceb3c5772a800dd46b1b628a79e2167bd6bb0e9844a04e9ffc8a550a182b`  
		Last Modified: Wed, 10 Apr 2024 04:33:40 GMT  
		Size: 189.9 MB (189914112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f2acf4f3dce2c3a2795f5dca30272ad70e7ee1791a9408f571c2ef4cba93e7`  
		Last Modified: Thu, 11 Apr 2024 09:05:00 GMT  
		Size: 241.6 MB (241616510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c55d4e3706c53b607de807dfe5b67c0a41dfbf3050aeb10e1466a6d6d57794fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14988253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7715d50b671577b7d31dd38c33ffcba338f92fe0787f979fda4ae5eb9cdd792a`

```dockerfile
```

-	Layers:
	-	`sha256:b88b1950f542b58e6a5e7e351442969a5cbc11b8b9addc4ffc305dcf4770bd41`  
		Last Modified: Thu, 11 Apr 2024 09:04:54 GMT  
		Size: 15.0 MB (14976847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90dc2dba9d291701a8e356d68176d87b7608fe5f13cd0bb213154866267432f5`  
		Last Modified: Thu, 11 Apr 2024 09:04:53 GMT  
		Size: 11.4 KB (11406 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bullseye` - linux; 386

```console
$ docker pull rust@sha256:99e80cd2bda0ca76de778c4bc0ba34c74e3de3956965791a351350aa2d53a7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.2 MB (515187676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964c90dd4b2891f01a4fbf7d61d46b5d47d2984449fdb31abed3fb4244ba9810`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:531ff4ee4f75fb0b1990fd185259fbec17670ebea9c3011de30a27e2de08c387`  
		Last Modified: Wed, 24 Apr 2024 03:43:58 GMT  
		Size: 56.1 MB (56076550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76062ffe019e6bfc91f0fe0510211f961184446e120461504dd7066278dbfb88`  
		Last Modified: Wed, 24 Apr 2024 04:42:41 GMT  
		Size: 16.3 MB (16269075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41af9e34185ddf73f8ecb610526409cc80e34f0aab2c2078a0effbe14be251`  
		Last Modified: Wed, 24 Apr 2024 04:43:06 GMT  
		Size: 55.9 MB (55929331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c343ec37d7971f52aa446a2e4bdf1947c24ac26c712f8d041bbde1de773ac`  
		Last Modified: Wed, 24 Apr 2024 04:43:51 GMT  
		Size: 199.9 MB (199892179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb203619e4b4cf64618cfa2c19ee1d65659b90ebdb6c6ee85de5f4da9c02e44c`  
		Last Modified: Wed, 24 Apr 2024 05:59:24 GMT  
		Size: 187.0 MB (187020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8c5065810bf725f4d006d056e2ecb13ca43faa90846226938e6ad83cbe5079ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14975802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07523a23b3c8e37e88a7e8e8a58a73eab78fd2627b3335433f824e07ba2d958`

```dockerfile
```

-	Layers:
	-	`sha256:62a66bf05356563138f65afc0e39dceefd84c1f7aca3fabaf5ecbca321bd679d`  
		Last Modified: Wed, 24 Apr 2024 05:59:20 GMT  
		Size: 15.0 MB (14963767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723a356feef7c199377ac324d03af4e1a42605c331083af3da8610fb9fc106b8`  
		Last Modified: Wed, 24 Apr 2024 05:59:19 GMT  
		Size: 12.0 KB (12035 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:29323ef01bbc112f2626a112df6540115e6815ef07ad2ec4e88aff3821006aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.5 MB (519468840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2151423f0c0c0cae1cc3858001cf459a34880c3542d1dd1ac89df8bb42db01c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:aac3759e46343ae5d9b035355707bd07abf04ff80e3d29e689ea89cc78633190`  
		Last Modified: Wed, 24 Apr 2024 03:27:06 GMT  
		Size: 59.0 MB (58968197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc915aadd544630a28ea807628347805a6b8bc6f250feae34a46f66ac5228d3`  
		Last Modified: Wed, 24 Apr 2024 04:24:14 GMT  
		Size: 16.8 MB (16767223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87809a577847ee55cd1298464ee16a72985d1700dcf4e546db6fca794086d7c7`  
		Last Modified: Wed, 24 Apr 2024 04:24:32 GMT  
		Size: 58.9 MB (58873993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b19380d6722f8bacf55a08edef5ab2bef7d748909aa0109770daf96177909f5`  
		Last Modified: Wed, 24 Apr 2024 04:25:08 GMT  
		Size: 196.3 MB (196343705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628886dc5a2cba117f1a160da40f7cdba890a9661d5b7ebf648b56daa9650bd1`  
		Last Modified: Thu, 25 Apr 2024 09:33:54 GMT  
		Size: 188.5 MB (188515722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:26e50deba46d7e0e49b0734934c375a1505b03dd640bef54ef6e5d182854a987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14953986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f593beaf1e613e4b46c5c999914c44bbcc87f30d78b21507d25d9a6047305dd4`

```dockerfile
```

-	Layers:
	-	`sha256:2e7e2d41aaffd5046784b0118f36fedbbbd9a80fa0e503d16067cade6134667c`  
		Last Modified: Thu, 25 Apr 2024 09:33:50 GMT  
		Size: 14.9 MB (14942547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a42423e593b1e4032328bd8df2924f0976804ba727dd0ae7fb996d9374e10b`  
		Last Modified: Thu, 25 Apr 2024 09:33:49 GMT  
		Size: 11.4 KB (11439 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-buster`

```console
$ docker pull rust@sha256:67afb05ae84c379fd1ef6c2af5a5988ae3a1402f5770b1c433716c3c8dcb2fe7
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

### `rust:1.77.2-buster` - linux; amd64

```console
$ docker pull rust@sha256:fd9265894ebb1726c08256cb3aacec8f4cb885d1060679f38aea5b912e24294e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.0 MB (484968446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783350f1d2be0610e2730df688417194ca785d80410ffbd196e066bf18264960`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
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
	-	`sha256:191249de5b7ca0b4a8a5b5d8c19f5e94207c98ac4748bbe000d55d4a9c36deaf`  
		Last Modified: Wed, 24 Apr 2024 05:10:48 GMT  
		Size: 172.9 MB (172884715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-buster` - unknown; unknown

```console
$ docker pull rust@sha256:0122d3cb2d238112d8ddf6530059ba7d3c5418e5fe10b6ce6f7bea70c24d5c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15978514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ddd78af473b781391d26953e04b4d00a22822fb134c6f3b616e239638d6039`

```dockerfile
```

-	Layers:
	-	`sha256:21e5e906506b573f52865ef471c93575cacb3df811f226d258e83d35df54893f`  
		Last Modified: Wed, 24 Apr 2024 05:10:43 GMT  
		Size: 16.0 MB (15966858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd656bc775aa85ed1d157d20989d1d938ef91e8ebaacdb1f059dd629824719f7`  
		Last Modified: Wed, 24 Apr 2024 05:10:42 GMT  
		Size: 11.7 KB (11656 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:d2a8509b3be550586f457a19b228cdc2de0b78ab062e7bf4ec198a8745cc21ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486339195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b65f67846b1f7ac4de8b0e6c3b61a864f968b815796c9bd1137d547800904d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:56eb0c1e9a01d2e3320b2f3d897736bfe09ccb53ef1ae8bfea2b9d4099bc1d6b in / 
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
	-	`sha256:300908ef79221077165ff78ff105758d14dd67c42610c4e0aafdd731a920a871`  
		Last Modified: Wed, 10 Apr 2024 01:05:35 GMT  
		Size: 46.0 MB (45962444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a28291d070880fd3bc1d1083c0a3dfd62197b6f8f9b8f0222bebfb7abc3998c`  
		Last Modified: Wed, 10 Apr 2024 07:02:28 GMT  
		Size: 16.2 MB (16217560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df332bea5b985c1c2dd5d35090367d1eeb17f766d81c69c6484a9dbdfb6a2a19`  
		Last Modified: Wed, 10 Apr 2024 07:02:46 GMT  
		Size: 47.4 MB (47411064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c429ea890a21b115686f06bcd8e64b77317af15fee22637d21494c7f7e8763`  
		Last Modified: Wed, 10 Apr 2024 07:03:24 GMT  
		Size: 168.1 MB (168135545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a8d87914e90936da310261b7cf6db3b8d4cd941ac36d01a329b6a539b8532d`  
		Last Modified: Fri, 12 Apr 2024 10:07:00 GMT  
		Size: 208.6 MB (208612582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-buster` - unknown; unknown

```console
$ docker pull rust@sha256:8d3df22872c5331a3b7dbd9ef6776ffeeed758d67b5577d16a3e9b04a5d2ac9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15423342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8934156cede7d8af64415e272e84c840fb7ae69b9a7fd35fa465ab349febf8`

```dockerfile
```

-	Layers:
	-	`sha256:7211e52e2624ee2d88410d49e28e0f8c9429402417cdc964037fc456623a6a1c`  
		Last Modified: Fri, 12 Apr 2024 10:06:55 GMT  
		Size: 15.4 MB (15412281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4bf7ecccbc2c3b7f1330ab90fab736d6467f54ca700dd24fb2e920cbdcb0fc`  
		Last Modified: Fri, 12 Apr 2024 10:06:54 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3f1b8288a64eaa661ef9d21d57965a6ce3af9c7fe1d4cf6eace903500c4d82e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544120500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c11826c12adf7e8e962ae839db1d4ea5e82b9df9958790153e5ac1b78711a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
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
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91b3908edaca8722a607f2265f615c82feb05f6440b5b8deab683e5f1338bfa`  
		Last Modified: Thu, 11 Apr 2024 09:03:31 GMT  
		Size: 241.6 MB (241616460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-buster` - unknown; unknown

```console
$ docker pull rust@sha256:1c1f949dcf2838a090f86a1847cac48ad01397a9edb0dff68e89d7193b0f9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15611975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ea129f23fc50bb965c6144abce71a0e69eccaf6989544d846c1ace9998e5a7`

```dockerfile
```

-	Layers:
	-	`sha256:df58017d086478c7376b7b37cf7f31b66e6987fa8f4fb639435f3daf7f77fe3f`  
		Last Modified: Thu, 11 Apr 2024 09:03:26 GMT  
		Size: 15.6 MB (15600976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174e8feb82f898148915b77b182fc9e1913079b6a09d883054bedac9a05eda6f`  
		Last Modified: Thu, 11 Apr 2024 09:03:26 GMT  
		Size: 11.0 KB (10999 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-buster` - linux; 386

```console
$ docker pull rust@sha256:505bfca6bd398b4f00fce2ca2f2557b66aee0f09794144211116711a68f26b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.5 MB (508529720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe99a8ac5417c69838900906c1c7e30fbb0e60dfee7d690412859cdc78e7c42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:5f943bcdbbb65accdf0b3bc452a1d4fafd2c64a9c6f6b3010b2a7ca20bedef36 in / 
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
	-	`sha256:1b3962c4dea2d1d71b72cea574044d31a38d535a42183f4cd4993e6868c8de0d`  
		Last Modified: Wed, 24 Apr 2024 05:59:21 GMT  
		Size: 187.0 MB (187020738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-buster` - unknown; unknown

```console
$ docker pull rust@sha256:14cc95a3b98a58a84c3b868c33797396615d28771f00ae4f18b86a4442ffe7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15984068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb23ba590670f34ed24d660fea07e3e81a4b7efc98779effadb10adcebae634`

```dockerfile
```

-	Layers:
	-	`sha256:4400aa22d51411366132ed581c0eceaf6d4506634547b51715e0a2e460edda3e`  
		Last Modified: Wed, 24 Apr 2024 05:59:15 GMT  
		Size: 16.0 MB (15972439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6736ab863825c83fd0375286ca8c26322fa3921013d3db8f900b976c99982a4`  
		Last Modified: Wed, 24 Apr 2024 05:59:15 GMT  
		Size: 11.6 KB (11629 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-slim`

```console
$ docker pull rust@sha256:a8f04112cc1892451320b241b0fe7c074d506de026ad7d96162c8482f9b8ce1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77.2-slim` - linux; amd64

```console
$ docker pull rust@sha256:638e3590f320c70f5edbfe1842d42ae385624f8c6071f91037d465e7bf7178f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272626407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226d76b23659549e4748842478c0207ab5f79656c520fcb856f4eb235de0bfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12808888e0a2157cb0269632bdee49433c9f8556ccda1464afb6f94479129ead`  
		Last Modified: Wed, 24 Apr 2024 05:13:05 GMT  
		Size: 243.5 MB (243475928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim` - unknown; unknown

```console
$ docker pull rust@sha256:5040f97f4a64566983b901b8fb9eae5ed9a1d4da8aa370cdff68de72249c4cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b52883aa5b9709eca3de616ddcc0c58126a33c1e0528ef6ff5f9a703697301c`

```dockerfile
```

-	Layers:
	-	`sha256:40a7699dc460633d2771085a3dc0e3d6f9aeb38030c5cd7a573799fae19a1fe4`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd14237218530973d0aee254a672a5a6fff80aab1f6eec85a9333d25355e634`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:8cfe44ff0e1d69b947a70df0359e48b4b7e1057d7c8849788ac4ef4da4f26a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd61a2122260688f839cbd2b8f940fd85eb6213d9be0561bc99d9d127dbbda89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd18c5ddc627e06a0ca56860a2c399710c2100cb5c189b0fabbe66dfb32f175`  
		Last Modified: Thu, 25 Apr 2024 00:16:57 GMT  
		Size: 256.2 MB (256248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim` - unknown; unknown

```console
$ docker pull rust@sha256:9fb4006e0666af50e2d9d516f1ee5bd14c6e8ee24e685e8f6c1066a72baf6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cc6bf9290ed472822b7c279a1146749b547500ed2b17cf92162d46ee0be09b`

```dockerfile
```

-	Layers:
	-	`sha256:7b7c864d459efcb9dcd68176e945b29238d18677fbf26fc97e155f5372e39a80`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65818ca85b37143c261fa4ff5bc754b1d6efb29dd4fa5a388c8c41cf9ef1b2d6`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 12.8 KB (12752 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fe4252019e0facdc82bd032d22eb0d1c4ca58f5c3540356840ea3f9a15b79c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336641733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738a4a3e15b336c497f51dd0341cebd130f98fc5e6ea5546d50463e3985f0f70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014c3ccaea43ce9fd3e3c56ffefc4fcc50ba52d2cac23c5776e1533bb9e7f634`  
		Last Modified: Wed, 10 Apr 2024 21:20:56 GMT  
		Size: 307.5 MB (307479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim` - unknown; unknown

```console
$ docker pull rust@sha256:4bd8788f5359ae12cb9bc1acc434ae90d51e6f7cd825268f70daa6bf97d2325d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003752c0fbdb6817f01a5ce924bea0fc77facd03291bd1bcd89b48034b53a37e`

```dockerfile
```

-	Layers:
	-	`sha256:a43e77b376b0764e2dd70d8f2bb3d33a1e3e3ed5dc88c771d83fa0525ca92868`  
		Last Modified: Wed, 10 Apr 2024 21:20:49 GMT  
		Size: 3.9 MB (3941346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bcfee754885be41d14895386082b6d75a7631863a2b3174b1fb4e7ea77225d`  
		Last Modified: Wed, 10 Apr 2024 21:20:48 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim` - linux; 386

```console
$ docker pull rust@sha256:08523c621a2f1d85417842ce00b1b9a42cae8216c42f87e18bdc421c713f7aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284576083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4981314b33e7ff1620efe817f2d72fc26a1c68c6a8a0c469c3bea63aa9b7a03c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad09fde316fe0e55a14718d6a0e81c083b2f8db66b02507b77a68117757c57a`  
		Last Modified: Wed, 24 Apr 2024 05:12:53 GMT  
		Size: 254.4 MB (254412900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim` - unknown; unknown

```console
$ docker pull rust@sha256:99ae02c25a1e078ad005a0fb13a480de4139db49eac3e367c19f9a19b1042c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a8378609675925b2f4b4b20f668ce4dc84d34f24b2cb8a26d32ce28a92535`

```dockerfile
```

-	Layers:
	-	`sha256:38704fffa432b9b8793aae63e4759b2f6b2f6e2bedf5dcd36d4c4fe39829037a`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da465366a30fda81b5c80fb19fa525c3093aa9fa32f0046ab820b871c201439f`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 12.8 KB (12769 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:189bd571f7eda5c3a23b70cbc343ed2cf7a24f72403e602fb71217cf569c94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290203818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31abbd30af48b3f5e0705a87cc896e94c40e7105e2d56fc679a29fefe8d8f9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27733677c7e7ffa3ae36f75ea55eca558d3b1535be93b58e60e358a3fa368deb`  
		Last Modified: Thu, 25 Apr 2024 09:39:52 GMT  
		Size: 257.1 MB (257062617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim` - unknown; unknown

```console
$ docker pull rust@sha256:850f59e79459f30440637f4f653d198d566176041d523a4ae01cb0498e12a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da07cd9aab3aa522fedda7cf41f03250557c862c629dc3a085cca69325b9aa`

```dockerfile
```

-	Layers:
	-	`sha256:aa0002bfc1a0d55e006eb61a57f2ec44a70a0758f0e5b78d46e00d75476b9ec6`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068a9188948e8d6cc2034275e59e9515d1cb420e57eda3a7f9a3600fb6039d21`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-slim-bookworm`

```console
$ docker pull rust@sha256:a8f04112cc1892451320b241b0fe7c074d506de026ad7d96162c8482f9b8ce1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77.2-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:638e3590f320c70f5edbfe1842d42ae385624f8c6071f91037d465e7bf7178f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272626407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226d76b23659549e4748842478c0207ab5f79656c520fcb856f4eb235de0bfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12808888e0a2157cb0269632bdee49433c9f8556ccda1464afb6f94479129ead`  
		Last Modified: Wed, 24 Apr 2024 05:13:05 GMT  
		Size: 243.5 MB (243475928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5040f97f4a64566983b901b8fb9eae5ed9a1d4da8aa370cdff68de72249c4cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b52883aa5b9709eca3de616ddcc0c58126a33c1e0528ef6ff5f9a703697301c`

```dockerfile
```

-	Layers:
	-	`sha256:40a7699dc460633d2771085a3dc0e3d6f9aeb38030c5cd7a573799fae19a1fe4`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd14237218530973d0aee254a672a5a6fff80aab1f6eec85a9333d25355e634`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:8cfe44ff0e1d69b947a70df0359e48b4b7e1057d7c8849788ac4ef4da4f26a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd61a2122260688f839cbd2b8f940fd85eb6213d9be0561bc99d9d127dbbda89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd18c5ddc627e06a0ca56860a2c399710c2100cb5c189b0fabbe66dfb32f175`  
		Last Modified: Thu, 25 Apr 2024 00:16:57 GMT  
		Size: 256.2 MB (256248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9fb4006e0666af50e2d9d516f1ee5bd14c6e8ee24e685e8f6c1066a72baf6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cc6bf9290ed472822b7c279a1146749b547500ed2b17cf92162d46ee0be09b`

```dockerfile
```

-	Layers:
	-	`sha256:7b7c864d459efcb9dcd68176e945b29238d18677fbf26fc97e155f5372e39a80`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65818ca85b37143c261fa4ff5bc754b1d6efb29dd4fa5a388c8c41cf9ef1b2d6`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 12.8 KB (12752 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fe4252019e0facdc82bd032d22eb0d1c4ca58f5c3540356840ea3f9a15b79c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336641733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738a4a3e15b336c497f51dd0341cebd130f98fc5e6ea5546d50463e3985f0f70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014c3ccaea43ce9fd3e3c56ffefc4fcc50ba52d2cac23c5776e1533bb9e7f634`  
		Last Modified: Wed, 10 Apr 2024 21:20:56 GMT  
		Size: 307.5 MB (307479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4bd8788f5359ae12cb9bc1acc434ae90d51e6f7cd825268f70daa6bf97d2325d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003752c0fbdb6817f01a5ce924bea0fc77facd03291bd1bcd89b48034b53a37e`

```dockerfile
```

-	Layers:
	-	`sha256:a43e77b376b0764e2dd70d8f2bb3d33a1e3e3ed5dc88c771d83fa0525ca92868`  
		Last Modified: Wed, 10 Apr 2024 21:20:49 GMT  
		Size: 3.9 MB (3941346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bcfee754885be41d14895386082b6d75a7631863a2b3174b1fb4e7ea77225d`  
		Last Modified: Wed, 10 Apr 2024 21:20:48 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:08523c621a2f1d85417842ce00b1b9a42cae8216c42f87e18bdc421c713f7aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284576083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4981314b33e7ff1620efe817f2d72fc26a1c68c6a8a0c469c3bea63aa9b7a03c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad09fde316fe0e55a14718d6a0e81c083b2f8db66b02507b77a68117757c57a`  
		Last Modified: Wed, 24 Apr 2024 05:12:53 GMT  
		Size: 254.4 MB (254412900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:99ae02c25a1e078ad005a0fb13a480de4139db49eac3e367c19f9a19b1042c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a8378609675925b2f4b4b20f668ce4dc84d34f24b2cb8a26d32ce28a92535`

```dockerfile
```

-	Layers:
	-	`sha256:38704fffa432b9b8793aae63e4759b2f6b2f6e2bedf5dcd36d4c4fe39829037a`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da465366a30fda81b5c80fb19fa525c3093aa9fa32f0046ab820b871c201439f`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 12.8 KB (12769 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:189bd571f7eda5c3a23b70cbc343ed2cf7a24f72403e602fb71217cf569c94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290203818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31abbd30af48b3f5e0705a87cc896e94c40e7105e2d56fc679a29fefe8d8f9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27733677c7e7ffa3ae36f75ea55eca558d3b1535be93b58e60e358a3fa368deb`  
		Last Modified: Thu, 25 Apr 2024 09:39:52 GMT  
		Size: 257.1 MB (257062617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:850f59e79459f30440637f4f653d198d566176041d523a4ae01cb0498e12a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da07cd9aab3aa522fedda7cf41f03250557c862c629dc3a085cca69325b9aa`

```dockerfile
```

-	Layers:
	-	`sha256:aa0002bfc1a0d55e006eb61a57f2ec44a70a0758f0e5b78d46e00d75476b9ec6`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068a9188948e8d6cc2034275e59e9515d1cb420e57eda3a7f9a3600fb6039d21`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-slim-bullseye`

```console
$ docker pull rust@sha256:caca164937940b63e2ae6292b2507fe6c2feec7fc17fe958f182eab8af018b84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:1.77.2-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:43ea72d42d2c038ea843c9b41316622f86f5374dc6dfb82a037587761a04b849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264265732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9e28bbeb4bfd6d136fe79aa0822e42176d77fd24f75c05e8458b105546c898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c309d2cedf4817a559551782149cdca9318d0a6c23018b97523a0fe91857f`  
		Last Modified: Wed, 24 Apr 2024 05:11:46 GMT  
		Size: 232.8 MB (232831469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8b95d9eb6aa93d0dc9fb69ff759960ed6ca6dffc91099527b5f001a00f624d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053dac136f29cad1cf8460c926ae37b678819959d2a4d6f351e2d57c76b04680`

```dockerfile
```

-	Layers:
	-	`sha256:3bf84e83a418f557d6b1f21933fed9e3f861d44845045ea89e0dbcb27c9bc330`  
		Last Modified: Wed, 24 Apr 2024 05:11:41 GMT  
		Size: 4.1 MB (4139833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf51e74c2bf86d87b3bd5677d94c687071178480fd648aa0c64a816c4ed6e0a`  
		Last Modified: Wed, 24 Apr 2024 05:11:41 GMT  
		Size: 11.6 KB (11630 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d87bd027a2ec897941ff0f691413f27f6ab798f47ffd1c6954fd687bf58928f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277276352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c859469ac3ba60ce123589a9d56e54f17c194a61ee18931acfd7e3133b2aec9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d54685378a8d57ac36e4ff6a2c342ac52809f585a7d4c8fb662229230e65ce`  
		Last Modified: Thu, 25 Apr 2024 00:15:07 GMT  
		Size: 250.7 MB (250681610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3ceebf9c5462589e2d813246b8a8b6852d230b823549fe33fbab50984fca842e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8625ff2e32464e91cc3d770313871c50321ca890b2a17a4e0a2092840860cd`

```dockerfile
```

-	Layers:
	-	`sha256:f5d89aa7dc719b61e8b5071c3b29c385557d01a1d8ded536e3e3559ebf05078e`  
		Last Modified: Thu, 25 Apr 2024 00:15:01 GMT  
		Size: 3.9 MB (3949756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9151d79ca50c92149bee7df68a8e9b97ed397aedf889f6cbd71f43a42f9f1d6`  
		Last Modified: Thu, 25 Apr 2024 00:15:01 GMT  
		Size: 11.5 KB (11533 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4c5434f97e2e831215a9c5ed5abdf21894ad3c1e7f85f3661cc20c4f1d5fdcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327435048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3e88fc0ee536589d8ff9f84db749baeb19f637ca9d3ca26f872061af6ab348`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ffe28413ff737e9319fc6b161f92951752ebcccd38ff443b7b7a1bf7c46ec`  
		Last Modified: Wed, 10 Apr 2024 21:19:30 GMT  
		Size: 297.4 MB (297358742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:07546376e3d6ff97ef9245f0ddf9c23c2343abfcfc0d612ecd603355351e4fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b9a0d3926f551a4aa8aa4b4aa20168cbead544a81f98131d46e0b3d74339b3`

```dockerfile
```

-	Layers:
	-	`sha256:80783504581f38a49f386edba09b9cd5153392c5ad0174015ef551f090f4452b`  
		Last Modified: Wed, 10 Apr 2024 21:19:23 GMT  
		Size: 4.1 MB (4136557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:333d3575ff26376a87ab3ee97463a3424ff3ef7b03e78b7c28d8433a6e4586b9`  
		Last Modified: Wed, 10 Apr 2024 21:19:23 GMT  
		Size: 11.5 KB (11469 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:9d5d2ddfdd6a58b18bb7f0b8e5f8f37047f9ea8f1e2aa50dbcd4977bab58cd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280018615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbfbb115c7bc121e9f0e8a7827e251c41349a8bd1984a1e769d5c0374d67939`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37221a01bece8cf821897f51b65bd44350746155d325214a918695731a66d3f`  
		Last Modified: Wed, 24 Apr 2024 05:12:24 GMT  
		Size: 247.6 MB (247593842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:790c11b457e330245a08ee08368b80c4f9ba2376cd04a83d8c1281b66b8c95ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31aebfaf8b74b4087da8d50d05aab6f15d452168841659b66338f8cdefa27db2`

```dockerfile
```

-	Layers:
	-	`sha256:7ded81c8554c4a76e11a1920802c6a674e41a6c19c84a7a708cb38fde0d159c8`  
		Last Modified: Wed, 24 Apr 2024 05:12:19 GMT  
		Size: 4.1 MB (4131887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86498619bcaaa39fefc2150c322446a6fcf7367d267078da6811a589fe3d3977`  
		Last Modified: Wed, 24 Apr 2024 05:12:19 GMT  
		Size: 11.6 KB (11601 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:d1fbaf1eb7c480f19373691dee46b7333091e312a0067cfff60e4f88125b1a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278620161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0eb2329b60e7b7a4c321b3eb186e7e8291157920a4c927c5b1239dcd290362`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1effd22b3d858125536254bd2d670cd1a720ea963a5f5b9a6295f1cf04c849f2`  
		Last Modified: Thu, 25 Apr 2024 09:35:52 GMT  
		Size: 243.3 MB (243308436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6c908c45ab479e9a650293593a45d8210151cc0acedb0d2b98bd1874afc7b2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ca374cdff5e57bddc8583419f72f992120d629a52de5d00744829a915b1da9`

```dockerfile
```

-	Layers:
	-	`sha256:409c6f41b6182bd1869c433f7aab4744d5fc0538822f779fc042144d994129ad`  
		Last Modified: Thu, 25 Apr 2024 09:35:46 GMT  
		Size: 4.1 MB (4100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020f597651f5972b28de5ed540ee23e227c15cab9910914b31894c8c48ed893f`  
		Last Modified: Thu, 25 Apr 2024 09:35:46 GMT  
		Size: 11.5 KB (11500 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-slim-buster`

```console
$ docker pull rust@sha256:c52682b3c2455ba53083c61fc7d888d9e5c05af0e9f1720cedfcccf9681fa1f5
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

### `rust:1.77.2-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:e07c7817a1f8c56703b7c838c9a1d935ff5564981ab688fa9e5fe8a90e281234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245641279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fede2e811700e9b934388f903e43604d03cb4b02baa1b22f9e413087e23b6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b134fdd9ab24eec74b1973bea2fd971ba7966b53832863f2203aab5b1d6f89d`  
		Last Modified: Wed, 24 Apr 2024 05:10:28 GMT  
		Size: 218.3 MB (218303704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e5f87c411463e875b33cd48735d0289a9f7360541f0a7e32517cdd0a524b74c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45862094e4737de29467a79fec0a29be59819e15e997285078a0863166b3f96f`

```dockerfile
```

-	Layers:
	-	`sha256:d67cbeec45f86edc9afc54108da384643c40148c2fcf4dfc1693ed69d478a260`  
		Last Modified: Wed, 24 Apr 2024 05:10:24 GMT  
		Size: 3.9 MB (3941693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6058ee49cb0823ba46e949353f949deae7132061fb1b1b6c1a08016edfff47f`  
		Last Modified: Wed, 24 Apr 2024 05:10:24 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:06c1a08af5dabc4454b1cc105c607d4d06c9b0814db93873ff926a1ee1ef7b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264467965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4b9e3843b862fb3d9313d353d263101bf53a6b5d8b5e5fc90bf323760a9189`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f904fd6bf6b41f2fa9b506f896ebdbe821cd028a693fdf7968eacbc7b23da79f`  
		Last Modified: Thu, 25 Apr 2024 00:13:15 GMT  
		Size: 241.5 MB (241522901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e89bf36198f7184854a7500fc86b2d9017d6dec89f9311e71ecc44493f5ea944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492e0ecf007f0e2320b0b6564175d11a3d1f73d3402844e54236f518ce9eee78`

```dockerfile
```

-	Layers:
	-	`sha256:34f4a9c71e486a6edc1e06711c9c2d0e0a73aac8cc3987e71e5a681711ebaada`  
		Last Modified: Thu, 25 Apr 2024 00:13:09 GMT  
		Size: 3.7 MB (3749343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fa92b499139c82ddeb20b2d912bdeb136fcb250880b3abb0507ed48c61ef2b`  
		Last Modified: Thu, 25 Apr 2024 00:13:09 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3d47794cfa590e602f949345fc56267448530e64cf207ba79a4a8ebb82dd5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307822239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b58e4d35c7954b401373ee5f917c051f71d431fa6428121ce81b12148ab192`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81eb727fb6d6e4fe3e3a1ca3b615eb88245d64c5376a62e8bf275616c3c6cbb`  
		Last Modified: Wed, 10 Apr 2024 21:18:05 GMT  
		Size: 281.9 MB (281858778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:2628255e922502afd4e4aa0c4e30f4a26a1866d57111adb0984f7099d6b6549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1ff19d2b3c12e6fa257c298f2817debf02d8779e528210e136f9067dea6452`

```dockerfile
```

-	Layers:
	-	`sha256:152b56576a1f9f73de903d5f06d63ced13edd3b6f90bbb2d7ed9e780766cbae4`  
		Last Modified: Wed, 10 Apr 2024 21:17:59 GMT  
		Size: 3.6 MB (3574733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ce6be4574a6a214b953ebd2d8aa8c578da1ee01ca9ee50a67e6c3e5064b46c`  
		Last Modified: Wed, 10 Apr 2024 21:17:58 GMT  
		Size: 11.1 KB (11063 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:03a4f59dd317b964c56e75b84763dc831da494e3ec21fd36ae34348eecbcbd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265011000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8693b85bfe42d16b6f845d8e99d4a830f075c232156916f63ad424ad023a5ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:32f0f06baa0e4f10bff55aaa215b511838432ecc5fe547373d9ac99494556801 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:204b51fc41806ed93b4ccb6ce8272fa49b5f0b099ba6e3b5a940a9e7cd3ce202`  
		Last Modified: Wed, 24 Apr 2024 03:45:03 GMT  
		Size: 28.0 MB (27994678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bbd5edd24ae790e1053c99262c3c1062e6a89592bd6cccc53fef0b1e87e5a0`  
		Last Modified: Wed, 24 Apr 2024 05:10:57 GMT  
		Size: 237.0 MB (237016322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e45b1cd901a13a4ce4276a8780227951cd768d74e51877fec136f5906be660cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883ed62f0760eff19d06298c55f6a6eb27a6b79873ea0a37ccbe2f0b6defd196`

```dockerfile
```

-	Layers:
	-	`sha256:cda5f4adc3ed394903a5491d8b6ca36016e55f666a851196b374d2075686d8a9`  
		Last Modified: Wed, 24 Apr 2024 05:10:52 GMT  
		Size: 3.9 MB (3948318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4b9dd3825cdc912de170e8e5e11c701ebb88ea3e6ff82af59b8053cdd2b527`  
		Last Modified: Wed, 24 Apr 2024 05:10:51 GMT  
		Size: 11.2 KB (11195 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:9b74675247503eb0c3e3831dfdf10985c254b3ba9aa9a36eac8917f912a134eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:dc037af6f82e10c9862879cfe7dcbeb883b23092013b3a1df295512a4ade5d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272492183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d9a62b548d2deef025a80cbb517fcdaab56526b8cfc88d0ef4ab90b8dab39d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f170ecb6344abd22a40dfedc95278fed4a73a9409a285b6a31c6994b8097ab`  
		Last Modified: Tue, 09 Apr 2024 23:50:39 GMT  
		Size: 55.3 MB (55346790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150084451e7317de7972997b74d7d7b3a6947e9e01a1a3cd1a3b799e8348208`  
		Last Modified: Tue, 09 Apr 2024 23:50:42 GMT  
		Size: 213.7 MB (213736664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:65412a414e6e29d6f1c17de3346d8babf260891f011363110e2ef9d34763d2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e244aa001a61ab57db8fdbd3135b351cc3c55962ee776136e5af23d4b0a303ee`

```dockerfile
```

-	Layers:
	-	`sha256:4e63ddf0710f8dcc924c71396e2f3b39819922b0db63df53204e50c9b9c396a6`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 710.6 KB (710617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4861d7790f28e1d13f2037ee5c69a885431a65a224621e3a0915312ccd1038`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 11.8 KB (11792 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d30747064955669d4e48ece7dc69776bf05abe2ffa4eb866314bc842f9231936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278817954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd976a496d7d864344a2b39dad2155dbb9ef5d526f06ac412d4a3e2a37cb0be1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651ca114e522c42e6bb17953edf4a18bba82fe2287f93e32f6b3957ff901c2`  
		Last Modified: Sat, 16 Mar 2024 17:12:47 GMT  
		Size: 53.0 MB (52970287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157aaa1f3fa9784926886cafbadb1c30dcd160078deb54be2c6a6b7452ba670`  
		Last Modified: Wed, 10 Apr 2024 00:03:58 GMT  
		Size: 222.5 MB (222499952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:07fcac075e46cdcd0b7ad2a6c17d6d167910b8b9e827ccef0d73092dd6f12499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.2 KB (753242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f9b404804f7716cd3fce2e04dae7f19c8620b407f12a708e1f3f9cd944f9e`

```dockerfile
```

-	Layers:
	-	`sha256:4c6e25bf8fa604c97f277fd247f3614d3c6a8a1844f4cb78b3c466115463a60c`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 741.6 KB (741598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233de60c24dbdbc3fdcb9f32aba1af2eea5604c7ded084a880fb98dabaa39275`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 11.6 KB (11644 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.18`

```console
$ docker pull rust@sha256:b8f4f707c6460f4228deecdcc4acdfc50045fa7396f8aec732dc4ea322a41066
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:f5762f07bc2d9d6699afb162b7f35dfa48e5945cf4395b4f9b9d6826cb1d3c4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268673214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d5e3a7dd699641a0c6368e65fad736d7c583359096663c1e4bf5e98b85d5a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f914773acc6db8be08970614a0ed0f5fce71828723bfcb6e6cf1d97a26c284eb`  
		Last Modified: Tue, 09 Apr 2024 23:50:41 GMT  
		Size: 51.5 MB (51534043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b0af00c163854d8ec5ea9d8a150960293bfd4aa34804a7a160ef80f44ce71d`  
		Last Modified: Tue, 09 Apr 2024 23:50:44 GMT  
		Size: 213.7 MB (213736629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:9bfd12461323300ebd4c975ebc91a40d5949fa914272a2abe34315cac6c58c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49a20d1e055b2d8dcd9f1dc20fe467a5b977e5e797847f63adebc0d7732c718`

```dockerfile
```

-	Layers:
	-	`sha256:d549196acdb3131a3a009a32ec149198450da016167ecb17316ed5105a440284`  
		Last Modified: Tue, 09 Apr 2024 23:50:40 GMT  
		Size: 701.9 KB (701886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ff0d60c39141b47c8ebf94551e1235d461f65e03b68df4a8ae19688754cc60b`  
		Last Modified: Tue, 09 Apr 2024 23:50:40 GMT  
		Size: 10.6 KB (10588 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3a178840b556deece46aeea0e6f3029a9bf525530b5eba1f6037531c098947a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.9 MB (271899543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78a508d74d054080dc4bcea6dc7bd9819bd806d6bfd06910138e6c94e384e19`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b1cd0d662b55abd28904427ae8befdb37b765cf7ff19dc4a587c51429117c7`  
		Last Modified: Sat, 16 Mar 2024 17:11:39 GMT  
		Size: 46.1 MB (46066359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a88ea76700e9b87c7238a55b12f22030ed622804d3c18cd00497bbf3d9760d`  
		Last Modified: Wed, 10 Apr 2024 00:02:53 GMT  
		Size: 222.5 MB (222499823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:bf2d6cdc43bc8c6f6942a7e2a4eec7dd93b4f8a2e51b5cdee8f402c636b252d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **747.2 KB (747167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd7d1515764e16148a0a685fa2c88831a6e8bae26f370009e24a37eb15c52f1`

```dockerfile
```

-	Layers:
	-	`sha256:817ff20e322fc42973b1489c74c9d5e24420023ac7706158646e0c8187ea53d9`  
		Last Modified: Wed, 10 Apr 2024 00:02:48 GMT  
		Size: 736.7 KB (736735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff708420c480e2a3ada601eacf662d093335bbf3c2b624e814c55dd24d3d368`  
		Last Modified: Wed, 10 Apr 2024 00:02:48 GMT  
		Size: 10.4 KB (10432 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.19`

```console
$ docker pull rust@sha256:9b74675247503eb0c3e3831dfdf10985c254b3ba9aa9a36eac8917f912a134eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:dc037af6f82e10c9862879cfe7dcbeb883b23092013b3a1df295512a4ade5d2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272492183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25d9a62b548d2deef025a80cbb517fcdaab56526b8cfc88d0ef4ab90b8dab39d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f170ecb6344abd22a40dfedc95278fed4a73a9409a285b6a31c6994b8097ab`  
		Last Modified: Tue, 09 Apr 2024 23:50:39 GMT  
		Size: 55.3 MB (55346790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150084451e7317de7972997b74d7d7b3a6947e9e01a1a3cd1a3b799e8348208`  
		Last Modified: Tue, 09 Apr 2024 23:50:42 GMT  
		Size: 213.7 MB (213736664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:65412a414e6e29d6f1c17de3346d8babf260891f011363110e2ef9d34763d2ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e244aa001a61ab57db8fdbd3135b351cc3c55962ee776136e5af23d4b0a303ee`

```dockerfile
```

-	Layers:
	-	`sha256:4e63ddf0710f8dcc924c71396e2f3b39819922b0db63df53204e50c9b9c396a6`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 710.6 KB (710617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff4861d7790f28e1d13f2037ee5c69a885431a65a224621e3a0915312ccd1038`  
		Last Modified: Tue, 09 Apr 2024 23:50:38 GMT  
		Size: 11.8 KB (11792 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d30747064955669d4e48ece7dc69776bf05abe2ffa4eb866314bc842f9231936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278817954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd976a496d7d864344a2b39dad2155dbb9ef5d526f06ac412d4a3e2a37cb0be1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d651ca114e522c42e6bb17953edf4a18bba82fe2287f93e32f6b3957ff901c2`  
		Last Modified: Sat, 16 Mar 2024 17:12:47 GMT  
		Size: 53.0 MB (52970287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7157aaa1f3fa9784926886cafbadb1c30dcd160078deb54be2c6a6b7452ba670`  
		Last Modified: Wed, 10 Apr 2024 00:03:58 GMT  
		Size: 222.5 MB (222499952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:07fcac075e46cdcd0b7ad2a6c17d6d167910b8b9e827ccef0d73092dd6f12499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.2 KB (753242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:691f9b404804f7716cd3fce2e04dae7f19c8620b407f12a708e1f3f9cd944f9e`

```dockerfile
```

-	Layers:
	-	`sha256:4c6e25bf8fa604c97f277fd247f3614d3c6a8a1844f4cb78b3c466115463a60c`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 741.6 KB (741598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233de60c24dbdbc3fdcb9f32aba1af2eea5604c7ded084a880fb98dabaa39275`  
		Last Modified: Wed, 10 Apr 2024 00:03:53 GMT  
		Size: 11.6 KB (11644 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:8824f00d57259b0b833257532b2a4ec94132d1bf00e4b36e87a56266aff3a40c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:bookworm` - linux; amd64

```console
$ docker pull rust@sha256:c5000325cce93b58cb94ed7a77c85fa8a35520e6119b10a0d3a0ccc95960cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521828909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bb4f02fb0e8300d16b98188d95219c00741eeaf7deb9be498dcd44a5076f6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c40c3e3cdf945721f480e1d939aac857876fdb5c33b8fbfcf655c63b0b9428`  
		Last Modified: Wed, 24 Apr 2024 04:21:09 GMT  
		Size: 64.1 MB (64142118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05cc1123d7e335d59b0f465c23b7ad2ad27f4875b6c3eab41c65a9b50efa382`  
		Last Modified: Wed, 24 Apr 2024 04:21:45 GMT  
		Size: 211.2 MB (211175606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803b1968af78ef789730661c289a7ec4f7df4e634c9bee1c4837346ca3f4ef27`  
		Last Modified: Wed, 24 Apr 2024 05:12:18 GMT  
		Size: 172.9 MB (172884762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ea2ab75a2c2b231008469686581ab02e095b9fe922c119ade3d1479d3a3cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a288afbc55e2553d0168a7df78f087461c3e1f16288ca208348ce7cc956d6732`

```dockerfile
```

-	Layers:
	-	`sha256:51b060ea2235773d7512609d22d18dc74debf609f249989b35d729c12f6aab34`  
		Last Modified: Wed, 24 Apr 2024 05:12:16 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf815ddf8eb88dfd476d46a5029e837216ec0c685187027d0aefdf4d2eafcab6`  
		Last Modified: Wed, 24 Apr 2024 05:12:15 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:02f414fb213df08e9b7333e1bc6b6197034057b124e931a621fad867f8421ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510038334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef39effc782b510f66eab7f223bcc443fe6b080f53b290010473d523bdf9f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0525f0e8022d3b0295c1e79a86a4f89704f111e1b222a81c92bc1cd11e968380`  
		Last Modified: Fri, 12 Apr 2024 10:10:51 GMT  
		Size: 208.6 MB (208612483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:bf7d1b36a17124b80128713cf3d086d5796c86dc372c6282cf498daf6c1395eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1beec69f650b1aebc630728883823a22b7d6678dd70d219c8e0a42fa58672ce`

```dockerfile
```

-	Layers:
	-	`sha256:703cb3fa1a3d5fecd4a490acbbca87494b9e3a268f01c0fcf9d5e3680d83130e`  
		Last Modified: Fri, 12 Apr 2024 10:10:47 GMT  
		Size: 15.2 MB (15176005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9869ff78ed8192003451c3741439e311265dc77f2e68f7449112268e7789237`  
		Last Modified: Fri, 12 Apr 2024 10:10:45 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3160cca3c6dda6fe0ab864a99ac7c140053d5d1eb607de1149d8ddf283291f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581324975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f4049f68d66356001e70d6436c367cca3844efe78889fcc32dc84b7c30c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03d269bebeec78b201e8b34ead41bf134d4d60a7a9487567cdf8c35741b6e6`  
		Last Modified: Thu, 11 Apr 2024 09:06:37 GMT  
		Size: 241.6 MB (241616470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:c60bcda0982aaadca0e716b39a6374a61127c1a6de578325b4dd1a522cb7ae9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb01e6329c5de88d432e822441857852f9ab3a22ddb8644d6e833d6c705ee0`

```dockerfile
```

-	Layers:
	-	`sha256:ce8cf433ca365e2b10c8bd5a4abea406fa4f9e3ac157ea49fc5512e07028b8bd`  
		Last Modified: Thu, 11 Apr 2024 09:06:32 GMT  
		Size: 15.4 MB (15398644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3621a57d1464a572d892b6cf38eb44c3744f32365aa7308fb2da4a2e713ffa1`  
		Last Modified: Thu, 11 Apr 2024 09:06:31 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:890ff0201af78ee848b18a52a4f4531488b4e59578aaceb80267d92a5a5b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538602380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dcdd8241e4fbe59faf26d535c41d723ac8d9bc7a5ffc066ce3cc3d6bcd9976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c7b4c0568972903287c2ba295779f478db7fc45d1844ec5d10e22332f4cd1d84`  
		Last Modified: Wed, 24 Apr 2024 03:43:10 GMT  
		Size: 50.6 MB (50602565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba4056eb3a537ebb74fd333c27daceac5385bc3101b6029e706a51de775f00`  
		Last Modified: Wed, 24 Apr 2024 04:41:08 GMT  
		Size: 24.9 MB (24888940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0583cb1d092e1ca2b9a9e9ad274c286cbda7804622a36572a00c3440b4d88`  
		Last Modified: Wed, 24 Apr 2024 04:41:36 GMT  
		Size: 66.0 MB (65989175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4346162f795b064031764e3d351299d91568e9a1cb9ff0ae23d323d99339d1`  
		Last Modified: Wed, 24 Apr 2024 04:42:27 GMT  
		Size: 210.1 MB (210101062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ac1055cd771ed58d7865a880ab6bdb9b418503c9c767d13f68c437558fa46b`  
		Last Modified: Wed, 24 Apr 2024 05:12:29 GMT  
		Size: 187.0 MB (187020638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:97a7f910b863aa2ed9321369136bc22e1676fa469a92973958256b086366154c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08a98dfd4d629087d8353ef923ae123298df4a8a02235b5ed9609d9911589c`

```dockerfile
```

-	Layers:
	-	`sha256:be07c0f3fc84146f8b856092f446a575df879c8175d38ad9587726f5548f7dce`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76565694008f6464d1b540c738ca7df8e8974bac84071148aef50fcdfba095c4`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 13.2 KB (13177 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:3e03cf7b5c139593ad629b57e55624da795a4e789e4826ae88a0ef68a9feed27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551593932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62106ad4d5b838965cd23e3c23325d159f7ba16e3c4a5f525a573b48831d1e4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bf47934b0700489c27f4b1918c464037353ebec2ebc12585ceea997c9a34c71c`  
		Last Modified: Wed, 24 Apr 2024 03:25:57 GMT  
		Size: 53.6 MB (53580168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677be8677970cb6c89d034144a91a8695625d82f32553778be503e17ab5f55b3`  
		Last Modified: Wed, 24 Apr 2024 04:22:57 GMT  
		Size: 25.7 MB (25699777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48162777bb1b177bfa77ee29ba9552a6c899119f959faa64ef54f0a5aab3116`  
		Last Modified: Wed, 24 Apr 2024 04:23:19 GMT  
		Size: 69.6 MB (69584472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e881f9e7d456fa7b2b9e91f26b48776888d7ca1975413e2554119bfef1024`  
		Last Modified: Wed, 24 Apr 2024 04:23:59 GMT  
		Size: 214.2 MB (214213767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1dbcd760ee8f07bc74473682877cfe356c1743a81028d53592a9a203cbfe1d`  
		Last Modified: Thu, 25 Apr 2024 09:37:45 GMT  
		Size: 188.5 MB (188515748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:55139c979bd14dda211e51a3877d62232d3d44423d7a50eccb13987f2a8fc4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028f773eef818abb6e7c12c5785e8f0bc2100c507b72b5a932ab4e3db8b15eb2`

```dockerfile
```

-	Layers:
	-	`sha256:370f05a65fe56210232e2a29f47c225fa190152fce2f2fd2173f04fd6eebe017`  
		Last Modified: Thu, 25 Apr 2024 09:37:40 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c82a7840b4a0f54d7ee75413d11f713e9e9abf3e2ac8616c18bd4b2245f37e1`  
		Last Modified: Thu, 25 Apr 2024 09:37:39 GMT  
		Size: 12.6 KB (12625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:d651343e195b96bd4304dc33066bddf01f5a173b400df3c917b867a6d1f373d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:bullseye` - linux; amd64

```console
$ docker pull rust@sha256:ccdf877ab59edf47e838cb586e8b37fd680a49a0a47d76ec4812142f8ab53f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 MB (495324610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ce2473fbb694edc3adf51a56951e6455e2f655a776a865bf3d50385554989e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:646e886fa3cfd015533cf777eb62fc903426f0b57806d1cbaa843f8f07a9f66d`  
		Last Modified: Wed, 24 Apr 2024 03:33:00 GMT  
		Size: 55.1 MB (55098870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a360c5f105e29623d30cc42a1b871c17a19cbafe3ed994b3b64f2449cd1695`  
		Last Modified: Wed, 24 Apr 2024 04:21:57 GMT  
		Size: 15.8 MB (15765279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cbeb8ef1d906919c518d52a9eb71cedf1ee5c3247b6ea106571a6252d5a4f05`  
		Last Modified: Wed, 24 Apr 2024 04:22:13 GMT  
		Size: 54.6 MB (54589380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e29bc91fb60d9860548fd0c66a11e7a14b5e9417059fd06a35fb120d542ee0`  
		Last Modified: Wed, 24 Apr 2024 04:22:47 GMT  
		Size: 197.0 MB (196986464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9e74378906d6fcccfb1da6ff001463c333214d1c0961407017b0d92af11e99c`  
		Last Modified: Wed, 24 Apr 2024 05:12:06 GMT  
		Size: 172.9 MB (172884617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:36cae1d27d3ffbeb7555c6e06ed91e6a6918856ccadacace444c64fb29ce5848
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14987008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5475ef900d52d6d072e8823424349abe8270e19b3c105e4786bba417fa3f04f2`

```dockerfile
```

-	Layers:
	-	`sha256:e387fd514acb6becdc86178a7dbcd8e2de771419ac6ea9fe70fbadd665d114b2`  
		Last Modified: Wed, 24 Apr 2024 05:12:03 GMT  
		Size: 15.0 MB (14974944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f594e55497c4d0d325d1ac218e2aa59c03166f2e40597564a2214fc39079c6`  
		Last Modified: Wed, 24 Apr 2024 05:12:02 GMT  
		Size: 12.1 KB (12064 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:df9cd31df4d327523202f35516a11da6137aaeda2a08adc293e833a621f32dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491537963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc193a8f3c4651a63b0d0686148c39f44211822b8951a59661f1f806d4ba4d2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:eb53aade3ed19f72413045948cad3084902fe630cc20789d2c2b5bc334679575 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:23ca580217f1a6b17dba868e7ec34ae7fff221e07640fca532510daca8ed46f6`  
		Last Modified: Wed, 10 Apr 2024 01:04:48 GMT  
		Size: 50.2 MB (50246481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab89b030e474718221560707f98fb967bd582bc0f355ca5caf120fc5f25b2d58`  
		Last Modified: Wed, 10 Apr 2024 07:01:21 GMT  
		Size: 14.9 MB (14879245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ef8c5cdb2957e3cc1b26c037acafd549c7286845f8007127da85b383702cee3`  
		Last Modified: Wed, 10 Apr 2024 07:01:40 GMT  
		Size: 50.4 MB (50357907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c48f55e50a2918f423e3f80c787998eca4a47eec492d7e81553c5a738f095b`  
		Last Modified: Wed, 10 Apr 2024 07:02:17 GMT  
		Size: 167.4 MB (167441750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d040ff95e5e69aef50846a70d877773fcac32ff0f9d06253de2ae1af716e5734`  
		Last Modified: Fri, 12 Apr 2024 10:08:54 GMT  
		Size: 208.6 MB (208612580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:27e0a1d5194760cbf075370163165605974c9c995ea10b77865e58f93297b83f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14787748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af251232f279d9d3d121b812683d85782f17d1bba6e318f2eb262560b385b1f`

```dockerfile
```

-	Layers:
	-	`sha256:b589bde1ab79c3fb90f18abb53e64717165bb517252d9cc4aa98393250dcd3d5`  
		Last Modified: Fri, 12 Apr 2024 10:08:48 GMT  
		Size: 14.8 MB (14776282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c521898116f82ca4982d8062c10f81c24a776f01ecadfc5280e29d90c17d9e03`  
		Last Modified: Fri, 12 Apr 2024 10:08:48 GMT  
		Size: 11.5 KB (11466 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:1a3393a2d46c70be9b5f94dbbdad036e81cd4f53d22093a2c5a1b787778ebbd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.7 MB (555703379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a93805309b544762c6959305d7a87882f3e00dde2cce0002faf220d1458abd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6fedb173fe261ff0e13b004ca692b7edcc74dcc3c4384fee092b96ef9508992c in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:197947a07d5f6c6ff020ca65dcea4e52671f85f67bee1b59af46cb0dc36580d9`  
		Last Modified: Wed, 10 Apr 2024 00:44:24 GMT  
		Size: 53.7 MB (53729176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e3f4a530684a6d51e431d14164bdf20c7ad515e8948ddbfbf5f9c2c3680727`  
		Last Modified: Wed, 10 Apr 2024 04:33:00 GMT  
		Size: 15.7 MB (15749239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27317b8832e116e0457de89bfb9097cbcd3165d6079c38230f3728894dfb3af1`  
		Last Modified: Wed, 10 Apr 2024 04:33:14 GMT  
		Size: 54.7 MB (54694342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191dceb3c5772a800dd46b1b628a79e2167bd6bb0e9844a04e9ffc8a550a182b`  
		Last Modified: Wed, 10 Apr 2024 04:33:40 GMT  
		Size: 189.9 MB (189914112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f2acf4f3dce2c3a2795f5dca30272ad70e7ee1791a9408f571c2ef4cba93e7`  
		Last Modified: Thu, 11 Apr 2024 09:05:00 GMT  
		Size: 241.6 MB (241616510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:c55d4e3706c53b607de807dfe5b67c0a41dfbf3050aeb10e1466a6d6d57794fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14988253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7715d50b671577b7d31dd38c33ffcba338f92fe0787f979fda4ae5eb9cdd792a`

```dockerfile
```

-	Layers:
	-	`sha256:b88b1950f542b58e6a5e7e351442969a5cbc11b8b9addc4ffc305dcf4770bd41`  
		Last Modified: Thu, 11 Apr 2024 09:04:54 GMT  
		Size: 15.0 MB (14976847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90dc2dba9d291701a8e356d68176d87b7608fe5f13cd0bb213154866267432f5`  
		Last Modified: Thu, 11 Apr 2024 09:04:53 GMT  
		Size: 11.4 KB (11406 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:99e80cd2bda0ca76de778c4bc0ba34c74e3de3956965791a351350aa2d53a7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.2 MB (515187676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:964c90dd4b2891f01a4fbf7d61d46b5d47d2984449fdb31abed3fb4244ba9810`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:531ff4ee4f75fb0b1990fd185259fbec17670ebea9c3011de30a27e2de08c387`  
		Last Modified: Wed, 24 Apr 2024 03:43:58 GMT  
		Size: 56.1 MB (56076550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76062ffe019e6bfc91f0fe0510211f961184446e120461504dd7066278dbfb88`  
		Last Modified: Wed, 24 Apr 2024 04:42:41 GMT  
		Size: 16.3 MB (16269075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41af9e34185ddf73f8ecb610526409cc80e34f0aab2c2078a0effbe14be251`  
		Last Modified: Wed, 24 Apr 2024 04:43:06 GMT  
		Size: 55.9 MB (55929331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c343ec37d7971f52aa446a2e4bdf1947c24ac26c712f8d041bbde1de773ac`  
		Last Modified: Wed, 24 Apr 2024 04:43:51 GMT  
		Size: 199.9 MB (199892179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb203619e4b4cf64618cfa2c19ee1d65659b90ebdb6c6ee85de5f4da9c02e44c`  
		Last Modified: Wed, 24 Apr 2024 05:59:24 GMT  
		Size: 187.0 MB (187020541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8c5065810bf725f4d006d056e2ecb13ca43faa90846226938e6ad83cbe5079ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14975802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07523a23b3c8e37e88a7e8e8a58a73eab78fd2627b3335433f824e07ba2d958`

```dockerfile
```

-	Layers:
	-	`sha256:62a66bf05356563138f65afc0e39dceefd84c1f7aca3fabaf5ecbca321bd679d`  
		Last Modified: Wed, 24 Apr 2024 05:59:20 GMT  
		Size: 15.0 MB (14963767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:723a356feef7c199377ac324d03af4e1a42605c331083af3da8610fb9fc106b8`  
		Last Modified: Wed, 24 Apr 2024 05:59:19 GMT  
		Size: 12.0 KB (12035 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:29323ef01bbc112f2626a112df6540115e6815ef07ad2ec4e88aff3821006aba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.5 MB (519468840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2151423f0c0c0cae1cc3858001cf459a34880c3542d1dd1ac89df8bb42db01c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
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
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:aac3759e46343ae5d9b035355707bd07abf04ff80e3d29e689ea89cc78633190`  
		Last Modified: Wed, 24 Apr 2024 03:27:06 GMT  
		Size: 59.0 MB (58968197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc915aadd544630a28ea807628347805a6b8bc6f250feae34a46f66ac5228d3`  
		Last Modified: Wed, 24 Apr 2024 04:24:14 GMT  
		Size: 16.8 MB (16767223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87809a577847ee55cd1298464ee16a72985d1700dcf4e546db6fca794086d7c7`  
		Last Modified: Wed, 24 Apr 2024 04:24:32 GMT  
		Size: 58.9 MB (58873993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b19380d6722f8bacf55a08edef5ab2bef7d748909aa0109770daf96177909f5`  
		Last Modified: Wed, 24 Apr 2024 04:25:08 GMT  
		Size: 196.3 MB (196343705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628886dc5a2cba117f1a160da40f7cdba890a9661d5b7ebf648b56daa9650bd1`  
		Last Modified: Thu, 25 Apr 2024 09:33:54 GMT  
		Size: 188.5 MB (188515722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:26e50deba46d7e0e49b0734934c375a1505b03dd640bef54ef6e5d182854a987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14953986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f593beaf1e613e4b46c5c999914c44bbcc87f30d78b21507d25d9a6047305dd4`

```dockerfile
```

-	Layers:
	-	`sha256:2e7e2d41aaffd5046784b0118f36fedbbbd9a80fa0e503d16067cade6134667c`  
		Last Modified: Thu, 25 Apr 2024 09:33:50 GMT  
		Size: 14.9 MB (14942547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0a42423e593b1e4032328bd8df2924f0976804ba727dd0ae7fb996d9374e10b`  
		Last Modified: Thu, 25 Apr 2024 09:33:49 GMT  
		Size: 11.4 KB (11439 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:buster`

```console
$ docker pull rust@sha256:67afb05ae84c379fd1ef6c2af5a5988ae3a1402f5770b1c433716c3c8dcb2fe7
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
$ docker pull rust@sha256:fd9265894ebb1726c08256cb3aacec8f4cb885d1060679f38aea5b912e24294e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **485.0 MB (484968446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:783350f1d2be0610e2730df688417194ca785d80410ffbd196e066bf18264960`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b604b7bddfed00352fcc1abb8f44014438aca55d833109520e80b61c5fb207a1 in / 
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
	-	`sha256:191249de5b7ca0b4a8a5b5d8c19f5e94207c98ac4748bbe000d55d4a9c36deaf`  
		Last Modified: Wed, 24 Apr 2024 05:10:48 GMT  
		Size: 172.9 MB (172884715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:0122d3cb2d238112d8ddf6530059ba7d3c5418e5fe10b6ce6f7bea70c24d5c2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15978514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84ddd78af473b781391d26953e04b4d00a22822fb134c6f3b616e239638d6039`

```dockerfile
```

-	Layers:
	-	`sha256:21e5e906506b573f52865ef471c93575cacb3df811f226d258e83d35df54893f`  
		Last Modified: Wed, 24 Apr 2024 05:10:43 GMT  
		Size: 16.0 MB (15966858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd656bc775aa85ed1d157d20989d1d938ef91e8ebaacdb1f059dd629824719f7`  
		Last Modified: Wed, 24 Apr 2024 05:10:42 GMT  
		Size: 11.7 KB (11656 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:d2a8509b3be550586f457a19b228cdc2de0b78ab062e7bf4ec198a8745cc21ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486339195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b65f67846b1f7ac4de8b0e6c3b61a864f968b815796c9bd1137d547800904d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:56eb0c1e9a01d2e3320b2f3d897736bfe09ccb53ef1ae8bfea2b9d4099bc1d6b in / 
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
	-	`sha256:300908ef79221077165ff78ff105758d14dd67c42610c4e0aafdd731a920a871`  
		Last Modified: Wed, 10 Apr 2024 01:05:35 GMT  
		Size: 46.0 MB (45962444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a28291d070880fd3bc1d1083c0a3dfd62197b6f8f9b8f0222bebfb7abc3998c`  
		Last Modified: Wed, 10 Apr 2024 07:02:28 GMT  
		Size: 16.2 MB (16217560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df332bea5b985c1c2dd5d35090367d1eeb17f766d81c69c6484a9dbdfb6a2a19`  
		Last Modified: Wed, 10 Apr 2024 07:02:46 GMT  
		Size: 47.4 MB (47411064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c429ea890a21b115686f06bcd8e64b77317af15fee22637d21494c7f7e8763`  
		Last Modified: Wed, 10 Apr 2024 07:03:24 GMT  
		Size: 168.1 MB (168135545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a8d87914e90936da310261b7cf6db3b8d4cd941ac36d01a329b6a539b8532d`  
		Last Modified: Fri, 12 Apr 2024 10:07:00 GMT  
		Size: 208.6 MB (208612582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:8d3df22872c5331a3b7dbd9ef6776ffeeed758d67b5577d16a3e9b04a5d2ac9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15423342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8934156cede7d8af64415e272e84c840fb7ae69b9a7fd35fa465ab349febf8`

```dockerfile
```

-	Layers:
	-	`sha256:7211e52e2624ee2d88410d49e28e0f8c9429402417cdc964037fc456623a6a1c`  
		Last Modified: Fri, 12 Apr 2024 10:06:55 GMT  
		Size: 15.4 MB (15412281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de4bf7ecccbc2c3b7f1330ab90fab736d6467f54ca700dd24fb2e920cbdcb0fc`  
		Last Modified: Fri, 12 Apr 2024 10:06:54 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:3f1b8288a64eaa661ef9d21d57965a6ce3af9c7fe1d4cf6eace903500c4d82e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544120500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c11826c12adf7e8e962ae839db1d4ea5e82b9df9958790153e5ac1b78711a3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
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
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91b3908edaca8722a607f2265f615c82feb05f6440b5b8deab683e5f1338bfa`  
		Last Modified: Thu, 11 Apr 2024 09:03:31 GMT  
		Size: 241.6 MB (241616460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:1c1f949dcf2838a090f86a1847cac48ad01397a9edb0dff68e89d7193b0f9863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15611975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70ea129f23fc50bb965c6144abce71a0e69eccaf6989544d846c1ace9998e5a7`

```dockerfile
```

-	Layers:
	-	`sha256:df58017d086478c7376b7b37cf7f31b66e6987fa8f4fb639435f3daf7f77fe3f`  
		Last Modified: Thu, 11 Apr 2024 09:03:26 GMT  
		Size: 15.6 MB (15600976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174e8feb82f898148915b77b182fc9e1913079b6a09d883054bedac9a05eda6f`  
		Last Modified: Thu, 11 Apr 2024 09:03:26 GMT  
		Size: 11.0 KB (10999 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; 386

```console
$ docker pull rust@sha256:505bfca6bd398b4f00fce2ca2f2557b66aee0f09794144211116711a68f26b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.5 MB (508529720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe99a8ac5417c69838900906c1c7e30fbb0e60dfee7d690412859cdc78e7c42`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:5f943bcdbbb65accdf0b3bc452a1d4fafd2c64a9c6f6b3010b2a7ca20bedef36 in / 
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
	-	`sha256:1b3962c4dea2d1d71b72cea574044d31a38d535a42183f4cd4993e6868c8de0d`  
		Last Modified: Wed, 24 Apr 2024 05:59:21 GMT  
		Size: 187.0 MB (187020738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:14cc95a3b98a58a84c3b868c33797396615d28771f00ae4f18b86a4442ffe7d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15984068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb23ba590670f34ed24d660fea07e3e81a4b7efc98779effadb10adcebae634`

```dockerfile
```

-	Layers:
	-	`sha256:4400aa22d51411366132ed581c0eceaf6d4506634547b51715e0a2e460edda3e`  
		Last Modified: Wed, 24 Apr 2024 05:59:15 GMT  
		Size: 16.0 MB (15972439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6736ab863825c83fd0375286ca8c26322fa3921013d3db8f900b976c99982a4`  
		Last Modified: Wed, 24 Apr 2024 05:59:15 GMT  
		Size: 11.6 KB (11629 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:8824f00d57259b0b833257532b2a4ec94132d1bf00e4b36e87a56266aff3a40c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:latest` - linux; amd64

```console
$ docker pull rust@sha256:c5000325cce93b58cb94ed7a77c85fa8a35520e6119b10a0d3a0ccc95960cb73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521828909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14bb4f02fb0e8300d16b98188d95219c00741eeaf7deb9be498dcd44a5076f6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1468e7ff95fcb865fbc4dee7094f8b99c4dcddd6eb2180cf044c7396baf6fc2f`  
		Last Modified: Wed, 24 Apr 2024 03:32:18 GMT  
		Size: 49.6 MB (49576283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf9c2b42f41b1845f3e4421b723d56146db82939dc884555e077768e18132f4`  
		Last Modified: Wed, 24 Apr 2024 04:20:50 GMT  
		Size: 24.1 MB (24050140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c40c3e3cdf945721f480e1d939aac857876fdb5c33b8fbfcf655c63b0b9428`  
		Last Modified: Wed, 24 Apr 2024 04:21:09 GMT  
		Size: 64.1 MB (64142118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05cc1123d7e335d59b0f465c23b7ad2ad27f4875b6c3eab41c65a9b50efa382`  
		Last Modified: Wed, 24 Apr 2024 04:21:45 GMT  
		Size: 211.2 MB (211175606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803b1968af78ef789730661c289a7ec4f7df4e634c9bee1c4837346ca3f4ef27`  
		Last Modified: Wed, 24 Apr 2024 05:12:18 GMT  
		Size: 172.9 MB (172884762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:8ea2ab75a2c2b231008469686581ab02e095b9fe922c119ade3d1479d3a3cb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a288afbc55e2553d0168a7df78f087461c3e1f16288ca208348ce7cc956d6732`

```dockerfile
```

-	Layers:
	-	`sha256:51b060ea2235773d7512609d22d18dc74debf609f249989b35d729c12f6aab34`  
		Last Modified: Wed, 24 Apr 2024 05:12:16 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf815ddf8eb88dfd476d46a5029e837216ec0c685187027d0aefdf4d2eafcab6`  
		Last Modified: Wed, 24 Apr 2024 05:12:15 GMT  
		Size: 13.2 KB (13226 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:02f414fb213df08e9b7333e1bc6b6197034057b124e931a621fad867f8421ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510038334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78ef39effc782b510f66eab7f223bcc443fe6b080f53b290010473d523bdf9f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0525f0e8022d3b0295c1e79a86a4f89704f111e1b222a81c92bc1cd11e968380`  
		Last Modified: Fri, 12 Apr 2024 10:10:51 GMT  
		Size: 208.6 MB (208612483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:bf7d1b36a17124b80128713cf3d086d5796c86dc372c6282cf498daf6c1395eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15188666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1beec69f650b1aebc630728883823a22b7d6678dd70d219c8e0a42fa58672ce`

```dockerfile
```

-	Layers:
	-	`sha256:703cb3fa1a3d5fecd4a490acbbca87494b9e3a268f01c0fcf9d5e3680d83130e`  
		Last Modified: Fri, 12 Apr 2024 10:10:47 GMT  
		Size: 15.2 MB (15176005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9869ff78ed8192003451c3741439e311265dc77f2e68f7449112268e7789237`  
		Last Modified: Fri, 12 Apr 2024 10:10:45 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3160cca3c6dda6fe0ab864a99ac7c140053d5d1eb607de1149d8ddf283291f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581324975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f4049f68d66356001e70d6436c367cca3844efe78889fcc32dc84b7c30c4e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb03d269bebeec78b201e8b34ead41bf134d4d60a7a9487567cdf8c35741b6e6`  
		Last Modified: Thu, 11 Apr 2024 09:06:37 GMT  
		Size: 241.6 MB (241616470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:c60bcda0982aaadca0e716b39a6374a61127c1a6de578325b4dd1a522cb7ae9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ffb01e6329c5de88d432e822441857852f9ab3a22ddb8644d6e833d6c705ee0`

```dockerfile
```

-	Layers:
	-	`sha256:ce8cf433ca365e2b10c8bd5a4abea406fa4f9e3ac157ea49fc5512e07028b8bd`  
		Last Modified: Thu, 11 Apr 2024 09:06:32 GMT  
		Size: 15.4 MB (15398644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3621a57d1464a572d892b6cf38eb44c3744f32365aa7308fb2da4a2e713ffa1`  
		Last Modified: Thu, 11 Apr 2024 09:06:31 GMT  
		Size: 12.6 KB (12576 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:890ff0201af78ee848b18a52a4f4531488b4e59578aaceb80267d92a5a5b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.6 MB (538602380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9dcdd8241e4fbe59faf26d535c41d723ac8d9bc7a5ffc066ce3cc3d6bcd9976`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c7b4c0568972903287c2ba295779f478db7fc45d1844ec5d10e22332f4cd1d84`  
		Last Modified: Wed, 24 Apr 2024 03:43:10 GMT  
		Size: 50.6 MB (50602565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdba4056eb3a537ebb74fd333c27daceac5385bc3101b6029e706a51de775f00`  
		Last Modified: Wed, 24 Apr 2024 04:41:08 GMT  
		Size: 24.9 MB (24888940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa0583cb1d092e1ca2b9a9e9ad274c286cbda7804622a36572a00c3440b4d88`  
		Last Modified: Wed, 24 Apr 2024 04:41:36 GMT  
		Size: 66.0 MB (65989175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4346162f795b064031764e3d351299d91568e9a1cb9ff0ae23d323d99339d1`  
		Last Modified: Wed, 24 Apr 2024 04:42:27 GMT  
		Size: 210.1 MB (210101062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ac1055cd771ed58d7865a880ab6bdb9b418503c9c767d13f68c437558fa46b`  
		Last Modified: Wed, 24 Apr 2024 05:12:29 GMT  
		Size: 187.0 MB (187020638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:97a7f910b863aa2ed9321369136bc22e1676fa469a92973958256b086366154c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c08a98dfd4d629087d8353ef923ae123298df4a8a02235b5ed9609d9911589c`

```dockerfile
```

-	Layers:
	-	`sha256:be07c0f3fc84146f8b856092f446a575df879c8175d38ad9587726f5548f7dce`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76565694008f6464d1b540c738ca7df8e8974bac84071148aef50fcdfba095c4`  
		Last Modified: Wed, 24 Apr 2024 05:12:25 GMT  
		Size: 13.2 KB (13177 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:3e03cf7b5c139593ad629b57e55624da795a4e789e4826ae88a0ef68a9feed27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.6 MB (551593932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62106ad4d5b838965cd23e3c23325d159f7ba16e3c4a5f525a573b48831d1e4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bf47934b0700489c27f4b1918c464037353ebec2ebc12585ceea997c9a34c71c`  
		Last Modified: Wed, 24 Apr 2024 03:25:57 GMT  
		Size: 53.6 MB (53580168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677be8677970cb6c89d034144a91a8695625d82f32553778be503e17ab5f55b3`  
		Last Modified: Wed, 24 Apr 2024 04:22:57 GMT  
		Size: 25.7 MB (25699777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48162777bb1b177bfa77ee29ba9552a6c899119f959faa64ef54f0a5aab3116`  
		Last Modified: Wed, 24 Apr 2024 04:23:19 GMT  
		Size: 69.6 MB (69584472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326e881f9e7d456fa7b2b9e91f26b48776888d7ca1975413e2554119bfef1024`  
		Last Modified: Wed, 24 Apr 2024 04:23:59 GMT  
		Size: 214.2 MB (214213767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed1dbcd760ee8f07bc74473682877cfe356c1743a81028d53592a9a203cbfe1d`  
		Last Modified: Thu, 25 Apr 2024 09:37:45 GMT  
		Size: 188.5 MB (188515748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:55139c979bd14dda211e51a3877d62232d3d44423d7a50eccb13987f2a8fc4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:028f773eef818abb6e7c12c5785e8f0bc2100c507b72b5a932ab4e3db8b15eb2`

```dockerfile
```

-	Layers:
	-	`sha256:370f05a65fe56210232e2a29f47c225fa190152fce2f2fd2173f04fd6eebe017`  
		Last Modified: Thu, 25 Apr 2024 09:37:40 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c82a7840b4a0f54d7ee75413d11f713e9e9abf3e2ac8616c18bd4b2245f37e1`  
		Last Modified: Thu, 25 Apr 2024 09:37:39 GMT  
		Size: 12.6 KB (12625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:a8f04112cc1892451320b241b0fe7c074d506de026ad7d96162c8482f9b8ce1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:slim` - linux; amd64

```console
$ docker pull rust@sha256:638e3590f320c70f5edbfe1842d42ae385624f8c6071f91037d465e7bf7178f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272626407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226d76b23659549e4748842478c0207ab5f79656c520fcb856f4eb235de0bfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12808888e0a2157cb0269632bdee49433c9f8556ccda1464afb6f94479129ead`  
		Last Modified: Wed, 24 Apr 2024 05:13:05 GMT  
		Size: 243.5 MB (243475928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:5040f97f4a64566983b901b8fb9eae5ed9a1d4da8aa370cdff68de72249c4cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b52883aa5b9709eca3de616ddcc0c58126a33c1e0528ef6ff5f9a703697301c`

```dockerfile
```

-	Layers:
	-	`sha256:40a7699dc460633d2771085a3dc0e3d6f9aeb38030c5cd7a573799fae19a1fe4`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd14237218530973d0aee254a672a5a6fff80aab1f6eec85a9333d25355e634`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:8cfe44ff0e1d69b947a70df0359e48b4b7e1057d7c8849788ac4ef4da4f26a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd61a2122260688f839cbd2b8f940fd85eb6213d9be0561bc99d9d127dbbda89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd18c5ddc627e06a0ca56860a2c399710c2100cb5c189b0fabbe66dfb32f175`  
		Last Modified: Thu, 25 Apr 2024 00:16:57 GMT  
		Size: 256.2 MB (256248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:9fb4006e0666af50e2d9d516f1ee5bd14c6e8ee24e685e8f6c1066a72baf6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cc6bf9290ed472822b7c279a1146749b547500ed2b17cf92162d46ee0be09b`

```dockerfile
```

-	Layers:
	-	`sha256:7b7c864d459efcb9dcd68176e945b29238d18677fbf26fc97e155f5372e39a80`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65818ca85b37143c261fa4ff5bc754b1d6efb29dd4fa5a388c8c41cf9ef1b2d6`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 12.8 KB (12752 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fe4252019e0facdc82bd032d22eb0d1c4ca58f5c3540356840ea3f9a15b79c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336641733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738a4a3e15b336c497f51dd0341cebd130f98fc5e6ea5546d50463e3985f0f70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014c3ccaea43ce9fd3e3c56ffefc4fcc50ba52d2cac23c5776e1533bb9e7f634`  
		Last Modified: Wed, 10 Apr 2024 21:20:56 GMT  
		Size: 307.5 MB (307479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:4bd8788f5359ae12cb9bc1acc434ae90d51e6f7cd825268f70daa6bf97d2325d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003752c0fbdb6817f01a5ce924bea0fc77facd03291bd1bcd89b48034b53a37e`

```dockerfile
```

-	Layers:
	-	`sha256:a43e77b376b0764e2dd70d8f2bb3d33a1e3e3ed5dc88c771d83fa0525ca92868`  
		Last Modified: Wed, 10 Apr 2024 21:20:49 GMT  
		Size: 3.9 MB (3941346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bcfee754885be41d14895386082b6d75a7631863a2b3174b1fb4e7ea77225d`  
		Last Modified: Wed, 10 Apr 2024 21:20:48 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:08523c621a2f1d85417842ce00b1b9a42cae8216c42f87e18bdc421c713f7aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284576083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4981314b33e7ff1620efe817f2d72fc26a1c68c6a8a0c469c3bea63aa9b7a03c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad09fde316fe0e55a14718d6a0e81c083b2f8db66b02507b77a68117757c57a`  
		Last Modified: Wed, 24 Apr 2024 05:12:53 GMT  
		Size: 254.4 MB (254412900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:99ae02c25a1e078ad005a0fb13a480de4139db49eac3e367c19f9a19b1042c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a8378609675925b2f4b4b20f668ce4dc84d34f24b2cb8a26d32ce28a92535`

```dockerfile
```

-	Layers:
	-	`sha256:38704fffa432b9b8793aae63e4759b2f6b2f6e2bedf5dcd36d4c4fe39829037a`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da465366a30fda81b5c80fb19fa525c3093aa9fa32f0046ab820b871c201439f`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 12.8 KB (12769 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:189bd571f7eda5c3a23b70cbc343ed2cf7a24f72403e602fb71217cf569c94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290203818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31abbd30af48b3f5e0705a87cc896e94c40e7105e2d56fc679a29fefe8d8f9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27733677c7e7ffa3ae36f75ea55eca558d3b1535be93b58e60e358a3fa368deb`  
		Last Modified: Thu, 25 Apr 2024 09:39:52 GMT  
		Size: 257.1 MB (257062617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:850f59e79459f30440637f4f653d198d566176041d523a4ae01cb0498e12a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da07cd9aab3aa522fedda7cf41f03250557c862c629dc3a085cca69325b9aa`

```dockerfile
```

-	Layers:
	-	`sha256:aa0002bfc1a0d55e006eb61a57f2ec44a70a0758f0e5b78d46e00d75476b9ec6`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068a9188948e8d6cc2034275e59e9515d1cb420e57eda3a7f9a3600fb6039d21`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:a8f04112cc1892451320b241b0fe7c074d506de026ad7d96162c8482f9b8ce1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:638e3590f320c70f5edbfe1842d42ae385624f8c6071f91037d465e7bf7178f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.6 MB (272626407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3226d76b23659549e4748842478c0207ab5f79656c520fcb856f4eb235de0bfe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12808888e0a2157cb0269632bdee49433c9f8556ccda1464afb6f94479129ead`  
		Last Modified: Wed, 24 Apr 2024 05:13:05 GMT  
		Size: 243.5 MB (243475928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5040f97f4a64566983b901b8fb9eae5ed9a1d4da8aa370cdff68de72249c4cce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b52883aa5b9709eca3de616ddcc0c58126a33c1e0528ef6ff5f9a703697301c`

```dockerfile
```

-	Layers:
	-	`sha256:40a7699dc460633d2771085a3dc0e3d6f9aeb38030c5cd7a573799fae19a1fe4`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fd14237218530973d0aee254a672a5a6fff80aab1f6eec85a9333d25355e634`  
		Last Modified: Wed, 24 Apr 2024 05:12:58 GMT  
		Size: 12.8 KB (12818 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:8cfe44ff0e1d69b947a70df0359e48b4b7e1057d7c8849788ac4ef4da4f26a25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280989281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd61a2122260688f839cbd2b8f940fd85eb6213d9be0561bc99d9d127dbbda89`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afd18c5ddc627e06a0ca56860a2c399710c2100cb5c189b0fabbe66dfb32f175`  
		Last Modified: Thu, 25 Apr 2024 00:16:57 GMT  
		Size: 256.2 MB (256248839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9fb4006e0666af50e2d9d516f1ee5bd14c6e8ee24e685e8f6c1066a72baf6be1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4cc6bf9290ed472822b7c279a1146749b547500ed2b17cf92162d46ee0be09b`

```dockerfile
```

-	Layers:
	-	`sha256:7b7c864d459efcb9dcd68176e945b29238d18677fbf26fc97e155f5372e39a80`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65818ca85b37143c261fa4ff5bc754b1d6efb29dd4fa5a388c8c41cf9ef1b2d6`  
		Last Modified: Thu, 25 Apr 2024 00:16:51 GMT  
		Size: 12.8 KB (12752 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:fe4252019e0facdc82bd032d22eb0d1c4ca58f5c3540356840ea3f9a15b79c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336641733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738a4a3e15b336c497f51dd0341cebd130f98fc5e6ea5546d50463e3985f0f70`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014c3ccaea43ce9fd3e3c56ffefc4fcc50ba52d2cac23c5776e1533bb9e7f634`  
		Last Modified: Wed, 10 Apr 2024 21:20:56 GMT  
		Size: 307.5 MB (307479576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:4bd8788f5359ae12cb9bc1acc434ae90d51e6f7cd825268f70daa6bf97d2325d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003752c0fbdb6817f01a5ce924bea0fc77facd03291bd1bcd89b48034b53a37e`

```dockerfile
```

-	Layers:
	-	`sha256:a43e77b376b0764e2dd70d8f2bb3d33a1e3e3ed5dc88c771d83fa0525ca92868`  
		Last Modified: Wed, 10 Apr 2024 21:20:49 GMT  
		Size: 3.9 MB (3941346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8bcfee754885be41d14895386082b6d75a7631863a2b3174b1fb4e7ea77225d`  
		Last Modified: Wed, 10 Apr 2024 21:20:48 GMT  
		Size: 12.7 KB (12665 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:08523c621a2f1d85417842ce00b1b9a42cae8216c42f87e18bdc421c713f7aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284576083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4981314b33e7ff1620efe817f2d72fc26a1c68c6a8a0c469c3bea63aa9b7a03c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad09fde316fe0e55a14718d6a0e81c083b2f8db66b02507b77a68117757c57a`  
		Last Modified: Wed, 24 Apr 2024 05:12:53 GMT  
		Size: 254.4 MB (254412900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:99ae02c25a1e078ad005a0fb13a480de4139db49eac3e367c19f9a19b1042c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a8378609675925b2f4b4b20f668ce4dc84d34f24b2cb8a26d32ce28a92535`

```dockerfile
```

-	Layers:
	-	`sha256:38704fffa432b9b8793aae63e4759b2f6b2f6e2bedf5dcd36d4c4fe39829037a`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da465366a30fda81b5c80fb19fa525c3093aa9fa32f0046ab820b871c201439f`  
		Last Modified: Wed, 24 Apr 2024 05:12:47 GMT  
		Size: 12.8 KB (12769 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:189bd571f7eda5c3a23b70cbc343ed2cf7a24f72403e602fb71217cf569c94bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.2 MB (290203818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31abbd30af48b3f5e0705a87cc896e94c40e7105e2d56fc679a29fefe8d8f9b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27733677c7e7ffa3ae36f75ea55eca558d3b1535be93b58e60e358a3fa368deb`  
		Last Modified: Thu, 25 Apr 2024 09:39:52 GMT  
		Size: 257.1 MB (257062617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:850f59e79459f30440637f4f653d198d566176041d523a4ae01cb0498e12a672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09da07cd9aab3aa522fedda7cf41f03250557c862c629dc3a085cca69325b9aa`

```dockerfile
```

-	Layers:
	-	`sha256:aa0002bfc1a0d55e006eb61a57f2ec44a70a0758f0e5b78d46e00d75476b9ec6`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:068a9188948e8d6cc2034275e59e9515d1cb420e57eda3a7f9a3600fb6039d21`  
		Last Modified: Thu, 25 Apr 2024 09:39:46 GMT  
		Size: 12.7 KB (12713 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:caca164937940b63e2ae6292b2507fe6c2feec7fc17fe958f182eab8af018b84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `rust:slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:43ea72d42d2c038ea843c9b41316622f86f5374dc6dfb82a037587761a04b849
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264265732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9e28bbeb4bfd6d136fe79aa0822e42176d77fd24f75c05e8458b105546c898`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c309d2cedf4817a559551782149cdca9318d0a6c23018b97523a0fe91857f`  
		Last Modified: Wed, 24 Apr 2024 05:11:46 GMT  
		Size: 232.8 MB (232831469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:8b95d9eb6aa93d0dc9fb69ff759960ed6ca6dffc91099527b5f001a00f624d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:053dac136f29cad1cf8460c926ae37b678819959d2a4d6f351e2d57c76b04680`

```dockerfile
```

-	Layers:
	-	`sha256:3bf84e83a418f557d6b1f21933fed9e3f861d44845045ea89e0dbcb27c9bc330`  
		Last Modified: Wed, 24 Apr 2024 05:11:41 GMT  
		Size: 4.1 MB (4139833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdf51e74c2bf86d87b3bd5677d94c687071178480fd648aa0c64a816c4ed6e0a`  
		Last Modified: Wed, 24 Apr 2024 05:11:41 GMT  
		Size: 11.6 KB (11630 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:d87bd027a2ec897941ff0f691413f27f6ab798f47ffd1c6954fd687bf58928f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277276352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c859469ac3ba60ce123589a9d56e54f17c194a61ee18931acfd7e3133b2aec9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d54685378a8d57ac36e4ff6a2c342ac52809f585a7d4c8fb662229230e65ce`  
		Last Modified: Thu, 25 Apr 2024 00:15:07 GMT  
		Size: 250.7 MB (250681610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:3ceebf9c5462589e2d813246b8a8b6852d230b823549fe33fbab50984fca842e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8625ff2e32464e91cc3d770313871c50321ca890b2a17a4e0a2092840860cd`

```dockerfile
```

-	Layers:
	-	`sha256:f5d89aa7dc719b61e8b5071c3b29c385557d01a1d8ded536e3e3559ebf05078e`  
		Last Modified: Thu, 25 Apr 2024 00:15:01 GMT  
		Size: 3.9 MB (3949756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9151d79ca50c92149bee7df68a8e9b97ed397aedf889f6cbd71f43a42f9f1d6`  
		Last Modified: Thu, 25 Apr 2024 00:15:01 GMT  
		Size: 11.5 KB (11533 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:4c5434f97e2e831215a9c5ed5abdf21894ad3c1e7f85f3661cc20c4f1d5fdcf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327435048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff3e88fc0ee536589d8ff9f84db749baeb19f637ca9d3ca26f872061af6ab348`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ffe28413ff737e9319fc6b161f92951752ebcccd38ff443b7b7a1bf7c46ec`  
		Last Modified: Wed, 10 Apr 2024 21:19:30 GMT  
		Size: 297.4 MB (297358742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:07546376e3d6ff97ef9245f0ddf9c23c2343abfcfc0d612ecd603355351e4fb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b9a0d3926f551a4aa8aa4b4aa20168cbead544a81f98131d46e0b3d74339b3`

```dockerfile
```

-	Layers:
	-	`sha256:80783504581f38a49f386edba09b9cd5153392c5ad0174015ef551f090f4452b`  
		Last Modified: Wed, 10 Apr 2024 21:19:23 GMT  
		Size: 4.1 MB (4136557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:333d3575ff26376a87ab3ee97463a3424ff3ef7b03e78b7c28d8433a6e4586b9`  
		Last Modified: Wed, 10 Apr 2024 21:19:23 GMT  
		Size: 11.5 KB (11469 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:9d5d2ddfdd6a58b18bb7f0b8e5f8f37047f9ea8f1e2aa50dbcd4977bab58cd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280018615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbfbb115c7bc121e9f0e8a7827e251c41349a8bd1984a1e769d5c0374d67939`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37221a01bece8cf821897f51b65bd44350746155d325214a918695731a66d3f`  
		Last Modified: Wed, 24 Apr 2024 05:12:24 GMT  
		Size: 247.6 MB (247593842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:790c11b457e330245a08ee08368b80c4f9ba2376cd04a83d8c1281b66b8c95ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31aebfaf8b74b4087da8d50d05aab6f15d452168841659b66338f8cdefa27db2`

```dockerfile
```

-	Layers:
	-	`sha256:7ded81c8554c4a76e11a1920802c6a674e41a6c19c84a7a708cb38fde0d159c8`  
		Last Modified: Wed, 24 Apr 2024 05:12:19 GMT  
		Size: 4.1 MB (4131887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86498619bcaaa39fefc2150c322446a6fcf7367d267078da6811a589fe3d3977`  
		Last Modified: Wed, 24 Apr 2024 05:12:19 GMT  
		Size: 11.6 KB (11601 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:d1fbaf1eb7c480f19373691dee46b7333091e312a0067cfff60e4f88125b1a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.6 MB (278620161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0eb2329b60e7b7a4c321b3eb186e7e8291157920a4c927c5b1239dcd290362`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1effd22b3d858125536254bd2d670cd1a720ea963a5f5b9a6295f1cf04c849f2`  
		Last Modified: Thu, 25 Apr 2024 09:35:52 GMT  
		Size: 243.3 MB (243308436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:6c908c45ab479e9a650293593a45d8210151cc0acedb0d2b98bd1874afc7b2d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ca374cdff5e57bddc8583419f72f992120d629a52de5d00744829a915b1da9`

```dockerfile
```

-	Layers:
	-	`sha256:409c6f41b6182bd1869c433f7aab4744d5fc0538822f779fc042144d994129ad`  
		Last Modified: Thu, 25 Apr 2024 09:35:46 GMT  
		Size: 4.1 MB (4100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:020f597651f5972b28de5ed540ee23e227c15cab9910914b31894c8c48ed893f`  
		Last Modified: Thu, 25 Apr 2024 09:35:46 GMT  
		Size: 11.5 KB (11500 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-buster`

```console
$ docker pull rust@sha256:c52682b3c2455ba53083c61fc7d888d9e5c05af0e9f1720cedfcccf9681fa1f5
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

### `rust:slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:e07c7817a1f8c56703b7c838c9a1d935ff5564981ab688fa9e5fe8a90e281234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245641279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fede2e811700e9b934388f903e43604d03cb4b02baa1b22f9e413087e23b6e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b134fdd9ab24eec74b1973bea2fd971ba7966b53832863f2203aab5b1d6f89d`  
		Last Modified: Wed, 24 Apr 2024 05:10:28 GMT  
		Size: 218.3 MB (218303704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e5f87c411463e875b33cd48735d0289a9f7360541f0a7e32517cdd0a524b74c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45862094e4737de29467a79fec0a29be59819e15e997285078a0863166b3f96f`

```dockerfile
```

-	Layers:
	-	`sha256:d67cbeec45f86edc9afc54108da384643c40148c2fcf4dfc1693ed69d478a260`  
		Last Modified: Wed, 24 Apr 2024 05:10:24 GMT  
		Size: 3.9 MB (3941693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6058ee49cb0823ba46e949353f949deae7132061fb1b1b6c1a08016edfff47f`  
		Last Modified: Wed, 24 Apr 2024 05:10:24 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:06c1a08af5dabc4454b1cc105c607d4d06c9b0814db93873ff926a1ee1ef7b20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264467965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e4b9e3843b862fb3d9313d353d263101bf53a6b5d8b5e5fc90bf323760a9189`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f904fd6bf6b41f2fa9b506f896ebdbe821cd028a693fdf7968eacbc7b23da79f`  
		Last Modified: Thu, 25 Apr 2024 00:13:15 GMT  
		Size: 241.5 MB (241522901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e89bf36198f7184854a7500fc86b2d9017d6dec89f9311e71ecc44493f5ea944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:492e0ecf007f0e2320b0b6564175d11a3d1f73d3402844e54236f518ce9eee78`

```dockerfile
```

-	Layers:
	-	`sha256:34f4a9c71e486a6edc1e06711c9c2d0e0a73aac8cc3987e71e5a681711ebaada`  
		Last Modified: Thu, 25 Apr 2024 00:13:09 GMT  
		Size: 3.7 MB (3749343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22fa92b499139c82ddeb20b2d912bdeb136fcb250880b3abb0507ed48c61ef2b`  
		Last Modified: Thu, 25 Apr 2024 00:13:09 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d3d47794cfa590e602f949345fc56267448530e64cf207ba79a4a8ebb82dd5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307822239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b58e4d35c7954b401373ee5f917c051f71d431fa6428121ce81b12148ab192`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81eb727fb6d6e4fe3e3a1ca3b615eb88245d64c5376a62e8bf275616c3c6cbb`  
		Last Modified: Wed, 10 Apr 2024 21:18:05 GMT  
		Size: 281.9 MB (281858778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:2628255e922502afd4e4aa0c4e30f4a26a1866d57111adb0984f7099d6b6549e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1ff19d2b3c12e6fa257c298f2817debf02d8779e528210e136f9067dea6452`

```dockerfile
```

-	Layers:
	-	`sha256:152b56576a1f9f73de903d5f06d63ced13edd3b6f90bbb2d7ed9e780766cbae4`  
		Last Modified: Wed, 10 Apr 2024 21:17:59 GMT  
		Size: 3.6 MB (3574733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30ce6be4574a6a214b953ebd2d8aa8c578da1ee01ca9ee50a67e6c3e5064b46c`  
		Last Modified: Wed, 10 Apr 2024 21:17:58 GMT  
		Size: 11.1 KB (11063 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; 386

```console
$ docker pull rust@sha256:03a4f59dd317b964c56e75b84763dc831da494e3ec21fd36ae34348eecbcbd06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265011000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8693b85bfe42d16b6f845d8e99d4a830f075c232156916f63ad424ad023a5ea`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:32f0f06baa0e4f10bff55aaa215b511838432ecc5fe547373d9ac99494556801 in / 
# Tue, 09 Apr 2024 22:06:26 GMT
CMD ["bash"]
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:204b51fc41806ed93b4ccb6ce8272fa49b5f0b099ba6e3b5a940a9e7cd3ce202`  
		Last Modified: Wed, 24 Apr 2024 03:45:03 GMT  
		Size: 28.0 MB (27994678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bbd5edd24ae790e1053c99262c3c1062e6a89592bd6cccc53fef0b1e87e5a0`  
		Last Modified: Wed, 24 Apr 2024 05:10:57 GMT  
		Size: 237.0 MB (237016322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e45b1cd901a13a4ce4276a8780227951cd768d74e51877fec136f5906be660cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883ed62f0760eff19d06298c55f6a6eb27a6b79873ea0a37ccbe2f0b6defd196`

```dockerfile
```

-	Layers:
	-	`sha256:cda5f4adc3ed394903a5491d8b6ca36016e55f666a851196b374d2075686d8a9`  
		Last Modified: Wed, 24 Apr 2024 05:10:52 GMT  
		Size: 3.9 MB (3948318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4b9dd3825cdc912de170e8e5e11c701ebb88ea3e6ff82af59b8053cdd2b527`  
		Last Modified: Wed, 24 Apr 2024 05:10:51 GMT  
		Size: 11.2 KB (11195 bytes)  
		MIME: application/vnd.in-toto+json
