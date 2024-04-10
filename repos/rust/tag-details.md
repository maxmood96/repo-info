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
$ docker pull rust@sha256:a22010a54d04ab9bde99a332f7d37f921bc73fcfce78738a5ae68ab21bcd46b2
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
$ docker pull rust@sha256:6361801bd55ffec96b953437f1083a8d730320b0809292d7d84425ff5f3223a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521770219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead19e243dc6f0b82077e2f7aca0a70a7e4fdd9300f6fa71b1557210b6bea496`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
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
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4251e2c0d85d5696b1917655ebc9009cc6d07741a7410385ecdbf440cc57e92`  
		Last Modified: Wed, 10 Apr 2024 06:54:51 GMT  
		Size: 172.9 MB (172884751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:7093785b7995fdc45f27f84b72d85b3425f8cedab6a4692fbb54cd3e8445fd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67072e65542c5c0a7f8c486648acf1470857af35bc22c9994006fe2869e992a`

```dockerfile
```

-	Layers:
	-	`sha256:f58c77986737873a4dd6d0f618ef90591136108b4a126550ab2cbd66d2d01cf5`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 15.4 MB (15370122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3172b133a2a58f28fdc38c6e63776bd4bffb56d2e180b31f207e9f19f4cb2197`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 13.2 KB (13222 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff8d4f50070f7fa5a52f2fcef4f8b51569023de2dde184cb2bf593d596f61547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510035646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb59b3cd57ab4f766666a6c3155019552626eaa52de6881231146e013d09d64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1200500c52f4429e643f87908b44e016ca7b67ac17bcdba07b3884ef8b98fed1`  
		Last Modified: Wed, 10 Apr 2024 00:05:32 GMT  
		Size: 208.6 MB (208612381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:b340eca81e3952b867d6121dd010fe5baf4dcf8782a035ef666803baf5a81d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4326b7d2aa5919c3772d38b9ffa6002f9a6b013c3447f507d0800b6c11d178a`

```dockerfile
```

-	Layers:
	-	`sha256:482cba46f5b18fa1452b104ca0bd84ab211676d10a643e56287b9b7477af6258`  
		Last Modified: Wed, 10 Apr 2024 00:05:27 GMT  
		Size: 15.2 MB (15185946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39172abfd0ca99841b69d6dd1903d428f3dfa92415f750b1584c92eae12a7b28`  
		Last Modified: Wed, 10 Apr 2024 00:05:26 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ce750647809bbeb76d60938398758b357a0b66fa60f7066f5195e430b4ab03ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581311877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b136805ec1040e311c556f1db756b3af16437a1c22a9d7c0bdedc4c837138002`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:25:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6faea05ead1ac9cd3244827816e2385b0d62299f7937a4574fc5a9651624c`  
		Last Modified: Tue, 12 Mar 2024 01:35:18 GMT  
		Size: 202.5 MB (202538246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b9ee712f6593072f4693a66c5913d1e384397b49ac2d98a1f3140fffe7df7`  
		Last Modified: Mon, 01 Apr 2024 22:00:00 GMT  
		Size: 241.6 MB (241608857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:5204201704e7de4bcdacf00558fafffc7c9b8c9e8900f12f7f97483bdcf56458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15421049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64787d4a6c8f814d976ed17ae2a7920712eed7e04f84ec633f422c49a232ad1`

```dockerfile
```

-	Layers:
	-	`sha256:a4cb9a5dec7e10b7988a8daa9275f100646f550b16ee910659c51897e56cb13f`  
		Last Modified: Mon, 01 Apr 2024 21:59:55 GMT  
		Size: 15.4 MB (15408585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338be08de37e05c5be4c24446c725b6c2b9cf0575449c5ea7c9347ce338e1522`  
		Last Modified: Mon, 01 Apr 2024 21:59:54 GMT  
		Size: 12.5 KB (12464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:a9bb8779de7f84f61b1b534d63ccab47a51f2b9d023747bc4c929b62dbaff1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.5 MB (538538471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b4b887cb142c95f41d1e6044283f57eae3ce754415c7597d11b8239226928`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
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
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d7a956f97c876348400069f4c082762ec5601b2d1fc8e0d06ad7470953b90`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:5e6d6cfa16c6880acd95cd6d1dfeddc01c9a35d292e9d41f7b1b0f965b17580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c2d02a2c3867ebfb256a9d73c98459ab97dabe4b35c11449b6217648ec2d06`

```dockerfile
```

-	Layers:
	-	`sha256:aab93fcb88ff947e4c0fd611f8cfae85a8c0b10ab803bf8d28cfd1ef568eb018`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 15.3 MB (15349163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e601202e79167711bc3330cb281453c48804c39665dd226b584b1e5bb462e0e4`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 13.2 KB (13173 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:4b41c521d075f5edb972830857e8a3c5173737cbab36139aa99fb25ec8b1da6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.5 MB (551483948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f212f212fd6d3995fc076ae937f33f91b67284d1e1a94a8cc986ab95c01f837`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:32:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45907c1aed496630969e5bd8d388ed0966cd10fcd415b40585cbc3d12e206b5d`  
		Last Modified: Tue, 12 Mar 2024 02:21:03 GMT  
		Size: 214.2 MB (214173497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ee9d09b245a78d4b88b6bf1a84d408018883f352e5f250707cd388f4f5cce`  
		Last Modified: Mon, 01 Apr 2024 21:56:09 GMT  
		Size: 188.5 MB (188474733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:d4cc824b1260175b98ac1b9a836402d870fd8e4381bdaa1a879f1a2579d7c8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15367591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cb603168de00dfd8c90265bea1041bbfc1b66ef59e9181b65b99fa12193e1b`

```dockerfile
```

-	Layers:
	-	`sha256:cdc78d6b31f0bf0f817d2ae7016377cd45fa292e6008a2602af08f61d279c404`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 15.4 MB (15355083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21591c0ee2c667a4fc7d3628d791444a31722bd5ff03a6d6ba6a660d8a75b49e`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 12.5 KB (12508 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:b6ea81b37c9ad8b2c875f64a963b5e418e86d33d41eed529671e86e86d30c884
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
$ docker pull rust@sha256:4c640cb99e88d7e7873a25e5dc693999cd4c5a0f486b54362513f80107920ac3
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
$ docker pull rust@sha256:b6ea81b37c9ad8b2c875f64a963b5e418e86d33d41eed529671e86e86d30c884
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
$ docker pull rust@sha256:a22010a54d04ab9bde99a332f7d37f921bc73fcfce78738a5ae68ab21bcd46b2
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
$ docker pull rust@sha256:6361801bd55ffec96b953437f1083a8d730320b0809292d7d84425ff5f3223a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521770219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead19e243dc6f0b82077e2f7aca0a70a7e4fdd9300f6fa71b1557210b6bea496`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
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
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4251e2c0d85d5696b1917655ebc9009cc6d07741a7410385ecdbf440cc57e92`  
		Last Modified: Wed, 10 Apr 2024 06:54:51 GMT  
		Size: 172.9 MB (172884751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7093785b7995fdc45f27f84b72d85b3425f8cedab6a4692fbb54cd3e8445fd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67072e65542c5c0a7f8c486648acf1470857af35bc22c9994006fe2869e992a`

```dockerfile
```

-	Layers:
	-	`sha256:f58c77986737873a4dd6d0f618ef90591136108b4a126550ab2cbd66d2d01cf5`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 15.4 MB (15370122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3172b133a2a58f28fdc38c6e63776bd4bffb56d2e180b31f207e9f19f4cb2197`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 13.2 KB (13222 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff8d4f50070f7fa5a52f2fcef4f8b51569023de2dde184cb2bf593d596f61547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510035646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb59b3cd57ab4f766666a6c3155019552626eaa52de6881231146e013d09d64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1200500c52f4429e643f87908b44e016ca7b67ac17bcdba07b3884ef8b98fed1`  
		Last Modified: Wed, 10 Apr 2024 00:05:32 GMT  
		Size: 208.6 MB (208612381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b340eca81e3952b867d6121dd010fe5baf4dcf8782a035ef666803baf5a81d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4326b7d2aa5919c3772d38b9ffa6002f9a6b013c3447f507d0800b6c11d178a`

```dockerfile
```

-	Layers:
	-	`sha256:482cba46f5b18fa1452b104ca0bd84ab211676d10a643e56287b9b7477af6258`  
		Last Modified: Wed, 10 Apr 2024 00:05:27 GMT  
		Size: 15.2 MB (15185946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39172abfd0ca99841b69d6dd1903d428f3dfa92415f750b1584c92eae12a7b28`  
		Last Modified: Wed, 10 Apr 2024 00:05:26 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ce750647809bbeb76d60938398758b357a0b66fa60f7066f5195e430b4ab03ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581311877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b136805ec1040e311c556f1db756b3af16437a1c22a9d7c0bdedc4c837138002`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:25:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6faea05ead1ac9cd3244827816e2385b0d62299f7937a4574fc5a9651624c`  
		Last Modified: Tue, 12 Mar 2024 01:35:18 GMT  
		Size: 202.5 MB (202538246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b9ee712f6593072f4693a66c5913d1e384397b49ac2d98a1f3140fffe7df7`  
		Last Modified: Mon, 01 Apr 2024 22:00:00 GMT  
		Size: 241.6 MB (241608857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5204201704e7de4bcdacf00558fafffc7c9b8c9e8900f12f7f97483bdcf56458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15421049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64787d4a6c8f814d976ed17ae2a7920712eed7e04f84ec633f422c49a232ad1`

```dockerfile
```

-	Layers:
	-	`sha256:a4cb9a5dec7e10b7988a8daa9275f100646f550b16ee910659c51897e56cb13f`  
		Last Modified: Mon, 01 Apr 2024 21:59:55 GMT  
		Size: 15.4 MB (15408585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338be08de37e05c5be4c24446c725b6c2b9cf0575449c5ea7c9347ce338e1522`  
		Last Modified: Mon, 01 Apr 2024 21:59:54 GMT  
		Size: 12.5 KB (12464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:a9bb8779de7f84f61b1b534d63ccab47a51f2b9d023747bc4c929b62dbaff1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.5 MB (538538471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b4b887cb142c95f41d1e6044283f57eae3ce754415c7597d11b8239226928`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
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
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d7a956f97c876348400069f4c082762ec5601b2d1fc8e0d06ad7470953b90`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5e6d6cfa16c6880acd95cd6d1dfeddc01c9a35d292e9d41f7b1b0f965b17580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c2d02a2c3867ebfb256a9d73c98459ab97dabe4b35c11449b6217648ec2d06`

```dockerfile
```

-	Layers:
	-	`sha256:aab93fcb88ff947e4c0fd611f8cfae85a8c0b10ab803bf8d28cfd1ef568eb018`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 15.3 MB (15349163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e601202e79167711bc3330cb281453c48804c39665dd226b584b1e5bb462e0e4`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 13.2 KB (13173 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4b41c521d075f5edb972830857e8a3c5173737cbab36139aa99fb25ec8b1da6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.5 MB (551483948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f212f212fd6d3995fc076ae937f33f91b67284d1e1a94a8cc986ab95c01f837`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:32:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45907c1aed496630969e5bd8d388ed0966cd10fcd415b40585cbc3d12e206b5d`  
		Last Modified: Tue, 12 Mar 2024 02:21:03 GMT  
		Size: 214.2 MB (214173497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ee9d09b245a78d4b88b6bf1a84d408018883f352e5f250707cd388f4f5cce`  
		Last Modified: Mon, 01 Apr 2024 21:56:09 GMT  
		Size: 188.5 MB (188474733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d4cc824b1260175b98ac1b9a836402d870fd8e4381bdaa1a879f1a2579d7c8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15367591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cb603168de00dfd8c90265bea1041bbfc1b66ef59e9181b65b99fa12193e1b`

```dockerfile
```

-	Layers:
	-	`sha256:cdc78d6b31f0bf0f817d2ae7016377cd45fa292e6008a2602af08f61d279c404`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 15.4 MB (15355083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21591c0ee2c667a4fc7d3628d791444a31722bd5ff03a6d6ba6a660d8a75b49e`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 12.5 KB (12508 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:f05f963212cd299ed68eb0c2fc11bce34b5e9c16d6315bb70b079478bc42c655
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
$ docker pull rust@sha256:b7dd0a9e0432309ac0ee6bd4058bb75bfeaba8ef8b6d4f946305e9d5ba1048ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 MB (495312885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dc2e90e12adfb05ffe7f3565324bb7b40682bfa9adae698e9870e62ec25ffa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
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
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff24b88ad3798f817849ad391d809ece121dc9b7f82f24bb68eed84561f048`  
		Last Modified: Wed, 10 Apr 2024 05:36:15 GMT  
		Size: 54.6 MB (54588743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f58f24df78e3aabf785017c3197c2a09fd606e7f19a830a1cfde41f681f39e`  
		Last Modified: Wed, 10 Apr 2024 05:36:46 GMT  
		Size: 197.0 MB (196985611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d396a8eca7ee95fff3e5c8b8a21c1df92ec18991eb40d3ca28fea8b5ed20f266`  
		Last Modified: Wed, 10 Apr 2024 06:54:44 GMT  
		Size: 172.9 MB (172884749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1bea0538e2b9f31e9afbd4c8d10b764514307976b5fcddef1f4a4d646cfafdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14986438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a02fe4ad97e458747fa44d8103d1a8f72d2661d05888460c243a2897a2a2e9`

```dockerfile
```

-	Layers:
	-	`sha256:871bcdf817d45ce38cb083572c574fd08e30362efb624894d1e50d5cfbadc210`  
		Last Modified: Wed, 10 Apr 2024 06:54:39 GMT  
		Size: 15.0 MB (14974378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dd175cbfe93b618d8ba22bf1498ee78f8ef178b62b9887454e3eb2c00f50c5`  
		Last Modified: Wed, 10 Apr 2024 06:54:39 GMT  
		Size: 12.1 KB (12060 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:3de59a1810552ce15b00537e55ace34a7cc372de707c6d9f3408f8a9540629cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491529912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe0365b61c725f4967fecee7b926a413ff21cddec137a74990f6a9fe45da2a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea5901896ab9c5ad236e05b73d2065621d4488b4c7d2d61bef4316c3c981b2`  
		Last Modified: Tue, 12 Mar 2024 02:22:12 GMT  
		Size: 167.4 MB (167439330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a22ce7aa75fe6849bccde6452ebda329b039bb673f149b807a6ebab6fc9b53`  
		Last Modified: Wed, 10 Apr 2024 00:01:09 GMT  
		Size: 208.6 MB (208612532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a6f7c82952074d71cb715e34087f3175445219133056ad7fa9670144e666a90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14787749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cad5c1b513434efa6f47f58a6a8e3d1c9bf7578c2cd30f23a787f1a7372b6ab`

```dockerfile
```

-	Layers:
	-	`sha256:6ed4c8aef46f131be746be5a89a077d8b28609cf00ec902b4c0911d45dabce8a`  
		Last Modified: Wed, 10 Apr 2024 00:01:04 GMT  
		Size: 14.8 MB (14776282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f065e754ae91ecf02a567b53fcf1e21d6124125220ed2dae885905e3528890`  
		Last Modified: Wed, 10 Apr 2024 00:01:04 GMT  
		Size: 11.5 KB (11467 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b587651647adb295cf6b122fee23e56562b5e997577aa327d6c1a0c6b649a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.7 MB (555689462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b4c2f9368002c1420b0be85d03984989f0a4e818a3fc18bf499eef1874d3a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d317b4db41e297cffa1559c871d84437b3544f7a4c04d6cf339cd4e8caa94c76`  
		Last Modified: Tue, 12 Mar 2024 01:36:09 GMT  
		Size: 189.9 MB (189914923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5418f8e13c8934d51e047556794e458fa5836df81997654a00e4fdc1073cb9`  
		Last Modified: Mon, 01 Apr 2024 21:56:51 GMT  
		Size: 241.6 MB (241608936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:007752e704a42ff34a74a4aedfffb805a72715dfc71040dec17ecb1db8724292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14988142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5194969bd09bd7a480f3a14dad516153c0148c1fd9ddd62164ef0a2b1520236`

```dockerfile
```

-	Layers:
	-	`sha256:3bc0c024ad242e35e5fa0cda2ccc5332c386bdcfec0cd0cc024e62ecf9fc1dde`  
		Last Modified: Mon, 01 Apr 2024 21:56:47 GMT  
		Size: 15.0 MB (14976847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0c21cae6999254524af2572e00c085a82381d81910fd1c7336c002b7aac74b0`  
		Last Modified: Mon, 01 Apr 2024 21:56:46 GMT  
		Size: 11.3 KB (11295 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:70fdeab84eff10abd352c3077ab7785ea921f5a019eb62f7106962b297969298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.2 MB (515173027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21e4bc28fb83f646ce347daa1059a5210007b3827a3baba597b7fd9465fe0a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
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
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125c557bd27681f5387605727a1b0d44605793da722ea6f8f66b86df9aa54384`  
		Last Modified: Wed, 10 Apr 2024 08:07:12 GMT  
		Size: 16.3 MB (16267921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13acd7d81d47808020936c58e9842c82c55c0205f369482de2b263fe21ed2dc6`  
		Last Modified: Wed, 10 Apr 2024 08:07:31 GMT  
		Size: 55.9 MB (55927749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed69373b65ed4263cd1d2ead3d6570264c8de6a744aa10974a8266c660515080`  
		Last Modified: Wed, 10 Apr 2024 08:08:16 GMT  
		Size: 199.9 MB (199890546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d5ec320ca15085353a9eac55306245a69c0c57ccc50a4011aaf6b70f87d3fb`  
		Last Modified: Wed, 10 Apr 2024 08:56:06 GMT  
		Size: 187.0 MB (187020623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:da43ec4a6be596a9a8ba8f2a6525924a2d26a9746e952339419dfa4065acdfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14975234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b4c78b31760218804790ec5ab591b04cf5d17e30e59b123209347d31c7656c`

```dockerfile
```

-	Layers:
	-	`sha256:e4039901b8fae7bbf1b656a6fbde410c408cd57f6ebe8e20e6e4c7405072ebf9`  
		Last Modified: Wed, 10 Apr 2024 08:56:02 GMT  
		Size: 15.0 MB (14963203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a066ce0f742bb5333d2b61590453bee5a925a2cf0ec058477f3821674fa65d9f`  
		Last Modified: Wed, 10 Apr 2024 08:56:01 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:8471b7c3efb93f5afbc21d7828fcda9fa0a2f7ebb6e55d659116235afda4a71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.4 MB (519415387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036cc170d8e81e97f632eeac3fb7aac0018dcec3088b88dc70bb60a972d57e23`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:37 GMT
ADD file:378e777c8961453a2c8c9a594105395e4a83f5e94a90756bc3eebe9ec18be242 in / 
# Tue, 12 Mar 2024 00:30:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:99575d2dfd5e66cfbe10e815aa8a7bfacb8fa923bf112abd5b9334bec5404161`  
		Last Modified: Tue, 12 Mar 2024 00:38:29 GMT  
		Size: 59.0 MB (58954475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce422567beb05db7b6d7eca359e7168a80a58b1c86d36287c6b86c9b76d845f`  
		Last Modified: Tue, 12 Mar 2024 02:21:17 GMT  
		Size: 16.8 MB (16765930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777aef5bbe7e540f91bd63fda95e7f25c0ba803d2a25a532b2f2306c6b2209d1`  
		Last Modified: Tue, 12 Mar 2024 02:21:36 GMT  
		Size: 58.9 MB (58873337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078e6b4fd896687174cc2013bea6ca7f49c8cd898255e8d37361b8486cb7fe25`  
		Last Modified: Tue, 12 Mar 2024 02:22:13 GMT  
		Size: 196.3 MB (196346975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd567a7f48ce9a547d2ed2aa59d0f4a817bad8643bb24efef2b49c60c022be25`  
		Last Modified: Mon, 01 Apr 2024 21:51:32 GMT  
		Size: 188.5 MB (188474670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5ecefd461ba9b7e9614c363b8ad717c5ed64dfa2ec4fe2d9e3c00aa2e07040cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14953306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69996fb9f6e80b9872d4c166ef6f9326fda8fb0a575c72930785b8692ecbce6`

```dockerfile
```

-	Layers:
	-	`sha256:37077dfb3fce4f1b82732e80df6e8ddd95bf19b0066dec1e8528f0aeaffaf6ab`  
		Last Modified: Mon, 01 Apr 2024 21:51:27 GMT  
		Size: 14.9 MB (14941983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5226f9f7a86e57b8c4914f44b244312869dedf73844351bad06b560a960266`  
		Last Modified: Mon, 01 Apr 2024 21:51:26 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-buster`

```console
$ docker pull rust@sha256:d94731e2a342d1736d23262c936821bfdf330198d757f430f3682c5844ff28c7
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
$ docker pull rust@sha256:ef4bd23ba9eb1fc17a271848ef3a8e11b0574868db455d2fafd61ae56263bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484813822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ef59296b3f783361ff9ecee292d7a3d701c9bf15748e18b947411a563b96f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
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
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e204ce2733ed28c5c2c45652e3fd6034257b2cc15670e98293092efdc65833ec`  
		Last Modified: Wed, 10 Apr 2024 06:55:04 GMT  
		Size: 172.9 MB (172884650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:a6286a89012d075f07d624270d53f0d0df8283771aac7a270eccd1a6ec720625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15621770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a2473f9ccc6c27bb501328c69f43eecbab161d7b4277a52933e462188df7bd`

```dockerfile
```

-	Layers:
	-	`sha256:f3998dec0353df1cec4c007c431ec1d097346b66751099e7cf175df0b6c0295d`  
		Last Modified: Wed, 10 Apr 2024 06:54:59 GMT  
		Size: 15.6 MB (15610116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2cdaeebcd398b7ffe5440b98f95202e4edd572ffd0d45344c138efe49be44ea`  
		Last Modified: Wed, 10 Apr 2024 06:54:58 GMT  
		Size: 11.7 KB (11654 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:f1163e13d71ffaf291be8d0e17de87300460c80bf6e44386811a5758d0764ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486340982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e374110670e91904baaab7f3ed7c6af22e757c9be10ee7b8f0a1b8e7dad38f0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec28d557d3104596d3ba5ab227e1e527ff8f93195f04af289dd5da1316ba29d9`  
		Last Modified: Tue, 12 Mar 2024 02:22:40 GMT  
		Size: 47.4 MB (47410735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb141b0531169976182ab39baba3c902bed903a2c25a2e2045f8c6cee114563c`  
		Last Modified: Tue, 12 Mar 2024 02:23:15 GMT  
		Size: 168.1 MB (168133921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8549a616e2a73c5409031ef4981fbf9ab21f8257e0492c65eb6095983f33d03`  
		Last Modified: Tue, 09 Apr 2024 23:56:04 GMT  
		Size: 208.6 MB (208612535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:65db45a78896d6997258088e0b5eac261a72871c29b3e2c53573b6ddd3fd5a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15423150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f7d3f85b9b79a109f763b2cdf82264b39bfa5029392bce77d3b858944387ba`

```dockerfile
```

-	Layers:
	-	`sha256:890e6de1a22bd1f71a395a5fdfc679a17725d6211ca1d73c0b403dca5e7f8f74`  
		Last Modified: Tue, 09 Apr 2024 23:56:00 GMT  
		Size: 15.4 MB (15412089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11079f1a552e59ef9774e79760fa4335bc5355ee2e30d84dc524fc26dccd032`  
		Last Modified: Tue, 09 Apr 2024 23:55:59 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d83db167f8b57f6fb23e0c1c978e0f0c249ee6e7a779481af62e0636bd6f40fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544097043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee814bf692b8e7c55b8e070bfa7c0b55a2f01a111874ad8000976ac91f9a8f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:28:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8987ebef52bd1e6f6f20b38f5dd0fa9030c75a5089144eabf4a20c7b2aa2605a`  
		Last Modified: Tue, 12 Mar 2024 01:36:57 GMT  
		Size: 52.2 MB (52225028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe09b4296b95b0c32948c55d4f978937b58f5a899208693bb4c304804492322`  
		Last Modified: Tue, 12 Mar 2024 01:37:27 GMT  
		Size: 183.5 MB (183517797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940961b85fdf2974f8776ada55477feb2f6cdfb8eef0be7a114dae57302f215c`  
		Last Modified: Mon, 01 Apr 2024 21:53:42 GMT  
		Size: 241.6 MB (241608909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:9380a50320d9bc998ae47a89e3d31fb990551367caeec9082029bf8639626916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15611676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcf6bea59be5926ea708c5ba672bc55be4ba6c82d2bf3951bae5db90bf8ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:673395325db4802c1fbda7722d59f6aca46826e9b8fdc64601eccc7e3502bbde`  
		Last Modified: Mon, 01 Apr 2024 21:53:37 GMT  
		Size: 15.6 MB (15600784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfee4d187200bc6ff2e874003b62ae48b59ee70de18013d5d21be69e442bc4d`  
		Last Modified: Mon, 01 Apr 2024 21:53:36 GMT  
		Size: 10.9 KB (10892 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; 386

```console
$ docker pull rust@sha256:49629f3d3a1b7cf41847d495f69754d266c3257db8d6c3a401be76e1e8f95e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.4 MB (508366490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8787cf9ea38af799d2c5aa0fc246337f220a2f67ce427d69e6a665f843959019`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
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
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f83de192d57649c06466addcbc7b9ccd636e9d291c22fdf5d7e4a4e6c59450d`  
		Last Modified: Wed, 10 Apr 2024 08:08:28 GMT  
		Size: 18.1 MB (18099188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bc8c20df52365967a4f48f20656372016f14141f60753323f354ed4eca05f0`  
		Last Modified: Wed, 10 Apr 2024 08:08:48 GMT  
		Size: 53.5 MB (53492155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042163e6e1fe3d8805f02202161cd324efea6901ddca3f722950dc6c835431b`  
		Last Modified: Wed, 10 Apr 2024 08:09:32 GMT  
		Size: 198.5 MB (198498026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d1a8f7ee151de43e2a5e7467f74e9aff1e8f94198bfb82e1b9256a16ed5cb6`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:7e6b07cf29947420afc7f3cb9d9b96eafc3cc70e75561c2725b2a8e9b239468a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15627322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2443bc59c40da04634089b702f9ea6ecd8914eeb638af3c06dde5563fc2dcc5f`

```dockerfile
```

-	Layers:
	-	`sha256:4632792f756ad995e692769d516cb8302193e42f60b7ab907b6273b06e339ab4`  
		Last Modified: Wed, 10 Apr 2024 08:56:03 GMT  
		Size: 15.6 MB (15615697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82575d53ebbbb2229ba5140118990013e95bf8e9198c294a5eb759e798c44bb5`  
		Last Modified: Wed, 10 Apr 2024 08:56:03 GMT  
		Size: 11.6 KB (11625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim`

```console
$ docker pull rust@sha256:78b5459dc7218e633da119c82b215d54e5029fe3cb7e0e9bd7ca19ffacda77ca
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
$ docker pull rust@sha256:ed00d3908ba2ade42982456c2f9b8b6db5fecf14e9d1d2f58a1dedbb6a7c924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272802753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e1b814adbb0a324618baf1524efbae1616c5450ef892429d2e0c5f3ddc188c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868daa4b67ac105f565dd9a057f7f4f10cc38f9816536d9e7a6bbd620b8ca37d`  
		Last Modified: Wed, 10 Apr 2024 02:56:18 GMT  
		Size: 243.7 MB (243671395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a5d7d5b8dc2e5968bffc0faf477c8fbc4077fbe3ca1631972e06d45cf80a35f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21623c7d2b56a2d1b34a660d9884654aa92743361e69b4f3c1f2e14d1be20598`

```dockerfile
```

-	Layers:
	-	`sha256:db88d5519f271b7d1221885138eb2cb745ff3908ba759b8646ac90e06f7f2527`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 3.9 MB (3919062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe0382e87e578e32ad71f989f31936ddc388b9faf74f0e736098ac3ba5c190c`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 12.8 KB (12814 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:8fae5654772edd365dfd01f53835efcd50c85e9a9124c88476d6cfd02b8987e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281125976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd3d4379b89c0b08406e6611007fc87b392af0616e7c7a78525dd7fef8954b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbdfe2d8afc590898b008ae5ac867b9c9ecaba2e23c4ce8242c8ff24dfcb4e`  
		Last Modified: Mon, 01 Apr 2024 22:05:59 GMT  
		Size: 256.4 MB (256409251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:57d8f50dd1c6b235d090f83fe48ae776dc009ae8e9446e0e98f71bc218118ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27fb31bede8afd182c86d6517398034aafef2892fe5a8533744f9a46d0427f8`

```dockerfile
```

-	Layers:
	-	`sha256:ae00f303130b0e32159908141b05a139cc824b82a42f44b70812b88a36ea65a4`  
		Last Modified: Mon, 01 Apr 2024 22:05:54 GMT  
		Size: 3.7 MB (3737518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de84682983e233db29c48bc5d1ad2738cbfbd5eb650bbe9fb47772d589981b85`  
		Last Modified: Mon, 01 Apr 2024 22:05:53 GMT  
		Size: 12.6 KB (12637 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6af0432b6d1b9274fbda00f1e31e2d3465171e66d32318c729d03bd3c51618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336617112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355ad31b2818638e6828730de81e62b4574f851cd03d587008dd227b5e75e1a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8aac4a9ac99feb14bacf4109c65ccefc4efa32032e32522c7fc72370be73c9`  
		Last Modified: Mon, 01 Apr 2024 22:01:33 GMT  
		Size: 307.5 MB (307460678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b269d7552b7b1b75d79080032ac62815904b266c69efe60dcaaf88ebe8194195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3fd44111ce2bb4129bc96af803aad106c6fd6cb819c617ad5392dfbf9b8f6b`

```dockerfile
```

-	Layers:
	-	`sha256:b13e178634ac422c29c30639e4a5404d22c1636919f1268cd8af918a15f25ff1`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 3.9 MB (3942630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29301f3480b2dcd0cc128b64522f960bcc98ecf37d6db7a527cbd65d59f31c34`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 12.6 KB (12553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:9a072848e2d833cf694b18aefa244a460553f7cf6c85b58f5e2e52286efd174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284750516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca43af6be05127a03ec4d1b7aca13a5833998f17cdb5af3206b6d55dd1991a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f760cffd225a2b32fbf671ab6251bed8d1a36d87cac79c98316872c7a69f93`  
		Last Modified: Wed, 10 Apr 2024 02:03:51 GMT  
		Size: 254.6 MB (254604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d144c1d027fa1f9b95ce873a14624a8040451e3f0e7bc3bf786fae4efc033a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98508d35fb64f25d374e4da636cff8ae441ac72ffc1e3d86d7dad746952d5109`

```dockerfile
```

-	Layers:
	-	`sha256:6af998bc21467f538e8f16857cbd4b31d5b202bdca8935602e1f72ce7eca98f5`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 3.9 MB (3900761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbc0607021120ea5a7abb310a8f1eb23efa63e81dad3298c28eb61e7e63eb70`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e8f8ec53a391d9113d8080ba20f31c338c4cf6cbe6aae3d3f04a972868df31a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290361922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e298b7e70665b3442d85e1806ad164a55a9f7b0a16463dad74a0bf044226f5fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4418400b66496376009e657c8080f4ea2dbbaaf1bccc166de6aac1b72a8e971`  
		Last Modified: Mon, 01 Apr 2024 21:58:19 GMT  
		Size: 257.2 MB (257242899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:da4ab5fbedd89882e94c6ff8acef6cc756b9b3d25f9d18c7ce53f61a46f74af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3905390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85edd0d98bb412cff6a24ffa03005353fc736121e05de765d98422afe663e20`

```dockerfile
```

-	Layers:
	-	`sha256:6feae90e068af601f73655101ccf01c3d659370b865a4b719e3b7fccf8b87d68`  
		Last Modified: Mon, 01 Apr 2024 21:58:13 GMT  
		Size: 3.9 MB (3892794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fc000faf56d83a6990e8558b09b2c09cb026e52b4ec329e598045f9fad096c`  
		Last Modified: Mon, 01 Apr 2024 21:58:12 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:78b5459dc7218e633da119c82b215d54e5029fe3cb7e0e9bd7ca19ffacda77ca
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
$ docker pull rust@sha256:ed00d3908ba2ade42982456c2f9b8b6db5fecf14e9d1d2f58a1dedbb6a7c924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272802753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e1b814adbb0a324618baf1524efbae1616c5450ef892429d2e0c5f3ddc188c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868daa4b67ac105f565dd9a057f7f4f10cc38f9816536d9e7a6bbd620b8ca37d`  
		Last Modified: Wed, 10 Apr 2024 02:56:18 GMT  
		Size: 243.7 MB (243671395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a5d7d5b8dc2e5968bffc0faf477c8fbc4077fbe3ca1631972e06d45cf80a35f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21623c7d2b56a2d1b34a660d9884654aa92743361e69b4f3c1f2e14d1be20598`

```dockerfile
```

-	Layers:
	-	`sha256:db88d5519f271b7d1221885138eb2cb745ff3908ba759b8646ac90e06f7f2527`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 3.9 MB (3919062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe0382e87e578e32ad71f989f31936ddc388b9faf74f0e736098ac3ba5c190c`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 12.8 KB (12814 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:8fae5654772edd365dfd01f53835efcd50c85e9a9124c88476d6cfd02b8987e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281125976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd3d4379b89c0b08406e6611007fc87b392af0616e7c7a78525dd7fef8954b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbdfe2d8afc590898b008ae5ac867b9c9ecaba2e23c4ce8242c8ff24dfcb4e`  
		Last Modified: Mon, 01 Apr 2024 22:05:59 GMT  
		Size: 256.4 MB (256409251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:57d8f50dd1c6b235d090f83fe48ae776dc009ae8e9446e0e98f71bc218118ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27fb31bede8afd182c86d6517398034aafef2892fe5a8533744f9a46d0427f8`

```dockerfile
```

-	Layers:
	-	`sha256:ae00f303130b0e32159908141b05a139cc824b82a42f44b70812b88a36ea65a4`  
		Last Modified: Mon, 01 Apr 2024 22:05:54 GMT  
		Size: 3.7 MB (3737518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de84682983e233db29c48bc5d1ad2738cbfbd5eb650bbe9fb47772d589981b85`  
		Last Modified: Mon, 01 Apr 2024 22:05:53 GMT  
		Size: 12.6 KB (12637 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6af0432b6d1b9274fbda00f1e31e2d3465171e66d32318c729d03bd3c51618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336617112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355ad31b2818638e6828730de81e62b4574f851cd03d587008dd227b5e75e1a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8aac4a9ac99feb14bacf4109c65ccefc4efa32032e32522c7fc72370be73c9`  
		Last Modified: Mon, 01 Apr 2024 22:01:33 GMT  
		Size: 307.5 MB (307460678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b269d7552b7b1b75d79080032ac62815904b266c69efe60dcaaf88ebe8194195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3fd44111ce2bb4129bc96af803aad106c6fd6cb819c617ad5392dfbf9b8f6b`

```dockerfile
```

-	Layers:
	-	`sha256:b13e178634ac422c29c30639e4a5404d22c1636919f1268cd8af918a15f25ff1`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 3.9 MB (3942630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29301f3480b2dcd0cc128b64522f960bcc98ecf37d6db7a527cbd65d59f31c34`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 12.6 KB (12553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:9a072848e2d833cf694b18aefa244a460553f7cf6c85b58f5e2e52286efd174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284750516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca43af6be05127a03ec4d1b7aca13a5833998f17cdb5af3206b6d55dd1991a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f760cffd225a2b32fbf671ab6251bed8d1a36d87cac79c98316872c7a69f93`  
		Last Modified: Wed, 10 Apr 2024 02:03:51 GMT  
		Size: 254.6 MB (254604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d144c1d027fa1f9b95ce873a14624a8040451e3f0e7bc3bf786fae4efc033a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98508d35fb64f25d374e4da636cff8ae441ac72ffc1e3d86d7dad746952d5109`

```dockerfile
```

-	Layers:
	-	`sha256:6af998bc21467f538e8f16857cbd4b31d5b202bdca8935602e1f72ce7eca98f5`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 3.9 MB (3900761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbc0607021120ea5a7abb310a8f1eb23efa63e81dad3298c28eb61e7e63eb70`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e8f8ec53a391d9113d8080ba20f31c338c4cf6cbe6aae3d3f04a972868df31a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290361922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e298b7e70665b3442d85e1806ad164a55a9f7b0a16463dad74a0bf044226f5fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4418400b66496376009e657c8080f4ea2dbbaaf1bccc166de6aac1b72a8e971`  
		Last Modified: Mon, 01 Apr 2024 21:58:19 GMT  
		Size: 257.2 MB (257242899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:da4ab5fbedd89882e94c6ff8acef6cc756b9b3d25f9d18c7ce53f61a46f74af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3905390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85edd0d98bb412cff6a24ffa03005353fc736121e05de765d98422afe663e20`

```dockerfile
```

-	Layers:
	-	`sha256:6feae90e068af601f73655101ccf01c3d659370b865a4b719e3b7fccf8b87d68`  
		Last Modified: Mon, 01 Apr 2024 21:58:13 GMT  
		Size: 3.9 MB (3892794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fc000faf56d83a6990e8558b09b2c09cb026e52b4ec329e598045f9fad096c`  
		Last Modified: Mon, 01 Apr 2024 21:58:12 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:81435e6e61bb826e17ff6e260461db26d579c96298ae22533028e2b03cfe1803
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
$ docker pull rust@sha256:e3703a692d6689cee0490363bfc8108a9c9e590df6988f2920eb71ab77937c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264463700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fc023abba24900ad681ae8421b1f2d1c477a0cdc7f8779c5147a5df2e64d1f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
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
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ab2f2a3ce344d856412bb76c0cbce30a35aeb53176eb5cec120e3c216f01a`  
		Last Modified: Wed, 10 Apr 2024 02:56:20 GMT  
		Size: 233.0 MB (233035962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:93f63b6fad174237aa1145d25dad1cc04f8aea997947828b38063021fe446db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78abe840ffae11375c7e3b134fad5ba0df3447f6e29e7245a2f7719df6a63b15`

```dockerfile
```

-	Layers:
	-	`sha256:6f58cc69594b21ac6cab79cbd7ffe7bb3572c3a95b2e9e4d2ab1e80b47bde438`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 4.1 MB (4139675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a713004d07c70ce533a189ac1c7759bf8978f36fa4e86386307445c2f7a4b4df`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 11.6 KB (11626 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:26d4f2c56522ea7ca8a330117e7f9494432528454e434b87d3918c83231e17ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277429232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc64990d1edbbaa7bcfb16939d5cae08f9cf6d2970c6dd863a2d09dcd8241e62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:38 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
# Tue, 12 Mar 2024 00:59:38 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c5b544693e63eaac90034284eef7243457a9a679d1e583cc55dafed1c8bf9`  
		Last Modified: Mon, 01 Apr 2024 22:01:28 GMT  
		Size: 250.8 MB (250846518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3d96ab8013fcb764254a3679f4dd5f4108b571415128e3ca7b3c8f8d493c203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4963c801a528cbe9ba8553e0af2c5993a827d1bf691b4357e00d091507420fdb`

```dockerfile
```

-	Layers:
	-	`sha256:b9c894fee7248dc0583cb4d373353376ca502b9f3d4aaf97f2fcedd57d580b5e`  
		Last Modified: Mon, 01 Apr 2024 22:01:23 GMT  
		Size: 3.9 MB (3949600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61a737341c5d2a8f46beb7e1cb2f2bcd72ccd316a605b269078c15eb13129c3`  
		Last Modified: Mon, 01 Apr 2024 22:01:22 GMT  
		Size: 11.4 KB (11417 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d70206b0586e8e64e875ea16ec912e8bd72d21906d2568856ce84d6689174290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327412046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5808e965af077392cd1baf609dcc56a41f121bd3eb9e5ae2fc6accac265d39f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3e8d71fd971f61b0388fb2834d9f24df7728ed3bbdc3a823b64ccf8ad2412`  
		Last Modified: Mon, 01 Apr 2024 21:58:19 GMT  
		Size: 297.3 MB (297340930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b42ec493301ad10133f471ed2fc7a794439d9b3951ba399efd8a158a0b0d4b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4147914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8005aa07b0305f1b50df5f923ef26f447e28d2ed655a4a5ba2f694a56a731c`

```dockerfile
```

-	Layers:
	-	`sha256:0a16db309db453f9938651346d32b0b8e35f96e842c13c0ffa1c396e7454325c`  
		Last Modified: Mon, 01 Apr 2024 21:58:13 GMT  
		Size: 4.1 MB (4136557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:416c38e8719f91a3859a3afb446eef65cbb8954ea7e58d945e61c4a799f15b9d`  
		Last Modified: Mon, 01 Apr 2024 21:58:12 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:e47eddf08aa277fd773b469789469b80214dc1c6eb89cc52dbaed2a45572b346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280210792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c34fb5b92c2203fcb8db1509344b4fad479143f90c59036e639d20e6cf231`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
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
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f761c683b352d393ff3a70a31f1cdb3309470baef708acaaec1d5f65178a780`  
		Last Modified: Wed, 10 Apr 2024 01:54:11 GMT  
		Size: 247.8 MB (247797376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d1306fc47b4244d7f9e7943f5aae84fd486ba130d8d39c608767cb956ddf3271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3908b559c177afd6719140b5a2a3541d95e0921cb245764b7a06f080971b6ac3`

```dockerfile
```

-	Layers:
	-	`sha256:a032ac7469111c4a51d7d1e1b0c75b35aa34e3c8b0d8d8e5bd42030f843b8926`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 4.1 MB (4131731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0b157250963b35b33549efb108518a419ccc9f570c228ba225ea203828b0aa6`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 11.6 KB (11597 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:c51654576d219a3c1810ec0f57d020a9a2fae17fa75a23f0d9d8b3744618660f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278761579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf13a40fa5213e2af5148bc8ba383c6887afb092fe4af03241476a167078cd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:31:08 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Tue, 12 Mar 2024 00:31:12 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37dc3072fd9cd9fa92e7d1b88a1a366b360bcbffaa4f190fc3ac03c4cd5a818`  
		Last Modified: Mon, 01 Apr 2024 21:53:46 GMT  
		Size: 243.5 MB (243463572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4c28805af771ded17532d58b5f8e663ecc6f2513a3d94048509e9f3606592e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713d1526554c91ba1f62906da53b3f136f6bd82097283d6f13d71589576ec883`

```dockerfile
```

-	Layers:
	-	`sha256:4bbad0dcb5d31db6ef4f6b52b195d24c5725f4de425b5776723a0c94a2a67df0`  
		Last Modified: Mon, 01 Apr 2024 21:53:36 GMT  
		Size: 4.1 MB (4100758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef88e86936a49014f33c8e5475ac58e3919976975996b989afde2c62f371ff8b`  
		Last Modified: Mon, 01 Apr 2024 21:53:35 GMT  
		Size: 11.4 KB (11385 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-buster`

```console
$ docker pull rust@sha256:bfa022f7f35ee14e7375de549deaddeaf1ae13bedd4ca845fb55c75fa48c37e0
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
$ docker pull rust@sha256:bef060961cbd2174621dbdc808519969112b6fbccb3e2c4c90b67c67ec186450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245495284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcb8545702f9a0e6721b40aaa469aefcb0622810562883d52ba50ba057c1c5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
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
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c72519ff7f40e33d03c7d3f47e19dcd8420c4c92434d03570faaff716312528`  
		Last Modified: Wed, 10 Apr 2024 02:56:19 GMT  
		Size: 218.3 MB (218304422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:8dcab7ab30592663a02fd73c824b93ceb27704fd316dfdc4a14a8fd53cadca34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858fb1eb2641158105afbe01ba8f4c231a8aae4ad85d82a1c25586aafbbc59da`

```dockerfile
```

-	Layers:
	-	`sha256:38f8d81ee6092d2bfbe77b6702062de3b7d23f5bde67d9773915331d261cb7c0`  
		Last Modified: Wed, 10 Apr 2024 02:56:16 GMT  
		Size: 3.6 MB (3585441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb65268fc77b08bd0a7fa791c3297b3bced6acd88a4bc12a1af05bcf384c5c8`  
		Last Modified: Wed, 10 Apr 2024 02:56:16 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:0c22e20adc4dc2f8053478d027b264ce618469bf08d54893fbf2377658558a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264285591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43db9b4246ad7f36b5cf421516f4d76ce05a39acf043747c47239008af2afb83`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:57 GMT
ADD file:87f5e14c74c217f7538860dd43d6b1910663955972cf5270e3d1a8254956878c in / 
# Tue, 12 Mar 2024 00:59:57 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f02c84b2c1c85cfdbae8bb78a52226f2b54d86f3eb2466ac3a81fc25ffde9eb`  
		Last Modified: Tue, 12 Mar 2024 01:05:07 GMT  
		Size: 22.8 MB (22795622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23601052881b5b7693660e13d60ad40a44fa6d28a6eab03e29bc335ef22614`  
		Last Modified: Mon, 01 Apr 2024 21:57:18 GMT  
		Size: 241.5 MB (241489969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:a259de885b15d5261cb5637679bd82b06cc553086bcc617ceabb1cbcd5911283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3403962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975b206faba1555d08aeb3b367f7e8ace57ef82f52c901953177d20e69f34da4`

```dockerfile
```

-	Layers:
	-	`sha256:a7ec9dae53125430f432e43fa64bb1b7617be4f96618022f8b1c9bd56d02e963`  
		Last Modified: Mon, 01 Apr 2024 21:57:13 GMT  
		Size: 3.4 MB (3392947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8fec98a1e9cbf26e1d3fbbe10104c9e731f2418317039f63184e7f4d36d2663`  
		Last Modified: Mon, 01 Apr 2024 21:57:13 GMT  
		Size: 11.0 KB (11015 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a5684abbc7f54bd9c58a5364b586316c5353fd8542509a6e13113239001c9fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307812606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5bde5f6654a3312b9f1f9f6ed51f121b8ad4edd013ae962ab6efcdef6ec0ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:05 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
# Tue, 12 Mar 2024 00:46:06 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f061dca4371eb34330ba3af7c2817b1504f610d9540f399dca1308b85fc26c6`  
		Last Modified: Mon, 01 Apr 2024 21:55:11 GMT  
		Size: 281.8 MB (281842017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:075ab39c9dbaadb406e6e27af9cc64e481f3ac8c6675922e221c65a580e52a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b111ed85dfdbef2cf909ba27fa12deebe2a85a1821a0c05d3c9a6f34856e0f`

```dockerfile
```

-	Layers:
	-	`sha256:413744a81638db98004c236d84b70a1ee323b42dd5316eb0c7b8109d75395654`  
		Last Modified: Mon, 01 Apr 2024 21:55:04 GMT  
		Size: 3.6 MB (3574589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c49bb1f862c0df67b88faca306222bd29aa102812117111de44057071d9b1bf2`  
		Last Modified: Mon, 01 Apr 2024 21:55:03 GMT  
		Size: 11.0 KB (10955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:f16cf382bb643b61546e0716b11c8865933e5ed812ac80169f0c1059d788a546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264864857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c822134f762bf9cdc5c0c15d0d06f50df5c808cbf81120d841f19ee30850f2c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6033d014a0c5c8d87a61d23e20506ec550ea93ef72866e76bfe5a468ceebf619 in / 
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
	-	`sha256:d349bc9800fc6053f91af64b3ce845b5191cc9e0ae2d2001951381ae2d08e46e`  
		Last Modified: Wed, 10 Apr 2024 01:03:40 GMT  
		Size: 27.8 MB (27848331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54caad959c94915ec006deffe9d9bd347eb55d50b70b7ac94922c1784fbdf03`  
		Last Modified: Wed, 10 Apr 2024 01:54:11 GMT  
		Size: 237.0 MB (237016526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:752c286f93a3ae53df42fe4c2153bcdb6523435d242f194aa2925996d9e0251f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c94b966dc0d5d95ee36fe5b571695e3b2992333e109cd314d4b496537982f2c`

```dockerfile
```

-	Layers:
	-	`sha256:f59e8592b975bb56e79e105cf29ff5ee1831a7336624007d7e81a302f3b159d6`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 3.6 MB (3592066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a39c68120f1cbcd3caaed0c37db595248763df96455ec3bccba15f6356f80efe`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 11.2 KB (11190 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77`

```console
$ docker pull rust@sha256:a22010a54d04ab9bde99a332f7d37f921bc73fcfce78738a5ae68ab21bcd46b2
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
$ docker pull rust@sha256:6361801bd55ffec96b953437f1083a8d730320b0809292d7d84425ff5f3223a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521770219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead19e243dc6f0b82077e2f7aca0a70a7e4fdd9300f6fa71b1557210b6bea496`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
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
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4251e2c0d85d5696b1917655ebc9009cc6d07741a7410385ecdbf440cc57e92`  
		Last Modified: Wed, 10 Apr 2024 06:54:51 GMT  
		Size: 172.9 MB (172884751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77` - unknown; unknown

```console
$ docker pull rust@sha256:7093785b7995fdc45f27f84b72d85b3425f8cedab6a4692fbb54cd3e8445fd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67072e65542c5c0a7f8c486648acf1470857af35bc22c9994006fe2869e992a`

```dockerfile
```

-	Layers:
	-	`sha256:f58c77986737873a4dd6d0f618ef90591136108b4a126550ab2cbd66d2d01cf5`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 15.4 MB (15370122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3172b133a2a58f28fdc38c6e63776bd4bffb56d2e180b31f207e9f19f4cb2197`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 13.2 KB (13222 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff8d4f50070f7fa5a52f2fcef4f8b51569023de2dde184cb2bf593d596f61547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510035646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb59b3cd57ab4f766666a6c3155019552626eaa52de6881231146e013d09d64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1200500c52f4429e643f87908b44e016ca7b67ac17bcdba07b3884ef8b98fed1`  
		Last Modified: Wed, 10 Apr 2024 00:05:32 GMT  
		Size: 208.6 MB (208612381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77` - unknown; unknown

```console
$ docker pull rust@sha256:b340eca81e3952b867d6121dd010fe5baf4dcf8782a035ef666803baf5a81d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4326b7d2aa5919c3772d38b9ffa6002f9a6b013c3447f507d0800b6c11d178a`

```dockerfile
```

-	Layers:
	-	`sha256:482cba46f5b18fa1452b104ca0bd84ab211676d10a643e56287b9b7477af6258`  
		Last Modified: Wed, 10 Apr 2024 00:05:27 GMT  
		Size: 15.2 MB (15185946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39172abfd0ca99841b69d6dd1903d428f3dfa92415f750b1584c92eae12a7b28`  
		Last Modified: Wed, 10 Apr 2024 00:05:26 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ce750647809bbeb76d60938398758b357a0b66fa60f7066f5195e430b4ab03ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581311877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b136805ec1040e311c556f1db756b3af16437a1c22a9d7c0bdedc4c837138002`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:25:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6faea05ead1ac9cd3244827816e2385b0d62299f7937a4574fc5a9651624c`  
		Last Modified: Tue, 12 Mar 2024 01:35:18 GMT  
		Size: 202.5 MB (202538246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b9ee712f6593072f4693a66c5913d1e384397b49ac2d98a1f3140fffe7df7`  
		Last Modified: Mon, 01 Apr 2024 22:00:00 GMT  
		Size: 241.6 MB (241608857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77` - unknown; unknown

```console
$ docker pull rust@sha256:5204201704e7de4bcdacf00558fafffc7c9b8c9e8900f12f7f97483bdcf56458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15421049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64787d4a6c8f814d976ed17ae2a7920712eed7e04f84ec633f422c49a232ad1`

```dockerfile
```

-	Layers:
	-	`sha256:a4cb9a5dec7e10b7988a8daa9275f100646f550b16ee910659c51897e56cb13f`  
		Last Modified: Mon, 01 Apr 2024 21:59:55 GMT  
		Size: 15.4 MB (15408585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338be08de37e05c5be4c24446c725b6c2b9cf0575449c5ea7c9347ce338e1522`  
		Last Modified: Mon, 01 Apr 2024 21:59:54 GMT  
		Size: 12.5 KB (12464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77` - linux; 386

```console
$ docker pull rust@sha256:a9bb8779de7f84f61b1b534d63ccab47a51f2b9d023747bc4c929b62dbaff1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.5 MB (538538471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b4b887cb142c95f41d1e6044283f57eae3ce754415c7597d11b8239226928`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
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
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d7a956f97c876348400069f4c082762ec5601b2d1fc8e0d06ad7470953b90`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77` - unknown; unknown

```console
$ docker pull rust@sha256:5e6d6cfa16c6880acd95cd6d1dfeddc01c9a35d292e9d41f7b1b0f965b17580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c2d02a2c3867ebfb256a9d73c98459ab97dabe4b35c11449b6217648ec2d06`

```dockerfile
```

-	Layers:
	-	`sha256:aab93fcb88ff947e4c0fd611f8cfae85a8c0b10ab803bf8d28cfd1ef568eb018`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 15.3 MB (15349163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e601202e79167711bc3330cb281453c48804c39665dd226b584b1e5bb462e0e4`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 13.2 KB (13173 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77` - linux; ppc64le

```console
$ docker pull rust@sha256:4b41c521d075f5edb972830857e8a3c5173737cbab36139aa99fb25ec8b1da6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.5 MB (551483948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f212f212fd6d3995fc076ae937f33f91b67284d1e1a94a8cc986ab95c01f837`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:32:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45907c1aed496630969e5bd8d388ed0966cd10fcd415b40585cbc3d12e206b5d`  
		Last Modified: Tue, 12 Mar 2024 02:21:03 GMT  
		Size: 214.2 MB (214173497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ee9d09b245a78d4b88b6bf1a84d408018883f352e5f250707cd388f4f5cce`  
		Last Modified: Mon, 01 Apr 2024 21:56:09 GMT  
		Size: 188.5 MB (188474733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77` - unknown; unknown

```console
$ docker pull rust@sha256:d4cc824b1260175b98ac1b9a836402d870fd8e4381bdaa1a879f1a2579d7c8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15367591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cb603168de00dfd8c90265bea1041bbfc1b66ef59e9181b65b99fa12193e1b`

```dockerfile
```

-	Layers:
	-	`sha256:cdc78d6b31f0bf0f817d2ae7016377cd45fa292e6008a2602af08f61d279c404`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 15.4 MB (15355083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21591c0ee2c667a4fc7d3628d791444a31722bd5ff03a6d6ba6a660d8a75b49e`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 12.5 KB (12508 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-alpine`

```console
$ docker pull rust@sha256:b6ea81b37c9ad8b2c875f64a963b5e418e86d33d41eed529671e86e86d30c884
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
$ docker pull rust@sha256:4c640cb99e88d7e7873a25e5dc693999cd4c5a0f486b54362513f80107920ac3
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
$ docker pull rust@sha256:b6ea81b37c9ad8b2c875f64a963b5e418e86d33d41eed529671e86e86d30c884
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
$ docker pull rust@sha256:a22010a54d04ab9bde99a332f7d37f921bc73fcfce78738a5ae68ab21bcd46b2
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
$ docker pull rust@sha256:6361801bd55ffec96b953437f1083a8d730320b0809292d7d84425ff5f3223a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521770219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead19e243dc6f0b82077e2f7aca0a70a7e4fdd9300f6fa71b1557210b6bea496`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
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
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4251e2c0d85d5696b1917655ebc9009cc6d07741a7410385ecdbf440cc57e92`  
		Last Modified: Wed, 10 Apr 2024 06:54:51 GMT  
		Size: 172.9 MB (172884751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7093785b7995fdc45f27f84b72d85b3425f8cedab6a4692fbb54cd3e8445fd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67072e65542c5c0a7f8c486648acf1470857af35bc22c9994006fe2869e992a`

```dockerfile
```

-	Layers:
	-	`sha256:f58c77986737873a4dd6d0f618ef90591136108b4a126550ab2cbd66d2d01cf5`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 15.4 MB (15370122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3172b133a2a58f28fdc38c6e63776bd4bffb56d2e180b31f207e9f19f4cb2197`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 13.2 KB (13222 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff8d4f50070f7fa5a52f2fcef4f8b51569023de2dde184cb2bf593d596f61547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510035646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb59b3cd57ab4f766666a6c3155019552626eaa52de6881231146e013d09d64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1200500c52f4429e643f87908b44e016ca7b67ac17bcdba07b3884ef8b98fed1`  
		Last Modified: Wed, 10 Apr 2024 00:05:32 GMT  
		Size: 208.6 MB (208612381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b340eca81e3952b867d6121dd010fe5baf4dcf8782a035ef666803baf5a81d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4326b7d2aa5919c3772d38b9ffa6002f9a6b013c3447f507d0800b6c11d178a`

```dockerfile
```

-	Layers:
	-	`sha256:482cba46f5b18fa1452b104ca0bd84ab211676d10a643e56287b9b7477af6258`  
		Last Modified: Wed, 10 Apr 2024 00:05:27 GMT  
		Size: 15.2 MB (15185946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39172abfd0ca99841b69d6dd1903d428f3dfa92415f750b1584c92eae12a7b28`  
		Last Modified: Wed, 10 Apr 2024 00:05:26 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ce750647809bbeb76d60938398758b357a0b66fa60f7066f5195e430b4ab03ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581311877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b136805ec1040e311c556f1db756b3af16437a1c22a9d7c0bdedc4c837138002`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:25:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6faea05ead1ac9cd3244827816e2385b0d62299f7937a4574fc5a9651624c`  
		Last Modified: Tue, 12 Mar 2024 01:35:18 GMT  
		Size: 202.5 MB (202538246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b9ee712f6593072f4693a66c5913d1e384397b49ac2d98a1f3140fffe7df7`  
		Last Modified: Mon, 01 Apr 2024 22:00:00 GMT  
		Size: 241.6 MB (241608857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5204201704e7de4bcdacf00558fafffc7c9b8c9e8900f12f7f97483bdcf56458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15421049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64787d4a6c8f814d976ed17ae2a7920712eed7e04f84ec633f422c49a232ad1`

```dockerfile
```

-	Layers:
	-	`sha256:a4cb9a5dec7e10b7988a8daa9275f100646f550b16ee910659c51897e56cb13f`  
		Last Modified: Mon, 01 Apr 2024 21:59:55 GMT  
		Size: 15.4 MB (15408585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338be08de37e05c5be4c24446c725b6c2b9cf0575449c5ea7c9347ce338e1522`  
		Last Modified: Mon, 01 Apr 2024 21:59:54 GMT  
		Size: 12.5 KB (12464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bookworm` - linux; 386

```console
$ docker pull rust@sha256:a9bb8779de7f84f61b1b534d63ccab47a51f2b9d023747bc4c929b62dbaff1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.5 MB (538538471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b4b887cb142c95f41d1e6044283f57eae3ce754415c7597d11b8239226928`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
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
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d7a956f97c876348400069f4c082762ec5601b2d1fc8e0d06ad7470953b90`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5e6d6cfa16c6880acd95cd6d1dfeddc01c9a35d292e9d41f7b1b0f965b17580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c2d02a2c3867ebfb256a9d73c98459ab97dabe4b35c11449b6217648ec2d06`

```dockerfile
```

-	Layers:
	-	`sha256:aab93fcb88ff947e4c0fd611f8cfae85a8c0b10ab803bf8d28cfd1ef568eb018`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 15.3 MB (15349163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e601202e79167711bc3330cb281453c48804c39665dd226b584b1e5bb462e0e4`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 13.2 KB (13173 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4b41c521d075f5edb972830857e8a3c5173737cbab36139aa99fb25ec8b1da6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.5 MB (551483948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f212f212fd6d3995fc076ae937f33f91b67284d1e1a94a8cc986ab95c01f837`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:32:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45907c1aed496630969e5bd8d388ed0966cd10fcd415b40585cbc3d12e206b5d`  
		Last Modified: Tue, 12 Mar 2024 02:21:03 GMT  
		Size: 214.2 MB (214173497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ee9d09b245a78d4b88b6bf1a84d408018883f352e5f250707cd388f4f5cce`  
		Last Modified: Mon, 01 Apr 2024 21:56:09 GMT  
		Size: 188.5 MB (188474733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d4cc824b1260175b98ac1b9a836402d870fd8e4381bdaa1a879f1a2579d7c8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15367591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cb603168de00dfd8c90265bea1041bbfc1b66ef59e9181b65b99fa12193e1b`

```dockerfile
```

-	Layers:
	-	`sha256:cdc78d6b31f0bf0f817d2ae7016377cd45fa292e6008a2602af08f61d279c404`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 15.4 MB (15355083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21591c0ee2c667a4fc7d3628d791444a31722bd5ff03a6d6ba6a660d8a75b49e`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 12.5 KB (12508 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-bullseye`

```console
$ docker pull rust@sha256:f05f963212cd299ed68eb0c2fc11bce34b5e9c16d6315bb70b079478bc42c655
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
$ docker pull rust@sha256:b7dd0a9e0432309ac0ee6bd4058bb75bfeaba8ef8b6d4f946305e9d5ba1048ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 MB (495312885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dc2e90e12adfb05ffe7f3565324bb7b40682bfa9adae698e9870e62ec25ffa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
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
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff24b88ad3798f817849ad391d809ece121dc9b7f82f24bb68eed84561f048`  
		Last Modified: Wed, 10 Apr 2024 05:36:15 GMT  
		Size: 54.6 MB (54588743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f58f24df78e3aabf785017c3197c2a09fd606e7f19a830a1cfde41f681f39e`  
		Last Modified: Wed, 10 Apr 2024 05:36:46 GMT  
		Size: 197.0 MB (196985611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d396a8eca7ee95fff3e5c8b8a21c1df92ec18991eb40d3ca28fea8b5ed20f266`  
		Last Modified: Wed, 10 Apr 2024 06:54:44 GMT  
		Size: 172.9 MB (172884749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1bea0538e2b9f31e9afbd4c8d10b764514307976b5fcddef1f4a4d646cfafdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14986438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a02fe4ad97e458747fa44d8103d1a8f72d2661d05888460c243a2897a2a2e9`

```dockerfile
```

-	Layers:
	-	`sha256:871bcdf817d45ce38cb083572c574fd08e30362efb624894d1e50d5cfbadc210`  
		Last Modified: Wed, 10 Apr 2024 06:54:39 GMT  
		Size: 15.0 MB (14974378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dd175cbfe93b618d8ba22bf1498ee78f8ef178b62b9887454e3eb2c00f50c5`  
		Last Modified: Wed, 10 Apr 2024 06:54:39 GMT  
		Size: 12.1 KB (12060 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:3de59a1810552ce15b00537e55ace34a7cc372de707c6d9f3408f8a9540629cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491529912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe0365b61c725f4967fecee7b926a413ff21cddec137a74990f6a9fe45da2a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea5901896ab9c5ad236e05b73d2065621d4488b4c7d2d61bef4316c3c981b2`  
		Last Modified: Tue, 12 Mar 2024 02:22:12 GMT  
		Size: 167.4 MB (167439330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a22ce7aa75fe6849bccde6452ebda329b039bb673f149b807a6ebab6fc9b53`  
		Last Modified: Wed, 10 Apr 2024 00:01:09 GMT  
		Size: 208.6 MB (208612532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a6f7c82952074d71cb715e34087f3175445219133056ad7fa9670144e666a90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14787749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cad5c1b513434efa6f47f58a6a8e3d1c9bf7578c2cd30f23a787f1a7372b6ab`

```dockerfile
```

-	Layers:
	-	`sha256:6ed4c8aef46f131be746be5a89a077d8b28609cf00ec902b4c0911d45dabce8a`  
		Last Modified: Wed, 10 Apr 2024 00:01:04 GMT  
		Size: 14.8 MB (14776282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f065e754ae91ecf02a567b53fcf1e21d6124125220ed2dae885905e3528890`  
		Last Modified: Wed, 10 Apr 2024 00:01:04 GMT  
		Size: 11.5 KB (11467 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b587651647adb295cf6b122fee23e56562b5e997577aa327d6c1a0c6b649a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.7 MB (555689462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b4c2f9368002c1420b0be85d03984989f0a4e818a3fc18bf499eef1874d3a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d317b4db41e297cffa1559c871d84437b3544f7a4c04d6cf339cd4e8caa94c76`  
		Last Modified: Tue, 12 Mar 2024 01:36:09 GMT  
		Size: 189.9 MB (189914923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5418f8e13c8934d51e047556794e458fa5836df81997654a00e4fdc1073cb9`  
		Last Modified: Mon, 01 Apr 2024 21:56:51 GMT  
		Size: 241.6 MB (241608936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:007752e704a42ff34a74a4aedfffb805a72715dfc71040dec17ecb1db8724292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14988142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5194969bd09bd7a480f3a14dad516153c0148c1fd9ddd62164ef0a2b1520236`

```dockerfile
```

-	Layers:
	-	`sha256:3bc0c024ad242e35e5fa0cda2ccc5332c386bdcfec0cd0cc024e62ecf9fc1dde`  
		Last Modified: Mon, 01 Apr 2024 21:56:47 GMT  
		Size: 15.0 MB (14976847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0c21cae6999254524af2572e00c085a82381d81910fd1c7336c002b7aac74b0`  
		Last Modified: Mon, 01 Apr 2024 21:56:46 GMT  
		Size: 11.3 KB (11295 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bullseye` - linux; 386

```console
$ docker pull rust@sha256:70fdeab84eff10abd352c3077ab7785ea921f5a019eb62f7106962b297969298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.2 MB (515173027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21e4bc28fb83f646ce347daa1059a5210007b3827a3baba597b7fd9465fe0a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
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
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125c557bd27681f5387605727a1b0d44605793da722ea6f8f66b86df9aa54384`  
		Last Modified: Wed, 10 Apr 2024 08:07:12 GMT  
		Size: 16.3 MB (16267921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13acd7d81d47808020936c58e9842c82c55c0205f369482de2b263fe21ed2dc6`  
		Last Modified: Wed, 10 Apr 2024 08:07:31 GMT  
		Size: 55.9 MB (55927749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed69373b65ed4263cd1d2ead3d6570264c8de6a744aa10974a8266c660515080`  
		Last Modified: Wed, 10 Apr 2024 08:08:16 GMT  
		Size: 199.9 MB (199890546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d5ec320ca15085353a9eac55306245a69c0c57ccc50a4011aaf6b70f87d3fb`  
		Last Modified: Wed, 10 Apr 2024 08:56:06 GMT  
		Size: 187.0 MB (187020623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:da43ec4a6be596a9a8ba8f2a6525924a2d26a9746e952339419dfa4065acdfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14975234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b4c78b31760218804790ec5ab591b04cf5d17e30e59b123209347d31c7656c`

```dockerfile
```

-	Layers:
	-	`sha256:e4039901b8fae7bbf1b656a6fbde410c408cd57f6ebe8e20e6e4c7405072ebf9`  
		Last Modified: Wed, 10 Apr 2024 08:56:02 GMT  
		Size: 15.0 MB (14963203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a066ce0f742bb5333d2b61590453bee5a925a2cf0ec058477f3821674fa65d9f`  
		Last Modified: Wed, 10 Apr 2024 08:56:01 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:8471b7c3efb93f5afbc21d7828fcda9fa0a2f7ebb6e55d659116235afda4a71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.4 MB (519415387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036cc170d8e81e97f632eeac3fb7aac0018dcec3088b88dc70bb60a972d57e23`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:37 GMT
ADD file:378e777c8961453a2c8c9a594105395e4a83f5e94a90756bc3eebe9ec18be242 in / 
# Tue, 12 Mar 2024 00:30:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:99575d2dfd5e66cfbe10e815aa8a7bfacb8fa923bf112abd5b9334bec5404161`  
		Last Modified: Tue, 12 Mar 2024 00:38:29 GMT  
		Size: 59.0 MB (58954475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce422567beb05db7b6d7eca359e7168a80a58b1c86d36287c6b86c9b76d845f`  
		Last Modified: Tue, 12 Mar 2024 02:21:17 GMT  
		Size: 16.8 MB (16765930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777aef5bbe7e540f91bd63fda95e7f25c0ba803d2a25a532b2f2306c6b2209d1`  
		Last Modified: Tue, 12 Mar 2024 02:21:36 GMT  
		Size: 58.9 MB (58873337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078e6b4fd896687174cc2013bea6ca7f49c8cd898255e8d37361b8486cb7fe25`  
		Last Modified: Tue, 12 Mar 2024 02:22:13 GMT  
		Size: 196.3 MB (196346975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd567a7f48ce9a547d2ed2aa59d0f4a817bad8643bb24efef2b49c60c022be25`  
		Last Modified: Mon, 01 Apr 2024 21:51:32 GMT  
		Size: 188.5 MB (188474670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5ecefd461ba9b7e9614c363b8ad717c5ed64dfa2ec4fe2d9e3c00aa2e07040cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14953306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69996fb9f6e80b9872d4c166ef6f9326fda8fb0a575c72930785b8692ecbce6`

```dockerfile
```

-	Layers:
	-	`sha256:37077dfb3fce4f1b82732e80df6e8ddd95bf19b0066dec1e8528f0aeaffaf6ab`  
		Last Modified: Mon, 01 Apr 2024 21:51:27 GMT  
		Size: 14.9 MB (14941983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5226f9f7a86e57b8c4914f44b244312869dedf73844351bad06b560a960266`  
		Last Modified: Mon, 01 Apr 2024 21:51:26 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-buster`

```console
$ docker pull rust@sha256:d94731e2a342d1736d23262c936821bfdf330198d757f430f3682c5844ff28c7
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
$ docker pull rust@sha256:ef4bd23ba9eb1fc17a271848ef3a8e11b0574868db455d2fafd61ae56263bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484813822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ef59296b3f783361ff9ecee292d7a3d701c9bf15748e18b947411a563b96f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
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
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e204ce2733ed28c5c2c45652e3fd6034257b2cc15670e98293092efdc65833ec`  
		Last Modified: Wed, 10 Apr 2024 06:55:04 GMT  
		Size: 172.9 MB (172884650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-buster` - unknown; unknown

```console
$ docker pull rust@sha256:a6286a89012d075f07d624270d53f0d0df8283771aac7a270eccd1a6ec720625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15621770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a2473f9ccc6c27bb501328c69f43eecbab161d7b4277a52933e462188df7bd`

```dockerfile
```

-	Layers:
	-	`sha256:f3998dec0353df1cec4c007c431ec1d097346b66751099e7cf175df0b6c0295d`  
		Last Modified: Wed, 10 Apr 2024 06:54:59 GMT  
		Size: 15.6 MB (15610116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2cdaeebcd398b7ffe5440b98f95202e4edd572ffd0d45344c138efe49be44ea`  
		Last Modified: Wed, 10 Apr 2024 06:54:58 GMT  
		Size: 11.7 KB (11654 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:f1163e13d71ffaf291be8d0e17de87300460c80bf6e44386811a5758d0764ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486340982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e374110670e91904baaab7f3ed7c6af22e757c9be10ee7b8f0a1b8e7dad38f0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec28d557d3104596d3ba5ab227e1e527ff8f93195f04af289dd5da1316ba29d9`  
		Last Modified: Tue, 12 Mar 2024 02:22:40 GMT  
		Size: 47.4 MB (47410735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb141b0531169976182ab39baba3c902bed903a2c25a2e2045f8c6cee114563c`  
		Last Modified: Tue, 12 Mar 2024 02:23:15 GMT  
		Size: 168.1 MB (168133921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8549a616e2a73c5409031ef4981fbf9ab21f8257e0492c65eb6095983f33d03`  
		Last Modified: Tue, 09 Apr 2024 23:56:04 GMT  
		Size: 208.6 MB (208612535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-buster` - unknown; unknown

```console
$ docker pull rust@sha256:65db45a78896d6997258088e0b5eac261a72871c29b3e2c53573b6ddd3fd5a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15423150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f7d3f85b9b79a109f763b2cdf82264b39bfa5029392bce77d3b858944387ba`

```dockerfile
```

-	Layers:
	-	`sha256:890e6de1a22bd1f71a395a5fdfc679a17725d6211ca1d73c0b403dca5e7f8f74`  
		Last Modified: Tue, 09 Apr 2024 23:56:00 GMT  
		Size: 15.4 MB (15412089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11079f1a552e59ef9774e79760fa4335bc5355ee2e30d84dc524fc26dccd032`  
		Last Modified: Tue, 09 Apr 2024 23:55:59 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d83db167f8b57f6fb23e0c1c978e0f0c249ee6e7a779481af62e0636bd6f40fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544097043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee814bf692b8e7c55b8e070bfa7c0b55a2f01a111874ad8000976ac91f9a8f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:28:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8987ebef52bd1e6f6f20b38f5dd0fa9030c75a5089144eabf4a20c7b2aa2605a`  
		Last Modified: Tue, 12 Mar 2024 01:36:57 GMT  
		Size: 52.2 MB (52225028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe09b4296b95b0c32948c55d4f978937b58f5a899208693bb4c304804492322`  
		Last Modified: Tue, 12 Mar 2024 01:37:27 GMT  
		Size: 183.5 MB (183517797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940961b85fdf2974f8776ada55477feb2f6cdfb8eef0be7a114dae57302f215c`  
		Last Modified: Mon, 01 Apr 2024 21:53:42 GMT  
		Size: 241.6 MB (241608909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-buster` - unknown; unknown

```console
$ docker pull rust@sha256:9380a50320d9bc998ae47a89e3d31fb990551367caeec9082029bf8639626916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15611676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcf6bea59be5926ea708c5ba672bc55be4ba6c82d2bf3951bae5db90bf8ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:673395325db4802c1fbda7722d59f6aca46826e9b8fdc64601eccc7e3502bbde`  
		Last Modified: Mon, 01 Apr 2024 21:53:37 GMT  
		Size: 15.6 MB (15600784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfee4d187200bc6ff2e874003b62ae48b59ee70de18013d5d21be69e442bc4d`  
		Last Modified: Mon, 01 Apr 2024 21:53:36 GMT  
		Size: 10.9 KB (10892 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-buster` - linux; 386

```console
$ docker pull rust@sha256:49629f3d3a1b7cf41847d495f69754d266c3257db8d6c3a401be76e1e8f95e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.4 MB (508366490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8787cf9ea38af799d2c5aa0fc246337f220a2f67ce427d69e6a665f843959019`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
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
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f83de192d57649c06466addcbc7b9ccd636e9d291c22fdf5d7e4a4e6c59450d`  
		Last Modified: Wed, 10 Apr 2024 08:08:28 GMT  
		Size: 18.1 MB (18099188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bc8c20df52365967a4f48f20656372016f14141f60753323f354ed4eca05f0`  
		Last Modified: Wed, 10 Apr 2024 08:08:48 GMT  
		Size: 53.5 MB (53492155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042163e6e1fe3d8805f02202161cd324efea6901ddca3f722950dc6c835431b`  
		Last Modified: Wed, 10 Apr 2024 08:09:32 GMT  
		Size: 198.5 MB (198498026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d1a8f7ee151de43e2a5e7467f74e9aff1e8f94198bfb82e1b9256a16ed5cb6`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-buster` - unknown; unknown

```console
$ docker pull rust@sha256:7e6b07cf29947420afc7f3cb9d9b96eafc3cc70e75561c2725b2a8e9b239468a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15627322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2443bc59c40da04634089b702f9ea6ecd8914eeb638af3c06dde5563fc2dcc5f`

```dockerfile
```

-	Layers:
	-	`sha256:4632792f756ad995e692769d516cb8302193e42f60b7ab907b6273b06e339ab4`  
		Last Modified: Wed, 10 Apr 2024 08:56:03 GMT  
		Size: 15.6 MB (15615697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82575d53ebbbb2229ba5140118990013e95bf8e9198c294a5eb759e798c44bb5`  
		Last Modified: Wed, 10 Apr 2024 08:56:03 GMT  
		Size: 11.6 KB (11625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-slim`

```console
$ docker pull rust@sha256:78b5459dc7218e633da119c82b215d54e5029fe3cb7e0e9bd7ca19ffacda77ca
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
$ docker pull rust@sha256:ed00d3908ba2ade42982456c2f9b8b6db5fecf14e9d1d2f58a1dedbb6a7c924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272802753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e1b814adbb0a324618baf1524efbae1616c5450ef892429d2e0c5f3ddc188c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868daa4b67ac105f565dd9a057f7f4f10cc38f9816536d9e7a6bbd620b8ca37d`  
		Last Modified: Wed, 10 Apr 2024 02:56:18 GMT  
		Size: 243.7 MB (243671395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a5d7d5b8dc2e5968bffc0faf477c8fbc4077fbe3ca1631972e06d45cf80a35f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21623c7d2b56a2d1b34a660d9884654aa92743361e69b4f3c1f2e14d1be20598`

```dockerfile
```

-	Layers:
	-	`sha256:db88d5519f271b7d1221885138eb2cb745ff3908ba759b8646ac90e06f7f2527`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 3.9 MB (3919062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe0382e87e578e32ad71f989f31936ddc388b9faf74f0e736098ac3ba5c190c`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 12.8 KB (12814 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:8fae5654772edd365dfd01f53835efcd50c85e9a9124c88476d6cfd02b8987e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281125976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd3d4379b89c0b08406e6611007fc87b392af0616e7c7a78525dd7fef8954b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbdfe2d8afc590898b008ae5ac867b9c9ecaba2e23c4ce8242c8ff24dfcb4e`  
		Last Modified: Mon, 01 Apr 2024 22:05:59 GMT  
		Size: 256.4 MB (256409251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim` - unknown; unknown

```console
$ docker pull rust@sha256:57d8f50dd1c6b235d090f83fe48ae776dc009ae8e9446e0e98f71bc218118ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27fb31bede8afd182c86d6517398034aafef2892fe5a8533744f9a46d0427f8`

```dockerfile
```

-	Layers:
	-	`sha256:ae00f303130b0e32159908141b05a139cc824b82a42f44b70812b88a36ea65a4`  
		Last Modified: Mon, 01 Apr 2024 22:05:54 GMT  
		Size: 3.7 MB (3737518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de84682983e233db29c48bc5d1ad2738cbfbd5eb650bbe9fb47772d589981b85`  
		Last Modified: Mon, 01 Apr 2024 22:05:53 GMT  
		Size: 12.6 KB (12637 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6af0432b6d1b9274fbda00f1e31e2d3465171e66d32318c729d03bd3c51618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336617112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355ad31b2818638e6828730de81e62b4574f851cd03d587008dd227b5e75e1a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8aac4a9ac99feb14bacf4109c65ccefc4efa32032e32522c7fc72370be73c9`  
		Last Modified: Mon, 01 Apr 2024 22:01:33 GMT  
		Size: 307.5 MB (307460678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b269d7552b7b1b75d79080032ac62815904b266c69efe60dcaaf88ebe8194195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3fd44111ce2bb4129bc96af803aad106c6fd6cb819c617ad5392dfbf9b8f6b`

```dockerfile
```

-	Layers:
	-	`sha256:b13e178634ac422c29c30639e4a5404d22c1636919f1268cd8af918a15f25ff1`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 3.9 MB (3942630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29301f3480b2dcd0cc128b64522f960bcc98ecf37d6db7a527cbd65d59f31c34`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 12.6 KB (12553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim` - linux; 386

```console
$ docker pull rust@sha256:9a072848e2d833cf694b18aefa244a460553f7cf6c85b58f5e2e52286efd174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284750516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca43af6be05127a03ec4d1b7aca13a5833998f17cdb5af3206b6d55dd1991a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f760cffd225a2b32fbf671ab6251bed8d1a36d87cac79c98316872c7a69f93`  
		Last Modified: Wed, 10 Apr 2024 02:03:51 GMT  
		Size: 254.6 MB (254604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d144c1d027fa1f9b95ce873a14624a8040451e3f0e7bc3bf786fae4efc033a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98508d35fb64f25d374e4da636cff8ae441ac72ffc1e3d86d7dad746952d5109`

```dockerfile
```

-	Layers:
	-	`sha256:6af998bc21467f538e8f16857cbd4b31d5b202bdca8935602e1f72ce7eca98f5`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 3.9 MB (3900761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbc0607021120ea5a7abb310a8f1eb23efa63e81dad3298c28eb61e7e63eb70`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e8f8ec53a391d9113d8080ba20f31c338c4cf6cbe6aae3d3f04a972868df31a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290361922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e298b7e70665b3442d85e1806ad164a55a9f7b0a16463dad74a0bf044226f5fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4418400b66496376009e657c8080f4ea2dbbaaf1bccc166de6aac1b72a8e971`  
		Last Modified: Mon, 01 Apr 2024 21:58:19 GMT  
		Size: 257.2 MB (257242899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim` - unknown; unknown

```console
$ docker pull rust@sha256:da4ab5fbedd89882e94c6ff8acef6cc756b9b3d25f9d18c7ce53f61a46f74af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3905390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85edd0d98bb412cff6a24ffa03005353fc736121e05de765d98422afe663e20`

```dockerfile
```

-	Layers:
	-	`sha256:6feae90e068af601f73655101ccf01c3d659370b865a4b719e3b7fccf8b87d68`  
		Last Modified: Mon, 01 Apr 2024 21:58:13 GMT  
		Size: 3.9 MB (3892794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fc000faf56d83a6990e8558b09b2c09cb026e52b4ec329e598045f9fad096c`  
		Last Modified: Mon, 01 Apr 2024 21:58:12 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-slim-bookworm`

```console
$ docker pull rust@sha256:78b5459dc7218e633da119c82b215d54e5029fe3cb7e0e9bd7ca19ffacda77ca
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
$ docker pull rust@sha256:ed00d3908ba2ade42982456c2f9b8b6db5fecf14e9d1d2f58a1dedbb6a7c924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272802753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e1b814adbb0a324618baf1524efbae1616c5450ef892429d2e0c5f3ddc188c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868daa4b67ac105f565dd9a057f7f4f10cc38f9816536d9e7a6bbd620b8ca37d`  
		Last Modified: Wed, 10 Apr 2024 02:56:18 GMT  
		Size: 243.7 MB (243671395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a5d7d5b8dc2e5968bffc0faf477c8fbc4077fbe3ca1631972e06d45cf80a35f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21623c7d2b56a2d1b34a660d9884654aa92743361e69b4f3c1f2e14d1be20598`

```dockerfile
```

-	Layers:
	-	`sha256:db88d5519f271b7d1221885138eb2cb745ff3908ba759b8646ac90e06f7f2527`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 3.9 MB (3919062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe0382e87e578e32ad71f989f31936ddc388b9faf74f0e736098ac3ba5c190c`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 12.8 KB (12814 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:8fae5654772edd365dfd01f53835efcd50c85e9a9124c88476d6cfd02b8987e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281125976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd3d4379b89c0b08406e6611007fc87b392af0616e7c7a78525dd7fef8954b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbdfe2d8afc590898b008ae5ac867b9c9ecaba2e23c4ce8242c8ff24dfcb4e`  
		Last Modified: Mon, 01 Apr 2024 22:05:59 GMT  
		Size: 256.4 MB (256409251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:57d8f50dd1c6b235d090f83fe48ae776dc009ae8e9446e0e98f71bc218118ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27fb31bede8afd182c86d6517398034aafef2892fe5a8533744f9a46d0427f8`

```dockerfile
```

-	Layers:
	-	`sha256:ae00f303130b0e32159908141b05a139cc824b82a42f44b70812b88a36ea65a4`  
		Last Modified: Mon, 01 Apr 2024 22:05:54 GMT  
		Size: 3.7 MB (3737518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de84682983e233db29c48bc5d1ad2738cbfbd5eb650bbe9fb47772d589981b85`  
		Last Modified: Mon, 01 Apr 2024 22:05:53 GMT  
		Size: 12.6 KB (12637 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6af0432b6d1b9274fbda00f1e31e2d3465171e66d32318c729d03bd3c51618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336617112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355ad31b2818638e6828730de81e62b4574f851cd03d587008dd227b5e75e1a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8aac4a9ac99feb14bacf4109c65ccefc4efa32032e32522c7fc72370be73c9`  
		Last Modified: Mon, 01 Apr 2024 22:01:33 GMT  
		Size: 307.5 MB (307460678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b269d7552b7b1b75d79080032ac62815904b266c69efe60dcaaf88ebe8194195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3fd44111ce2bb4129bc96af803aad106c6fd6cb819c617ad5392dfbf9b8f6b`

```dockerfile
```

-	Layers:
	-	`sha256:b13e178634ac422c29c30639e4a5404d22c1636919f1268cd8af918a15f25ff1`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 3.9 MB (3942630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29301f3480b2dcd0cc128b64522f960bcc98ecf37d6db7a527cbd65d59f31c34`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 12.6 KB (12553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:9a072848e2d833cf694b18aefa244a460553f7cf6c85b58f5e2e52286efd174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284750516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca43af6be05127a03ec4d1b7aca13a5833998f17cdb5af3206b6d55dd1991a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f760cffd225a2b32fbf671ab6251bed8d1a36d87cac79c98316872c7a69f93`  
		Last Modified: Wed, 10 Apr 2024 02:03:51 GMT  
		Size: 254.6 MB (254604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d144c1d027fa1f9b95ce873a14624a8040451e3f0e7bc3bf786fae4efc033a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98508d35fb64f25d374e4da636cff8ae441ac72ffc1e3d86d7dad746952d5109`

```dockerfile
```

-	Layers:
	-	`sha256:6af998bc21467f538e8f16857cbd4b31d5b202bdca8935602e1f72ce7eca98f5`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 3.9 MB (3900761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbc0607021120ea5a7abb310a8f1eb23efa63e81dad3298c28eb61e7e63eb70`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e8f8ec53a391d9113d8080ba20f31c338c4cf6cbe6aae3d3f04a972868df31a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290361922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e298b7e70665b3442d85e1806ad164a55a9f7b0a16463dad74a0bf044226f5fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4418400b66496376009e657c8080f4ea2dbbaaf1bccc166de6aac1b72a8e971`  
		Last Modified: Mon, 01 Apr 2024 21:58:19 GMT  
		Size: 257.2 MB (257242899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:da4ab5fbedd89882e94c6ff8acef6cc756b9b3d25f9d18c7ce53f61a46f74af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3905390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85edd0d98bb412cff6a24ffa03005353fc736121e05de765d98422afe663e20`

```dockerfile
```

-	Layers:
	-	`sha256:6feae90e068af601f73655101ccf01c3d659370b865a4b719e3b7fccf8b87d68`  
		Last Modified: Mon, 01 Apr 2024 21:58:13 GMT  
		Size: 3.9 MB (3892794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fc000faf56d83a6990e8558b09b2c09cb026e52b4ec329e598045f9fad096c`  
		Last Modified: Mon, 01 Apr 2024 21:58:12 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-slim-bullseye`

```console
$ docker pull rust@sha256:81435e6e61bb826e17ff6e260461db26d579c96298ae22533028e2b03cfe1803
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
$ docker pull rust@sha256:e3703a692d6689cee0490363bfc8108a9c9e590df6988f2920eb71ab77937c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264463700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fc023abba24900ad681ae8421b1f2d1c477a0cdc7f8779c5147a5df2e64d1f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
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
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ab2f2a3ce344d856412bb76c0cbce30a35aeb53176eb5cec120e3c216f01a`  
		Last Modified: Wed, 10 Apr 2024 02:56:20 GMT  
		Size: 233.0 MB (233035962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:93f63b6fad174237aa1145d25dad1cc04f8aea997947828b38063021fe446db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78abe840ffae11375c7e3b134fad5ba0df3447f6e29e7245a2f7719df6a63b15`

```dockerfile
```

-	Layers:
	-	`sha256:6f58cc69594b21ac6cab79cbd7ffe7bb3572c3a95b2e9e4d2ab1e80b47bde438`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 4.1 MB (4139675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a713004d07c70ce533a189ac1c7759bf8978f36fa4e86386307445c2f7a4b4df`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 11.6 KB (11626 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:26d4f2c56522ea7ca8a330117e7f9494432528454e434b87d3918c83231e17ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277429232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc64990d1edbbaa7bcfb16939d5cae08f9cf6d2970c6dd863a2d09dcd8241e62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:38 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
# Tue, 12 Mar 2024 00:59:38 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c5b544693e63eaac90034284eef7243457a9a679d1e583cc55dafed1c8bf9`  
		Last Modified: Mon, 01 Apr 2024 22:01:28 GMT  
		Size: 250.8 MB (250846518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3d96ab8013fcb764254a3679f4dd5f4108b571415128e3ca7b3c8f8d493c203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4963c801a528cbe9ba8553e0af2c5993a827d1bf691b4357e00d091507420fdb`

```dockerfile
```

-	Layers:
	-	`sha256:b9c894fee7248dc0583cb4d373353376ca502b9f3d4aaf97f2fcedd57d580b5e`  
		Last Modified: Mon, 01 Apr 2024 22:01:23 GMT  
		Size: 3.9 MB (3949600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61a737341c5d2a8f46beb7e1cb2f2bcd72ccd316a605b269078c15eb13129c3`  
		Last Modified: Mon, 01 Apr 2024 22:01:22 GMT  
		Size: 11.4 KB (11417 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d70206b0586e8e64e875ea16ec912e8bd72d21906d2568856ce84d6689174290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327412046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5808e965af077392cd1baf609dcc56a41f121bd3eb9e5ae2fc6accac265d39f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3e8d71fd971f61b0388fb2834d9f24df7728ed3bbdc3a823b64ccf8ad2412`  
		Last Modified: Mon, 01 Apr 2024 21:58:19 GMT  
		Size: 297.3 MB (297340930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b42ec493301ad10133f471ed2fc7a794439d9b3951ba399efd8a158a0b0d4b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4147914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8005aa07b0305f1b50df5f923ef26f447e28d2ed655a4a5ba2f694a56a731c`

```dockerfile
```

-	Layers:
	-	`sha256:0a16db309db453f9938651346d32b0b8e35f96e842c13c0ffa1c396e7454325c`  
		Last Modified: Mon, 01 Apr 2024 21:58:13 GMT  
		Size: 4.1 MB (4136557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:416c38e8719f91a3859a3afb446eef65cbb8954ea7e58d945e61c4a799f15b9d`  
		Last Modified: Mon, 01 Apr 2024 21:58:12 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:e47eddf08aa277fd773b469789469b80214dc1c6eb89cc52dbaed2a45572b346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280210792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c34fb5b92c2203fcb8db1509344b4fad479143f90c59036e639d20e6cf231`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
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
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f761c683b352d393ff3a70a31f1cdb3309470baef708acaaec1d5f65178a780`  
		Last Modified: Wed, 10 Apr 2024 01:54:11 GMT  
		Size: 247.8 MB (247797376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d1306fc47b4244d7f9e7943f5aae84fd486ba130d8d39c608767cb956ddf3271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3908b559c177afd6719140b5a2a3541d95e0921cb245764b7a06f080971b6ac3`

```dockerfile
```

-	Layers:
	-	`sha256:a032ac7469111c4a51d7d1e1b0c75b35aa34e3c8b0d8d8e5bd42030f843b8926`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 4.1 MB (4131731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0b157250963b35b33549efb108518a419ccc9f570c228ba225ea203828b0aa6`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 11.6 KB (11597 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:c51654576d219a3c1810ec0f57d020a9a2fae17fa75a23f0d9d8b3744618660f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278761579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf13a40fa5213e2af5148bc8ba383c6887afb092fe4af03241476a167078cd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:31:08 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Tue, 12 Mar 2024 00:31:12 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37dc3072fd9cd9fa92e7d1b88a1a366b360bcbffaa4f190fc3ac03c4cd5a818`  
		Last Modified: Mon, 01 Apr 2024 21:53:46 GMT  
		Size: 243.5 MB (243463572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4c28805af771ded17532d58b5f8e663ecc6f2513a3d94048509e9f3606592e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713d1526554c91ba1f62906da53b3f136f6bd82097283d6f13d71589576ec883`

```dockerfile
```

-	Layers:
	-	`sha256:4bbad0dcb5d31db6ef4f6b52b195d24c5725f4de425b5776723a0c94a2a67df0`  
		Last Modified: Mon, 01 Apr 2024 21:53:36 GMT  
		Size: 4.1 MB (4100758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef88e86936a49014f33c8e5475ac58e3919976975996b989afde2c62f371ff8b`  
		Last Modified: Mon, 01 Apr 2024 21:53:35 GMT  
		Size: 11.4 KB (11385 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77-slim-buster`

```console
$ docker pull rust@sha256:bfa022f7f35ee14e7375de549deaddeaf1ae13bedd4ca845fb55c75fa48c37e0
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
$ docker pull rust@sha256:bef060961cbd2174621dbdc808519969112b6fbccb3e2c4c90b67c67ec186450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245495284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcb8545702f9a0e6721b40aaa469aefcb0622810562883d52ba50ba057c1c5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
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
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c72519ff7f40e33d03c7d3f47e19dcd8420c4c92434d03570faaff716312528`  
		Last Modified: Wed, 10 Apr 2024 02:56:19 GMT  
		Size: 218.3 MB (218304422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:8dcab7ab30592663a02fd73c824b93ceb27704fd316dfdc4a14a8fd53cadca34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858fb1eb2641158105afbe01ba8f4c231a8aae4ad85d82a1c25586aafbbc59da`

```dockerfile
```

-	Layers:
	-	`sha256:38f8d81ee6092d2bfbe77b6702062de3b7d23f5bde67d9773915331d261cb7c0`  
		Last Modified: Wed, 10 Apr 2024 02:56:16 GMT  
		Size: 3.6 MB (3585441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb65268fc77b08bd0a7fa791c3297b3bced6acd88a4bc12a1af05bcf384c5c8`  
		Last Modified: Wed, 10 Apr 2024 02:56:16 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:0c22e20adc4dc2f8053478d027b264ce618469bf08d54893fbf2377658558a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264285591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43db9b4246ad7f36b5cf421516f4d76ce05a39acf043747c47239008af2afb83`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:57 GMT
ADD file:87f5e14c74c217f7538860dd43d6b1910663955972cf5270e3d1a8254956878c in / 
# Tue, 12 Mar 2024 00:59:57 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f02c84b2c1c85cfdbae8bb78a52226f2b54d86f3eb2466ac3a81fc25ffde9eb`  
		Last Modified: Tue, 12 Mar 2024 01:05:07 GMT  
		Size: 22.8 MB (22795622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23601052881b5b7693660e13d60ad40a44fa6d28a6eab03e29bc335ef22614`  
		Last Modified: Mon, 01 Apr 2024 21:57:18 GMT  
		Size: 241.5 MB (241489969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:a259de885b15d5261cb5637679bd82b06cc553086bcc617ceabb1cbcd5911283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3403962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975b206faba1555d08aeb3b367f7e8ace57ef82f52c901953177d20e69f34da4`

```dockerfile
```

-	Layers:
	-	`sha256:a7ec9dae53125430f432e43fa64bb1b7617be4f96618022f8b1c9bd56d02e963`  
		Last Modified: Mon, 01 Apr 2024 21:57:13 GMT  
		Size: 3.4 MB (3392947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8fec98a1e9cbf26e1d3fbbe10104c9e731f2418317039f63184e7f4d36d2663`  
		Last Modified: Mon, 01 Apr 2024 21:57:13 GMT  
		Size: 11.0 KB (11015 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a5684abbc7f54bd9c58a5364b586316c5353fd8542509a6e13113239001c9fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307812606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5bde5f6654a3312b9f1f9f6ed51f121b8ad4edd013ae962ab6efcdef6ec0ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:05 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
# Tue, 12 Mar 2024 00:46:06 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f061dca4371eb34330ba3af7c2817b1504f610d9540f399dca1308b85fc26c6`  
		Last Modified: Mon, 01 Apr 2024 21:55:11 GMT  
		Size: 281.8 MB (281842017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:075ab39c9dbaadb406e6e27af9cc64e481f3ac8c6675922e221c65a580e52a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b111ed85dfdbef2cf909ba27fa12deebe2a85a1821a0c05d3c9a6f34856e0f`

```dockerfile
```

-	Layers:
	-	`sha256:413744a81638db98004c236d84b70a1ee323b42dd5316eb0c7b8109d75395654`  
		Last Modified: Mon, 01 Apr 2024 21:55:04 GMT  
		Size: 3.6 MB (3574589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c49bb1f862c0df67b88faca306222bd29aa102812117111de44057071d9b1bf2`  
		Last Modified: Mon, 01 Apr 2024 21:55:03 GMT  
		Size: 11.0 KB (10955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:f16cf382bb643b61546e0716b11c8865933e5ed812ac80169f0c1059d788a546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264864857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c822134f762bf9cdc5c0c15d0d06f50df5c808cbf81120d841f19ee30850f2c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6033d014a0c5c8d87a61d23e20506ec550ea93ef72866e76bfe5a468ceebf619 in / 
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
	-	`sha256:d349bc9800fc6053f91af64b3ce845b5191cc9e0ae2d2001951381ae2d08e46e`  
		Last Modified: Wed, 10 Apr 2024 01:03:40 GMT  
		Size: 27.8 MB (27848331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54caad959c94915ec006deffe9d9bd347eb55d50b70b7ac94922c1784fbdf03`  
		Last Modified: Wed, 10 Apr 2024 01:54:11 GMT  
		Size: 237.0 MB (237016526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:752c286f93a3ae53df42fe4c2153bcdb6523435d242f194aa2925996d9e0251f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c94b966dc0d5d95ee36fe5b571695e3b2992333e109cd314d4b496537982f2c`

```dockerfile
```

-	Layers:
	-	`sha256:f59e8592b975bb56e79e105cf29ff5ee1831a7336624007d7e81a302f3b159d6`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 3.6 MB (3592066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a39c68120f1cbcd3caaed0c37db595248763df96455ec3bccba15f6356f80efe`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 11.2 KB (11190 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2`

```console
$ docker pull rust@sha256:5fbf82e820eee97bf4d4b2db0146adf8318f072e4c3e36c1f4d95682fd8f5cfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.77.2` - linux; amd64

```console
$ docker pull rust@sha256:6361801bd55ffec96b953437f1083a8d730320b0809292d7d84425ff5f3223a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521770219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead19e243dc6f0b82077e2f7aca0a70a7e4fdd9300f6fa71b1557210b6bea496`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
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
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4251e2c0d85d5696b1917655ebc9009cc6d07741a7410385ecdbf440cc57e92`  
		Last Modified: Wed, 10 Apr 2024 06:54:51 GMT  
		Size: 172.9 MB (172884751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2` - unknown; unknown

```console
$ docker pull rust@sha256:7093785b7995fdc45f27f84b72d85b3425f8cedab6a4692fbb54cd3e8445fd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67072e65542c5c0a7f8c486648acf1470857af35bc22c9994006fe2869e992a`

```dockerfile
```

-	Layers:
	-	`sha256:f58c77986737873a4dd6d0f618ef90591136108b4a126550ab2cbd66d2d01cf5`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 15.4 MB (15370122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3172b133a2a58f28fdc38c6e63776bd4bffb56d2e180b31f207e9f19f4cb2197`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 13.2 KB (13222 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff8d4f50070f7fa5a52f2fcef4f8b51569023de2dde184cb2bf593d596f61547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510035646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb59b3cd57ab4f766666a6c3155019552626eaa52de6881231146e013d09d64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1200500c52f4429e643f87908b44e016ca7b67ac17bcdba07b3884ef8b98fed1`  
		Last Modified: Wed, 10 Apr 2024 00:05:32 GMT  
		Size: 208.6 MB (208612381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2` - unknown; unknown

```console
$ docker pull rust@sha256:b340eca81e3952b867d6121dd010fe5baf4dcf8782a035ef666803baf5a81d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4326b7d2aa5919c3772d38b9ffa6002f9a6b013c3447f507d0800b6c11d178a`

```dockerfile
```

-	Layers:
	-	`sha256:482cba46f5b18fa1452b104ca0bd84ab211676d10a643e56287b9b7477af6258`  
		Last Modified: Wed, 10 Apr 2024 00:05:27 GMT  
		Size: 15.2 MB (15185946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39172abfd0ca99841b69d6dd1903d428f3dfa92415f750b1584c92eae12a7b28`  
		Last Modified: Wed, 10 Apr 2024 00:05:26 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2` - linux; 386

```console
$ docker pull rust@sha256:a9bb8779de7f84f61b1b534d63ccab47a51f2b9d023747bc4c929b62dbaff1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.5 MB (538538471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b4b887cb142c95f41d1e6044283f57eae3ce754415c7597d11b8239226928`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
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
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d7a956f97c876348400069f4c082762ec5601b2d1fc8e0d06ad7470953b90`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2` - unknown; unknown

```console
$ docker pull rust@sha256:5e6d6cfa16c6880acd95cd6d1dfeddc01c9a35d292e9d41f7b1b0f965b17580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c2d02a2c3867ebfb256a9d73c98459ab97dabe4b35c11449b6217648ec2d06`

```dockerfile
```

-	Layers:
	-	`sha256:aab93fcb88ff947e4c0fd611f8cfae85a8c0b10ab803bf8d28cfd1ef568eb018`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 15.3 MB (15349163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e601202e79167711bc3330cb281453c48804c39665dd226b584b1e5bb462e0e4`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 13.2 KB (13173 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-alpine`

```console
$ docker pull rust@sha256:b6ea81b37c9ad8b2c875f64a963b5e418e86d33d41eed529671e86e86d30c884
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
$ docker pull rust@sha256:4c640cb99e88d7e7873a25e5dc693999cd4c5a0f486b54362513f80107920ac3
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
$ docker pull rust@sha256:b6ea81b37c9ad8b2c875f64a963b5e418e86d33d41eed529671e86e86d30c884
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
$ docker pull rust@sha256:5fbf82e820eee97bf4d4b2db0146adf8318f072e4c3e36c1f4d95682fd8f5cfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.77.2-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:6361801bd55ffec96b953437f1083a8d730320b0809292d7d84425ff5f3223a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521770219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead19e243dc6f0b82077e2f7aca0a70a7e4fdd9300f6fa71b1557210b6bea496`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
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
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4251e2c0d85d5696b1917655ebc9009cc6d07741a7410385ecdbf440cc57e92`  
		Last Modified: Wed, 10 Apr 2024 06:54:51 GMT  
		Size: 172.9 MB (172884751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7093785b7995fdc45f27f84b72d85b3425f8cedab6a4692fbb54cd3e8445fd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67072e65542c5c0a7f8c486648acf1470857af35bc22c9994006fe2869e992a`

```dockerfile
```

-	Layers:
	-	`sha256:f58c77986737873a4dd6d0f618ef90591136108b4a126550ab2cbd66d2d01cf5`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 15.4 MB (15370122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3172b133a2a58f28fdc38c6e63776bd4bffb56d2e180b31f207e9f19f4cb2197`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 13.2 KB (13222 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff8d4f50070f7fa5a52f2fcef4f8b51569023de2dde184cb2bf593d596f61547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510035646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb59b3cd57ab4f766666a6c3155019552626eaa52de6881231146e013d09d64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1200500c52f4429e643f87908b44e016ca7b67ac17bcdba07b3884ef8b98fed1`  
		Last Modified: Wed, 10 Apr 2024 00:05:32 GMT  
		Size: 208.6 MB (208612381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b340eca81e3952b867d6121dd010fe5baf4dcf8782a035ef666803baf5a81d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4326b7d2aa5919c3772d38b9ffa6002f9a6b013c3447f507d0800b6c11d178a`

```dockerfile
```

-	Layers:
	-	`sha256:482cba46f5b18fa1452b104ca0bd84ab211676d10a643e56287b9b7477af6258`  
		Last Modified: Wed, 10 Apr 2024 00:05:27 GMT  
		Size: 15.2 MB (15185946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39172abfd0ca99841b69d6dd1903d428f3dfa92415f750b1584c92eae12a7b28`  
		Last Modified: Wed, 10 Apr 2024 00:05:26 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bookworm` - linux; 386

```console
$ docker pull rust@sha256:a9bb8779de7f84f61b1b534d63ccab47a51f2b9d023747bc4c929b62dbaff1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.5 MB (538538471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b4b887cb142c95f41d1e6044283f57eae3ce754415c7597d11b8239226928`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
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
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d7a956f97c876348400069f4c082762ec5601b2d1fc8e0d06ad7470953b90`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5e6d6cfa16c6880acd95cd6d1dfeddc01c9a35d292e9d41f7b1b0f965b17580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c2d02a2c3867ebfb256a9d73c98459ab97dabe4b35c11449b6217648ec2d06`

```dockerfile
```

-	Layers:
	-	`sha256:aab93fcb88ff947e4c0fd611f8cfae85a8c0b10ab803bf8d28cfd1ef568eb018`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 15.3 MB (15349163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e601202e79167711bc3330cb281453c48804c39665dd226b584b1e5bb462e0e4`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 13.2 KB (13173 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-bullseye`

```console
$ docker pull rust@sha256:aee2ab3906997dbff37197f6616e27b7ead887e92a2d263f2c7a0904deec9581
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.77.2-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:b7dd0a9e0432309ac0ee6bd4058bb75bfeaba8ef8b6d4f946305e9d5ba1048ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 MB (495312885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dc2e90e12adfb05ffe7f3565324bb7b40682bfa9adae698e9870e62ec25ffa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
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
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff24b88ad3798f817849ad391d809ece121dc9b7f82f24bb68eed84561f048`  
		Last Modified: Wed, 10 Apr 2024 05:36:15 GMT  
		Size: 54.6 MB (54588743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f58f24df78e3aabf785017c3197c2a09fd606e7f19a830a1cfde41f681f39e`  
		Last Modified: Wed, 10 Apr 2024 05:36:46 GMT  
		Size: 197.0 MB (196985611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d396a8eca7ee95fff3e5c8b8a21c1df92ec18991eb40d3ca28fea8b5ed20f266`  
		Last Modified: Wed, 10 Apr 2024 06:54:44 GMT  
		Size: 172.9 MB (172884749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1bea0538e2b9f31e9afbd4c8d10b764514307976b5fcddef1f4a4d646cfafdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14986438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a02fe4ad97e458747fa44d8103d1a8f72d2661d05888460c243a2897a2a2e9`

```dockerfile
```

-	Layers:
	-	`sha256:871bcdf817d45ce38cb083572c574fd08e30362efb624894d1e50d5cfbadc210`  
		Last Modified: Wed, 10 Apr 2024 06:54:39 GMT  
		Size: 15.0 MB (14974378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dd175cbfe93b618d8ba22bf1498ee78f8ef178b62b9887454e3eb2c00f50c5`  
		Last Modified: Wed, 10 Apr 2024 06:54:39 GMT  
		Size: 12.1 KB (12060 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:3de59a1810552ce15b00537e55ace34a7cc372de707c6d9f3408f8a9540629cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491529912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe0365b61c725f4967fecee7b926a413ff21cddec137a74990f6a9fe45da2a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea5901896ab9c5ad236e05b73d2065621d4488b4c7d2d61bef4316c3c981b2`  
		Last Modified: Tue, 12 Mar 2024 02:22:12 GMT  
		Size: 167.4 MB (167439330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a22ce7aa75fe6849bccde6452ebda329b039bb673f149b807a6ebab6fc9b53`  
		Last Modified: Wed, 10 Apr 2024 00:01:09 GMT  
		Size: 208.6 MB (208612532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a6f7c82952074d71cb715e34087f3175445219133056ad7fa9670144e666a90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14787749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cad5c1b513434efa6f47f58a6a8e3d1c9bf7578c2cd30f23a787f1a7372b6ab`

```dockerfile
```

-	Layers:
	-	`sha256:6ed4c8aef46f131be746be5a89a077d8b28609cf00ec902b4c0911d45dabce8a`  
		Last Modified: Wed, 10 Apr 2024 00:01:04 GMT  
		Size: 14.8 MB (14776282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f065e754ae91ecf02a567b53fcf1e21d6124125220ed2dae885905e3528890`  
		Last Modified: Wed, 10 Apr 2024 00:01:04 GMT  
		Size: 11.5 KB (11467 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-bullseye` - linux; 386

```console
$ docker pull rust@sha256:70fdeab84eff10abd352c3077ab7785ea921f5a019eb62f7106962b297969298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.2 MB (515173027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21e4bc28fb83f646ce347daa1059a5210007b3827a3baba597b7fd9465fe0a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
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
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125c557bd27681f5387605727a1b0d44605793da722ea6f8f66b86df9aa54384`  
		Last Modified: Wed, 10 Apr 2024 08:07:12 GMT  
		Size: 16.3 MB (16267921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13acd7d81d47808020936c58e9842c82c55c0205f369482de2b263fe21ed2dc6`  
		Last Modified: Wed, 10 Apr 2024 08:07:31 GMT  
		Size: 55.9 MB (55927749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed69373b65ed4263cd1d2ead3d6570264c8de6a744aa10974a8266c660515080`  
		Last Modified: Wed, 10 Apr 2024 08:08:16 GMT  
		Size: 199.9 MB (199890546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d5ec320ca15085353a9eac55306245a69c0c57ccc50a4011aaf6b70f87d3fb`  
		Last Modified: Wed, 10 Apr 2024 08:56:06 GMT  
		Size: 187.0 MB (187020623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:da43ec4a6be596a9a8ba8f2a6525924a2d26a9746e952339419dfa4065acdfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14975234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b4c78b31760218804790ec5ab591b04cf5d17e30e59b123209347d31c7656c`

```dockerfile
```

-	Layers:
	-	`sha256:e4039901b8fae7bbf1b656a6fbde410c408cd57f6ebe8e20e6e4c7405072ebf9`  
		Last Modified: Wed, 10 Apr 2024 08:56:02 GMT  
		Size: 15.0 MB (14963203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a066ce0f742bb5333d2b61590453bee5a925a2cf0ec058477f3821674fa65d9f`  
		Last Modified: Wed, 10 Apr 2024 08:56:01 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-buster`

```console
$ docker pull rust@sha256:8e108e99b2c0a10f5df2676ba82dfdfdc9bd3693ea53d71361dcc22dffe328cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.77.2-buster` - linux; amd64

```console
$ docker pull rust@sha256:ef4bd23ba9eb1fc17a271848ef3a8e11b0574868db455d2fafd61ae56263bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484813822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ef59296b3f783361ff9ecee292d7a3d701c9bf15748e18b947411a563b96f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
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
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e204ce2733ed28c5c2c45652e3fd6034257b2cc15670e98293092efdc65833ec`  
		Last Modified: Wed, 10 Apr 2024 06:55:04 GMT  
		Size: 172.9 MB (172884650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-buster` - unknown; unknown

```console
$ docker pull rust@sha256:a6286a89012d075f07d624270d53f0d0df8283771aac7a270eccd1a6ec720625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15621770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a2473f9ccc6c27bb501328c69f43eecbab161d7b4277a52933e462188df7bd`

```dockerfile
```

-	Layers:
	-	`sha256:f3998dec0353df1cec4c007c431ec1d097346b66751099e7cf175df0b6c0295d`  
		Last Modified: Wed, 10 Apr 2024 06:54:59 GMT  
		Size: 15.6 MB (15610116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2cdaeebcd398b7ffe5440b98f95202e4edd572ffd0d45344c138efe49be44ea`  
		Last Modified: Wed, 10 Apr 2024 06:54:58 GMT  
		Size: 11.7 KB (11654 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:f1163e13d71ffaf291be8d0e17de87300460c80bf6e44386811a5758d0764ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486340982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e374110670e91904baaab7f3ed7c6af22e757c9be10ee7b8f0a1b8e7dad38f0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec28d557d3104596d3ba5ab227e1e527ff8f93195f04af289dd5da1316ba29d9`  
		Last Modified: Tue, 12 Mar 2024 02:22:40 GMT  
		Size: 47.4 MB (47410735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb141b0531169976182ab39baba3c902bed903a2c25a2e2045f8c6cee114563c`  
		Last Modified: Tue, 12 Mar 2024 02:23:15 GMT  
		Size: 168.1 MB (168133921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8549a616e2a73c5409031ef4981fbf9ab21f8257e0492c65eb6095983f33d03`  
		Last Modified: Tue, 09 Apr 2024 23:56:04 GMT  
		Size: 208.6 MB (208612535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-buster` - unknown; unknown

```console
$ docker pull rust@sha256:65db45a78896d6997258088e0b5eac261a72871c29b3e2c53573b6ddd3fd5a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15423150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f7d3f85b9b79a109f763b2cdf82264b39bfa5029392bce77d3b858944387ba`

```dockerfile
```

-	Layers:
	-	`sha256:890e6de1a22bd1f71a395a5fdfc679a17725d6211ca1d73c0b403dca5e7f8f74`  
		Last Modified: Tue, 09 Apr 2024 23:56:00 GMT  
		Size: 15.4 MB (15412089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11079f1a552e59ef9774e79760fa4335bc5355ee2e30d84dc524fc26dccd032`  
		Last Modified: Tue, 09 Apr 2024 23:55:59 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-buster` - linux; 386

```console
$ docker pull rust@sha256:49629f3d3a1b7cf41847d495f69754d266c3257db8d6c3a401be76e1e8f95e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.4 MB (508366490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8787cf9ea38af799d2c5aa0fc246337f220a2f67ce427d69e6a665f843959019`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
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
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f83de192d57649c06466addcbc7b9ccd636e9d291c22fdf5d7e4a4e6c59450d`  
		Last Modified: Wed, 10 Apr 2024 08:08:28 GMT  
		Size: 18.1 MB (18099188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bc8c20df52365967a4f48f20656372016f14141f60753323f354ed4eca05f0`  
		Last Modified: Wed, 10 Apr 2024 08:08:48 GMT  
		Size: 53.5 MB (53492155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042163e6e1fe3d8805f02202161cd324efea6901ddca3f722950dc6c835431b`  
		Last Modified: Wed, 10 Apr 2024 08:09:32 GMT  
		Size: 198.5 MB (198498026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d1a8f7ee151de43e2a5e7467f74e9aff1e8f94198bfb82e1b9256a16ed5cb6`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-buster` - unknown; unknown

```console
$ docker pull rust@sha256:7e6b07cf29947420afc7f3cb9d9b96eafc3cc70e75561c2725b2a8e9b239468a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15627322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2443bc59c40da04634089b702f9ea6ecd8914eeb638af3c06dde5563fc2dcc5f`

```dockerfile
```

-	Layers:
	-	`sha256:4632792f756ad995e692769d516cb8302193e42f60b7ab907b6273b06e339ab4`  
		Last Modified: Wed, 10 Apr 2024 08:56:03 GMT  
		Size: 15.6 MB (15615697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82575d53ebbbb2229ba5140118990013e95bf8e9198c294a5eb759e798c44bb5`  
		Last Modified: Wed, 10 Apr 2024 08:56:03 GMT  
		Size: 11.6 KB (11625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-slim`

```console
$ docker pull rust@sha256:cc74954c41d0c598b54ac119fa829163f0d8348060a6c6abeb1540d2bdfaffcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.77.2-slim` - linux; amd64

```console
$ docker pull rust@sha256:ed00d3908ba2ade42982456c2f9b8b6db5fecf14e9d1d2f58a1dedbb6a7c924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272802753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e1b814adbb0a324618baf1524efbae1616c5450ef892429d2e0c5f3ddc188c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868daa4b67ac105f565dd9a057f7f4f10cc38f9816536d9e7a6bbd620b8ca37d`  
		Last Modified: Wed, 10 Apr 2024 02:56:18 GMT  
		Size: 243.7 MB (243671395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a5d7d5b8dc2e5968bffc0faf477c8fbc4077fbe3ca1631972e06d45cf80a35f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21623c7d2b56a2d1b34a660d9884654aa92743361e69b4f3c1f2e14d1be20598`

```dockerfile
```

-	Layers:
	-	`sha256:db88d5519f271b7d1221885138eb2cb745ff3908ba759b8646ac90e06f7f2527`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 3.9 MB (3919062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe0382e87e578e32ad71f989f31936ddc388b9faf74f0e736098ac3ba5c190c`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 12.8 KB (12814 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim` - linux; 386

```console
$ docker pull rust@sha256:9a072848e2d833cf694b18aefa244a460553f7cf6c85b58f5e2e52286efd174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284750516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca43af6be05127a03ec4d1b7aca13a5833998f17cdb5af3206b6d55dd1991a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f760cffd225a2b32fbf671ab6251bed8d1a36d87cac79c98316872c7a69f93`  
		Last Modified: Wed, 10 Apr 2024 02:03:51 GMT  
		Size: 254.6 MB (254604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim` - unknown; unknown

```console
$ docker pull rust@sha256:d144c1d027fa1f9b95ce873a14624a8040451e3f0e7bc3bf786fae4efc033a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98508d35fb64f25d374e4da636cff8ae441ac72ffc1e3d86d7dad746952d5109`

```dockerfile
```

-	Layers:
	-	`sha256:6af998bc21467f538e8f16857cbd4b31d5b202bdca8935602e1f72ce7eca98f5`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 3.9 MB (3900761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbc0607021120ea5a7abb310a8f1eb23efa63e81dad3298c28eb61e7e63eb70`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-slim-bookworm`

```console
$ docker pull rust@sha256:cc74954c41d0c598b54ac119fa829163f0d8348060a6c6abeb1540d2bdfaffcc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.77.2-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:ed00d3908ba2ade42982456c2f9b8b6db5fecf14e9d1d2f58a1dedbb6a7c924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272802753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e1b814adbb0a324618baf1524efbae1616c5450ef892429d2e0c5f3ddc188c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868daa4b67ac105f565dd9a057f7f4f10cc38f9816536d9e7a6bbd620b8ca37d`  
		Last Modified: Wed, 10 Apr 2024 02:56:18 GMT  
		Size: 243.7 MB (243671395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a5d7d5b8dc2e5968bffc0faf477c8fbc4077fbe3ca1631972e06d45cf80a35f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21623c7d2b56a2d1b34a660d9884654aa92743361e69b4f3c1f2e14d1be20598`

```dockerfile
```

-	Layers:
	-	`sha256:db88d5519f271b7d1221885138eb2cb745ff3908ba759b8646ac90e06f7f2527`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 3.9 MB (3919062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe0382e87e578e32ad71f989f31936ddc388b9faf74f0e736098ac3ba5c190c`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 12.8 KB (12814 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:9a072848e2d833cf694b18aefa244a460553f7cf6c85b58f5e2e52286efd174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284750516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca43af6be05127a03ec4d1b7aca13a5833998f17cdb5af3206b6d55dd1991a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f760cffd225a2b32fbf671ab6251bed8d1a36d87cac79c98316872c7a69f93`  
		Last Modified: Wed, 10 Apr 2024 02:03:51 GMT  
		Size: 254.6 MB (254604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d144c1d027fa1f9b95ce873a14624a8040451e3f0e7bc3bf786fae4efc033a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98508d35fb64f25d374e4da636cff8ae441ac72ffc1e3d86d7dad746952d5109`

```dockerfile
```

-	Layers:
	-	`sha256:6af998bc21467f538e8f16857cbd4b31d5b202bdca8935602e1f72ce7eca98f5`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 3.9 MB (3900761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbc0607021120ea5a7abb310a8f1eb23efa63e81dad3298c28eb61e7e63eb70`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-slim-bullseye`

```console
$ docker pull rust@sha256:604bffc4c1ed68a410b8ab862a3dff5557146a464ee83017cac8982826c56260
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.77.2-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:e3703a692d6689cee0490363bfc8108a9c9e590df6988f2920eb71ab77937c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264463700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fc023abba24900ad681ae8421b1f2d1c477a0cdc7f8779c5147a5df2e64d1f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
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
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ab2f2a3ce344d856412bb76c0cbce30a35aeb53176eb5cec120e3c216f01a`  
		Last Modified: Wed, 10 Apr 2024 02:56:20 GMT  
		Size: 233.0 MB (233035962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:93f63b6fad174237aa1145d25dad1cc04f8aea997947828b38063021fe446db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78abe840ffae11375c7e3b134fad5ba0df3447f6e29e7245a2f7719df6a63b15`

```dockerfile
```

-	Layers:
	-	`sha256:6f58cc69594b21ac6cab79cbd7ffe7bb3572c3a95b2e9e4d2ab1e80b47bde438`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 4.1 MB (4139675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a713004d07c70ce533a189ac1c7759bf8978f36fa4e86386307445c2f7a4b4df`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 11.6 KB (11626 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:e47eddf08aa277fd773b469789469b80214dc1c6eb89cc52dbaed2a45572b346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280210792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c34fb5b92c2203fcb8db1509344b4fad479143f90c59036e639d20e6cf231`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
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
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f761c683b352d393ff3a70a31f1cdb3309470baef708acaaec1d5f65178a780`  
		Last Modified: Wed, 10 Apr 2024 01:54:11 GMT  
		Size: 247.8 MB (247797376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d1306fc47b4244d7f9e7943f5aae84fd486ba130d8d39c608767cb956ddf3271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3908b559c177afd6719140b5a2a3541d95e0921cb245764b7a06f080971b6ac3`

```dockerfile
```

-	Layers:
	-	`sha256:a032ac7469111c4a51d7d1e1b0c75b35aa34e3c8b0d8d8e5bd42030f843b8926`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 4.1 MB (4131731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0b157250963b35b33549efb108518a419ccc9f570c228ba225ea203828b0aa6`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 11.6 KB (11597 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.77.2-slim-buster`

```console
$ docker pull rust@sha256:ee9b8953515c730772e8dd34874dfc44f7ef80020e9a9a773f983cc93f285717
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `rust:1.77.2-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:bef060961cbd2174621dbdc808519969112b6fbccb3e2c4c90b67c67ec186450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245495284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcb8545702f9a0e6721b40aaa469aefcb0622810562883d52ba50ba057c1c5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
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
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c72519ff7f40e33d03c7d3f47e19dcd8420c4c92434d03570faaff716312528`  
		Last Modified: Wed, 10 Apr 2024 02:56:19 GMT  
		Size: 218.3 MB (218304422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:8dcab7ab30592663a02fd73c824b93ceb27704fd316dfdc4a14a8fd53cadca34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858fb1eb2641158105afbe01ba8f4c231a8aae4ad85d82a1c25586aafbbc59da`

```dockerfile
```

-	Layers:
	-	`sha256:38f8d81ee6092d2bfbe77b6702062de3b7d23f5bde67d9773915331d261cb7c0`  
		Last Modified: Wed, 10 Apr 2024 02:56:16 GMT  
		Size: 3.6 MB (3585441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb65268fc77b08bd0a7fa791c3297b3bced6acd88a4bc12a1af05bcf384c5c8`  
		Last Modified: Wed, 10 Apr 2024 02:56:16 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.77.2-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:f16cf382bb643b61546e0716b11c8865933e5ed812ac80169f0c1059d788a546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264864857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c822134f762bf9cdc5c0c15d0d06f50df5c808cbf81120d841f19ee30850f2c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6033d014a0c5c8d87a61d23e20506ec550ea93ef72866e76bfe5a468ceebf619 in / 
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
	-	`sha256:d349bc9800fc6053f91af64b3ce845b5191cc9e0ae2d2001951381ae2d08e46e`  
		Last Modified: Wed, 10 Apr 2024 01:03:40 GMT  
		Size: 27.8 MB (27848331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54caad959c94915ec006deffe9d9bd347eb55d50b70b7ac94922c1784fbdf03`  
		Last Modified: Wed, 10 Apr 2024 01:54:11 GMT  
		Size: 237.0 MB (237016526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.77.2-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:752c286f93a3ae53df42fe4c2153bcdb6523435d242f194aa2925996d9e0251f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c94b966dc0d5d95ee36fe5b571695e3b2992333e109cd314d4b496537982f2c`

```dockerfile
```

-	Layers:
	-	`sha256:f59e8592b975bb56e79e105cf29ff5ee1831a7336624007d7e81a302f3b159d6`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 3.6 MB (3592066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a39c68120f1cbcd3caaed0c37db595248763df96455ec3bccba15f6356f80efe`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 11.2 KB (11190 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:b6ea81b37c9ad8b2c875f64a963b5e418e86d33d41eed529671e86e86d30c884
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
$ docker pull rust@sha256:4c640cb99e88d7e7873a25e5dc693999cd4c5a0f486b54362513f80107920ac3
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
$ docker pull rust@sha256:b6ea81b37c9ad8b2c875f64a963b5e418e86d33d41eed529671e86e86d30c884
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
$ docker pull rust@sha256:a22010a54d04ab9bde99a332f7d37f921bc73fcfce78738a5ae68ab21bcd46b2
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
$ docker pull rust@sha256:6361801bd55ffec96b953437f1083a8d730320b0809292d7d84425ff5f3223a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521770219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead19e243dc6f0b82077e2f7aca0a70a7e4fdd9300f6fa71b1557210b6bea496`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
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
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4251e2c0d85d5696b1917655ebc9009cc6d07741a7410385ecdbf440cc57e92`  
		Last Modified: Wed, 10 Apr 2024 06:54:51 GMT  
		Size: 172.9 MB (172884751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7093785b7995fdc45f27f84b72d85b3425f8cedab6a4692fbb54cd3e8445fd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67072e65542c5c0a7f8c486648acf1470857af35bc22c9994006fe2869e992a`

```dockerfile
```

-	Layers:
	-	`sha256:f58c77986737873a4dd6d0f618ef90591136108b4a126550ab2cbd66d2d01cf5`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 15.4 MB (15370122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3172b133a2a58f28fdc38c6e63776bd4bffb56d2e180b31f207e9f19f4cb2197`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 13.2 KB (13222 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff8d4f50070f7fa5a52f2fcef4f8b51569023de2dde184cb2bf593d596f61547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510035646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb59b3cd57ab4f766666a6c3155019552626eaa52de6881231146e013d09d64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1200500c52f4429e643f87908b44e016ca7b67ac17bcdba07b3884ef8b98fed1`  
		Last Modified: Wed, 10 Apr 2024 00:05:32 GMT  
		Size: 208.6 MB (208612381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b340eca81e3952b867d6121dd010fe5baf4dcf8782a035ef666803baf5a81d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4326b7d2aa5919c3772d38b9ffa6002f9a6b013c3447f507d0800b6c11d178a`

```dockerfile
```

-	Layers:
	-	`sha256:482cba46f5b18fa1452b104ca0bd84ab211676d10a643e56287b9b7477af6258`  
		Last Modified: Wed, 10 Apr 2024 00:05:27 GMT  
		Size: 15.2 MB (15185946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39172abfd0ca99841b69d6dd1903d428f3dfa92415f750b1584c92eae12a7b28`  
		Last Modified: Wed, 10 Apr 2024 00:05:26 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ce750647809bbeb76d60938398758b357a0b66fa60f7066f5195e430b4ab03ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581311877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b136805ec1040e311c556f1db756b3af16437a1c22a9d7c0bdedc4c837138002`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:25:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6faea05ead1ac9cd3244827816e2385b0d62299f7937a4574fc5a9651624c`  
		Last Modified: Tue, 12 Mar 2024 01:35:18 GMT  
		Size: 202.5 MB (202538246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b9ee712f6593072f4693a66c5913d1e384397b49ac2d98a1f3140fffe7df7`  
		Last Modified: Mon, 01 Apr 2024 22:00:00 GMT  
		Size: 241.6 MB (241608857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5204201704e7de4bcdacf00558fafffc7c9b8c9e8900f12f7f97483bdcf56458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15421049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64787d4a6c8f814d976ed17ae2a7920712eed7e04f84ec633f422c49a232ad1`

```dockerfile
```

-	Layers:
	-	`sha256:a4cb9a5dec7e10b7988a8daa9275f100646f550b16ee910659c51897e56cb13f`  
		Last Modified: Mon, 01 Apr 2024 21:59:55 GMT  
		Size: 15.4 MB (15408585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338be08de37e05c5be4c24446c725b6c2b9cf0575449c5ea7c9347ce338e1522`  
		Last Modified: Mon, 01 Apr 2024 21:59:54 GMT  
		Size: 12.5 KB (12464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:a9bb8779de7f84f61b1b534d63ccab47a51f2b9d023747bc4c929b62dbaff1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.5 MB (538538471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b4b887cb142c95f41d1e6044283f57eae3ce754415c7597d11b8239226928`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
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
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d7a956f97c876348400069f4c082762ec5601b2d1fc8e0d06ad7470953b90`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:5e6d6cfa16c6880acd95cd6d1dfeddc01c9a35d292e9d41f7b1b0f965b17580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c2d02a2c3867ebfb256a9d73c98459ab97dabe4b35c11449b6217648ec2d06`

```dockerfile
```

-	Layers:
	-	`sha256:aab93fcb88ff947e4c0fd611f8cfae85a8c0b10ab803bf8d28cfd1ef568eb018`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 15.3 MB (15349163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e601202e79167711bc3330cb281453c48804c39665dd226b584b1e5bb462e0e4`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 13.2 KB (13173 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:4b41c521d075f5edb972830857e8a3c5173737cbab36139aa99fb25ec8b1da6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.5 MB (551483948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f212f212fd6d3995fc076ae937f33f91b67284d1e1a94a8cc986ab95c01f837`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:32:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45907c1aed496630969e5bd8d388ed0966cd10fcd415b40585cbc3d12e206b5d`  
		Last Modified: Tue, 12 Mar 2024 02:21:03 GMT  
		Size: 214.2 MB (214173497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ee9d09b245a78d4b88b6bf1a84d408018883f352e5f250707cd388f4f5cce`  
		Last Modified: Mon, 01 Apr 2024 21:56:09 GMT  
		Size: 188.5 MB (188474733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d4cc824b1260175b98ac1b9a836402d870fd8e4381bdaa1a879f1a2579d7c8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15367591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cb603168de00dfd8c90265bea1041bbfc1b66ef59e9181b65b99fa12193e1b`

```dockerfile
```

-	Layers:
	-	`sha256:cdc78d6b31f0bf0f817d2ae7016377cd45fa292e6008a2602af08f61d279c404`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 15.4 MB (15355083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21591c0ee2c667a4fc7d3628d791444a31722bd5ff03a6d6ba6a660d8a75b49e`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 12.5 KB (12508 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:f05f963212cd299ed68eb0c2fc11bce34b5e9c16d6315bb70b079478bc42c655
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
$ docker pull rust@sha256:b7dd0a9e0432309ac0ee6bd4058bb75bfeaba8ef8b6d4f946305e9d5ba1048ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 MB (495312885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8dc2e90e12adfb05ffe7f3565324bb7b40682bfa9adae698e9870e62ec25ffa`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:8efdcc3201e79c8a09fc9c1ade08492ea33f838047332a7c61988f6357339dee in / 
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
	-	`sha256:ac323bdaa10f869bd9e7adecd8f5326e44acc4c59168868108b1cdf3891089cc`  
		Last Modified: Wed, 10 Apr 2024 01:55:52 GMT  
		Size: 55.1 MB (55090264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84811b2a563b9003abbd1c06f6e45a857315b931855030bdd0443d13d950a996`  
		Last Modified: Wed, 10 Apr 2024 05:36:00 GMT  
		Size: 15.8 MB (15763518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ff24b88ad3798f817849ad391d809ece121dc9b7f82f24bb68eed84561f048`  
		Last Modified: Wed, 10 Apr 2024 05:36:15 GMT  
		Size: 54.6 MB (54588743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f58f24df78e3aabf785017c3197c2a09fd606e7f19a830a1cfde41f681f39e`  
		Last Modified: Wed, 10 Apr 2024 05:36:46 GMT  
		Size: 197.0 MB (196985611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d396a8eca7ee95fff3e5c8b8a21c1df92ec18991eb40d3ca28fea8b5ed20f266`  
		Last Modified: Wed, 10 Apr 2024 06:54:44 GMT  
		Size: 172.9 MB (172884749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1bea0538e2b9f31e9afbd4c8d10b764514307976b5fcddef1f4a4d646cfafdc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14986438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a02fe4ad97e458747fa44d8103d1a8f72d2661d05888460c243a2897a2a2e9`

```dockerfile
```

-	Layers:
	-	`sha256:871bcdf817d45ce38cb083572c574fd08e30362efb624894d1e50d5cfbadc210`  
		Last Modified: Wed, 10 Apr 2024 06:54:39 GMT  
		Size: 15.0 MB (14974378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55dd175cbfe93b618d8ba22bf1498ee78f8ef178b62b9887454e3eb2c00f50c5`  
		Last Modified: Wed, 10 Apr 2024 06:54:39 GMT  
		Size: 12.1 KB (12060 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:3de59a1810552ce15b00537e55ace34a7cc372de707c6d9f3408f8a9540629cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.5 MB (491529912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe0365b61c725f4967fecee7b926a413ff21cddec137a74990f6a9fe45da2a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:25 GMT
ADD file:477c339ed6ec658bb1d0025e1568290c3cbbc98d9f973379f3133b83c2de9128 in / 
# Tue, 12 Mar 2024 00:59:28 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:11:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ab40cb80ac5229a1c48dfbfe9aaa04da29109444982d90d4bca2c7b6842beceb`  
		Last Modified: Tue, 12 Mar 2024 01:03:56 GMT  
		Size: 50.2 MB (50241442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3dae685361a941719b8f1aafa21f93305a1df032b9e9940f90b7dafabb394d`  
		Last Modified: Tue, 12 Mar 2024 02:20:17 GMT  
		Size: 14.9 MB (14878987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a08f233733bf767f50d39c3e0a1ce20900043f44a7e4df655c1c5556a9e2834`  
		Last Modified: Tue, 12 Mar 2024 02:20:36 GMT  
		Size: 50.4 MB (50357621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fea5901896ab9c5ad236e05b73d2065621d4488b4c7d2d61bef4316c3c981b2`  
		Last Modified: Tue, 12 Mar 2024 02:22:12 GMT  
		Size: 167.4 MB (167439330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a22ce7aa75fe6849bccde6452ebda329b039bb673f149b807a6ebab6fc9b53`  
		Last Modified: Wed, 10 Apr 2024 00:01:09 GMT  
		Size: 208.6 MB (208612532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a6f7c82952074d71cb715e34087f3175445219133056ad7fa9670144e666a90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14787749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cad5c1b513434efa6f47f58a6a8e3d1c9bf7578c2cd30f23a787f1a7372b6ab`

```dockerfile
```

-	Layers:
	-	`sha256:6ed4c8aef46f131be746be5a89a077d8b28609cf00ec902b4c0911d45dabce8a`  
		Last Modified: Wed, 10 Apr 2024 00:01:04 GMT  
		Size: 14.8 MB (14776282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40f065e754ae91ecf02a567b53fcf1e21d6124125220ed2dae885905e3528890`  
		Last Modified: Wed, 10 Apr 2024 00:01:04 GMT  
		Size: 11.5 KB (11467 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b587651647adb295cf6b122fee23e56562b5e997577aa327d6c1a0c6b649a524
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **555.7 MB (555689462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35b4c2f9368002c1420b0be85d03984989f0a4e818a3fc18bf499eef1874d3a8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:43 GMT
ADD file:7cb312b5f676a37f5c3172be6eb95e30986e5da0dcf21985d2176f8a9a037012 in / 
# Tue, 12 Mar 2024 00:45:44 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:26:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:26:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:f53ee134f2f58aa9d86f682cbedb185619a5b857474f430e6dc3384fafdec81c`  
		Last Modified: Tue, 12 Mar 2024 00:49:12 GMT  
		Size: 53.7 MB (53722099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289bcd9f29514582dfa181c0dd78e701e54e4abb9988a08a2175a3b8de2d4b3e`  
		Last Modified: Tue, 12 Mar 2024 01:35:30 GMT  
		Size: 15.7 MB (15749203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b26e715641714983e979229284b3dd79698d1c59197f4e33089c8c196e2956`  
		Last Modified: Tue, 12 Mar 2024 01:35:44 GMT  
		Size: 54.7 MB (54694301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d317b4db41e297cffa1559c871d84437b3544f7a4c04d6cf339cd4e8caa94c76`  
		Last Modified: Tue, 12 Mar 2024 01:36:09 GMT  
		Size: 189.9 MB (189914923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5418f8e13c8934d51e047556794e458fa5836df81997654a00e4fdc1073cb9`  
		Last Modified: Mon, 01 Apr 2024 21:56:51 GMT  
		Size: 241.6 MB (241608936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:007752e704a42ff34a74a4aedfffb805a72715dfc71040dec17ecb1db8724292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14988142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5194969bd09bd7a480f3a14dad516153c0148c1fd9ddd62164ef0a2b1520236`

```dockerfile
```

-	Layers:
	-	`sha256:3bc0c024ad242e35e5fa0cda2ccc5332c386bdcfec0cd0cc024e62ecf9fc1dde`  
		Last Modified: Mon, 01 Apr 2024 21:56:47 GMT  
		Size: 15.0 MB (14976847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0c21cae6999254524af2572e00c085a82381d81910fd1c7336c002b7aac74b0`  
		Last Modified: Mon, 01 Apr 2024 21:56:46 GMT  
		Size: 11.3 KB (11295 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:70fdeab84eff10abd352c3077ab7785ea921f5a019eb62f7106962b297969298
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.2 MB (515173027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c21e4bc28fb83f646ce347daa1059a5210007b3827a3baba597b7fd9465fe0a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:34b6b0eca66bdded42723d3cb7b488ca726fedb7fd2a42c047e2790ccf93f08b in / 
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
	-	`sha256:1dc10b34406db63eacc8d006ba4d0103014a3a863134cdfe43622d4706753fa7`  
		Last Modified: Wed, 10 Apr 2024 01:02:27 GMT  
		Size: 56.1 MB (56066188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125c557bd27681f5387605727a1b0d44605793da722ea6f8f66b86df9aa54384`  
		Last Modified: Wed, 10 Apr 2024 08:07:12 GMT  
		Size: 16.3 MB (16267921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13acd7d81d47808020936c58e9842c82c55c0205f369482de2b263fe21ed2dc6`  
		Last Modified: Wed, 10 Apr 2024 08:07:31 GMT  
		Size: 55.9 MB (55927749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed69373b65ed4263cd1d2ead3d6570264c8de6a744aa10974a8266c660515080`  
		Last Modified: Wed, 10 Apr 2024 08:08:16 GMT  
		Size: 199.9 MB (199890546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d5ec320ca15085353a9eac55306245a69c0c57ccc50a4011aaf6b70f87d3fb`  
		Last Modified: Wed, 10 Apr 2024 08:56:06 GMT  
		Size: 187.0 MB (187020623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:da43ec4a6be596a9a8ba8f2a6525924a2d26a9746e952339419dfa4065acdfe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14975234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b4c78b31760218804790ec5ab591b04cf5d17e30e59b123209347d31c7656c`

```dockerfile
```

-	Layers:
	-	`sha256:e4039901b8fae7bbf1b656a6fbde410c408cd57f6ebe8e20e6e4c7405072ebf9`  
		Last Modified: Wed, 10 Apr 2024 08:56:02 GMT  
		Size: 15.0 MB (14963203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a066ce0f742bb5333d2b61590453bee5a925a2cf0ec058477f3821674fa65d9f`  
		Last Modified: Wed, 10 Apr 2024 08:56:01 GMT  
		Size: 12.0 KB (12031 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:8471b7c3efb93f5afbc21d7828fcda9fa0a2f7ebb6e55d659116235afda4a71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **519.4 MB (519415387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036cc170d8e81e97f632eeac3fb7aac0018dcec3088b88dc70bb60a972d57e23`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:37 GMT
ADD file:378e777c8961453a2c8c9a594105395e4a83f5e94a90756bc3eebe9ec18be242 in / 
# Tue, 12 Mar 2024 00:30:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:35:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:37:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:99575d2dfd5e66cfbe10e815aa8a7bfacb8fa923bf112abd5b9334bec5404161`  
		Last Modified: Tue, 12 Mar 2024 00:38:29 GMT  
		Size: 59.0 MB (58954475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce422567beb05db7b6d7eca359e7168a80a58b1c86d36287c6b86c9b76d845f`  
		Last Modified: Tue, 12 Mar 2024 02:21:17 GMT  
		Size: 16.8 MB (16765930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777aef5bbe7e540f91bd63fda95e7f25c0ba803d2a25a532b2f2306c6b2209d1`  
		Last Modified: Tue, 12 Mar 2024 02:21:36 GMT  
		Size: 58.9 MB (58873337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078e6b4fd896687174cc2013bea6ca7f49c8cd898255e8d37361b8486cb7fe25`  
		Last Modified: Tue, 12 Mar 2024 02:22:13 GMT  
		Size: 196.3 MB (196346975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd567a7f48ce9a547d2ed2aa59d0f4a817bad8643bb24efef2b49c60c022be25`  
		Last Modified: Mon, 01 Apr 2024 21:51:32 GMT  
		Size: 188.5 MB (188474670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:5ecefd461ba9b7e9614c363b8ad717c5ed64dfa2ec4fe2d9e3c00aa2e07040cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14953306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69996fb9f6e80b9872d4c166ef6f9326fda8fb0a575c72930785b8692ecbce6`

```dockerfile
```

-	Layers:
	-	`sha256:37077dfb3fce4f1b82732e80df6e8ddd95bf19b0066dec1e8528f0aeaffaf6ab`  
		Last Modified: Mon, 01 Apr 2024 21:51:27 GMT  
		Size: 14.9 MB (14941983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5226f9f7a86e57b8c4914f44b244312869dedf73844351bad06b560a960266`  
		Last Modified: Mon, 01 Apr 2024 21:51:26 GMT  
		Size: 11.3 KB (11323 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:buster`

```console
$ docker pull rust@sha256:d94731e2a342d1736d23262c936821bfdf330198d757f430f3682c5844ff28c7
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
$ docker pull rust@sha256:ef4bd23ba9eb1fc17a271848ef3a8e11b0574868db455d2fafd61ae56263bf0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **484.8 MB (484813822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54ef59296b3f783361ff9ecee292d7a3d701c9bf15748e18b947411a563b96f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
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
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e204ce2733ed28c5c2c45652e3fd6034257b2cc15670e98293092efdc65833ec`  
		Last Modified: Wed, 10 Apr 2024 06:55:04 GMT  
		Size: 172.9 MB (172884650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:a6286a89012d075f07d624270d53f0d0df8283771aac7a270eccd1a6ec720625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15621770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8a2473f9ccc6c27bb501328c69f43eecbab161d7b4277a52933e462188df7bd`

```dockerfile
```

-	Layers:
	-	`sha256:f3998dec0353df1cec4c007c431ec1d097346b66751099e7cf175df0b6c0295d`  
		Last Modified: Wed, 10 Apr 2024 06:54:59 GMT  
		Size: 15.6 MB (15610116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2cdaeebcd398b7ffe5440b98f95202e4edd572ffd0d45344c138efe49be44ea`  
		Last Modified: Wed, 10 Apr 2024 06:54:58 GMT  
		Size: 11.7 KB (11654 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:f1163e13d71ffaf291be8d0e17de87300460c80bf6e44386811a5758d0764ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **486.3 MB (486340982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e374110670e91904baaab7f3ed7c6af22e757c9be10ee7b8f0a1b8e7dad38f0a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec28d557d3104596d3ba5ab227e1e527ff8f93195f04af289dd5da1316ba29d9`  
		Last Modified: Tue, 12 Mar 2024 02:22:40 GMT  
		Size: 47.4 MB (47410735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb141b0531169976182ab39baba3c902bed903a2c25a2e2045f8c6cee114563c`  
		Last Modified: Tue, 12 Mar 2024 02:23:15 GMT  
		Size: 168.1 MB (168133921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8549a616e2a73c5409031ef4981fbf9ab21f8257e0492c65eb6095983f33d03`  
		Last Modified: Tue, 09 Apr 2024 23:56:04 GMT  
		Size: 208.6 MB (208612535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:65db45a78896d6997258088e0b5eac261a72871c29b3e2c53573b6ddd3fd5a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15423150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f7d3f85b9b79a109f763b2cdf82264b39bfa5029392bce77d3b858944387ba`

```dockerfile
```

-	Layers:
	-	`sha256:890e6de1a22bd1f71a395a5fdfc679a17725d6211ca1d73c0b403dca5e7f8f74`  
		Last Modified: Tue, 09 Apr 2024 23:56:00 GMT  
		Size: 15.4 MB (15412089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11079f1a552e59ef9774e79760fa4335bc5355ee2e30d84dc524fc26dccd032`  
		Last Modified: Tue, 09 Apr 2024 23:55:59 GMT  
		Size: 11.1 KB (11061 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d83db167f8b57f6fb23e0c1c978e0f0c249ee6e7a779481af62e0636bd6f40fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **544.1 MB (544097043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ee814bf692b8e7c55b8e070bfa7c0b55a2f01a111874ad8000976ac91f9a8f6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:28:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8987ebef52bd1e6f6f20b38f5dd0fa9030c75a5089144eabf4a20c7b2aa2605a`  
		Last Modified: Tue, 12 Mar 2024 01:36:57 GMT  
		Size: 52.2 MB (52225028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe09b4296b95b0c32948c55d4f978937b58f5a899208693bb4c304804492322`  
		Last Modified: Tue, 12 Mar 2024 01:37:27 GMT  
		Size: 183.5 MB (183517797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940961b85fdf2974f8776ada55477feb2f6cdfb8eef0be7a114dae57302f215c`  
		Last Modified: Mon, 01 Apr 2024 21:53:42 GMT  
		Size: 241.6 MB (241608909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:9380a50320d9bc998ae47a89e3d31fb990551367caeec9082029bf8639626916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15611676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcf6bea59be5926ea708c5ba672bc55be4ba6c82d2bf3951bae5db90bf8ffb5`

```dockerfile
```

-	Layers:
	-	`sha256:673395325db4802c1fbda7722d59f6aca46826e9b8fdc64601eccc7e3502bbde`  
		Last Modified: Mon, 01 Apr 2024 21:53:37 GMT  
		Size: 15.6 MB (15600784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abfee4d187200bc6ff2e874003b62ae48b59ee70de18013d5d21be69e442bc4d`  
		Last Modified: Mon, 01 Apr 2024 21:53:36 GMT  
		Size: 10.9 KB (10892 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; 386

```console
$ docker pull rust@sha256:49629f3d3a1b7cf41847d495f69754d266c3257db8d6c3a401be76e1e8f95e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.4 MB (508366490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8787cf9ea38af799d2c5aa0fc246337f220a2f67ce427d69e6a665f843959019`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:b0be520dbc93fbc08e051c8ea8793595dbd38e91643b1d941ad956d2a4397f8f in / 
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
	-	`sha256:f0d58f6fa9239b96dd44a4bb70c4da4650d0ca0b4b35f492bda37d153b9ed6ba`  
		Last Modified: Wed, 10 Apr 2024 01:03:15 GMT  
		Size: 51.3 MB (51256498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f83de192d57649c06466addcbc7b9ccd636e9d291c22fdf5d7e4a4e6c59450d`  
		Last Modified: Wed, 10 Apr 2024 08:08:28 GMT  
		Size: 18.1 MB (18099188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bc8c20df52365967a4f48f20656372016f14141f60753323f354ed4eca05f0`  
		Last Modified: Wed, 10 Apr 2024 08:08:48 GMT  
		Size: 53.5 MB (53492155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1042163e6e1fe3d8805f02202161cd324efea6901ddca3f722950dc6c835431b`  
		Last Modified: Wed, 10 Apr 2024 08:09:32 GMT  
		Size: 198.5 MB (198498026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90d1a8f7ee151de43e2a5e7467f74e9aff1e8f94198bfb82e1b9256a16ed5cb6`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:7e6b07cf29947420afc7f3cb9d9b96eafc3cc70e75561c2725b2a8e9b239468a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15627322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2443bc59c40da04634089b702f9ea6ecd8914eeb638af3c06dde5563fc2dcc5f`

```dockerfile
```

-	Layers:
	-	`sha256:4632792f756ad995e692769d516cb8302193e42f60b7ab907b6273b06e339ab4`  
		Last Modified: Wed, 10 Apr 2024 08:56:03 GMT  
		Size: 15.6 MB (15615697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82575d53ebbbb2229ba5140118990013e95bf8e9198c294a5eb759e798c44bb5`  
		Last Modified: Wed, 10 Apr 2024 08:56:03 GMT  
		Size: 11.6 KB (11625 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:latest`

```console
$ docker pull rust@sha256:a22010a54d04ab9bde99a332f7d37f921bc73fcfce78738a5ae68ab21bcd46b2
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
$ docker pull rust@sha256:6361801bd55ffec96b953437f1083a8d730320b0809292d7d84425ff5f3223a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.8 MB (521770219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead19e243dc6f0b82077e2f7aca0a70a7e4fdd9300f6fa71b1557210b6bea496`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
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
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4251e2c0d85d5696b1917655ebc9009cc6d07741a7410385ecdbf440cc57e92`  
		Last Modified: Wed, 10 Apr 2024 06:54:51 GMT  
		Size: 172.9 MB (172884751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:7093785b7995fdc45f27f84b72d85b3425f8cedab6a4692fbb54cd3e8445fd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15383344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67072e65542c5c0a7f8c486648acf1470857af35bc22c9994006fe2869e992a`

```dockerfile
```

-	Layers:
	-	`sha256:f58c77986737873a4dd6d0f618ef90591136108b4a126550ab2cbd66d2d01cf5`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 15.4 MB (15370122 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3172b133a2a58f28fdc38c6e63776bd4bffb56d2e180b31f207e9f19f4cb2197`  
		Last Modified: Wed, 10 Apr 2024 06:54:49 GMT  
		Size: 13.2 KB (13222 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:ff8d4f50070f7fa5a52f2fcef4f8b51569023de2dde184cb2bf593d596f61547
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **510.0 MB (510035646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb59b3cd57ab4f766666a6c3155019552626eaa52de6881231146e013d09d64`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Apr 2024 22:06:26 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Tue, 09 Apr 2024 22:06:26 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.2
# Tue, 09 Apr 2024 22:06:26 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c41c61f6174f60169420d32957e496b1d382932c8ceb86da9fd7484a7210398`  
		Last Modified: Tue, 12 Mar 2024 02:19:27 GMT  
		Size: 59.2 MB (59213166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b80994404300d9b15d70f0499bf342d2201561d20bd0ee4fac8c6e5db74261`  
		Last Modified: Tue, 12 Mar 2024 02:20:05 GMT  
		Size: 175.1 MB (175105976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1200500c52f4429e643f87908b44e016ca7b67ac17bcdba07b3884ef8b98fed1`  
		Last Modified: Wed, 10 Apr 2024 00:05:32 GMT  
		Size: 208.6 MB (208612381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:b340eca81e3952b867d6121dd010fe5baf4dcf8782a035ef666803baf5a81d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4326b7d2aa5919c3772d38b9ffa6002f9a6b013c3447f507d0800b6c11d178a`

```dockerfile
```

-	Layers:
	-	`sha256:482cba46f5b18fa1452b104ca0bd84ab211676d10a643e56287b9b7477af6258`  
		Last Modified: Wed, 10 Apr 2024 00:05:27 GMT  
		Size: 15.2 MB (15185946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39172abfd0ca99841b69d6dd1903d428f3dfa92415f750b1584c92eae12a7b28`  
		Last Modified: Wed, 10 Apr 2024 00:05:26 GMT  
		Size: 12.7 KB (12661 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ce750647809bbeb76d60938398758b357a0b66fa60f7066f5195e430b4ab03ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **581.3 MB (581311877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b136805ec1040e311c556f1db756b3af16437a1c22a9d7c0bdedc4c837138002`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:25:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3861a6536e4e911503e7d2fc8f93228491ba45d1e5def0d2f3723e32e03d7466`  
		Last Modified: Tue, 12 Mar 2024 01:34:50 GMT  
		Size: 64.0 MB (63990914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5e6faea05ead1ac9cd3244827816e2385b0d62299f7937a4574fc5a9651624c`  
		Last Modified: Tue, 12 Mar 2024 01:35:18 GMT  
		Size: 202.5 MB (202538246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b9ee712f6593072f4693a66c5913d1e384397b49ac2d98a1f3140fffe7df7`  
		Last Modified: Mon, 01 Apr 2024 22:00:00 GMT  
		Size: 241.6 MB (241608857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:5204201704e7de4bcdacf00558fafffc7c9b8c9e8900f12f7f97483bdcf56458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15421049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c64787d4a6c8f814d976ed17ae2a7920712eed7e04f84ec633f422c49a232ad1`

```dockerfile
```

-	Layers:
	-	`sha256:a4cb9a5dec7e10b7988a8daa9275f100646f550b16ee910659c51897e56cb13f`  
		Last Modified: Mon, 01 Apr 2024 21:59:55 GMT  
		Size: 15.4 MB (15408585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:338be08de37e05c5be4c24446c725b6c2b9cf0575449c5ea7c9347ce338e1522`  
		Last Modified: Mon, 01 Apr 2024 21:59:54 GMT  
		Size: 12.5 KB (12464 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:a9bb8779de7f84f61b1b534d63ccab47a51f2b9d023747bc4c929b62dbaff1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.5 MB (538538471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236b4b887cb142c95f41d1e6044283f57eae3ce754415c7597d11b8239226928`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
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
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6d7a956f97c876348400069f4c082762ec5601b2d1fc8e0d06ad7470953b90`  
		Last Modified: Wed, 10 Apr 2024 08:56:09 GMT  
		Size: 187.0 MB (187020652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:5e6d6cfa16c6880acd95cd6d1dfeddc01c9a35d292e9d41f7b1b0f965b17580f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15362336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40c2d02a2c3867ebfb256a9d73c98459ab97dabe4b35c11449b6217648ec2d06`

```dockerfile
```

-	Layers:
	-	`sha256:aab93fcb88ff947e4c0fd611f8cfae85a8c0b10ab803bf8d28cfd1ef568eb018`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 15.3 MB (15349163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e601202e79167711bc3330cb281453c48804c39665dd226b584b1e5bb462e0e4`  
		Last Modified: Wed, 10 Apr 2024 08:56:05 GMT  
		Size: 13.2 KB (13173 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:4b41c521d075f5edb972830857e8a3c5173737cbab36139aa99fb25ec8b1da6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **551.5 MB (551483948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f212f212fd6d3995fc076ae937f33f91b67284d1e1a94a8cc986ab95c01f837`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:29:51 GMT
ADD file:c5929f4b94168a6c2b67522cc5aea49aef7e290fc5c328f387523a3d16154100 in / 
# Tue, 12 Mar 2024 00:29:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:19:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:21:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:32:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ace76237e931cd48dae2ec361ac06fa249ce4c2877f599ed74f188ca39974407`  
		Last Modified: Tue, 12 Mar 2024 00:37:38 GMT  
		Size: 53.6 MB (53556955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a30711853e1103e2a5ce889e2b171af6e0587cbe00d19b777a831e8e78143df`  
		Last Modified: Tue, 12 Mar 2024 02:19:58 GMT  
		Size: 25.7 MB (25696864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7f6b2d513138ada95189d6b9402e50953a70524968e742ada51774c5f48fd0`  
		Last Modified: Tue, 12 Mar 2024 02:20:20 GMT  
		Size: 69.6 MB (69581899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45907c1aed496630969e5bd8d388ed0966cd10fcd415b40585cbc3d12e206b5d`  
		Last Modified: Tue, 12 Mar 2024 02:21:03 GMT  
		Size: 214.2 MB (214173497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ee9d09b245a78d4b88b6bf1a84d408018883f352e5f250707cd388f4f5cce`  
		Last Modified: Mon, 01 Apr 2024 21:56:09 GMT  
		Size: 188.5 MB (188474733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:d4cc824b1260175b98ac1b9a836402d870fd8e4381bdaa1a879f1a2579d7c8e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15367591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cb603168de00dfd8c90265bea1041bbfc1b66ef59e9181b65b99fa12193e1b`

```dockerfile
```

-	Layers:
	-	`sha256:cdc78d6b31f0bf0f817d2ae7016377cd45fa292e6008a2602af08f61d279c404`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 15.4 MB (15355083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21591c0ee2c667a4fc7d3628d791444a31722bd5ff03a6d6ba6a660d8a75b49e`  
		Last Modified: Mon, 01 Apr 2024 21:56:05 GMT  
		Size: 12.5 KB (12508 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:78b5459dc7218e633da119c82b215d54e5029fe3cb7e0e9bd7ca19ffacda77ca
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
$ docker pull rust@sha256:ed00d3908ba2ade42982456c2f9b8b6db5fecf14e9d1d2f58a1dedbb6a7c924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272802753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e1b814adbb0a324618baf1524efbae1616c5450ef892429d2e0c5f3ddc188c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868daa4b67ac105f565dd9a057f7f4f10cc38f9816536d9e7a6bbd620b8ca37d`  
		Last Modified: Wed, 10 Apr 2024 02:56:18 GMT  
		Size: 243.7 MB (243671395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:a5d7d5b8dc2e5968bffc0faf477c8fbc4077fbe3ca1631972e06d45cf80a35f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21623c7d2b56a2d1b34a660d9884654aa92743361e69b4f3c1f2e14d1be20598`

```dockerfile
```

-	Layers:
	-	`sha256:db88d5519f271b7d1221885138eb2cb745ff3908ba759b8646ac90e06f7f2527`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 3.9 MB (3919062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe0382e87e578e32ad71f989f31936ddc388b9faf74f0e736098ac3ba5c190c`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 12.8 KB (12814 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:8fae5654772edd365dfd01f53835efcd50c85e9a9124c88476d6cfd02b8987e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281125976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd3d4379b89c0b08406e6611007fc87b392af0616e7c7a78525dd7fef8954b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbdfe2d8afc590898b008ae5ac867b9c9ecaba2e23c4ce8242c8ff24dfcb4e`  
		Last Modified: Mon, 01 Apr 2024 22:05:59 GMT  
		Size: 256.4 MB (256409251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:57d8f50dd1c6b235d090f83fe48ae776dc009ae8e9446e0e98f71bc218118ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27fb31bede8afd182c86d6517398034aafef2892fe5a8533744f9a46d0427f8`

```dockerfile
```

-	Layers:
	-	`sha256:ae00f303130b0e32159908141b05a139cc824b82a42f44b70812b88a36ea65a4`  
		Last Modified: Mon, 01 Apr 2024 22:05:54 GMT  
		Size: 3.7 MB (3737518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de84682983e233db29c48bc5d1ad2738cbfbd5eb650bbe9fb47772d589981b85`  
		Last Modified: Mon, 01 Apr 2024 22:05:53 GMT  
		Size: 12.6 KB (12637 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6af0432b6d1b9274fbda00f1e31e2d3465171e66d32318c729d03bd3c51618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336617112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355ad31b2818638e6828730de81e62b4574f851cd03d587008dd227b5e75e1a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8aac4a9ac99feb14bacf4109c65ccefc4efa32032e32522c7fc72370be73c9`  
		Last Modified: Mon, 01 Apr 2024 22:01:33 GMT  
		Size: 307.5 MB (307460678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:b269d7552b7b1b75d79080032ac62815904b266c69efe60dcaaf88ebe8194195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3fd44111ce2bb4129bc96af803aad106c6fd6cb819c617ad5392dfbf9b8f6b`

```dockerfile
```

-	Layers:
	-	`sha256:b13e178634ac422c29c30639e4a5404d22c1636919f1268cd8af918a15f25ff1`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 3.9 MB (3942630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29301f3480b2dcd0cc128b64522f960bcc98ecf37d6db7a527cbd65d59f31c34`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 12.6 KB (12553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:9a072848e2d833cf694b18aefa244a460553f7cf6c85b58f5e2e52286efd174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284750516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca43af6be05127a03ec4d1b7aca13a5833998f17cdb5af3206b6d55dd1991a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f760cffd225a2b32fbf671ab6251bed8d1a36d87cac79c98316872c7a69f93`  
		Last Modified: Wed, 10 Apr 2024 02:03:51 GMT  
		Size: 254.6 MB (254604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:d144c1d027fa1f9b95ce873a14624a8040451e3f0e7bc3bf786fae4efc033a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98508d35fb64f25d374e4da636cff8ae441ac72ffc1e3d86d7dad746952d5109`

```dockerfile
```

-	Layers:
	-	`sha256:6af998bc21467f538e8f16857cbd4b31d5b202bdca8935602e1f72ce7eca98f5`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 3.9 MB (3900761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbc0607021120ea5a7abb310a8f1eb23efa63e81dad3298c28eb61e7e63eb70`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:e8f8ec53a391d9113d8080ba20f31c338c4cf6cbe6aae3d3f04a972868df31a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290361922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e298b7e70665b3442d85e1806ad164a55a9f7b0a16463dad74a0bf044226f5fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4418400b66496376009e657c8080f4ea2dbbaaf1bccc166de6aac1b72a8e971`  
		Last Modified: Mon, 01 Apr 2024 21:58:19 GMT  
		Size: 257.2 MB (257242899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:da4ab5fbedd89882e94c6ff8acef6cc756b9b3d25f9d18c7ce53f61a46f74af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3905390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85edd0d98bb412cff6a24ffa03005353fc736121e05de765d98422afe663e20`

```dockerfile
```

-	Layers:
	-	`sha256:6feae90e068af601f73655101ccf01c3d659370b865a4b719e3b7fccf8b87d68`  
		Last Modified: Mon, 01 Apr 2024 21:58:13 GMT  
		Size: 3.9 MB (3892794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fc000faf56d83a6990e8558b09b2c09cb026e52b4ec329e598045f9fad096c`  
		Last Modified: Mon, 01 Apr 2024 21:58:12 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:78b5459dc7218e633da119c82b215d54e5029fe3cb7e0e9bd7ca19ffacda77ca
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
$ docker pull rust@sha256:ed00d3908ba2ade42982456c2f9b8b6db5fecf14e9d1d2f58a1dedbb6a7c924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272802753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e1b814adbb0a324618baf1524efbae1616c5450ef892429d2e0c5f3ddc188c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
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
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868daa4b67ac105f565dd9a057f7f4f10cc38f9816536d9e7a6bbd620b8ca37d`  
		Last Modified: Wed, 10 Apr 2024 02:56:18 GMT  
		Size: 243.7 MB (243671395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a5d7d5b8dc2e5968bffc0faf477c8fbc4077fbe3ca1631972e06d45cf80a35f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3931876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21623c7d2b56a2d1b34a660d9884654aa92743361e69b4f3c1f2e14d1be20598`

```dockerfile
```

-	Layers:
	-	`sha256:db88d5519f271b7d1221885138eb2cb745ff3908ba759b8646ac90e06f7f2527`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 3.9 MB (3919062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebe0382e87e578e32ad71f989f31936ddc388b9faf74f0e736098ac3ba5c190c`  
		Last Modified: Wed, 10 Apr 2024 02:56:15 GMT  
		Size: 12.8 KB (12814 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:8fae5654772edd365dfd01f53835efcd50c85e9a9124c88476d6cfd02b8987e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.1 MB (281125976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd3d4379b89c0b08406e6611007fc87b392af0616e7c7a78525dd7fef8954b6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:15 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 12 Mar 2024 00:59:16 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbbdfe2d8afc590898b008ae5ac867b9c9ecaba2e23c4ce8242c8ff24dfcb4e`  
		Last Modified: Mon, 01 Apr 2024 22:05:59 GMT  
		Size: 256.4 MB (256409251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:57d8f50dd1c6b235d090f83fe48ae776dc009ae8e9446e0e98f71bc218118ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3750155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27fb31bede8afd182c86d6517398034aafef2892fe5a8533744f9a46d0427f8`

```dockerfile
```

-	Layers:
	-	`sha256:ae00f303130b0e32159908141b05a139cc824b82a42f44b70812b88a36ea65a4`  
		Last Modified: Mon, 01 Apr 2024 22:05:54 GMT  
		Size: 3.7 MB (3737518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de84682983e233db29c48bc5d1ad2738cbfbd5eb650bbe9fb47772d589981b85`  
		Last Modified: Mon, 01 Apr 2024 22:05:53 GMT  
		Size: 12.6 KB (12637 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:5a6af0432b6d1b9274fbda00f1e31e2d3465171e66d32318c729d03bd3c51618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336617112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355ad31b2818638e6828730de81e62b4574f851cd03d587008dd227b5e75e1a2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8aac4a9ac99feb14bacf4109c65ccefc4efa32032e32522c7fc72370be73c9`  
		Last Modified: Mon, 01 Apr 2024 22:01:33 GMT  
		Size: 307.5 MB (307460678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b269d7552b7b1b75d79080032ac62815904b266c69efe60dcaaf88ebe8194195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3955183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3fd44111ce2bb4129bc96af803aad106c6fd6cb819c617ad5392dfbf9b8f6b`

```dockerfile
```

-	Layers:
	-	`sha256:b13e178634ac422c29c30639e4a5404d22c1636919f1268cd8af918a15f25ff1`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 3.9 MB (3942630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29301f3480b2dcd0cc128b64522f960bcc98ecf37d6db7a527cbd65d59f31c34`  
		Last Modified: Mon, 01 Apr 2024 22:01:25 GMT  
		Size: 12.6 KB (12553 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:9a072848e2d833cf694b18aefa244a460553f7cf6c85b58f5e2e52286efd174a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284750516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eca43af6be05127a03ec4d1b7aca13a5833998f17cdb5af3206b6d55dd1991a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f760cffd225a2b32fbf671ab6251bed8d1a36d87cac79c98316872c7a69f93`  
		Last Modified: Wed, 10 Apr 2024 02:03:51 GMT  
		Size: 254.6 MB (254604001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:d144c1d027fa1f9b95ce873a14624a8040451e3f0e7bc3bf786fae4efc033a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98508d35fb64f25d374e4da636cff8ae441ac72ffc1e3d86d7dad746952d5109`

```dockerfile
```

-	Layers:
	-	`sha256:6af998bc21467f538e8f16857cbd4b31d5b202bdca8935602e1f72ce7eca98f5`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 3.9 MB (3900761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfbc0607021120ea5a7abb310a8f1eb23efa63e81dad3298c28eb61e7e63eb70`  
		Last Modified: Wed, 10 Apr 2024 02:03:46 GMT  
		Size: 12.8 KB (12765 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:e8f8ec53a391d9113d8080ba20f31c338c4cf6cbe6aae3d3f04a972868df31a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.4 MB (290361922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e298b7e70665b3442d85e1806ad164a55a9f7b0a16463dad74a0bf044226f5fc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:30:19 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 12 Mar 2024 00:30:24 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4418400b66496376009e657c8080f4ea2dbbaaf1bccc166de6aac1b72a8e971`  
		Last Modified: Mon, 01 Apr 2024 21:58:19 GMT  
		Size: 257.2 MB (257242899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:da4ab5fbedd89882e94c6ff8acef6cc756b9b3d25f9d18c7ce53f61a46f74af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3905390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85edd0d98bb412cff6a24ffa03005353fc736121e05de765d98422afe663e20`

```dockerfile
```

-	Layers:
	-	`sha256:6feae90e068af601f73655101ccf01c3d659370b865a4b719e3b7fccf8b87d68`  
		Last Modified: Mon, 01 Apr 2024 21:58:13 GMT  
		Size: 3.9 MB (3892794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78fc000faf56d83a6990e8558b09b2c09cb026e52b4ec329e598045f9fad096c`  
		Last Modified: Mon, 01 Apr 2024 21:58:12 GMT  
		Size: 12.6 KB (12596 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:81435e6e61bb826e17ff6e260461db26d579c96298ae22533028e2b03cfe1803
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
$ docker pull rust@sha256:e3703a692d6689cee0490363bfc8108a9c9e590df6988f2920eb71ab77937c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.5 MB (264463700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71fc023abba24900ad681ae8421b1f2d1c477a0cdc7f8779c5147a5df2e64d1f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:5d6b639e8b6bcc01149b7486502558088f9816200063ca72b91a1f989bc8d85e in / 
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
	-	`sha256:04e7578caeaa5a84ad5d534aabbb307a37c85f9444b94949d37544a1c69c8f15`  
		Last Modified: Wed, 10 Apr 2024 01:56:15 GMT  
		Size: 31.4 MB (31427738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345ab2f2a3ce344d856412bb76c0cbce30a35aeb53176eb5cec120e3c216f01a`  
		Last Modified: Wed, 10 Apr 2024 02:56:20 GMT  
		Size: 233.0 MB (233035962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:93f63b6fad174237aa1145d25dad1cc04f8aea997947828b38063021fe446db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78abe840ffae11375c7e3b134fad5ba0df3447f6e29e7245a2f7719df6a63b15`

```dockerfile
```

-	Layers:
	-	`sha256:6f58cc69594b21ac6cab79cbd7ffe7bb3572c3a95b2e9e4d2ab1e80b47bde438`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 4.1 MB (4139675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a713004d07c70ce533a189ac1c7759bf8978f36fa4e86386307445c2f7a4b4df`  
		Last Modified: Wed, 10 Apr 2024 02:56:14 GMT  
		Size: 11.6 KB (11626 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:26d4f2c56522ea7ca8a330117e7f9494432528454e434b87d3918c83231e17ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277429232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc64990d1edbbaa7bcfb16939d5cae08f9cf6d2970c6dd863a2d09dcd8241e62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:38 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
# Tue, 12 Mar 2024 00:59:38 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420c5b544693e63eaac90034284eef7243457a9a679d1e583cc55dafed1c8bf9`  
		Last Modified: Mon, 01 Apr 2024 22:01:28 GMT  
		Size: 250.8 MB (250846518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a3d96ab8013fcb764254a3679f4dd5f4108b571415128e3ca7b3c8f8d493c203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4963c801a528cbe9ba8553e0af2c5993a827d1bf691b4357e00d091507420fdb`

```dockerfile
```

-	Layers:
	-	`sha256:b9c894fee7248dc0583cb4d373353376ca502b9f3d4aaf97f2fcedd57d580b5e`  
		Last Modified: Mon, 01 Apr 2024 22:01:23 GMT  
		Size: 3.9 MB (3949600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61a737341c5d2a8f46beb7e1cb2f2bcd72ccd316a605b269078c15eb13129c3`  
		Last Modified: Mon, 01 Apr 2024 22:01:22 GMT  
		Size: 11.4 KB (11417 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:d70206b0586e8e64e875ea16ec912e8bd72d21906d2568856ce84d6689174290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327412046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5808e965af077392cd1baf609dcc56a41f121bd3eb9e5ae2fc6accac265d39f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:51 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Tue, 12 Mar 2024 00:45:51 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a3e8d71fd971f61b0388fb2834d9f24df7728ed3bbdc3a823b64ccf8ad2412`  
		Last Modified: Mon, 01 Apr 2024 21:58:19 GMT  
		Size: 297.3 MB (297340930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:b42ec493301ad10133f471ed2fc7a794439d9b3951ba399efd8a158a0b0d4b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4147914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8005aa07b0305f1b50df5f923ef26f447e28d2ed655a4a5ba2f694a56a731c`

```dockerfile
```

-	Layers:
	-	`sha256:0a16db309db453f9938651346d32b0b8e35f96e842c13c0ffa1c396e7454325c`  
		Last Modified: Mon, 01 Apr 2024 21:58:13 GMT  
		Size: 4.1 MB (4136557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:416c38e8719f91a3859a3afb446eef65cbb8954ea7e58d945e61c4a799f15b9d`  
		Last Modified: Mon, 01 Apr 2024 21:58:12 GMT  
		Size: 11.4 KB (11357 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:e47eddf08aa277fd773b469789469b80214dc1c6eb89cc52dbaed2a45572b346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280210792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637c34fb5b92c2203fcb8db1509344b4fad479143f90c59036e639d20e6cf231`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:107da403005e1b6808da193b1f269be14ac31b0bd6d87b7609e9080e75f08eab in / 
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
	-	`sha256:ec8b01fa71b8466600831f50045cfc2951257ac6eee36ce2a0fbe3dbe0098d42`  
		Last Modified: Wed, 10 Apr 2024 01:02:53 GMT  
		Size: 32.4 MB (32413416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f761c683b352d393ff3a70a31f1cdb3309470baef708acaaec1d5f65178a780`  
		Last Modified: Wed, 10 Apr 2024 01:54:11 GMT  
		Size: 247.8 MB (247797376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:d1306fc47b4244d7f9e7943f5aae84fd486ba130d8d39c608767cb956ddf3271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3908b559c177afd6719140b5a2a3541d95e0921cb245764b7a06f080971b6ac3`

```dockerfile
```

-	Layers:
	-	`sha256:a032ac7469111c4a51d7d1e1b0c75b35aa34e3c8b0d8d8e5bd42030f843b8926`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 4.1 MB (4131731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0b157250963b35b33549efb108518a419ccc9f570c228ba225ea203828b0aa6`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 11.6 KB (11597 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:c51654576d219a3c1810ec0f57d020a9a2fae17fa75a23f0d9d8b3744618660f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.8 MB (278761579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdf13a40fa5213e2af5148bc8ba383c6887afb092fe4af03241476a167078cd0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:31:08 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Tue, 12 Mar 2024 00:31:12 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37dc3072fd9cd9fa92e7d1b88a1a366b360bcbffaa4f190fc3ac03c4cd5a818`  
		Last Modified: Mon, 01 Apr 2024 21:53:46 GMT  
		Size: 243.5 MB (243463572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:4c28805af771ded17532d58b5f8e663ecc6f2513a3d94048509e9f3606592e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713d1526554c91ba1f62906da53b3f136f6bd82097283d6f13d71589576ec883`

```dockerfile
```

-	Layers:
	-	`sha256:4bbad0dcb5d31db6ef4f6b52b195d24c5725f4de425b5776723a0c94a2a67df0`  
		Last Modified: Mon, 01 Apr 2024 21:53:36 GMT  
		Size: 4.1 MB (4100758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef88e86936a49014f33c8e5475ac58e3919976975996b989afde2c62f371ff8b`  
		Last Modified: Mon, 01 Apr 2024 21:53:35 GMT  
		Size: 11.4 KB (11385 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-buster`

```console
$ docker pull rust@sha256:bfa022f7f35ee14e7375de549deaddeaf1ae13bedd4ca845fb55c75fa48c37e0
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
$ docker pull rust@sha256:bef060961cbd2174621dbdc808519969112b6fbccb3e2c4c90b67c67ec186450
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245495284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcb8545702f9a0e6721b40aaa469aefcb0622810562883d52ba50ba057c1c5a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
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
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c72519ff7f40e33d03c7d3f47e19dcd8420c4c92434d03570faaff716312528`  
		Last Modified: Wed, 10 Apr 2024 02:56:19 GMT  
		Size: 218.3 MB (218304422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:8dcab7ab30592663a02fd73c824b93ceb27704fd316dfdc4a14a8fd53cadca34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3596661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858fb1eb2641158105afbe01ba8f4c231a8aae4ad85d82a1c25586aafbbc59da`

```dockerfile
```

-	Layers:
	-	`sha256:38f8d81ee6092d2bfbe77b6702062de3b7d23f5bde67d9773915331d261cb7c0`  
		Last Modified: Wed, 10 Apr 2024 02:56:16 GMT  
		Size: 3.6 MB (3585441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bb65268fc77b08bd0a7fa791c3297b3bced6acd88a4bc12a1af05bcf384c5c8`  
		Last Modified: Wed, 10 Apr 2024 02:56:16 GMT  
		Size: 11.2 KB (11220 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:0c22e20adc4dc2f8053478d027b264ce618469bf08d54893fbf2377658558a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.3 MB (264285591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43db9b4246ad7f36b5cf421516f4d76ce05a39acf043747c47239008af2afb83`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:57 GMT
ADD file:87f5e14c74c217f7538860dd43d6b1910663955972cf5270e3d1a8254956878c in / 
# Tue, 12 Mar 2024 00:59:57 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:3f02c84b2c1c85cfdbae8bb78a52226f2b54d86f3eb2466ac3a81fc25ffde9eb`  
		Last Modified: Tue, 12 Mar 2024 01:05:07 GMT  
		Size: 22.8 MB (22795622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f23601052881b5b7693660e13d60ad40a44fa6d28a6eab03e29bc335ef22614`  
		Last Modified: Mon, 01 Apr 2024 21:57:18 GMT  
		Size: 241.5 MB (241489969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:a259de885b15d5261cb5637679bd82b06cc553086bcc617ceabb1cbcd5911283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3403962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975b206faba1555d08aeb3b367f7e8ace57ef82f52c901953177d20e69f34da4`

```dockerfile
```

-	Layers:
	-	`sha256:a7ec9dae53125430f432e43fa64bb1b7617be4f96618022f8b1c9bd56d02e963`  
		Last Modified: Mon, 01 Apr 2024 21:57:13 GMT  
		Size: 3.4 MB (3392947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8fec98a1e9cbf26e1d3fbbe10104c9e731f2418317039f63184e7f4d36d2663`  
		Last Modified: Mon, 01 Apr 2024 21:57:13 GMT  
		Size: 11.0 KB (11015 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:a5684abbc7f54bd9c58a5364b586316c5353fd8542509a6e13113239001c9fab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.8 MB (307812606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5bde5f6654a3312b9f1f9f6ed51f121b8ad4edd013ae962ab6efcdef6ec0ce`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:05 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
# Tue, 12 Mar 2024 00:46:06 GMT
CMD ["bash"]
# Fri, 29 Mar 2024 15:09:47 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.77.1
# Fri, 29 Mar 2024 15:09:47 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f061dca4371eb34330ba3af7c2817b1504f610d9540f399dca1308b85fc26c6`  
		Last Modified: Mon, 01 Apr 2024 21:55:11 GMT  
		Size: 281.8 MB (281842017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:075ab39c9dbaadb406e6e27af9cc64e481f3ac8c6675922e221c65a580e52a94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3585544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b111ed85dfdbef2cf909ba27fa12deebe2a85a1821a0c05d3c9a6f34856e0f`

```dockerfile
```

-	Layers:
	-	`sha256:413744a81638db98004c236d84b70a1ee323b42dd5316eb0c7b8109d75395654`  
		Last Modified: Mon, 01 Apr 2024 21:55:04 GMT  
		Size: 3.6 MB (3574589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c49bb1f862c0df67b88faca306222bd29aa102812117111de44057071d9b1bf2`  
		Last Modified: Mon, 01 Apr 2024 21:55:03 GMT  
		Size: 11.0 KB (10955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; 386

```console
$ docker pull rust@sha256:f16cf382bb643b61546e0716b11c8865933e5ed812ac80169f0c1059d788a546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264864857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c822134f762bf9cdc5c0c15d0d06f50df5c808cbf81120d841f19ee30850f2c1`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Apr 2024 22:06:26 GMT
ADD file:6033d014a0c5c8d87a61d23e20506ec550ea93ef72866e76bfe5a468ceebf619 in / 
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
	-	`sha256:d349bc9800fc6053f91af64b3ce845b5191cc9e0ae2d2001951381ae2d08e46e`  
		Last Modified: Wed, 10 Apr 2024 01:03:40 GMT  
		Size: 27.8 MB (27848331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54caad959c94915ec006deffe9d9bd347eb55d50b70b7ac94922c1784fbdf03`  
		Last Modified: Wed, 10 Apr 2024 01:54:11 GMT  
		Size: 237.0 MB (237016526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:752c286f93a3ae53df42fe4c2153bcdb6523435d242f194aa2925996d9e0251f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c94b966dc0d5d95ee36fe5b571695e3b2992333e109cd314d4b496537982f2c`

```dockerfile
```

-	Layers:
	-	`sha256:f59e8592b975bb56e79e105cf29ff5ee1831a7336624007d7e81a302f3b159d6`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 3.6 MB (3592066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a39c68120f1cbcd3caaed0c37db595248763df96455ec3bccba15f6356f80efe`  
		Last Modified: Wed, 10 Apr 2024 01:54:05 GMT  
		Size: 11.2 KB (11190 bytes)  
		MIME: application/vnd.in-toto+json
