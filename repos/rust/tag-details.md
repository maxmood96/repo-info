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
-	[`rust:1.78`](#rust178)
-	[`rust:1.78-alpine`](#rust178-alpine)
-	[`rust:1.78-alpine3.18`](#rust178-alpine318)
-	[`rust:1.78-alpine3.19`](#rust178-alpine319)
-	[`rust:1.78-bookworm`](#rust178-bookworm)
-	[`rust:1.78-bullseye`](#rust178-bullseye)
-	[`rust:1.78-buster`](#rust178-buster)
-	[`rust:1.78-slim`](#rust178-slim)
-	[`rust:1.78-slim-bookworm`](#rust178-slim-bookworm)
-	[`rust:1.78-slim-bullseye`](#rust178-slim-bullseye)
-	[`rust:1.78-slim-buster`](#rust178-slim-buster)
-	[`rust:1.78.0`](#rust1780)
-	[`rust:1.78.0-alpine`](#rust1780-alpine)
-	[`rust:1.78.0-alpine3.18`](#rust1780-alpine318)
-	[`rust:1.78.0-alpine3.19`](#rust1780-alpine319)
-	[`rust:1.78.0-bookworm`](#rust1780-bookworm)
-	[`rust:1.78.0-bullseye`](#rust1780-bullseye)
-	[`rust:1.78.0-buster`](#rust1780-buster)
-	[`rust:1.78.0-slim`](#rust1780-slim)
-	[`rust:1.78.0-slim-bookworm`](#rust1780-slim-bookworm)
-	[`rust:1.78.0-slim-bullseye`](#rust1780-slim-bullseye)
-	[`rust:1.78.0-slim-buster`](#rust1780-slim-buster)
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
$ docker pull rust@sha256:0dd183faf7bc5b9b8efe81cfd42701a5283577520b185b511e322e5bf52f8fc7
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
$ docker pull rust@sha256:d50e312c75fbd66f5cc7b1ab6d76892529751526629c294f34ca217016fe0425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526535638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d8eec96e0ea00b3ec3c6c2e03ef8a15113d8dd0682170d3757c06a78e73dce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:6b9f9d886ac307c9982286da0ae1d85ad364df502e05f2c5c14c9505f30a4feb`  
		Last Modified: Thu, 02 May 2024 17:53:26 GMT  
		Size: 177.6 MB (177591491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:9d352cd5f6a779bed1be7057ea6557c8de8f96c40e26e555b469d2c2f8405643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15384104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511f0cc56710400a858b2b313a1fb6c554e2ca7debcdcfd5d6ae3ac4870e716f`

```dockerfile
```

-	Layers:
	-	`sha256:f4420d9292d76286420dd7187c5b08b956041f3a4d90ecee23f7d1f91f3638ac`  
		Last Modified: Thu, 02 May 2024 17:53:24 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6daf94a67a74ecaca457f9fc6812857963aae03a4bdf69ffece0604d2d071e2c`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 13.6 KB (13580 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm variant v7

```console
$ docker pull rust@sha256:225556750412cc8f6f468fd8c3bd1176e9b06c90153acb0e045b500c21265bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514307156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d9947ff3490d7e91dbee0aade813ded906312a29924c5226904b76432127e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07170ec327fa1117b5289697e5555f4c3ba76d00200d7c7cc5c143086856f`  
		Last Modified: Wed, 24 Apr 2024 05:03:03 GMT  
		Size: 59.2 MB (59216995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937bd8fccb438207fe0e77a48873de07dbe1fbea251206222298b72dbd2b3d8`  
		Last Modified: Wed, 24 Apr 2024 05:03:45 GMT  
		Size: 175.1 MB (175141109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499a6710f841b95850a0e6c3589a558408d5ecdb1efe2d461015241a86667d9`  
		Last Modified: Thu, 02 May 2024 18:16:14 GMT  
		Size: 212.8 MB (212820090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:a8d872088f3bc18ac36bb4ee06e93eac69f16897387344fcfd238be07505d19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15189426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f357e10dda11cec2f915422dbbb7f4dc9ef73032fc8aa82efe6609b3de03843`

```dockerfile
```

-	Layers:
	-	`sha256:67f172e545903f27510fe2841e22b7f07947e3314640824e648cc35a5e4af23c`  
		Last Modified: Thu, 02 May 2024 18:16:09 GMT  
		Size: 15.2 MB (15176407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becad9a5634f77e5e49e5e8f1bda8454cd92e0059d86c4ae3e43d13bba5c36d9`  
		Last Modified: Thu, 02 May 2024 18:16:08 GMT  
		Size: 13.0 KB (13019 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cb3fe1b45243325da5aaafb59bc75f8541697bfd9acbfedc914c0f132c7949ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.0 MB (586021653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b44c56b25c83977fc9ebfdf243d37b0b15ab1a4fcf0c647f0878847949cf84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476478a1e1450b999421118cb8f193aa62f1816e0cadd988a084385cf0a5696`  
		Last Modified: Wed, 24 Apr 2024 08:42:20 GMT  
		Size: 202.6 MB (202575289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ab2e8f65d41c1e5e2c493944dc3f6ca456b65a5275ac05e12bc31af0b697d`  
		Last Modified: Thu, 02 May 2024 18:26:37 GMT  
		Size: 246.3 MB (246251422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:9562e2467c5e3f2f6ee0ccff2633f57a5ff3cd388a582fca74510f46aba072bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6aaf4016fa5c395bc612fd990fc2d7422e8623e54ebe02b7b2625e179f7920`

```dockerfile
```

-	Layers:
	-	`sha256:1c4d0653a7e064d93a08cf2e3cb73351a07d67c388a1a2590326a06812bff5f3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 15.4 MB (15399046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790e84f88528ef27e0f653b5aeba1fafd203db38ba551366c785a778180828b3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 12.9 KB (12935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; 386

```console
$ docker pull rust@sha256:d1f3c3a8b571383507c4e76f99678f065d5a03aa90eea84693c767e32fc869c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542180953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009dec677b8280c20069beef31c3fbbbc461bc0ab36f0558b2ec40439a5f6079`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:48 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Wed, 24 Apr 2024 03:38:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:29:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:30:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:1614889c1e665cd335548134ca677fb6f9f1910d4ab6488c04424418a97f495a`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 190.6 MB (190599211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:de08ac7a06b5af621f4e0fb99dabf08168a533017d45b6ff2510485f17d0b355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15363096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc533d073cc58cb332d3410a63a6c6f32d775b9febedb13c3c8b78a6d6079a9`

```dockerfile
```

-	Layers:
	-	`sha256:64ac9f5f1c25c9fffc99c099a79689856019c48dfffddbb43b51cba223012a11`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921284eb6647f818f95a3f3db77efe9fa3b4c28d2bf2158f08f1c984fe96fef0`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 13.5 KB (13531 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; ppc64le

```console
$ docker pull rust@sha256:eb08c0b17cc0c417388189ce35bf4fb1f087a9e6ff51c1bfcec9ff410f2a8733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.2 MB (550221275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3bcff95d0b422fd84f7fcd46bf86991ba30fb41078803b6b6f6722b17322d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:20:52 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Wed, 24 Apr 2024 03:20:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:a6e8bb341b139fa8aae0ba05045cf5f0ef66e8260b98cda6950cadf916ed0f41`  
		Last Modified: Thu, 02 May 2024 18:12:45 GMT  
		Size: 187.1 MB (187143091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:7903613b4182abe216e7e36c9ee4ae650fe4a14316160360cdd8f94e459cf946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbc8ff473cd3ae52f9b1427e15706fae4d3d9591a2c8bf3f28b31a19f1a09c4`

```dockerfile
```

-	Layers:
	-	`sha256:6c78d4a4191a65c7af0530480d11f289861eab1ee86584e8133ba9ae8bb2de48`  
		Last Modified: Thu, 02 May 2024 18:12:41 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef473a7f3ff3cbb5e5bff01f89d91164174143787bc52b54999cd47006cd918`  
		Last Modified: Thu, 02 May 2024 18:12:40 GMT  
		Size: 13.0 KB (12979 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1` - linux; s390x

```console
$ docker pull rust@sha256:35a2f27aa7b8300d5a2e4aed602e03edcc950d6dcfbd9d7f8b8a86be19752041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578756361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008c354d831f826547ccd2d2a946c706ca40e6916ef33806ecaa916a21041dd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:42:45 GMT
ADD file:6b0e091009ac95d80973222b4f56557fc521253f20bb18eea1c9da2b61ed5cc2 in / 
# Wed, 24 Apr 2024 03:42:53 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea1cd174fa855055f0cc0296260c9e987dbd4cddfc8655fe48891b91e5af95b7`  
		Last Modified: Wed, 24 Apr 2024 03:48:59 GMT  
		Size: 47.9 MB (47942206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e212650b3684bdd95eb8c4cd55ad81ca7f992455cbcc5c126d1aac521b5399`  
		Last Modified: Wed, 24 Apr 2024 04:23:04 GMT  
		Size: 24.0 MB (24047036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5049d590d068e07d3557ef371a6ccc2fc96ffadeabbf0c1115204536ff84b`  
		Last Modified: Wed, 24 Apr 2024 04:23:21 GMT  
		Size: 63.1 MB (63130514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74409f156b70503c3e2227e45d964aec57dadc484e6492078584c8cad2e0884f`  
		Last Modified: Wed, 24 Apr 2024 04:23:50 GMT  
		Size: 183.2 MB (183208845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0a40d21a23b6b34012eaf7b342b43911c5d236a2f478d1df55a213f5b8247d`  
		Last Modified: Thu, 02 May 2024 18:17:05 GMT  
		Size: 260.4 MB (260427760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1` - unknown; unknown

```console
$ docker pull rust@sha256:70d0ae53ab927ca2824b1543a39761aaa621f8f640351e84e30c9cffcdada927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e4231ef234646dcaa8923b11a5a42334f73cdcc3a2467a2ef8ea47342e8f4`

```dockerfile
```

-	Layers:
	-	`sha256:2d98932b6c77d39b088f5fb17d27824d35fa3db3a89f0dc9677db81f3f0b219b`  
		Last Modified: Thu, 02 May 2024 18:17:02 GMT  
		Size: 15.2 MB (15185203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9bb7ba18a7a3be562faf0170f9215c5065bafb098b5bf71c12feccc9dce19c`  
		Last Modified: Thu, 02 May 2024 18:17:01 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine`

```console
$ docker pull rust@sha256:d4d3f81f3111991353bd7c7fa513ad3725a27027575fd82e24fb7babcd8f26f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine` - linux; amd64

```console
$ docker pull rust@sha256:41bf7d335c39fd25bb73f3183713b1fdcb77f0fc70def6634e40992e66119292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276648359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9be41f0a10e18d4183096b0d91821b4f93cd1eb4e4884a8fd5fdc8b7ee34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c6c611323bdd864b20f293097226e373d0e34b9108e12e65481c955804c26`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 55.3 MB (55346841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245c9984f45dd6d2464604e214a0391a1b399705f140a8b96469f84d6e1f61e`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 217.9 MB (217892789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:8be526e7cb5aa9bc6b6d8c73fb8ee6e81a9c8164a4c5bfa97533ab5bfc0b6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcc214e8f56925c61fb2680fb60504b652116af551962b9d82c4683a88dc59`

```dockerfile
```

-	Layers:
	-	`sha256:f47a0d5a9bacd02cd11840d2f1a2adc07cd5bdb00e97770f9c417e49c8d49f29`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 710.6 KB (710621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232259c5160cb554f445085a6e5765832b7c088ca5c17fa09d0fb5f2a2dda48`  
		Last Modified: Thu, 02 May 2024 17:53:11 GMT  
		Size: 11.8 KB (11794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b7075f2ddfde9ede284e71e74bade0576f8ea97e0f49b2c8a4ead2a101a1cc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282899712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ab7c4bfc7646c65e0a623ab2551468819a7e5047057601317c046321a3c6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1475e7bc8776b6a5d5098e107869ccf04a61b48d632658ab4bf934b5340337c2`  
		Last Modified: Thu, 02 May 2024 18:30:18 GMT  
		Size: 53.0 MB (52995527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3cbfb4539306a5cd558b71b91000e4f05d22445cf79e04281bf881f3bfd22`  
		Last Modified: Thu, 02 May 2024 18:30:21 GMT  
		Size: 226.6 MB (226556470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f02f381f9fa338bae9204fb7e52a19b44779316d227092aa2fb77ea0a62cea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.2 KB (758219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e2876b12a57c6260b8a220b6a82f40ccb6b3f85bced4f5e908a46f1175e9c`

```dockerfile
```

-	Layers:
	-	`sha256:0f5adf947b65a86f48dfa44a9462e156913eca4be72ad307f8b70e63904defcc`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 746.6 KB (746571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd319de530a5221d01b41f952f79922b81a42473dd697d14646929354af7f96c`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 11.6 KB (11648 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.18`

```console
$ docker pull rust@sha256:34f1c35f62e192f39cd0c809982bf90c354f7e5746682a2f4c9e4c43bd516dbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:909cfdd11b0a96aa82d86c96c17cddf3864bca150a6228d18ab6a658e7006d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272829333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787b53dee543c9d07c38258423856c4ce44a7bb0e10dd80b6ce8d3d6be6d688b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d8cca761111b3832e2234b2a7c144570d1ceaa6a6eab4447a39633b2a0c9e6`  
		Last Modified: Thu, 02 May 2024 17:53:03 GMT  
		Size: 51.5 MB (51534006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94392fe86146798eeda301677559c748ac0525075773894cb651ef44b47f89cf`  
		Last Modified: Thu, 02 May 2024 17:53:06 GMT  
		Size: 217.9 MB (217892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:828ea566785e422ca858dcd98738715dc31eb43e85aa4ac91f75e0f3c0d1a46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13ead6d1e1a8601c572bfe57d56165b246d74fecdc009ab88410fe102fdb904`

```dockerfile
```

-	Layers:
	-	`sha256:022a488b72ff619b6be7c5b9d74e5a88f50c0e8179a478751063a2baa139c1ca`  
		Last Modified: Thu, 02 May 2024 17:53:02 GMT  
		Size: 701.9 KB (701890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d53ac36334ec5e522ca13debbc666b6df6ad9bb97c9efa7639b75bec875183c`  
		Last Modified: Thu, 02 May 2024 17:53:02 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ee1d16c1cc031559875424b27cb090136df31c18dd9e97966cf12391b59ba403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (275971039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0325d780023f87c7f06c8d7e4ee3aadb87e82528ad4b2da06a341cc8e42438bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecadc98c87cbba10a8cd3e79aee52d2aa3670ae6272cc2b29b27128e710a536`  
		Last Modified: Thu, 02 May 2024 18:29:15 GMT  
		Size: 46.1 MB (46081224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688cf2745b0216764a0d813aa9bf3d0c02af25fae1ef4c9bfce32c558a0d640f`  
		Last Modified: Thu, 02 May 2024 18:29:18 GMT  
		Size: 226.6 MB (226556454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:a6e2823b379b899207fbbdc6d8f2181cb7668892e2f31ce8f272302781d6a274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.1 KB (752144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa78da9cdd7dc3787e280f8a86f29faba9f60305898cf6d9486dc01fdc2def2`

```dockerfile
```

-	Layers:
	-	`sha256:2508e1ec9f010359afe8d8e516417a297aa32d170c071185c0be86d2c697cb2f`  
		Last Modified: Thu, 02 May 2024 18:29:13 GMT  
		Size: 741.7 KB (741708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af17300661fa62bda831f09a0938360f387b14cb172b980a435cff240801bee8`  
		Last Modified: Thu, 02 May 2024 18:29:13 GMT  
		Size: 10.4 KB (10436 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-alpine3.19`

```console
$ docker pull rust@sha256:d4d3f81f3111991353bd7c7fa513ad3725a27027575fd82e24fb7babcd8f26f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:41bf7d335c39fd25bb73f3183713b1fdcb77f0fc70def6634e40992e66119292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276648359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9be41f0a10e18d4183096b0d91821b4f93cd1eb4e4884a8fd5fdc8b7ee34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c6c611323bdd864b20f293097226e373d0e34b9108e12e65481c955804c26`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 55.3 MB (55346841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245c9984f45dd6d2464604e214a0391a1b399705f140a8b96469f84d6e1f61e`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 217.9 MB (217892789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:8be526e7cb5aa9bc6b6d8c73fb8ee6e81a9c8164a4c5bfa97533ab5bfc0b6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcc214e8f56925c61fb2680fb60504b652116af551962b9d82c4683a88dc59`

```dockerfile
```

-	Layers:
	-	`sha256:f47a0d5a9bacd02cd11840d2f1a2adc07cd5bdb00e97770f9c417e49c8d49f29`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 710.6 KB (710621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232259c5160cb554f445085a6e5765832b7c088ca5c17fa09d0fb5f2a2dda48`  
		Last Modified: Thu, 02 May 2024 17:53:11 GMT  
		Size: 11.8 KB (11794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b7075f2ddfde9ede284e71e74bade0576f8ea97e0f49b2c8a4ead2a101a1cc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282899712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ab7c4bfc7646c65e0a623ab2551468819a7e5047057601317c046321a3c6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1475e7bc8776b6a5d5098e107869ccf04a61b48d632658ab4bf934b5340337c2`  
		Last Modified: Thu, 02 May 2024 18:30:18 GMT  
		Size: 53.0 MB (52995527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3cbfb4539306a5cd558b71b91000e4f05d22445cf79e04281bf881f3bfd22`  
		Last Modified: Thu, 02 May 2024 18:30:21 GMT  
		Size: 226.6 MB (226556470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:f02f381f9fa338bae9204fb7e52a19b44779316d227092aa2fb77ea0a62cea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.2 KB (758219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e2876b12a57c6260b8a220b6a82f40ccb6b3f85bced4f5e908a46f1175e9c`

```dockerfile
```

-	Layers:
	-	`sha256:0f5adf947b65a86f48dfa44a9462e156913eca4be72ad307f8b70e63904defcc`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 746.6 KB (746571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd319de530a5221d01b41f952f79922b81a42473dd697d14646929354af7f96c`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 11.6 KB (11648 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bookworm`

```console
$ docker pull rust@sha256:0dd183faf7bc5b9b8efe81cfd42701a5283577520b185b511e322e5bf52f8fc7
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
$ docker pull rust@sha256:d50e312c75fbd66f5cc7b1ab6d76892529751526629c294f34ca217016fe0425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526535638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d8eec96e0ea00b3ec3c6c2e03ef8a15113d8dd0682170d3757c06a78e73dce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:6b9f9d886ac307c9982286da0ae1d85ad364df502e05f2c5c14c9505f30a4feb`  
		Last Modified: Thu, 02 May 2024 17:53:26 GMT  
		Size: 177.6 MB (177591491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9d352cd5f6a779bed1be7057ea6557c8de8f96c40e26e555b469d2c2f8405643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15384104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511f0cc56710400a858b2b313a1fb6c554e2ca7debcdcfd5d6ae3ac4870e716f`

```dockerfile
```

-	Layers:
	-	`sha256:f4420d9292d76286420dd7187c5b08b956041f3a4d90ecee23f7d1f91f3638ac`  
		Last Modified: Thu, 02 May 2024 17:53:24 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6daf94a67a74ecaca457f9fc6812857963aae03a4bdf69ffece0604d2d071e2c`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 13.6 KB (13580 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:225556750412cc8f6f468fd8c3bd1176e9b06c90153acb0e045b500c21265bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514307156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d9947ff3490d7e91dbee0aade813ded906312a29924c5226904b76432127e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07170ec327fa1117b5289697e5555f4c3ba76d00200d7c7cc5c143086856f`  
		Last Modified: Wed, 24 Apr 2024 05:03:03 GMT  
		Size: 59.2 MB (59216995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937bd8fccb438207fe0e77a48873de07dbe1fbea251206222298b72dbd2b3d8`  
		Last Modified: Wed, 24 Apr 2024 05:03:45 GMT  
		Size: 175.1 MB (175141109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499a6710f841b95850a0e6c3589a558408d5ecdb1efe2d461015241a86667d9`  
		Last Modified: Thu, 02 May 2024 18:16:14 GMT  
		Size: 212.8 MB (212820090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a8d872088f3bc18ac36bb4ee06e93eac69f16897387344fcfd238be07505d19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15189426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f357e10dda11cec2f915422dbbb7f4dc9ef73032fc8aa82efe6609b3de03843`

```dockerfile
```

-	Layers:
	-	`sha256:67f172e545903f27510fe2841e22b7f07947e3314640824e648cc35a5e4af23c`  
		Last Modified: Thu, 02 May 2024 18:16:09 GMT  
		Size: 15.2 MB (15176407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becad9a5634f77e5e49e5e8f1bda8454cd92e0059d86c4ae3e43d13bba5c36d9`  
		Last Modified: Thu, 02 May 2024 18:16:08 GMT  
		Size: 13.0 KB (13019 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cb3fe1b45243325da5aaafb59bc75f8541697bfd9acbfedc914c0f132c7949ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.0 MB (586021653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b44c56b25c83977fc9ebfdf243d37b0b15ab1a4fcf0c647f0878847949cf84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476478a1e1450b999421118cb8f193aa62f1816e0cadd988a084385cf0a5696`  
		Last Modified: Wed, 24 Apr 2024 08:42:20 GMT  
		Size: 202.6 MB (202575289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ab2e8f65d41c1e5e2c493944dc3f6ca456b65a5275ac05e12bc31af0b697d`  
		Last Modified: Thu, 02 May 2024 18:26:37 GMT  
		Size: 246.3 MB (246251422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9562e2467c5e3f2f6ee0ccff2633f57a5ff3cd388a582fca74510f46aba072bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6aaf4016fa5c395bc612fd990fc2d7422e8623e54ebe02b7b2625e179f7920`

```dockerfile
```

-	Layers:
	-	`sha256:1c4d0653a7e064d93a08cf2e3cb73351a07d67c388a1a2590326a06812bff5f3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 15.4 MB (15399046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790e84f88528ef27e0f653b5aeba1fafd203db38ba551366c785a778180828b3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 12.9 KB (12935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d1f3c3a8b571383507c4e76f99678f065d5a03aa90eea84693c767e32fc869c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542180953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009dec677b8280c20069beef31c3fbbbc461bc0ab36f0558b2ec40439a5f6079`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:48 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Wed, 24 Apr 2024 03:38:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:29:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:30:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:1614889c1e665cd335548134ca677fb6f9f1910d4ab6488c04424418a97f495a`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 190.6 MB (190599211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:de08ac7a06b5af621f4e0fb99dabf08168a533017d45b6ff2510485f17d0b355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15363096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc533d073cc58cb332d3410a63a6c6f32d775b9febedb13c3c8b78a6d6079a9`

```dockerfile
```

-	Layers:
	-	`sha256:64ac9f5f1c25c9fffc99c099a79689856019c48dfffddbb43b51cba223012a11`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921284eb6647f818f95a3f3db77efe9fa3b4c28d2bf2158f08f1c984fe96fef0`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 13.5 KB (13531 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:eb08c0b17cc0c417388189ce35bf4fb1f087a9e6ff51c1bfcec9ff410f2a8733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.2 MB (550221275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3bcff95d0b422fd84f7fcd46bf86991ba30fb41078803b6b6f6722b17322d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:20:52 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Wed, 24 Apr 2024 03:20:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:a6e8bb341b139fa8aae0ba05045cf5f0ef66e8260b98cda6950cadf916ed0f41`  
		Last Modified: Thu, 02 May 2024 18:12:45 GMT  
		Size: 187.1 MB (187143091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7903613b4182abe216e7e36c9ee4ae650fe4a14316160360cdd8f94e459cf946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbc8ff473cd3ae52f9b1427e15706fae4d3d9591a2c8bf3f28b31a19f1a09c4`

```dockerfile
```

-	Layers:
	-	`sha256:6c78d4a4191a65c7af0530480d11f289861eab1ee86584e8133ba9ae8bb2de48`  
		Last Modified: Thu, 02 May 2024 18:12:41 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef473a7f3ff3cbb5e5bff01f89d91164174143787bc52b54999cd47006cd918`  
		Last Modified: Thu, 02 May 2024 18:12:40 GMT  
		Size: 13.0 KB (12979 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:35a2f27aa7b8300d5a2e4aed602e03edcc950d6dcfbd9d7f8b8a86be19752041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578756361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008c354d831f826547ccd2d2a946c706ca40e6916ef33806ecaa916a21041dd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:42:45 GMT
ADD file:6b0e091009ac95d80973222b4f56557fc521253f20bb18eea1c9da2b61ed5cc2 in / 
# Wed, 24 Apr 2024 03:42:53 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea1cd174fa855055f0cc0296260c9e987dbd4cddfc8655fe48891b91e5af95b7`  
		Last Modified: Wed, 24 Apr 2024 03:48:59 GMT  
		Size: 47.9 MB (47942206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e212650b3684bdd95eb8c4cd55ad81ca7f992455cbcc5c126d1aac521b5399`  
		Last Modified: Wed, 24 Apr 2024 04:23:04 GMT  
		Size: 24.0 MB (24047036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5049d590d068e07d3557ef371a6ccc2fc96ffadeabbf0c1115204536ff84b`  
		Last Modified: Wed, 24 Apr 2024 04:23:21 GMT  
		Size: 63.1 MB (63130514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74409f156b70503c3e2227e45d964aec57dadc484e6492078584c8cad2e0884f`  
		Last Modified: Wed, 24 Apr 2024 04:23:50 GMT  
		Size: 183.2 MB (183208845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0a40d21a23b6b34012eaf7b342b43911c5d236a2f478d1df55a213f5b8247d`  
		Last Modified: Thu, 02 May 2024 18:17:05 GMT  
		Size: 260.4 MB (260427760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:70d0ae53ab927ca2824b1543a39761aaa621f8f640351e84e30c9cffcdada927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e4231ef234646dcaa8923b11a5a42334f73cdcc3a2467a2ef8ea47342e8f4`

```dockerfile
```

-	Layers:
	-	`sha256:2d98932b6c77d39b088f5fb17d27824d35fa3db3a89f0dc9677db81f3f0b219b`  
		Last Modified: Thu, 02 May 2024 18:17:02 GMT  
		Size: 15.2 MB (15185203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9bb7ba18a7a3be562faf0170f9215c5065bafb098b5bf71c12feccc9dce19c`  
		Last Modified: Thu, 02 May 2024 18:17:01 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-bullseye`

```console
$ docker pull rust@sha256:2552dc030938db6be68061470bb1d06a614e2523bc28aca5ae3db334fe4b3476
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
$ docker pull rust@sha256:e6d6b30cc542e783d7c99f59c4981a1dfc16854065004dd2031731c1f39bde8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.0 MB (500031479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcad364931eede82edf28ce9a8b0d641d449dfc7c66a5409117906b6b6b8b4ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:13:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:534d57e3d7c23ea864729859cd9639d95758dc80d3fae7c2f1a781369374f72c`  
		Last Modified: Thu, 02 May 2024 17:53:19 GMT  
		Size: 177.6 MB (177591486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:394674afd531ba7ba75772c582acf4520d9dfde25713860cf929548250230b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14987362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd227c9c6937e47e8c7124353322fb9c95d173d5e40454385bc62a5de0a4d204`

```dockerfile
```

-	Layers:
	-	`sha256:5175f4542d292457f1a4530967191286a12c21391a2bb9a183579ff56267c300`  
		Last Modified: Thu, 02 May 2024 17:53:17 GMT  
		Size: 15.0 MB (14974944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da52b512eddefa1c1ecbaaa573257018e0b1790c5832c459900ce53606e1b2a`  
		Last Modified: Thu, 02 May 2024 17:53:16 GMT  
		Size: 12.4 KB (12418 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:04d28c769d11d7e8647f2cb4abc12e4772bf7ac447fdc05e7a6713bf8619ec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.8 MB (495758778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021e7713c700cad89a3873cd2bcb165eeda0cba39d5eac5e6c0ceb0433e2015f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:15 GMT
ADD file:59046a1e0987059e779fff5a0f35e03203c109d778a75058e9474705d3fcfdff in / 
# Wed, 24 Apr 2024 04:07:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:51:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:53:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:853e2341066ebc3a07d3c44ebac8c3ce40daf429fb9cc3f49f2d35115e9cc93f`  
		Last Modified: Wed, 24 Apr 2024 04:11:34 GMT  
		Size: 50.3 MB (50255574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d5c1aa98981d0ab503d79e97e4eeed8435372346757065a98c291d66c74df`  
		Last Modified: Wed, 24 Apr 2024 05:03:57 GMT  
		Size: 14.9 MB (14880390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94741efe025699cbcd617a32ea95a4fea8cfaeedfa3b93bd9cbc7ed02063a74a`  
		Last Modified: Wed, 24 Apr 2024 05:04:17 GMT  
		Size: 50.4 MB (50359575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba251a5fa80ede4ef9bfae4161563b58236318c68e2a17d1cbd5afa4ba9a2c68`  
		Last Modified: Wed, 24 Apr 2024 05:04:53 GMT  
		Size: 167.4 MB (167442932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5d2b6834c7a0899f1680cc6d8cc388f1d0dca62c4f7a8ebe01f44f45352ed7`  
		Last Modified: Thu, 02 May 2024 18:12:01 GMT  
		Size: 212.8 MB (212820307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80b041026f0b46d413060fd8525a3ba151a2eacd151071f8c61fc152cdfd39d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14788669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51b3ef7ff5219f52138329d10cb8348d58ffc8198540c1b328f90fbc8a82ea6`

```dockerfile
```

-	Layers:
	-	`sha256:6c813ccd1a4df3a4bbbbe45bfed024331d0fd2c3308c8a3d7d111ea597aafb5f`  
		Last Modified: Thu, 02 May 2024 18:11:56 GMT  
		Size: 14.8 MB (14776844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19847e3e85938bfccef756d696d053d674fb2f4065a928f39c3451d036e26c9d`  
		Last Modified: Thu, 02 May 2024 18:11:55 GMT  
		Size: 11.8 KB (11825 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:82d27aac8d8758af4166b14ffb1cc316fa08b2fd8cfaf238846ba54bc171e9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.4 MB (560350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423aa11d7bda4aed73983759f01bf96699ace117c8ea8c844c414b738c64bcd7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33008ff0928e624ce22cedd5d004edd66b80372bfd1223e8900206330213ee34`  
		Last Modified: Wed, 24 Apr 2024 08:42:31 GMT  
		Size: 15.8 MB (15750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36972983386f768dbeff5de37af34ed4e2f59541b2e3c43575f29758c3591923`  
		Last Modified: Wed, 24 Apr 2024 08:42:45 GMT  
		Size: 54.7 MB (54696233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3224178d7041e10ec03b66358ce4ba6bb5aeaf26b593f3e8672ca38f7b70769e`  
		Last Modified: Wed, 24 Apr 2024 08:43:09 GMT  
		Size: 189.9 MB (189912094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97275dd0257b83d60c67c3d70971c98640014802ea42bae0e7414eaacf4f365b`  
		Last Modified: Thu, 02 May 2024 18:22:28 GMT  
		Size: 246.3 MB (246251467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cb31ecf48d87fa71df2cb5a2933820e8ecbdd1dbb690d4b5aff13d7fbd87755e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14989175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2aef4675fe30517f9f710edbba6c5a198def25e9b99362e323b7e9b30a6d4d`

```dockerfile
```

-	Layers:
	-	`sha256:eb1b6d19dba8c8c9789a080460223469c5e39861aabf0abb48fe6a856f49572f`  
		Last Modified: Thu, 02 May 2024 18:22:23 GMT  
		Size: 15.0 MB (14977411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed5b26cdc4f076066fac6d6878fca32b53fbe9a0c5bf6b5429bb951a8de7223`  
		Last Modified: Thu, 02 May 2024 18:22:22 GMT  
		Size: 11.8 KB (11764 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; 386

```console
$ docker pull rust@sha256:232c18232dd7076711f3603df35b9bfe483c49663e03b9259edbd30810dfc02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518766287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858075fb8a3b54656c0ee7518ef0b22601a2d1b7d4d1f2fd037699198b2bef9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:08 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
# Wed, 24 Apr 2024 03:39:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:30:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:32:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:df053a23eab4180eece3d17162346216b301343de9fb6226cd226f21702be82f`  
		Last Modified: Thu, 02 May 2024 17:53:36 GMT  
		Size: 190.6 MB (190599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cf1fa86ecf03dd1fbb4dcce34d4a6d575a64d018570476a025626d21108bf3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14976156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0056775c2d4a3ef6fbace0e34ff6db97f0f12ad062f8875c69193a8f497145ad`

```dockerfile
```

-	Layers:
	-	`sha256:189cacbc159513dae1c96778228fcacb8fa5341832b01271f051b1124b140d81`  
		Last Modified: Thu, 02 May 2024 17:53:30 GMT  
		Size: 15.0 MB (14963767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86ac21aeb5f940ce0d749c02477c27d23e1023a107afeb492eedaa85b35f6e8`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 12.4 KB (12389 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:74f6d27411b0fe1655b74893221edde39cc79b5c54f779b8f924d0f94e5b6ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.1 MB (518096210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655131ce8b88722fe88822b0323c0f901ee374ed6e1eb86f90e53c8a0f1031de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:25 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
# Wed, 24 Apr 2024 03:21:30 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:04:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:f315af7fc149bdbb645add44aaef365e14662b9bf33a24ebcdeda2ed49bcef6f`  
		Last Modified: Thu, 02 May 2024 18:07:04 GMT  
		Size: 187.1 MB (187143092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:02041686275df55e6c1cde2ab50a36777b23e5f0bfa0620bcea85ce288d8403d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14954340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c14dc83c058acbfa6bd18b2ba83506e0f719407a324008942f86a2d4dcc87af`

```dockerfile
```

-	Layers:
	-	`sha256:ce1abb7d3006b3e51d88e3b055b4055bbc25212003172c9a9aa9532a8425ad91`  
		Last Modified: Thu, 02 May 2024 18:06:59 GMT  
		Size: 14.9 MB (14942547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c168268955e9148deab9bdffcc4c0a75e9a8cea798c2286a9aab8cdf5599398f`  
		Last Modified: Thu, 02 May 2024 18:06:58 GMT  
		Size: 11.8 KB (11793 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:e3c00ec457a002c90f44ff20936bcfee6bd86f03ab1cc7750785060a7895e5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.5 MB (556478959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3364960915922de42d06974605b4e00f6fc171fd9a6475446ac1f876a6543c0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:33 GMT
ADD file:e0a1fc1de1477cea6fe41bdd15378013c680928cad3988dd16926cc1562c775e in / 
# Wed, 24 Apr 2024 03:43:38 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b57a10abb081ff40e5bb34246c3875a71b8d258f767c4f8384d7054b1bc42725`  
		Last Modified: Wed, 24 Apr 2024 03:49:31 GMT  
		Size: 53.3 MB (53337419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ed92794c4710c20ea615a0e07fe947837768482be7bcd9d1fccb335072a92`  
		Last Modified: Wed, 24 Apr 2024 04:24:03 GMT  
		Size: 15.6 MB (15642846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0318d2197701d71929fa882d8d64bdc0c65ee6bc9abd4bd4063694d92acb7`  
		Last Modified: Wed, 24 Apr 2024 04:24:17 GMT  
		Size: 54.1 MB (54076626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c3f9b4c72abaa52996d64ffc8754f8500b075a8a677c0fe59c310548e9af5c`  
		Last Modified: Wed, 24 Apr 2024 04:24:43 GMT  
		Size: 173.0 MB (172994116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66302c05a1f58a25604176a4b9b6bc0e717fb72ff97e0334ea79fb2895e26df7`  
		Last Modified: Thu, 02 May 2024 18:08:54 GMT  
		Size: 260.4 MB (260427952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:52b39a86a4ea99cb0237d970a10213cddfe8f113046bf4abdd5d3e4a3cda1363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14808368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bec0dfd4f38a0e9dad4996be6db3bacd06333698fa0cae356936fc13be9fd4`

```dockerfile
```

-	Layers:
	-	`sha256:83ce677ca56d4a667f9518ab5babc3e5b9ad1f44c3a5dbd0ff5ba123690f4055`  
		Last Modified: Thu, 02 May 2024 18:08:50 GMT  
		Size: 14.8 MB (14796613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f959e24eefab058ecc036f364b2858652b6977cafed184475b485ec952b32bc`  
		Last Modified: Thu, 02 May 2024 18:08:50 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-buster`

```console
$ docker pull rust@sha256:fcb09007a565e6705c6d49835377d7d18e050b309203edc9e412977e91269257
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

### `rust:1-buster` - unknown; unknown

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

### `rust:1-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:47eacf3b5d2efd391224926939f061ff7acd7574beacdbcf721c82b01a65715e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 MB (490711222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bef0c9fda88c0ce49bbbe4e82e4c8d2496752121e8e07c5f59170f61ca0d31d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:33 GMT
ADD file:eea1eb05334cd4d0032909b2c56fc86a54faad563cbc3d2d46e763ce9e8922ab in / 
# Wed, 24 Apr 2024 04:07:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:53:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:54:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:55:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
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
	-	`sha256:fe0f6a4b48afbd61f9ef055b862b89cc5fc3980c4be6d4ccdc4e71eb6bd56d0d`  
		Last Modified: Thu, 02 May 2024 18:07:53 GMT  
		Size: 212.8 MB (212820147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:752d344513be8e413c08339a72a1696e061067a176479b706f0ae0a0c25048f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15780088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c18d957fb0511cfe9d344a4de14bcc9b40ee6d3bfbc1d980e180ae8df9d7aea`

```dockerfile
```

-	Layers:
	-	`sha256:da347c4aa030e17d6c56379e77bbdc5e28dab4fed5f89adbf67d26f052266c5f`  
		Last Modified: Thu, 02 May 2024 18:07:47 GMT  
		Size: 15.8 MB (15769023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52097463634c6c7d47e034b943ee50d0b5c9c9b3d2a8be616e9ebc076bb95f37`  
		Last Modified: Thu, 02 May 2024 18:07:46 GMT  
		Size: 11.1 KB (11065 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:775daa3419885651f2e284f10b29385f68347c1b99caf12ee7dbf82edc24947f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548916487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5233d262b43ce5dd1ff865b0ee9ac12ae4be5844a39f716b3cd8396774e15b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:00 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
# Wed, 24 Apr 2024 04:11:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:36:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
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
	-	`sha256:af5cdf87e38274705e7b47b4d3a5ccbab3f4bf94894cac0c5b2d82abfcf1989e`  
		Last Modified: Thu, 02 May 2024 18:19:24 GMT  
		Size: 246.3 MB (246251497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-buster` - unknown; unknown

```console
$ docker pull rust@sha256:dac6fc781e375c3f98871b1045ea01bd75fc62f126ba52697ba0c6b38a1f4aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15969386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2c1d63305c600acd748d5093b508df829037b295ab55b92bcc3998cf8ce8aa`

```dockerfile
```

-	Layers:
	-	`sha256:65b7feb61540a8b5987675be790620a8a6a102d1c29faafbb53fc91011a7161d`  
		Last Modified: Thu, 02 May 2024 18:19:19 GMT  
		Size: 16.0 MB (15957718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccd3a895875d4cbfb484b9fb55f5e778d710cf340062cd3a9484aadb5c29130`  
		Last Modified: Thu, 02 May 2024 18:19:19 GMT  
		Size: 11.7 KB (11668 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-buster` - linux; 386

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

### `rust:1-buster` - unknown; unknown

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

## `rust:1-slim`

```console
$ docker pull rust@sha256:517c6272b328bc51c87e099ef4adfbc7ab4558af2d757e8d423c7c3f1cbbf9d5
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
$ docker pull rust@sha256:144edf7af2e5e374afdee02fd458df5bad41aba4cae314ace9d43f7933d44c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277315532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036d20da216ad2e94545e4e82700ee8c8ee3ad79fa0e2dca1261f8a69a87a937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8f9fca3e1073639d97fde71b99e2ef803078e36ed1cd97b74ce545ee7b17`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 248.2 MB (248165053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a10481a084e247a58cb63c17b394d4e65463e3c8369e21bcfc769abbdfffb9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911a63093a97a45bdf3e678240c96fe3b7f81befc1871a5542db741b9b51a7d`

```dockerfile
```

-	Layers:
	-	`sha256:371755c5d7b19c0c727d6c961f8c6528bc0cbd0b3d2c7067a40ddd1f9eaa4e74`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6556d0382c9b778b94f7cc91b1d3f7659518e567fab6462da86ebe4ac90c6382`  
		Last Modified: Thu, 02 May 2024 17:53:22 GMT  
		Size: 13.2 KB (13172 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:ffc8f22bbcaf9c443db0c997aba6a8f0773d989e29a5865d0f164a36f15e8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285223017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d69dbc41e535f1c4657a7b35fe40a346dce9c4f07b392370b716e1c4ea8c45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f060f4605d55cb88006aa78ea1433f0129af80557306aa6ef11d728ad8c15`  
		Last Modified: Thu, 02 May 2024 18:18:12 GMT  
		Size: 260.5 MB (260482575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8ee1faa28bc0f8ec0e92ba67f71be26d4570984f23660ad77c52f9cdaf0e4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14586c5fd8ae352e99facffdc8e47f2ffe4a171ae426fa7163a3033099714f4d`

```dockerfile
```

-	Layers:
	-	`sha256:f920b7810ae2eb89611842b3c8d00f4e763ddaa0dbb6dc67bc77bc0979211af2`  
		Last Modified: Thu, 02 May 2024 18:18:06 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6070f226a82471804b25ddfcd5994dfb20c75710288cb8fa305eeecbc9689a`  
		Last Modified: Thu, 02 May 2024 18:18:05 GMT  
		Size: 13.1 KB (13107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:701d523927f60aa6594b6b639e16b2872b090efd77b38206eb07f8a5ab5f4b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341067862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d7c8b33fff18a1de7a58bd9764df34dcb7689471c8332703ef166a3be91dbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b6ff75fe73e0b624033411b211e30ab65a0dfe2f196bc831afaa3f262ad40`  
		Last Modified: Thu, 02 May 2024 18:28:13 GMT  
		Size: 311.9 MB (311887927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3068c80cfcc050b7d2f84d2daa26eb1bb6646dbef2cdc889b4706d0ecec10c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94192de4d427019b53f8d6f476258f84f6c701b7cc313fbe20aac8356c685388`

```dockerfile
```

-	Layers:
	-	`sha256:fe0470bf526cfabeeff81d8175f1ad542787eb63d46eac59584aa0c9700cb865`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 3.9 MB (3941462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e741b4e2feaf42a20f56bbcccb528e05e69b28f20a30f471dab96b02dd26885d`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 13.0 KB (13023 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; 386

```console
$ docker pull rust@sha256:9a0ff69ac63b29617f2772d8af475f42b17376ae675690bd4b6ffbd6fa013a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288155332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730521317992ca457b5e32b681e5c2fc6a9985f74b26c05ab75a898d70063efd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be463c23e962e7814d7269dd918a3abf7fe7480f3491260b6939bc093b40232`  
		Last Modified: Thu, 02 May 2024 17:53:34 GMT  
		Size: 258.0 MB (257992149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:406577ad4a920a84505e527616fcb1f008cff2e259737b980109d6586c441132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94959a9ba35ac8e7aa52d2c9634583789f540a6ce1cdf8970c1aeafbeb383266`

```dockerfile
```

-	Layers:
	-	`sha256:5fccb080d41ea034eca85abe7287cd6513b3fcf1304c5b0ab744b5e4f7604ee2`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5ee26d72cca7cd34f6faa2688b32a264613f3b88beb239a82737e7a7bdd0b8`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:ea7984b98ee3317d77412b9077362d5f7934cbed7f5d5ce18a977f899e9386c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288845524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a166a0772dcf6517a472407901b610b01b80c50d7487fd756971dc08ca26d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bdd5b65845940ee92c4225121c6b04def8a421d1c550f7d8d65db0e37bf19`  
		Last Modified: Thu, 02 May 2024 18:15:05 GMT  
		Size: 255.7 MB (255704323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b8cf1c2e22630a3fb96504ce4e0109e450e2f91f2338965264da180dffb4be0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e443bda8941eefcf331e18425d4d04513900c67b623379aae5f5c3ba60799f`

```dockerfile
```

-	Layers:
	-	`sha256:57c7d4ef78d8836d083ed51f7584a8611e874b74c989c77cbdaefba43cf9c737`  
		Last Modified: Thu, 02 May 2024 18:14:59 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721e6450ded9a8224165692a227cf32021b20727fa9e27b7eb51b9ee46c98d64`  
		Last Modified: Thu, 02 May 2024 18:14:58 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim` - linux; s390x

```console
$ docker pull rust@sha256:f2f85fb1ee50bb9ddd8312a215bd06ef84d9d8a32ae978df573ac5b9b84ab38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337865924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2db01fe12c831f8b1c810ff63f0059a28b15cebb3fc607f041e7f43ba47394a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c36f802355139032b4b3b2815d90b8684055c93beadd105d203de5c4574421`  
		Last Modified: Thu, 02 May 2024 18:19:38 GMT  
		Size: 310.4 MB (310353569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1d010d6d80dc73fcb8b111939211fe047c868a66965107fe6522c5ac238f2882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67848fc2610daa3a0488587b7d72d3197b8f69b13b8bc20914dec3e53cac68c4`

```dockerfile
```

-	Layers:
	-	`sha256:45465cb45a531518db8458bf81a4591118d814a4fcc27d32e893ed00128240f1`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 3.8 MB (3762075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ba7b0835f73f3eba7b3413925b87bc83556d2ccd55606dfd68c5715cec19c7b`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bookworm`

```console
$ docker pull rust@sha256:517c6272b328bc51c87e099ef4adfbc7ab4558af2d757e8d423c7c3f1cbbf9d5
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
$ docker pull rust@sha256:144edf7af2e5e374afdee02fd458df5bad41aba4cae314ace9d43f7933d44c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277315532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036d20da216ad2e94545e4e82700ee8c8ee3ad79fa0e2dca1261f8a69a87a937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8f9fca3e1073639d97fde71b99e2ef803078e36ed1cd97b74ce545ee7b17`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 248.2 MB (248165053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a10481a084e247a58cb63c17b394d4e65463e3c8369e21bcfc769abbdfffb9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911a63093a97a45bdf3e678240c96fe3b7f81befc1871a5542db741b9b51a7d`

```dockerfile
```

-	Layers:
	-	`sha256:371755c5d7b19c0c727d6c961f8c6528bc0cbd0b3d2c7067a40ddd1f9eaa4e74`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6556d0382c9b778b94f7cc91b1d3f7659518e567fab6462da86ebe4ac90c6382`  
		Last Modified: Thu, 02 May 2024 17:53:22 GMT  
		Size: 13.2 KB (13172 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ffc8f22bbcaf9c443db0c997aba6a8f0773d989e29a5865d0f164a36f15e8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285223017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d69dbc41e535f1c4657a7b35fe40a346dce9c4f07b392370b716e1c4ea8c45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f060f4605d55cb88006aa78ea1433f0129af80557306aa6ef11d728ad8c15`  
		Last Modified: Thu, 02 May 2024 18:18:12 GMT  
		Size: 260.5 MB (260482575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ee1faa28bc0f8ec0e92ba67f71be26d4570984f23660ad77c52f9cdaf0e4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14586c5fd8ae352e99facffdc8e47f2ffe4a171ae426fa7163a3033099714f4d`

```dockerfile
```

-	Layers:
	-	`sha256:f920b7810ae2eb89611842b3c8d00f4e763ddaa0dbb6dc67bc77bc0979211af2`  
		Last Modified: Thu, 02 May 2024 18:18:06 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6070f226a82471804b25ddfcd5994dfb20c75710288cb8fa305eeecbc9689a`  
		Last Modified: Thu, 02 May 2024 18:18:05 GMT  
		Size: 13.1 KB (13107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:701d523927f60aa6594b6b639e16b2872b090efd77b38206eb07f8a5ab5f4b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341067862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d7c8b33fff18a1de7a58bd9764df34dcb7689471c8332703ef166a3be91dbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b6ff75fe73e0b624033411b211e30ab65a0dfe2f196bc831afaa3f262ad40`  
		Last Modified: Thu, 02 May 2024 18:28:13 GMT  
		Size: 311.9 MB (311887927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3068c80cfcc050b7d2f84d2daa26eb1bb6646dbef2cdc889b4706d0ecec10c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94192de4d427019b53f8d6f476258f84f6c701b7cc313fbe20aac8356c685388`

```dockerfile
```

-	Layers:
	-	`sha256:fe0470bf526cfabeeff81d8175f1ad542787eb63d46eac59584aa0c9700cb865`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 3.9 MB (3941462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e741b4e2feaf42a20f56bbcccb528e05e69b28f20a30f471dab96b02dd26885d`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 13.0 KB (13023 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:9a0ff69ac63b29617f2772d8af475f42b17376ae675690bd4b6ffbd6fa013a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288155332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730521317992ca457b5e32b681e5c2fc6a9985f74b26c05ab75a898d70063efd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be463c23e962e7814d7269dd918a3abf7fe7480f3491260b6939bc093b40232`  
		Last Modified: Thu, 02 May 2024 17:53:34 GMT  
		Size: 258.0 MB (257992149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:406577ad4a920a84505e527616fcb1f008cff2e259737b980109d6586c441132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94959a9ba35ac8e7aa52d2c9634583789f540a6ce1cdf8970c1aeafbeb383266`

```dockerfile
```

-	Layers:
	-	`sha256:5fccb080d41ea034eca85abe7287cd6513b3fcf1304c5b0ab744b5e4f7604ee2`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5ee26d72cca7cd34f6faa2688b32a264613f3b88beb239a82737e7a7bdd0b8`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:ea7984b98ee3317d77412b9077362d5f7934cbed7f5d5ce18a977f899e9386c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288845524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a166a0772dcf6517a472407901b610b01b80c50d7487fd756971dc08ca26d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bdd5b65845940ee92c4225121c6b04def8a421d1c550f7d8d65db0e37bf19`  
		Last Modified: Thu, 02 May 2024 18:15:05 GMT  
		Size: 255.7 MB (255704323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b8cf1c2e22630a3fb96504ce4e0109e450e2f91f2338965264da180dffb4be0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e443bda8941eefcf331e18425d4d04513900c67b623379aae5f5c3ba60799f`

```dockerfile
```

-	Layers:
	-	`sha256:57c7d4ef78d8836d083ed51f7584a8611e874b74c989c77cbdaefba43cf9c737`  
		Last Modified: Thu, 02 May 2024 18:14:59 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721e6450ded9a8224165692a227cf32021b20727fa9e27b7eb51b9ee46c98d64`  
		Last Modified: Thu, 02 May 2024 18:14:58 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:f2f85fb1ee50bb9ddd8312a215bd06ef84d9d8a32ae978df573ac5b9b84ab38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337865924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2db01fe12c831f8b1c810ff63f0059a28b15cebb3fc607f041e7f43ba47394a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c36f802355139032b4b3b2815d90b8684055c93beadd105d203de5c4574421`  
		Last Modified: Thu, 02 May 2024 18:19:38 GMT  
		Size: 310.4 MB (310353569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1d010d6d80dc73fcb8b111939211fe047c868a66965107fe6522c5ac238f2882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67848fc2610daa3a0488587b7d72d3197b8f69b13b8bc20914dec3e53cac68c4`

```dockerfile
```

-	Layers:
	-	`sha256:45465cb45a531518db8458bf81a4591118d814a4fcc27d32e893ed00128240f1`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 3.8 MB (3762075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ba7b0835f73f3eba7b3413925b87bc83556d2ccd55606dfd68c5715cec19c7b`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-bullseye`

```console
$ docker pull rust@sha256:33baf245a3be288ec45d6534ebf94de088b834ef9202fd8e1176a3c1a0d9b730
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
$ docker pull rust@sha256:ebd24f6078bcc9f6b23f99a23e450f07d593f570d4bf072b5077added128bf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268954860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0502ee249ca6bfa22cfade789d5296feac6f0928a18703146f522c7cbf7ced10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e70c0d176523de333ba6a5be57344d80ccfba2589ed97a0714e502d2a34ca43`  
		Last Modified: Thu, 02 May 2024 17:53:20 GMT  
		Size: 237.5 MB (237520597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a4dcfa88f53f7b2928efe6b3b835f897d81e20fddd853c43354998e2e042cabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ef9d771e215a52ef1e40b292ede0d829c632e49e4c2367b41dac17ea648ac2`

```dockerfile
```

-	Layers:
	-	`sha256:cef011c9722bb44d4620b4e6bf096623230158399e11cb7d6d6f6c1a1af4bd58`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 4.1 MB (4139833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599c91eec4cbd0f1ff1398eba0b589af02754a51f58dcd99213c8a7b227dac30`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 12.0 KB (11983 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b2d51c493ce70a6df64cc9294f39b991ed51caad0d1b6b4df3aa73ebc0059308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281482631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1845601085edf0de75fa06cb3587d42cc4e40938d1b8a5f3ee758b9356526b5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb88c27c011a0bf4095b4dad73f3b89a8b7d5926dd1b563ef8b60cc2f6c06c3`  
		Last Modified: Thu, 02 May 2024 18:13:56 GMT  
		Size: 254.9 MB (254887889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ede45ee3c4bebfd74b4c54b87023ff6f1af70c483ef9065a07b00b14ba55e7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb61ef780ac05b5018cad0ca9872b446a694f9a1b4446f0d1738749ea277525`

```dockerfile
```

-	Layers:
	-	`sha256:f821ed482f1443a1e918b75b417cb399f4cdb75370c37d86cca0be80d3b3b835`  
		Last Modified: Thu, 02 May 2024 18:13:50 GMT  
		Size: 3.9 MB (3949756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e6fac619e4f33ae52bdc1063f1d01d4404064b385b8d19745a745c85900723`  
		Last Modified: Thu, 02 May 2024 18:13:50 GMT  
		Size: 11.9 KB (11887 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:55184f8e235a387dc47570d3c45c18868da64c7441759ff319bb02b00a30dd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331830874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2efb3db0f1f86b252af2ac6422352121d26077fc46501dc669c95b75f8b7e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a148bfdb5477b5b28e8af64d0d2c9d4cd738688d1ec0104833fc0685436c0c3`  
		Last Modified: Thu, 02 May 2024 18:23:57 GMT  
		Size: 301.7 MB (301743538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:47addcc74cfa8ab7f351d70c100db444ad71814d83f6c96928b852f42598e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0390a7297d4caf490960ab4c3265747cbbd92e4748bed00b3c994f72c02f2`

```dockerfile
```

-	Layers:
	-	`sha256:0508b7e94192ab544e987c54492b371e546f31d0f9919bc0c8cc1c452aa454c4`  
		Last Modified: Thu, 02 May 2024 18:23:49 GMT  
		Size: 4.1 MB (4136713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dccf37e519bcea3696ecfb195e4a0b38348a412004399eb8308b338effdba8b`  
		Last Modified: Thu, 02 May 2024 18:23:48 GMT  
		Size: 11.8 KB (11827 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b189e96e3c85ca97178eb44feb77efb715773ecfe115c08226820247f7cd4371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283597724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d042e33fb45d8dbb5ab9375e1f445cca9f0842403742ac8e16e14a492d1379b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:20 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Wed, 24 Apr 2024 03:39:20 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d994d194bfa3acf9a46df705316048a9e421612eb43dc8e67d2fc7c4b47dc8cd`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 251.2 MB (251172951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:23c07842a4cfddec1e1f1e230639073243847f2eb36626a93f578ed729e42f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9ef9f2ac9c96e93217e0d144744e8d8278050716ca0834c70afa220c7c8939`

```dockerfile
```

-	Layers:
	-	`sha256:80add452afc9acafbae3ebdaf81b51e772270d4168261abc531caa3d40d6f8f2`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 4.1 MB (4131887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9032987821a421011b12f5c932db84722ec77469e7d51d50c7f52fc9d678ac72`  
		Last Modified: Thu, 02 May 2024 17:53:17 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:f231b14bfd93102c404e608edce59336c32bbf5bc5b16dde3b83c3b3058aa530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277263350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6022c77c11237120364d8daebc5e4a7f79b239f345aadfe10e08162f3991d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a8be3c69cc41100693d385b45a719b06420c1a8633ddefd2cd065116e4a80f`  
		Last Modified: Thu, 02 May 2024 18:10:20 GMT  
		Size: 242.0 MB (241951625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1bb874168defcf306f4d12a18fa1d1a431164a64175ab74ccc234d19145dafe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf50d0079f8c3085c91f49970a4c034af187ead7b500a47212bad01b95a54c4`

```dockerfile
```

-	Layers:
	-	`sha256:c87e1c0879f136a39e78ff54f5cea16d36b7126d98ada10edad69ab8afe45793`  
		Last Modified: Thu, 02 May 2024 18:10:13 GMT  
		Size: 4.1 MB (4100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee003b3c784435c5aab66ccdc806e9767a27f9edd3cef32418dbc7142a51ac6`  
		Last Modified: Thu, 02 May 2024 18:10:13 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:a4b95ec70b2c183bd9cd02364c93389c429f8ff07d8a86c91e8830923039acc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332291021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08e265a0280e57d06e189c5f7c3e1e12b10bb2d5eb9c7e0f2004ac291a514f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:03 GMT
ADD file:acaea4e054f1ab7ae5cbc8f02c73b546c367aebfcc48c7fb4f0dd9f3628bc25e in / 
# Wed, 24 Apr 2024 03:44:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6f588995519e0e04ef4c150b91ad96c3c85667869db0ad72e5a78d4fab796e70`  
		Last Modified: Wed, 24 Apr 2024 03:49:47 GMT  
		Size: 29.7 MB (29673934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784d1c6d27c0fa82885a8be868f2c1ed573b39823970c4d06846ef9b4058af1e`  
		Last Modified: Thu, 02 May 2024 18:12:25 GMT  
		Size: 302.6 MB (302617087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ee3b2c41de9bf97e7b05b8905fb5d0e70b4d8b48dcdbd11a87197a0e8af288de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fa73fb55843e1fc73565ef3eb0db89dd88c65c76748308419e9a61dddb5569`

```dockerfile
```

-	Layers:
	-	`sha256:8de35856b398f950ff03181d5960ac2487203d9e917fd71ab33559d927b58a50`  
		Last Modified: Thu, 02 May 2024 18:12:20 GMT  
		Size: 4.0 MB (3972037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad823fcf4f244656c879ab7e131ca3a63d49fb60f964019942d1d0722a7aef41`  
		Last Modified: Thu, 02 May 2024 18:12:19 GMT  
		Size: 11.8 KB (11817 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1-slim-buster`

```console
$ docker pull rust@sha256:d30c7ad62c2044e0d1174d742f0efbc02c1e43aea988193b6686ee8aaaf79170
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
$ docker pull rust@sha256:562d6f211888cbd784790e7fb47d3cea4b20480634543579297832b7fd1c25a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250335520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6261cf21c8a87571e9f4b502375b16f30e624d67d46e199388cdf0bc36235`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906e6ed35d183754f56330a654a033329ee5826a5608612dde75a12c80dfbda`  
		Last Modified: Thu, 02 May 2024 17:53:08 GMT  
		Size: 223.0 MB (222997945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e7b9c6cdb9dc891a721e37b31279d12f59a2aeaa33d3a50cd04c15ed9fdac0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a326d7714ebb85020a2b5bc3eb2f017a246b9349e259e29adf9cf787cd097`

```dockerfile
```

-	Layers:
	-	`sha256:3d7cefbfd3006121cdf982e776f479a01d0119707b7d9103dd24cdb58f580975`  
		Last Modified: Thu, 02 May 2024 17:53:05 GMT  
		Size: 3.9 MB (3941693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca2968425f2c6d21765305834771a5c51369246bdfafc5ca52300a944a9f50d`  
		Last Modified: Thu, 02 May 2024 17:53:05 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:94dda1ea419d69d0e38543407f33117c87a59c53c8e45b2fa3729496d76462c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268702412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb522a78fe20e96dd37a3094bd8201f8bc75d59d78c8672653761f8389e82b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab99a29678006ca048ee3cec2a39dd336045cbef1f173b20313118c42dcc53f3`  
		Last Modified: Thu, 02 May 2024 18:09:45 GMT  
		Size: 245.8 MB (245757348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:870cd6eb7305f07b9e0a9384fb585ac261058d1821c291dae7d3e76c80bb744a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4231130c9d88f75df6ed09cac4d31aa678269b42aa3df4dabb3e9675ce564037`

```dockerfile
```

-	Layers:
	-	`sha256:2dc32a76ad84dbf82ef236a5ee11a01cd7c24687433eb86f7be3f1cfa7568a9b`  
		Last Modified: Thu, 02 May 2024 18:09:40 GMT  
		Size: 3.7 MB (3749343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cd37df8a47dfdf9952876a899f07158606f3fe042c2c85d5825fd83d506bf7`  
		Last Modified: Thu, 02 May 2024 18:09:39 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:489aac5b79003a727f4571932d0a03b2aa17db922cca485942fe79de33c5cb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312574944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fc5383529ef82de9ea2eb11d095ad1d1f517c836bc95f1ecc709194a04799d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:06 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
# Wed, 24 Apr 2024 04:11:07 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62497221c4fce50e070a112fde5ee41270ed6a3a085e7b1825fd24a956f1f4c7`  
		Last Modified: Thu, 02 May 2024 18:20:54 GMT  
		Size: 286.5 MB (286465114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:612bde9c6fe77167e879e6f3787a339655d4b7a1cbfa4ce1d3731711d4aa5508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6441cb64ca635d2e44dba773323ae3d87e7f6d0d4f4aee982365fa0652812d06`

```dockerfile
```

-	Layers:
	-	`sha256:e2fb474d4ff49f24441eccc92c2f1c16d30efe46b4c082a210ed49e145d5e5ee`  
		Last Modified: Thu, 02 May 2024 18:20:47 GMT  
		Size: 3.9 MB (3930985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80129d72be4749680a0777a4fb88afb3ad6bfae867c9ae93c316ad94e7112176`  
		Last Modified: Thu, 02 May 2024 18:20:47 GMT  
		Size: 11.2 KB (11234 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:862f761b55bdfb9b687ccd73c39ea5db75ab570112ac0d7d9da5f5c5196dc67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268610066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12d3e0efa5e20f2dffb6cca638c9d030e51183e0ed6dea06200bb6fa61abb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:39 GMT
ADD file:32f0f06baa0e4f10bff55aaa215b511838432ecc5fe547373d9ac99494556801 in / 
# Wed, 24 Apr 2024 03:39:40 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:204b51fc41806ed93b4ccb6ce8272fa49b5f0b099ba6e3b5a940a9e7cd3ce202`  
		Last Modified: Wed, 24 Apr 2024 03:45:03 GMT  
		Size: 28.0 MB (27994678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3981a552b28468ee69108184598097965a5265b74ad064e8e657f3897f599f3`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 240.6 MB (240615388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:4a7ce102abb3a846743437756ea063f781583ab5bea6f40c2612550634e10222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb6026b631db1e909e1f420b7086445db95e1f00ef7bc7c365ad507c9a54fdb`

```dockerfile
```

-	Layers:
	-	`sha256:2e03fc3bfe125dba62e18faebb42c04d798624900a87a5dc953c3be75072510d`  
		Last Modified: Thu, 02 May 2024 17:53:10 GMT  
		Size: 3.9 MB (3948318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e394e2a792e8d275adc332b5b935d4c9db65a83fe54fda94e7437645d5b02114`  
		Last Modified: Thu, 02 May 2024 17:53:10 GMT  
		Size: 11.2 KB (11195 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78`

```console
$ docker pull rust@sha256:0dd183faf7bc5b9b8efe81cfd42701a5283577520b185b511e322e5bf52f8fc7
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

### `rust:1.78` - linux; amd64

```console
$ docker pull rust@sha256:d50e312c75fbd66f5cc7b1ab6d76892529751526629c294f34ca217016fe0425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526535638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d8eec96e0ea00b3ec3c6c2e03ef8a15113d8dd0682170d3757c06a78e73dce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:6b9f9d886ac307c9982286da0ae1d85ad364df502e05f2c5c14c9505f30a4feb`  
		Last Modified: Thu, 02 May 2024 17:53:26 GMT  
		Size: 177.6 MB (177591491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78` - unknown; unknown

```console
$ docker pull rust@sha256:9d352cd5f6a779bed1be7057ea6557c8de8f96c40e26e555b469d2c2f8405643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15384104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511f0cc56710400a858b2b313a1fb6c554e2ca7debcdcfd5d6ae3ac4870e716f`

```dockerfile
```

-	Layers:
	-	`sha256:f4420d9292d76286420dd7187c5b08b956041f3a4d90ecee23f7d1f91f3638ac`  
		Last Modified: Thu, 02 May 2024 17:53:24 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6daf94a67a74ecaca457f9fc6812857963aae03a4bdf69ffece0604d2d071e2c`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 13.6 KB (13580 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78` - linux; arm variant v7

```console
$ docker pull rust@sha256:225556750412cc8f6f468fd8c3bd1176e9b06c90153acb0e045b500c21265bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514307156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d9947ff3490d7e91dbee0aade813ded906312a29924c5226904b76432127e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07170ec327fa1117b5289697e5555f4c3ba76d00200d7c7cc5c143086856f`  
		Last Modified: Wed, 24 Apr 2024 05:03:03 GMT  
		Size: 59.2 MB (59216995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937bd8fccb438207fe0e77a48873de07dbe1fbea251206222298b72dbd2b3d8`  
		Last Modified: Wed, 24 Apr 2024 05:03:45 GMT  
		Size: 175.1 MB (175141109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499a6710f841b95850a0e6c3589a558408d5ecdb1efe2d461015241a86667d9`  
		Last Modified: Thu, 02 May 2024 18:16:14 GMT  
		Size: 212.8 MB (212820090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78` - unknown; unknown

```console
$ docker pull rust@sha256:a8d872088f3bc18ac36bb4ee06e93eac69f16897387344fcfd238be07505d19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15189426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f357e10dda11cec2f915422dbbb7f4dc9ef73032fc8aa82efe6609b3de03843`

```dockerfile
```

-	Layers:
	-	`sha256:67f172e545903f27510fe2841e22b7f07947e3314640824e648cc35a5e4af23c`  
		Last Modified: Thu, 02 May 2024 18:16:09 GMT  
		Size: 15.2 MB (15176407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becad9a5634f77e5e49e5e8f1bda8454cd92e0059d86c4ae3e43d13bba5c36d9`  
		Last Modified: Thu, 02 May 2024 18:16:08 GMT  
		Size: 13.0 KB (13019 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cb3fe1b45243325da5aaafb59bc75f8541697bfd9acbfedc914c0f132c7949ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.0 MB (586021653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b44c56b25c83977fc9ebfdf243d37b0b15ab1a4fcf0c647f0878847949cf84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476478a1e1450b999421118cb8f193aa62f1816e0cadd988a084385cf0a5696`  
		Last Modified: Wed, 24 Apr 2024 08:42:20 GMT  
		Size: 202.6 MB (202575289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ab2e8f65d41c1e5e2c493944dc3f6ca456b65a5275ac05e12bc31af0b697d`  
		Last Modified: Thu, 02 May 2024 18:26:37 GMT  
		Size: 246.3 MB (246251422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78` - unknown; unknown

```console
$ docker pull rust@sha256:9562e2467c5e3f2f6ee0ccff2633f57a5ff3cd388a582fca74510f46aba072bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6aaf4016fa5c395bc612fd990fc2d7422e8623e54ebe02b7b2625e179f7920`

```dockerfile
```

-	Layers:
	-	`sha256:1c4d0653a7e064d93a08cf2e3cb73351a07d67c388a1a2590326a06812bff5f3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 15.4 MB (15399046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790e84f88528ef27e0f653b5aeba1fafd203db38ba551366c785a778180828b3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 12.9 KB (12935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78` - linux; 386

```console
$ docker pull rust@sha256:d1f3c3a8b571383507c4e76f99678f065d5a03aa90eea84693c767e32fc869c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542180953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009dec677b8280c20069beef31c3fbbbc461bc0ab36f0558b2ec40439a5f6079`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:48 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Wed, 24 Apr 2024 03:38:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:29:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:30:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:1614889c1e665cd335548134ca677fb6f9f1910d4ab6488c04424418a97f495a`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 190.6 MB (190599211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78` - unknown; unknown

```console
$ docker pull rust@sha256:de08ac7a06b5af621f4e0fb99dabf08168a533017d45b6ff2510485f17d0b355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15363096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc533d073cc58cb332d3410a63a6c6f32d775b9febedb13c3c8b78a6d6079a9`

```dockerfile
```

-	Layers:
	-	`sha256:64ac9f5f1c25c9fffc99c099a79689856019c48dfffddbb43b51cba223012a11`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921284eb6647f818f95a3f3db77efe9fa3b4c28d2bf2158f08f1c984fe96fef0`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 13.5 KB (13531 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78` - linux; ppc64le

```console
$ docker pull rust@sha256:eb08c0b17cc0c417388189ce35bf4fb1f087a9e6ff51c1bfcec9ff410f2a8733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.2 MB (550221275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3bcff95d0b422fd84f7fcd46bf86991ba30fb41078803b6b6f6722b17322d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:20:52 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Wed, 24 Apr 2024 03:20:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:a6e8bb341b139fa8aae0ba05045cf5f0ef66e8260b98cda6950cadf916ed0f41`  
		Last Modified: Thu, 02 May 2024 18:12:45 GMT  
		Size: 187.1 MB (187143091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78` - unknown; unknown

```console
$ docker pull rust@sha256:7903613b4182abe216e7e36c9ee4ae650fe4a14316160360cdd8f94e459cf946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbc8ff473cd3ae52f9b1427e15706fae4d3d9591a2c8bf3f28b31a19f1a09c4`

```dockerfile
```

-	Layers:
	-	`sha256:6c78d4a4191a65c7af0530480d11f289861eab1ee86584e8133ba9ae8bb2de48`  
		Last Modified: Thu, 02 May 2024 18:12:41 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef473a7f3ff3cbb5e5bff01f89d91164174143787bc52b54999cd47006cd918`  
		Last Modified: Thu, 02 May 2024 18:12:40 GMT  
		Size: 13.0 KB (12979 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78` - linux; s390x

```console
$ docker pull rust@sha256:35a2f27aa7b8300d5a2e4aed602e03edcc950d6dcfbd9d7f8b8a86be19752041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578756361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008c354d831f826547ccd2d2a946c706ca40e6916ef33806ecaa916a21041dd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:42:45 GMT
ADD file:6b0e091009ac95d80973222b4f56557fc521253f20bb18eea1c9da2b61ed5cc2 in / 
# Wed, 24 Apr 2024 03:42:53 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea1cd174fa855055f0cc0296260c9e987dbd4cddfc8655fe48891b91e5af95b7`  
		Last Modified: Wed, 24 Apr 2024 03:48:59 GMT  
		Size: 47.9 MB (47942206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e212650b3684bdd95eb8c4cd55ad81ca7f992455cbcc5c126d1aac521b5399`  
		Last Modified: Wed, 24 Apr 2024 04:23:04 GMT  
		Size: 24.0 MB (24047036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5049d590d068e07d3557ef371a6ccc2fc96ffadeabbf0c1115204536ff84b`  
		Last Modified: Wed, 24 Apr 2024 04:23:21 GMT  
		Size: 63.1 MB (63130514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74409f156b70503c3e2227e45d964aec57dadc484e6492078584c8cad2e0884f`  
		Last Modified: Wed, 24 Apr 2024 04:23:50 GMT  
		Size: 183.2 MB (183208845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0a40d21a23b6b34012eaf7b342b43911c5d236a2f478d1df55a213f5b8247d`  
		Last Modified: Thu, 02 May 2024 18:17:05 GMT  
		Size: 260.4 MB (260427760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78` - unknown; unknown

```console
$ docker pull rust@sha256:70d0ae53ab927ca2824b1543a39761aaa621f8f640351e84e30c9cffcdada927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e4231ef234646dcaa8923b11a5a42334f73cdcc3a2467a2ef8ea47342e8f4`

```dockerfile
```

-	Layers:
	-	`sha256:2d98932b6c77d39b088f5fb17d27824d35fa3db3a89f0dc9677db81f3f0b219b`  
		Last Modified: Thu, 02 May 2024 18:17:02 GMT  
		Size: 15.2 MB (15185203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9bb7ba18a7a3be562faf0170f9215c5065bafb098b5bf71c12feccc9dce19c`  
		Last Modified: Thu, 02 May 2024 18:17:01 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78-alpine`

```console
$ docker pull rust@sha256:d4d3f81f3111991353bd7c7fa513ad3725a27027575fd82e24fb7babcd8f26f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.78-alpine` - linux; amd64

```console
$ docker pull rust@sha256:41bf7d335c39fd25bb73f3183713b1fdcb77f0fc70def6634e40992e66119292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276648359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9be41f0a10e18d4183096b0d91821b4f93cd1eb4e4884a8fd5fdc8b7ee34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c6c611323bdd864b20f293097226e373d0e34b9108e12e65481c955804c26`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 55.3 MB (55346841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245c9984f45dd6d2464604e214a0391a1b399705f140a8b96469f84d6e1f61e`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 217.9 MB (217892789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:8be526e7cb5aa9bc6b6d8c73fb8ee6e81a9c8164a4c5bfa97533ab5bfc0b6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcc214e8f56925c61fb2680fb60504b652116af551962b9d82c4683a88dc59`

```dockerfile
```

-	Layers:
	-	`sha256:f47a0d5a9bacd02cd11840d2f1a2adc07cd5bdb00e97770f9c417e49c8d49f29`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 710.6 KB (710621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232259c5160cb554f445085a6e5765832b7c088ca5c17fa09d0fb5f2a2dda48`  
		Last Modified: Thu, 02 May 2024 17:53:11 GMT  
		Size: 11.8 KB (11794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b7075f2ddfde9ede284e71e74bade0576f8ea97e0f49b2c8a4ead2a101a1cc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282899712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ab7c4bfc7646c65e0a623ab2551468819a7e5047057601317c046321a3c6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1475e7bc8776b6a5d5098e107869ccf04a61b48d632658ab4bf934b5340337c2`  
		Last Modified: Thu, 02 May 2024 18:30:18 GMT  
		Size: 53.0 MB (52995527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3cbfb4539306a5cd558b71b91000e4f05d22445cf79e04281bf881f3bfd22`  
		Last Modified: Thu, 02 May 2024 18:30:21 GMT  
		Size: 226.6 MB (226556470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f02f381f9fa338bae9204fb7e52a19b44779316d227092aa2fb77ea0a62cea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.2 KB (758219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e2876b12a57c6260b8a220b6a82f40ccb6b3f85bced4f5e908a46f1175e9c`

```dockerfile
```

-	Layers:
	-	`sha256:0f5adf947b65a86f48dfa44a9462e156913eca4be72ad307f8b70e63904defcc`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 746.6 KB (746571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd319de530a5221d01b41f952f79922b81a42473dd697d14646929354af7f96c`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 11.6 KB (11648 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78-alpine3.18`

```console
$ docker pull rust@sha256:34f1c35f62e192f39cd0c809982bf90c354f7e5746682a2f4c9e4c43bd516dbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.78-alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:909cfdd11b0a96aa82d86c96c17cddf3864bca150a6228d18ab6a658e7006d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272829333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787b53dee543c9d07c38258423856c4ce44a7bb0e10dd80b6ce8d3d6be6d688b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d8cca761111b3832e2234b2a7c144570d1ceaa6a6eab4447a39633b2a0c9e6`  
		Last Modified: Thu, 02 May 2024 17:53:03 GMT  
		Size: 51.5 MB (51534006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94392fe86146798eeda301677559c748ac0525075773894cb651ef44b47f89cf`  
		Last Modified: Thu, 02 May 2024 17:53:06 GMT  
		Size: 217.9 MB (217892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:828ea566785e422ca858dcd98738715dc31eb43e85aa4ac91f75e0f3c0d1a46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13ead6d1e1a8601c572bfe57d56165b246d74fecdc009ab88410fe102fdb904`

```dockerfile
```

-	Layers:
	-	`sha256:022a488b72ff619b6be7c5b9d74e5a88f50c0e8179a478751063a2baa139c1ca`  
		Last Modified: Thu, 02 May 2024 17:53:02 GMT  
		Size: 701.9 KB (701890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d53ac36334ec5e522ca13debbc666b6df6ad9bb97c9efa7639b75bec875183c`  
		Last Modified: Thu, 02 May 2024 17:53:02 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ee1d16c1cc031559875424b27cb090136df31c18dd9e97966cf12391b59ba403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (275971039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0325d780023f87c7f06c8d7e4ee3aadb87e82528ad4b2da06a341cc8e42438bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecadc98c87cbba10a8cd3e79aee52d2aa3670ae6272cc2b29b27128e710a536`  
		Last Modified: Thu, 02 May 2024 18:29:15 GMT  
		Size: 46.1 MB (46081224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688cf2745b0216764a0d813aa9bf3d0c02af25fae1ef4c9bfce32c558a0d640f`  
		Last Modified: Thu, 02 May 2024 18:29:18 GMT  
		Size: 226.6 MB (226556454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:a6e2823b379b899207fbbdc6d8f2181cb7668892e2f31ce8f272302781d6a274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.1 KB (752144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa78da9cdd7dc3787e280f8a86f29faba9f60305898cf6d9486dc01fdc2def2`

```dockerfile
```

-	Layers:
	-	`sha256:2508e1ec9f010359afe8d8e516417a297aa32d170c071185c0be86d2c697cb2f`  
		Last Modified: Thu, 02 May 2024 18:29:13 GMT  
		Size: 741.7 KB (741708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af17300661fa62bda831f09a0938360f387b14cb172b980a435cff240801bee8`  
		Last Modified: Thu, 02 May 2024 18:29:13 GMT  
		Size: 10.4 KB (10436 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78-alpine3.19`

```console
$ docker pull rust@sha256:d4d3f81f3111991353bd7c7fa513ad3725a27027575fd82e24fb7babcd8f26f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.78-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:41bf7d335c39fd25bb73f3183713b1fdcb77f0fc70def6634e40992e66119292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276648359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9be41f0a10e18d4183096b0d91821b4f93cd1eb4e4884a8fd5fdc8b7ee34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c6c611323bdd864b20f293097226e373d0e34b9108e12e65481c955804c26`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 55.3 MB (55346841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245c9984f45dd6d2464604e214a0391a1b399705f140a8b96469f84d6e1f61e`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 217.9 MB (217892789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:8be526e7cb5aa9bc6b6d8c73fb8ee6e81a9c8164a4c5bfa97533ab5bfc0b6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcc214e8f56925c61fb2680fb60504b652116af551962b9d82c4683a88dc59`

```dockerfile
```

-	Layers:
	-	`sha256:f47a0d5a9bacd02cd11840d2f1a2adc07cd5bdb00e97770f9c417e49c8d49f29`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 710.6 KB (710621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232259c5160cb554f445085a6e5765832b7c088ca5c17fa09d0fb5f2a2dda48`  
		Last Modified: Thu, 02 May 2024 17:53:11 GMT  
		Size: 11.8 KB (11794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b7075f2ddfde9ede284e71e74bade0576f8ea97e0f49b2c8a4ead2a101a1cc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282899712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ab7c4bfc7646c65e0a623ab2551468819a7e5047057601317c046321a3c6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1475e7bc8776b6a5d5098e107869ccf04a61b48d632658ab4bf934b5340337c2`  
		Last Modified: Thu, 02 May 2024 18:30:18 GMT  
		Size: 53.0 MB (52995527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3cbfb4539306a5cd558b71b91000e4f05d22445cf79e04281bf881f3bfd22`  
		Last Modified: Thu, 02 May 2024 18:30:21 GMT  
		Size: 226.6 MB (226556470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:f02f381f9fa338bae9204fb7e52a19b44779316d227092aa2fb77ea0a62cea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.2 KB (758219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e2876b12a57c6260b8a220b6a82f40ccb6b3f85bced4f5e908a46f1175e9c`

```dockerfile
```

-	Layers:
	-	`sha256:0f5adf947b65a86f48dfa44a9462e156913eca4be72ad307f8b70e63904defcc`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 746.6 KB (746571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd319de530a5221d01b41f952f79922b81a42473dd697d14646929354af7f96c`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 11.6 KB (11648 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78-bookworm`

```console
$ docker pull rust@sha256:0dd183faf7bc5b9b8efe81cfd42701a5283577520b185b511e322e5bf52f8fc7
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

### `rust:1.78-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:d50e312c75fbd66f5cc7b1ab6d76892529751526629c294f34ca217016fe0425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526535638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d8eec96e0ea00b3ec3c6c2e03ef8a15113d8dd0682170d3757c06a78e73dce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:6b9f9d886ac307c9982286da0ae1d85ad364df502e05f2c5c14c9505f30a4feb`  
		Last Modified: Thu, 02 May 2024 17:53:26 GMT  
		Size: 177.6 MB (177591491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9d352cd5f6a779bed1be7057ea6557c8de8f96c40e26e555b469d2c2f8405643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15384104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511f0cc56710400a858b2b313a1fb6c554e2ca7debcdcfd5d6ae3ac4870e716f`

```dockerfile
```

-	Layers:
	-	`sha256:f4420d9292d76286420dd7187c5b08b956041f3a4d90ecee23f7d1f91f3638ac`  
		Last Modified: Thu, 02 May 2024 17:53:24 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6daf94a67a74ecaca457f9fc6812857963aae03a4bdf69ffece0604d2d071e2c`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 13.6 KB (13580 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:225556750412cc8f6f468fd8c3bd1176e9b06c90153acb0e045b500c21265bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514307156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d9947ff3490d7e91dbee0aade813ded906312a29924c5226904b76432127e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07170ec327fa1117b5289697e5555f4c3ba76d00200d7c7cc5c143086856f`  
		Last Modified: Wed, 24 Apr 2024 05:03:03 GMT  
		Size: 59.2 MB (59216995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937bd8fccb438207fe0e77a48873de07dbe1fbea251206222298b72dbd2b3d8`  
		Last Modified: Wed, 24 Apr 2024 05:03:45 GMT  
		Size: 175.1 MB (175141109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499a6710f841b95850a0e6c3589a558408d5ecdb1efe2d461015241a86667d9`  
		Last Modified: Thu, 02 May 2024 18:16:14 GMT  
		Size: 212.8 MB (212820090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a8d872088f3bc18ac36bb4ee06e93eac69f16897387344fcfd238be07505d19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15189426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f357e10dda11cec2f915422dbbb7f4dc9ef73032fc8aa82efe6609b3de03843`

```dockerfile
```

-	Layers:
	-	`sha256:67f172e545903f27510fe2841e22b7f07947e3314640824e648cc35a5e4af23c`  
		Last Modified: Thu, 02 May 2024 18:16:09 GMT  
		Size: 15.2 MB (15176407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becad9a5634f77e5e49e5e8f1bda8454cd92e0059d86c4ae3e43d13bba5c36d9`  
		Last Modified: Thu, 02 May 2024 18:16:08 GMT  
		Size: 13.0 KB (13019 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cb3fe1b45243325da5aaafb59bc75f8541697bfd9acbfedc914c0f132c7949ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.0 MB (586021653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b44c56b25c83977fc9ebfdf243d37b0b15ab1a4fcf0c647f0878847949cf84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476478a1e1450b999421118cb8f193aa62f1816e0cadd988a084385cf0a5696`  
		Last Modified: Wed, 24 Apr 2024 08:42:20 GMT  
		Size: 202.6 MB (202575289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ab2e8f65d41c1e5e2c493944dc3f6ca456b65a5275ac05e12bc31af0b697d`  
		Last Modified: Thu, 02 May 2024 18:26:37 GMT  
		Size: 246.3 MB (246251422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9562e2467c5e3f2f6ee0ccff2633f57a5ff3cd388a582fca74510f46aba072bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6aaf4016fa5c395bc612fd990fc2d7422e8623e54ebe02b7b2625e179f7920`

```dockerfile
```

-	Layers:
	-	`sha256:1c4d0653a7e064d93a08cf2e3cb73351a07d67c388a1a2590326a06812bff5f3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 15.4 MB (15399046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790e84f88528ef27e0f653b5aeba1fafd203db38ba551366c785a778180828b3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 12.9 KB (12935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d1f3c3a8b571383507c4e76f99678f065d5a03aa90eea84693c767e32fc869c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542180953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009dec677b8280c20069beef31c3fbbbc461bc0ab36f0558b2ec40439a5f6079`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:48 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Wed, 24 Apr 2024 03:38:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:29:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:30:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:1614889c1e665cd335548134ca677fb6f9f1910d4ab6488c04424418a97f495a`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 190.6 MB (190599211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:de08ac7a06b5af621f4e0fb99dabf08168a533017d45b6ff2510485f17d0b355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15363096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc533d073cc58cb332d3410a63a6c6f32d775b9febedb13c3c8b78a6d6079a9`

```dockerfile
```

-	Layers:
	-	`sha256:64ac9f5f1c25c9fffc99c099a79689856019c48dfffddbb43b51cba223012a11`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921284eb6647f818f95a3f3db77efe9fa3b4c28d2bf2158f08f1c984fe96fef0`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 13.5 KB (13531 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:eb08c0b17cc0c417388189ce35bf4fb1f087a9e6ff51c1bfcec9ff410f2a8733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.2 MB (550221275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3bcff95d0b422fd84f7fcd46bf86991ba30fb41078803b6b6f6722b17322d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:20:52 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Wed, 24 Apr 2024 03:20:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:a6e8bb341b139fa8aae0ba05045cf5f0ef66e8260b98cda6950cadf916ed0f41`  
		Last Modified: Thu, 02 May 2024 18:12:45 GMT  
		Size: 187.1 MB (187143091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7903613b4182abe216e7e36c9ee4ae650fe4a14316160360cdd8f94e459cf946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbc8ff473cd3ae52f9b1427e15706fae4d3d9591a2c8bf3f28b31a19f1a09c4`

```dockerfile
```

-	Layers:
	-	`sha256:6c78d4a4191a65c7af0530480d11f289861eab1ee86584e8133ba9ae8bb2de48`  
		Last Modified: Thu, 02 May 2024 18:12:41 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef473a7f3ff3cbb5e5bff01f89d91164174143787bc52b54999cd47006cd918`  
		Last Modified: Thu, 02 May 2024 18:12:40 GMT  
		Size: 13.0 KB (12979 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:35a2f27aa7b8300d5a2e4aed602e03edcc950d6dcfbd9d7f8b8a86be19752041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578756361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008c354d831f826547ccd2d2a946c706ca40e6916ef33806ecaa916a21041dd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:42:45 GMT
ADD file:6b0e091009ac95d80973222b4f56557fc521253f20bb18eea1c9da2b61ed5cc2 in / 
# Wed, 24 Apr 2024 03:42:53 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea1cd174fa855055f0cc0296260c9e987dbd4cddfc8655fe48891b91e5af95b7`  
		Last Modified: Wed, 24 Apr 2024 03:48:59 GMT  
		Size: 47.9 MB (47942206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e212650b3684bdd95eb8c4cd55ad81ca7f992455cbcc5c126d1aac521b5399`  
		Last Modified: Wed, 24 Apr 2024 04:23:04 GMT  
		Size: 24.0 MB (24047036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5049d590d068e07d3557ef371a6ccc2fc96ffadeabbf0c1115204536ff84b`  
		Last Modified: Wed, 24 Apr 2024 04:23:21 GMT  
		Size: 63.1 MB (63130514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74409f156b70503c3e2227e45d964aec57dadc484e6492078584c8cad2e0884f`  
		Last Modified: Wed, 24 Apr 2024 04:23:50 GMT  
		Size: 183.2 MB (183208845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0a40d21a23b6b34012eaf7b342b43911c5d236a2f478d1df55a213f5b8247d`  
		Last Modified: Thu, 02 May 2024 18:17:05 GMT  
		Size: 260.4 MB (260427760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:70d0ae53ab927ca2824b1543a39761aaa621f8f640351e84e30c9cffcdada927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e4231ef234646dcaa8923b11a5a42334f73cdcc3a2467a2ef8ea47342e8f4`

```dockerfile
```

-	Layers:
	-	`sha256:2d98932b6c77d39b088f5fb17d27824d35fa3db3a89f0dc9677db81f3f0b219b`  
		Last Modified: Thu, 02 May 2024 18:17:02 GMT  
		Size: 15.2 MB (15185203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9bb7ba18a7a3be562faf0170f9215c5065bafb098b5bf71c12feccc9dce19c`  
		Last Modified: Thu, 02 May 2024 18:17:01 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78-bullseye`

```console
$ docker pull rust@sha256:2552dc030938db6be68061470bb1d06a614e2523bc28aca5ae3db334fe4b3476
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

### `rust:1.78-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:e6d6b30cc542e783d7c99f59c4981a1dfc16854065004dd2031731c1f39bde8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.0 MB (500031479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcad364931eede82edf28ce9a8b0d641d449dfc7c66a5409117906b6b6b8b4ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:13:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:534d57e3d7c23ea864729859cd9639d95758dc80d3fae7c2f1a781369374f72c`  
		Last Modified: Thu, 02 May 2024 17:53:19 GMT  
		Size: 177.6 MB (177591486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:394674afd531ba7ba75772c582acf4520d9dfde25713860cf929548250230b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14987362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd227c9c6937e47e8c7124353322fb9c95d173d5e40454385bc62a5de0a4d204`

```dockerfile
```

-	Layers:
	-	`sha256:5175f4542d292457f1a4530967191286a12c21391a2bb9a183579ff56267c300`  
		Last Modified: Thu, 02 May 2024 17:53:17 GMT  
		Size: 15.0 MB (14974944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da52b512eddefa1c1ecbaaa573257018e0b1790c5832c459900ce53606e1b2a`  
		Last Modified: Thu, 02 May 2024 17:53:16 GMT  
		Size: 12.4 KB (12418 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:04d28c769d11d7e8647f2cb4abc12e4772bf7ac447fdc05e7a6713bf8619ec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.8 MB (495758778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021e7713c700cad89a3873cd2bcb165eeda0cba39d5eac5e6c0ceb0433e2015f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:15 GMT
ADD file:59046a1e0987059e779fff5a0f35e03203c109d778a75058e9474705d3fcfdff in / 
# Wed, 24 Apr 2024 04:07:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:51:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:53:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:853e2341066ebc3a07d3c44ebac8c3ce40daf429fb9cc3f49f2d35115e9cc93f`  
		Last Modified: Wed, 24 Apr 2024 04:11:34 GMT  
		Size: 50.3 MB (50255574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d5c1aa98981d0ab503d79e97e4eeed8435372346757065a98c291d66c74df`  
		Last Modified: Wed, 24 Apr 2024 05:03:57 GMT  
		Size: 14.9 MB (14880390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94741efe025699cbcd617a32ea95a4fea8cfaeedfa3b93bd9cbc7ed02063a74a`  
		Last Modified: Wed, 24 Apr 2024 05:04:17 GMT  
		Size: 50.4 MB (50359575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba251a5fa80ede4ef9bfae4161563b58236318c68e2a17d1cbd5afa4ba9a2c68`  
		Last Modified: Wed, 24 Apr 2024 05:04:53 GMT  
		Size: 167.4 MB (167442932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5d2b6834c7a0899f1680cc6d8cc388f1d0dca62c4f7a8ebe01f44f45352ed7`  
		Last Modified: Thu, 02 May 2024 18:12:01 GMT  
		Size: 212.8 MB (212820307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80b041026f0b46d413060fd8525a3ba151a2eacd151071f8c61fc152cdfd39d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14788669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51b3ef7ff5219f52138329d10cb8348d58ffc8198540c1b328f90fbc8a82ea6`

```dockerfile
```

-	Layers:
	-	`sha256:6c813ccd1a4df3a4bbbbe45bfed024331d0fd2c3308c8a3d7d111ea597aafb5f`  
		Last Modified: Thu, 02 May 2024 18:11:56 GMT  
		Size: 14.8 MB (14776844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19847e3e85938bfccef756d696d053d674fb2f4065a928f39c3451d036e26c9d`  
		Last Modified: Thu, 02 May 2024 18:11:55 GMT  
		Size: 11.8 KB (11825 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:82d27aac8d8758af4166b14ffb1cc316fa08b2fd8cfaf238846ba54bc171e9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.4 MB (560350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423aa11d7bda4aed73983759f01bf96699ace117c8ea8c844c414b738c64bcd7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33008ff0928e624ce22cedd5d004edd66b80372bfd1223e8900206330213ee34`  
		Last Modified: Wed, 24 Apr 2024 08:42:31 GMT  
		Size: 15.8 MB (15750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36972983386f768dbeff5de37af34ed4e2f59541b2e3c43575f29758c3591923`  
		Last Modified: Wed, 24 Apr 2024 08:42:45 GMT  
		Size: 54.7 MB (54696233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3224178d7041e10ec03b66358ce4ba6bb5aeaf26b593f3e8672ca38f7b70769e`  
		Last Modified: Wed, 24 Apr 2024 08:43:09 GMT  
		Size: 189.9 MB (189912094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97275dd0257b83d60c67c3d70971c98640014802ea42bae0e7414eaacf4f365b`  
		Last Modified: Thu, 02 May 2024 18:22:28 GMT  
		Size: 246.3 MB (246251467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cb31ecf48d87fa71df2cb5a2933820e8ecbdd1dbb690d4b5aff13d7fbd87755e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14989175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2aef4675fe30517f9f710edbba6c5a198def25e9b99362e323b7e9b30a6d4d`

```dockerfile
```

-	Layers:
	-	`sha256:eb1b6d19dba8c8c9789a080460223469c5e39861aabf0abb48fe6a856f49572f`  
		Last Modified: Thu, 02 May 2024 18:22:23 GMT  
		Size: 15.0 MB (14977411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed5b26cdc4f076066fac6d6878fca32b53fbe9a0c5bf6b5429bb951a8de7223`  
		Last Modified: Thu, 02 May 2024 18:22:22 GMT  
		Size: 11.8 KB (11764 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-bullseye` - linux; 386

```console
$ docker pull rust@sha256:232c18232dd7076711f3603df35b9bfe483c49663e03b9259edbd30810dfc02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518766287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858075fb8a3b54656c0ee7518ef0b22601a2d1b7d4d1f2fd037699198b2bef9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:08 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
# Wed, 24 Apr 2024 03:39:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:30:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:32:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:df053a23eab4180eece3d17162346216b301343de9fb6226cd226f21702be82f`  
		Last Modified: Thu, 02 May 2024 17:53:36 GMT  
		Size: 190.6 MB (190599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cf1fa86ecf03dd1fbb4dcce34d4a6d575a64d018570476a025626d21108bf3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14976156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0056775c2d4a3ef6fbace0e34ff6db97f0f12ad062f8875c69193a8f497145ad`

```dockerfile
```

-	Layers:
	-	`sha256:189cacbc159513dae1c96778228fcacb8fa5341832b01271f051b1124b140d81`  
		Last Modified: Thu, 02 May 2024 17:53:30 GMT  
		Size: 15.0 MB (14963767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86ac21aeb5f940ce0d749c02477c27d23e1023a107afeb492eedaa85b35f6e8`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 12.4 KB (12389 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:74f6d27411b0fe1655b74893221edde39cc79b5c54f779b8f924d0f94e5b6ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.1 MB (518096210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655131ce8b88722fe88822b0323c0f901ee374ed6e1eb86f90e53c8a0f1031de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:25 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
# Wed, 24 Apr 2024 03:21:30 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:04:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:f315af7fc149bdbb645add44aaef365e14662b9bf33a24ebcdeda2ed49bcef6f`  
		Last Modified: Thu, 02 May 2024 18:07:04 GMT  
		Size: 187.1 MB (187143092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:02041686275df55e6c1cde2ab50a36777b23e5f0bfa0620bcea85ce288d8403d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14954340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c14dc83c058acbfa6bd18b2ba83506e0f719407a324008942f86a2d4dcc87af`

```dockerfile
```

-	Layers:
	-	`sha256:ce1abb7d3006b3e51d88e3b055b4055bbc25212003172c9a9aa9532a8425ad91`  
		Last Modified: Thu, 02 May 2024 18:06:59 GMT  
		Size: 14.9 MB (14942547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c168268955e9148deab9bdffcc4c0a75e9a8cea798c2286a9aab8cdf5599398f`  
		Last Modified: Thu, 02 May 2024 18:06:58 GMT  
		Size: 11.8 KB (11793 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:e3c00ec457a002c90f44ff20936bcfee6bd86f03ab1cc7750785060a7895e5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.5 MB (556478959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3364960915922de42d06974605b4e00f6fc171fd9a6475446ac1f876a6543c0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:33 GMT
ADD file:e0a1fc1de1477cea6fe41bdd15378013c680928cad3988dd16926cc1562c775e in / 
# Wed, 24 Apr 2024 03:43:38 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b57a10abb081ff40e5bb34246c3875a71b8d258f767c4f8384d7054b1bc42725`  
		Last Modified: Wed, 24 Apr 2024 03:49:31 GMT  
		Size: 53.3 MB (53337419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ed92794c4710c20ea615a0e07fe947837768482be7bcd9d1fccb335072a92`  
		Last Modified: Wed, 24 Apr 2024 04:24:03 GMT  
		Size: 15.6 MB (15642846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0318d2197701d71929fa882d8d64bdc0c65ee6bc9abd4bd4063694d92acb7`  
		Last Modified: Wed, 24 Apr 2024 04:24:17 GMT  
		Size: 54.1 MB (54076626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c3f9b4c72abaa52996d64ffc8754f8500b075a8a677c0fe59c310548e9af5c`  
		Last Modified: Wed, 24 Apr 2024 04:24:43 GMT  
		Size: 173.0 MB (172994116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66302c05a1f58a25604176a4b9b6bc0e717fb72ff97e0334ea79fb2895e26df7`  
		Last Modified: Thu, 02 May 2024 18:08:54 GMT  
		Size: 260.4 MB (260427952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:52b39a86a4ea99cb0237d970a10213cddfe8f113046bf4abdd5d3e4a3cda1363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14808368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bec0dfd4f38a0e9dad4996be6db3bacd06333698fa0cae356936fc13be9fd4`

```dockerfile
```

-	Layers:
	-	`sha256:83ce677ca56d4a667f9518ab5babc3e5b9ad1f44c3a5dbd0ff5ba123690f4055`  
		Last Modified: Thu, 02 May 2024 18:08:50 GMT  
		Size: 14.8 MB (14796613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f959e24eefab058ecc036f364b2858652b6977cafed184475b485ec952b32bc`  
		Last Modified: Thu, 02 May 2024 18:08:50 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78-buster`

```console
$ docker pull rust@sha256:fcb09007a565e6705c6d49835377d7d18e050b309203edc9e412977e91269257
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

### `rust:1.78-buster` - linux; amd64

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

### `rust:1.78-buster` - unknown; unknown

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

### `rust:1.78-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:47eacf3b5d2efd391224926939f061ff7acd7574beacdbcf721c82b01a65715e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 MB (490711222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bef0c9fda88c0ce49bbbe4e82e4c8d2496752121e8e07c5f59170f61ca0d31d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:33 GMT
ADD file:eea1eb05334cd4d0032909b2c56fc86a54faad563cbc3d2d46e763ce9e8922ab in / 
# Wed, 24 Apr 2024 04:07:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:53:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:54:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:55:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
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
	-	`sha256:fe0f6a4b48afbd61f9ef055b862b89cc5fc3980c4be6d4ccdc4e71eb6bd56d0d`  
		Last Modified: Thu, 02 May 2024 18:07:53 GMT  
		Size: 212.8 MB (212820147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-buster` - unknown; unknown

```console
$ docker pull rust@sha256:752d344513be8e413c08339a72a1696e061067a176479b706f0ae0a0c25048f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15780088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c18d957fb0511cfe9d344a4de14bcc9b40ee6d3bfbc1d980e180ae8df9d7aea`

```dockerfile
```

-	Layers:
	-	`sha256:da347c4aa030e17d6c56379e77bbdc5e28dab4fed5f89adbf67d26f052266c5f`  
		Last Modified: Thu, 02 May 2024 18:07:47 GMT  
		Size: 15.8 MB (15769023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52097463634c6c7d47e034b943ee50d0b5c9c9b3d2a8be616e9ebc076bb95f37`  
		Last Modified: Thu, 02 May 2024 18:07:46 GMT  
		Size: 11.1 KB (11065 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:775daa3419885651f2e284f10b29385f68347c1b99caf12ee7dbf82edc24947f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548916487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5233d262b43ce5dd1ff865b0ee9ac12ae4be5844a39f716b3cd8396774e15b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:00 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
# Wed, 24 Apr 2024 04:11:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:36:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
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
	-	`sha256:af5cdf87e38274705e7b47b4d3a5ccbab3f4bf94894cac0c5b2d82abfcf1989e`  
		Last Modified: Thu, 02 May 2024 18:19:24 GMT  
		Size: 246.3 MB (246251497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-buster` - unknown; unknown

```console
$ docker pull rust@sha256:dac6fc781e375c3f98871b1045ea01bd75fc62f126ba52697ba0c6b38a1f4aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15969386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2c1d63305c600acd748d5093b508df829037b295ab55b92bcc3998cf8ce8aa`

```dockerfile
```

-	Layers:
	-	`sha256:65b7feb61540a8b5987675be790620a8a6a102d1c29faafbb53fc91011a7161d`  
		Last Modified: Thu, 02 May 2024 18:19:19 GMT  
		Size: 16.0 MB (15957718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccd3a895875d4cbfb484b9fb55f5e778d710cf340062cd3a9484aadb5c29130`  
		Last Modified: Thu, 02 May 2024 18:19:19 GMT  
		Size: 11.7 KB (11668 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-buster` - linux; 386

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

### `rust:1.78-buster` - unknown; unknown

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

## `rust:1.78-slim`

```console
$ docker pull rust@sha256:517c6272b328bc51c87e099ef4adfbc7ab4558af2d757e8d423c7c3f1cbbf9d5
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

### `rust:1.78-slim` - linux; amd64

```console
$ docker pull rust@sha256:144edf7af2e5e374afdee02fd458df5bad41aba4cae314ace9d43f7933d44c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277315532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036d20da216ad2e94545e4e82700ee8c8ee3ad79fa0e2dca1261f8a69a87a937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8f9fca3e1073639d97fde71b99e2ef803078e36ed1cd97b74ce545ee7b17`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 248.2 MB (248165053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a10481a084e247a58cb63c17b394d4e65463e3c8369e21bcfc769abbdfffb9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911a63093a97a45bdf3e678240c96fe3b7f81befc1871a5542db741b9b51a7d`

```dockerfile
```

-	Layers:
	-	`sha256:371755c5d7b19c0c727d6c961f8c6528bc0cbd0b3d2c7067a40ddd1f9eaa4e74`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6556d0382c9b778b94f7cc91b1d3f7659518e567fab6462da86ebe4ac90c6382`  
		Last Modified: Thu, 02 May 2024 17:53:22 GMT  
		Size: 13.2 KB (13172 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:ffc8f22bbcaf9c443db0c997aba6a8f0773d989e29a5865d0f164a36f15e8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285223017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d69dbc41e535f1c4657a7b35fe40a346dce9c4f07b392370b716e1c4ea8c45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f060f4605d55cb88006aa78ea1433f0129af80557306aa6ef11d728ad8c15`  
		Last Modified: Thu, 02 May 2024 18:18:12 GMT  
		Size: 260.5 MB (260482575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8ee1faa28bc0f8ec0e92ba67f71be26d4570984f23660ad77c52f9cdaf0e4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14586c5fd8ae352e99facffdc8e47f2ffe4a171ae426fa7163a3033099714f4d`

```dockerfile
```

-	Layers:
	-	`sha256:f920b7810ae2eb89611842b3c8d00f4e763ddaa0dbb6dc67bc77bc0979211af2`  
		Last Modified: Thu, 02 May 2024 18:18:06 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6070f226a82471804b25ddfcd5994dfb20c75710288cb8fa305eeecbc9689a`  
		Last Modified: Thu, 02 May 2024 18:18:05 GMT  
		Size: 13.1 KB (13107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:701d523927f60aa6594b6b639e16b2872b090efd77b38206eb07f8a5ab5f4b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341067862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d7c8b33fff18a1de7a58bd9764df34dcb7689471c8332703ef166a3be91dbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b6ff75fe73e0b624033411b211e30ab65a0dfe2f196bc831afaa3f262ad40`  
		Last Modified: Thu, 02 May 2024 18:28:13 GMT  
		Size: 311.9 MB (311887927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3068c80cfcc050b7d2f84d2daa26eb1bb6646dbef2cdc889b4706d0ecec10c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94192de4d427019b53f8d6f476258f84f6c701b7cc313fbe20aac8356c685388`

```dockerfile
```

-	Layers:
	-	`sha256:fe0470bf526cfabeeff81d8175f1ad542787eb63d46eac59584aa0c9700cb865`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 3.9 MB (3941462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e741b4e2feaf42a20f56bbcccb528e05e69b28f20a30f471dab96b02dd26885d`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 13.0 KB (13023 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim` - linux; 386

```console
$ docker pull rust@sha256:9a0ff69ac63b29617f2772d8af475f42b17376ae675690bd4b6ffbd6fa013a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288155332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730521317992ca457b5e32b681e5c2fc6a9985f74b26c05ab75a898d70063efd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be463c23e962e7814d7269dd918a3abf7fe7480f3491260b6939bc093b40232`  
		Last Modified: Thu, 02 May 2024 17:53:34 GMT  
		Size: 258.0 MB (257992149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim` - unknown; unknown

```console
$ docker pull rust@sha256:406577ad4a920a84505e527616fcb1f008cff2e259737b980109d6586c441132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94959a9ba35ac8e7aa52d2c9634583789f540a6ce1cdf8970c1aeafbeb383266`

```dockerfile
```

-	Layers:
	-	`sha256:5fccb080d41ea034eca85abe7287cd6513b3fcf1304c5b0ab744b5e4f7604ee2`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5ee26d72cca7cd34f6faa2688b32a264613f3b88beb239a82737e7a7bdd0b8`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:ea7984b98ee3317d77412b9077362d5f7934cbed7f5d5ce18a977f899e9386c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288845524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a166a0772dcf6517a472407901b610b01b80c50d7487fd756971dc08ca26d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bdd5b65845940ee92c4225121c6b04def8a421d1c550f7d8d65db0e37bf19`  
		Last Modified: Thu, 02 May 2024 18:15:05 GMT  
		Size: 255.7 MB (255704323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b8cf1c2e22630a3fb96504ce4e0109e450e2f91f2338965264da180dffb4be0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e443bda8941eefcf331e18425d4d04513900c67b623379aae5f5c3ba60799f`

```dockerfile
```

-	Layers:
	-	`sha256:57c7d4ef78d8836d083ed51f7584a8611e874b74c989c77cbdaefba43cf9c737`  
		Last Modified: Thu, 02 May 2024 18:14:59 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721e6450ded9a8224165692a227cf32021b20727fa9e27b7eb51b9ee46c98d64`  
		Last Modified: Thu, 02 May 2024 18:14:58 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim` - linux; s390x

```console
$ docker pull rust@sha256:f2f85fb1ee50bb9ddd8312a215bd06ef84d9d8a32ae978df573ac5b9b84ab38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337865924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2db01fe12c831f8b1c810ff63f0059a28b15cebb3fc607f041e7f43ba47394a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c36f802355139032b4b3b2815d90b8684055c93beadd105d203de5c4574421`  
		Last Modified: Thu, 02 May 2024 18:19:38 GMT  
		Size: 310.4 MB (310353569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1d010d6d80dc73fcb8b111939211fe047c868a66965107fe6522c5ac238f2882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67848fc2610daa3a0488587b7d72d3197b8f69b13b8bc20914dec3e53cac68c4`

```dockerfile
```

-	Layers:
	-	`sha256:45465cb45a531518db8458bf81a4591118d814a4fcc27d32e893ed00128240f1`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 3.8 MB (3762075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ba7b0835f73f3eba7b3413925b87bc83556d2ccd55606dfd68c5715cec19c7b`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78-slim-bookworm`

```console
$ docker pull rust@sha256:517c6272b328bc51c87e099ef4adfbc7ab4558af2d757e8d423c7c3f1cbbf9d5
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

### `rust:1.78-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:144edf7af2e5e374afdee02fd458df5bad41aba4cae314ace9d43f7933d44c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277315532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036d20da216ad2e94545e4e82700ee8c8ee3ad79fa0e2dca1261f8a69a87a937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8f9fca3e1073639d97fde71b99e2ef803078e36ed1cd97b74ce545ee7b17`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 248.2 MB (248165053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a10481a084e247a58cb63c17b394d4e65463e3c8369e21bcfc769abbdfffb9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911a63093a97a45bdf3e678240c96fe3b7f81befc1871a5542db741b9b51a7d`

```dockerfile
```

-	Layers:
	-	`sha256:371755c5d7b19c0c727d6c961f8c6528bc0cbd0b3d2c7067a40ddd1f9eaa4e74`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6556d0382c9b778b94f7cc91b1d3f7659518e567fab6462da86ebe4ac90c6382`  
		Last Modified: Thu, 02 May 2024 17:53:22 GMT  
		Size: 13.2 KB (13172 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ffc8f22bbcaf9c443db0c997aba6a8f0773d989e29a5865d0f164a36f15e8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285223017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d69dbc41e535f1c4657a7b35fe40a346dce9c4f07b392370b716e1c4ea8c45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f060f4605d55cb88006aa78ea1433f0129af80557306aa6ef11d728ad8c15`  
		Last Modified: Thu, 02 May 2024 18:18:12 GMT  
		Size: 260.5 MB (260482575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ee1faa28bc0f8ec0e92ba67f71be26d4570984f23660ad77c52f9cdaf0e4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14586c5fd8ae352e99facffdc8e47f2ffe4a171ae426fa7163a3033099714f4d`

```dockerfile
```

-	Layers:
	-	`sha256:f920b7810ae2eb89611842b3c8d00f4e763ddaa0dbb6dc67bc77bc0979211af2`  
		Last Modified: Thu, 02 May 2024 18:18:06 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6070f226a82471804b25ddfcd5994dfb20c75710288cb8fa305eeecbc9689a`  
		Last Modified: Thu, 02 May 2024 18:18:05 GMT  
		Size: 13.1 KB (13107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:701d523927f60aa6594b6b639e16b2872b090efd77b38206eb07f8a5ab5f4b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341067862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d7c8b33fff18a1de7a58bd9764df34dcb7689471c8332703ef166a3be91dbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b6ff75fe73e0b624033411b211e30ab65a0dfe2f196bc831afaa3f262ad40`  
		Last Modified: Thu, 02 May 2024 18:28:13 GMT  
		Size: 311.9 MB (311887927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3068c80cfcc050b7d2f84d2daa26eb1bb6646dbef2cdc889b4706d0ecec10c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94192de4d427019b53f8d6f476258f84f6c701b7cc313fbe20aac8356c685388`

```dockerfile
```

-	Layers:
	-	`sha256:fe0470bf526cfabeeff81d8175f1ad542787eb63d46eac59584aa0c9700cb865`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 3.9 MB (3941462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e741b4e2feaf42a20f56bbcccb528e05e69b28f20a30f471dab96b02dd26885d`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 13.0 KB (13023 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:9a0ff69ac63b29617f2772d8af475f42b17376ae675690bd4b6ffbd6fa013a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288155332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730521317992ca457b5e32b681e5c2fc6a9985f74b26c05ab75a898d70063efd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be463c23e962e7814d7269dd918a3abf7fe7480f3491260b6939bc093b40232`  
		Last Modified: Thu, 02 May 2024 17:53:34 GMT  
		Size: 258.0 MB (257992149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:406577ad4a920a84505e527616fcb1f008cff2e259737b980109d6586c441132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94959a9ba35ac8e7aa52d2c9634583789f540a6ce1cdf8970c1aeafbeb383266`

```dockerfile
```

-	Layers:
	-	`sha256:5fccb080d41ea034eca85abe7287cd6513b3fcf1304c5b0ab744b5e4f7604ee2`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5ee26d72cca7cd34f6faa2688b32a264613f3b88beb239a82737e7a7bdd0b8`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:ea7984b98ee3317d77412b9077362d5f7934cbed7f5d5ce18a977f899e9386c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288845524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a166a0772dcf6517a472407901b610b01b80c50d7487fd756971dc08ca26d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bdd5b65845940ee92c4225121c6b04def8a421d1c550f7d8d65db0e37bf19`  
		Last Modified: Thu, 02 May 2024 18:15:05 GMT  
		Size: 255.7 MB (255704323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b8cf1c2e22630a3fb96504ce4e0109e450e2f91f2338965264da180dffb4be0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e443bda8941eefcf331e18425d4d04513900c67b623379aae5f5c3ba60799f`

```dockerfile
```

-	Layers:
	-	`sha256:57c7d4ef78d8836d083ed51f7584a8611e874b74c989c77cbdaefba43cf9c737`  
		Last Modified: Thu, 02 May 2024 18:14:59 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721e6450ded9a8224165692a227cf32021b20727fa9e27b7eb51b9ee46c98d64`  
		Last Modified: Thu, 02 May 2024 18:14:58 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:f2f85fb1ee50bb9ddd8312a215bd06ef84d9d8a32ae978df573ac5b9b84ab38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337865924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2db01fe12c831f8b1c810ff63f0059a28b15cebb3fc607f041e7f43ba47394a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c36f802355139032b4b3b2815d90b8684055c93beadd105d203de5c4574421`  
		Last Modified: Thu, 02 May 2024 18:19:38 GMT  
		Size: 310.4 MB (310353569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1d010d6d80dc73fcb8b111939211fe047c868a66965107fe6522c5ac238f2882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67848fc2610daa3a0488587b7d72d3197b8f69b13b8bc20914dec3e53cac68c4`

```dockerfile
```

-	Layers:
	-	`sha256:45465cb45a531518db8458bf81a4591118d814a4fcc27d32e893ed00128240f1`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 3.8 MB (3762075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ba7b0835f73f3eba7b3413925b87bc83556d2ccd55606dfd68c5715cec19c7b`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78-slim-bullseye`

```console
$ docker pull rust@sha256:33baf245a3be288ec45d6534ebf94de088b834ef9202fd8e1176a3c1a0d9b730
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

### `rust:1.78-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:ebd24f6078bcc9f6b23f99a23e450f07d593f570d4bf072b5077added128bf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268954860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0502ee249ca6bfa22cfade789d5296feac6f0928a18703146f522c7cbf7ced10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e70c0d176523de333ba6a5be57344d80ccfba2589ed97a0714e502d2a34ca43`  
		Last Modified: Thu, 02 May 2024 17:53:20 GMT  
		Size: 237.5 MB (237520597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a4dcfa88f53f7b2928efe6b3b835f897d81e20fddd853c43354998e2e042cabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ef9d771e215a52ef1e40b292ede0d829c632e49e4c2367b41dac17ea648ac2`

```dockerfile
```

-	Layers:
	-	`sha256:cef011c9722bb44d4620b4e6bf096623230158399e11cb7d6d6f6c1a1af4bd58`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 4.1 MB (4139833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599c91eec4cbd0f1ff1398eba0b589af02754a51f58dcd99213c8a7b227dac30`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 12.0 KB (11983 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b2d51c493ce70a6df64cc9294f39b991ed51caad0d1b6b4df3aa73ebc0059308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281482631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1845601085edf0de75fa06cb3587d42cc4e40938d1b8a5f3ee758b9356526b5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb88c27c011a0bf4095b4dad73f3b89a8b7d5926dd1b563ef8b60cc2f6c06c3`  
		Last Modified: Thu, 02 May 2024 18:13:56 GMT  
		Size: 254.9 MB (254887889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ede45ee3c4bebfd74b4c54b87023ff6f1af70c483ef9065a07b00b14ba55e7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb61ef780ac05b5018cad0ca9872b446a694f9a1b4446f0d1738749ea277525`

```dockerfile
```

-	Layers:
	-	`sha256:f821ed482f1443a1e918b75b417cb399f4cdb75370c37d86cca0be80d3b3b835`  
		Last Modified: Thu, 02 May 2024 18:13:50 GMT  
		Size: 3.9 MB (3949756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e6fac619e4f33ae52bdc1063f1d01d4404064b385b8d19745a745c85900723`  
		Last Modified: Thu, 02 May 2024 18:13:50 GMT  
		Size: 11.9 KB (11887 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:55184f8e235a387dc47570d3c45c18868da64c7441759ff319bb02b00a30dd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331830874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2efb3db0f1f86b252af2ac6422352121d26077fc46501dc669c95b75f8b7e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a148bfdb5477b5b28e8af64d0d2c9d4cd738688d1ec0104833fc0685436c0c3`  
		Last Modified: Thu, 02 May 2024 18:23:57 GMT  
		Size: 301.7 MB (301743538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:47addcc74cfa8ab7f351d70c100db444ad71814d83f6c96928b852f42598e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0390a7297d4caf490960ab4c3265747cbbd92e4748bed00b3c994f72c02f2`

```dockerfile
```

-	Layers:
	-	`sha256:0508b7e94192ab544e987c54492b371e546f31d0f9919bc0c8cc1c452aa454c4`  
		Last Modified: Thu, 02 May 2024 18:23:49 GMT  
		Size: 4.1 MB (4136713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dccf37e519bcea3696ecfb195e4a0b38348a412004399eb8308b338effdba8b`  
		Last Modified: Thu, 02 May 2024 18:23:48 GMT  
		Size: 11.8 KB (11827 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b189e96e3c85ca97178eb44feb77efb715773ecfe115c08226820247f7cd4371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283597724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d042e33fb45d8dbb5ab9375e1f445cca9f0842403742ac8e16e14a492d1379b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:20 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Wed, 24 Apr 2024 03:39:20 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d994d194bfa3acf9a46df705316048a9e421612eb43dc8e67d2fc7c4b47dc8cd`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 251.2 MB (251172951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:23c07842a4cfddec1e1f1e230639073243847f2eb36626a93f578ed729e42f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9ef9f2ac9c96e93217e0d144744e8d8278050716ca0834c70afa220c7c8939`

```dockerfile
```

-	Layers:
	-	`sha256:80add452afc9acafbae3ebdaf81b51e772270d4168261abc531caa3d40d6f8f2`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 4.1 MB (4131887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9032987821a421011b12f5c932db84722ec77469e7d51d50c7f52fc9d678ac72`  
		Last Modified: Thu, 02 May 2024 17:53:17 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:f231b14bfd93102c404e608edce59336c32bbf5bc5b16dde3b83c3b3058aa530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277263350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6022c77c11237120364d8daebc5e4a7f79b239f345aadfe10e08162f3991d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a8be3c69cc41100693d385b45a719b06420c1a8633ddefd2cd065116e4a80f`  
		Last Modified: Thu, 02 May 2024 18:10:20 GMT  
		Size: 242.0 MB (241951625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1bb874168defcf306f4d12a18fa1d1a431164a64175ab74ccc234d19145dafe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf50d0079f8c3085c91f49970a4c034af187ead7b500a47212bad01b95a54c4`

```dockerfile
```

-	Layers:
	-	`sha256:c87e1c0879f136a39e78ff54f5cea16d36b7126d98ada10edad69ab8afe45793`  
		Last Modified: Thu, 02 May 2024 18:10:13 GMT  
		Size: 4.1 MB (4100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee003b3c784435c5aab66ccdc806e9767a27f9edd3cef32418dbc7142a51ac6`  
		Last Modified: Thu, 02 May 2024 18:10:13 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:a4b95ec70b2c183bd9cd02364c93389c429f8ff07d8a86c91e8830923039acc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332291021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08e265a0280e57d06e189c5f7c3e1e12b10bb2d5eb9c7e0f2004ac291a514f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:03 GMT
ADD file:acaea4e054f1ab7ae5cbc8f02c73b546c367aebfcc48c7fb4f0dd9f3628bc25e in / 
# Wed, 24 Apr 2024 03:44:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6f588995519e0e04ef4c150b91ad96c3c85667869db0ad72e5a78d4fab796e70`  
		Last Modified: Wed, 24 Apr 2024 03:49:47 GMT  
		Size: 29.7 MB (29673934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784d1c6d27c0fa82885a8be868f2c1ed573b39823970c4d06846ef9b4058af1e`  
		Last Modified: Thu, 02 May 2024 18:12:25 GMT  
		Size: 302.6 MB (302617087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ee3b2c41de9bf97e7b05b8905fb5d0e70b4d8b48dcdbd11a87197a0e8af288de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fa73fb55843e1fc73565ef3eb0db89dd88c65c76748308419e9a61dddb5569`

```dockerfile
```

-	Layers:
	-	`sha256:8de35856b398f950ff03181d5960ac2487203d9e917fd71ab33559d927b58a50`  
		Last Modified: Thu, 02 May 2024 18:12:20 GMT  
		Size: 4.0 MB (3972037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad823fcf4f244656c879ab7e131ca3a63d49fb60f964019942d1d0722a7aef41`  
		Last Modified: Thu, 02 May 2024 18:12:19 GMT  
		Size: 11.8 KB (11817 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78-slim-buster`

```console
$ docker pull rust@sha256:d30c7ad62c2044e0d1174d742f0efbc02c1e43aea988193b6686ee8aaaf79170
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

### `rust:1.78-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:562d6f211888cbd784790e7fb47d3cea4b20480634543579297832b7fd1c25a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250335520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6261cf21c8a87571e9f4b502375b16f30e624d67d46e199388cdf0bc36235`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906e6ed35d183754f56330a654a033329ee5826a5608612dde75a12c80dfbda`  
		Last Modified: Thu, 02 May 2024 17:53:08 GMT  
		Size: 223.0 MB (222997945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e7b9c6cdb9dc891a721e37b31279d12f59a2aeaa33d3a50cd04c15ed9fdac0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a326d7714ebb85020a2b5bc3eb2f017a246b9349e259e29adf9cf787cd097`

```dockerfile
```

-	Layers:
	-	`sha256:3d7cefbfd3006121cdf982e776f479a01d0119707b7d9103dd24cdb58f580975`  
		Last Modified: Thu, 02 May 2024 17:53:05 GMT  
		Size: 3.9 MB (3941693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca2968425f2c6d21765305834771a5c51369246bdfafc5ca52300a944a9f50d`  
		Last Modified: Thu, 02 May 2024 17:53:05 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:94dda1ea419d69d0e38543407f33117c87a59c53c8e45b2fa3729496d76462c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268702412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb522a78fe20e96dd37a3094bd8201f8bc75d59d78c8672653761f8389e82b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab99a29678006ca048ee3cec2a39dd336045cbef1f173b20313118c42dcc53f3`  
		Last Modified: Thu, 02 May 2024 18:09:45 GMT  
		Size: 245.8 MB (245757348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:870cd6eb7305f07b9e0a9384fb585ac261058d1821c291dae7d3e76c80bb744a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4231130c9d88f75df6ed09cac4d31aa678269b42aa3df4dabb3e9675ce564037`

```dockerfile
```

-	Layers:
	-	`sha256:2dc32a76ad84dbf82ef236a5ee11a01cd7c24687433eb86f7be3f1cfa7568a9b`  
		Last Modified: Thu, 02 May 2024 18:09:40 GMT  
		Size: 3.7 MB (3749343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cd37df8a47dfdf9952876a899f07158606f3fe042c2c85d5825fd83d506bf7`  
		Last Modified: Thu, 02 May 2024 18:09:39 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:489aac5b79003a727f4571932d0a03b2aa17db922cca485942fe79de33c5cb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312574944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fc5383529ef82de9ea2eb11d095ad1d1f517c836bc95f1ecc709194a04799d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:06 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
# Wed, 24 Apr 2024 04:11:07 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62497221c4fce50e070a112fde5ee41270ed6a3a085e7b1825fd24a956f1f4c7`  
		Last Modified: Thu, 02 May 2024 18:20:54 GMT  
		Size: 286.5 MB (286465114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:612bde9c6fe77167e879e6f3787a339655d4b7a1cbfa4ce1d3731711d4aa5508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6441cb64ca635d2e44dba773323ae3d87e7f6d0d4f4aee982365fa0652812d06`

```dockerfile
```

-	Layers:
	-	`sha256:e2fb474d4ff49f24441eccc92c2f1c16d30efe46b4c082a210ed49e145d5e5ee`  
		Last Modified: Thu, 02 May 2024 18:20:47 GMT  
		Size: 3.9 MB (3930985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80129d72be4749680a0777a4fb88afb3ad6bfae867c9ae93c316ad94e7112176`  
		Last Modified: Thu, 02 May 2024 18:20:47 GMT  
		Size: 11.2 KB (11234 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:862f761b55bdfb9b687ccd73c39ea5db75ab570112ac0d7d9da5f5c5196dc67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268610066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12d3e0efa5e20f2dffb6cca638c9d030e51183e0ed6dea06200bb6fa61abb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:39 GMT
ADD file:32f0f06baa0e4f10bff55aaa215b511838432ecc5fe547373d9ac99494556801 in / 
# Wed, 24 Apr 2024 03:39:40 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:204b51fc41806ed93b4ccb6ce8272fa49b5f0b099ba6e3b5a940a9e7cd3ce202`  
		Last Modified: Wed, 24 Apr 2024 03:45:03 GMT  
		Size: 28.0 MB (27994678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3981a552b28468ee69108184598097965a5265b74ad064e8e657f3897f599f3`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 240.6 MB (240615388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:4a7ce102abb3a846743437756ea063f781583ab5bea6f40c2612550634e10222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb6026b631db1e909e1f420b7086445db95e1f00ef7bc7c365ad507c9a54fdb`

```dockerfile
```

-	Layers:
	-	`sha256:2e03fc3bfe125dba62e18faebb42c04d798624900a87a5dc953c3be75072510d`  
		Last Modified: Thu, 02 May 2024 17:53:10 GMT  
		Size: 3.9 MB (3948318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e394e2a792e8d275adc332b5b935d4c9db65a83fe54fda94e7437645d5b02114`  
		Last Modified: Thu, 02 May 2024 17:53:10 GMT  
		Size: 11.2 KB (11195 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78.0`

```console
$ docker pull rust@sha256:0dd183faf7bc5b9b8efe81cfd42701a5283577520b185b511e322e5bf52f8fc7
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

### `rust:1.78.0` - linux; amd64

```console
$ docker pull rust@sha256:d50e312c75fbd66f5cc7b1ab6d76892529751526629c294f34ca217016fe0425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526535638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d8eec96e0ea00b3ec3c6c2e03ef8a15113d8dd0682170d3757c06a78e73dce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:6b9f9d886ac307c9982286da0ae1d85ad364df502e05f2c5c14c9505f30a4feb`  
		Last Modified: Thu, 02 May 2024 17:53:26 GMT  
		Size: 177.6 MB (177591491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0` - unknown; unknown

```console
$ docker pull rust@sha256:9d352cd5f6a779bed1be7057ea6557c8de8f96c40e26e555b469d2c2f8405643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15384104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511f0cc56710400a858b2b313a1fb6c554e2ca7debcdcfd5d6ae3ac4870e716f`

```dockerfile
```

-	Layers:
	-	`sha256:f4420d9292d76286420dd7187c5b08b956041f3a4d90ecee23f7d1f91f3638ac`  
		Last Modified: Thu, 02 May 2024 17:53:24 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6daf94a67a74ecaca457f9fc6812857963aae03a4bdf69ffece0604d2d071e2c`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 13.6 KB (13580 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0` - linux; arm variant v7

```console
$ docker pull rust@sha256:225556750412cc8f6f468fd8c3bd1176e9b06c90153acb0e045b500c21265bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514307156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d9947ff3490d7e91dbee0aade813ded906312a29924c5226904b76432127e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07170ec327fa1117b5289697e5555f4c3ba76d00200d7c7cc5c143086856f`  
		Last Modified: Wed, 24 Apr 2024 05:03:03 GMT  
		Size: 59.2 MB (59216995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937bd8fccb438207fe0e77a48873de07dbe1fbea251206222298b72dbd2b3d8`  
		Last Modified: Wed, 24 Apr 2024 05:03:45 GMT  
		Size: 175.1 MB (175141109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499a6710f841b95850a0e6c3589a558408d5ecdb1efe2d461015241a86667d9`  
		Last Modified: Thu, 02 May 2024 18:16:14 GMT  
		Size: 212.8 MB (212820090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0` - unknown; unknown

```console
$ docker pull rust@sha256:a8d872088f3bc18ac36bb4ee06e93eac69f16897387344fcfd238be07505d19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15189426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f357e10dda11cec2f915422dbbb7f4dc9ef73032fc8aa82efe6609b3de03843`

```dockerfile
```

-	Layers:
	-	`sha256:67f172e545903f27510fe2841e22b7f07947e3314640824e648cc35a5e4af23c`  
		Last Modified: Thu, 02 May 2024 18:16:09 GMT  
		Size: 15.2 MB (15176407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becad9a5634f77e5e49e5e8f1bda8454cd92e0059d86c4ae3e43d13bba5c36d9`  
		Last Modified: Thu, 02 May 2024 18:16:08 GMT  
		Size: 13.0 KB (13019 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cb3fe1b45243325da5aaafb59bc75f8541697bfd9acbfedc914c0f132c7949ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.0 MB (586021653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b44c56b25c83977fc9ebfdf243d37b0b15ab1a4fcf0c647f0878847949cf84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476478a1e1450b999421118cb8f193aa62f1816e0cadd988a084385cf0a5696`  
		Last Modified: Wed, 24 Apr 2024 08:42:20 GMT  
		Size: 202.6 MB (202575289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ab2e8f65d41c1e5e2c493944dc3f6ca456b65a5275ac05e12bc31af0b697d`  
		Last Modified: Thu, 02 May 2024 18:26:37 GMT  
		Size: 246.3 MB (246251422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0` - unknown; unknown

```console
$ docker pull rust@sha256:9562e2467c5e3f2f6ee0ccff2633f57a5ff3cd388a582fca74510f46aba072bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6aaf4016fa5c395bc612fd990fc2d7422e8623e54ebe02b7b2625e179f7920`

```dockerfile
```

-	Layers:
	-	`sha256:1c4d0653a7e064d93a08cf2e3cb73351a07d67c388a1a2590326a06812bff5f3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 15.4 MB (15399046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790e84f88528ef27e0f653b5aeba1fafd203db38ba551366c785a778180828b3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 12.9 KB (12935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0` - linux; 386

```console
$ docker pull rust@sha256:d1f3c3a8b571383507c4e76f99678f065d5a03aa90eea84693c767e32fc869c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542180953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009dec677b8280c20069beef31c3fbbbc461bc0ab36f0558b2ec40439a5f6079`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:48 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Wed, 24 Apr 2024 03:38:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:29:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:30:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:1614889c1e665cd335548134ca677fb6f9f1910d4ab6488c04424418a97f495a`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 190.6 MB (190599211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0` - unknown; unknown

```console
$ docker pull rust@sha256:de08ac7a06b5af621f4e0fb99dabf08168a533017d45b6ff2510485f17d0b355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15363096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc533d073cc58cb332d3410a63a6c6f32d775b9febedb13c3c8b78a6d6079a9`

```dockerfile
```

-	Layers:
	-	`sha256:64ac9f5f1c25c9fffc99c099a79689856019c48dfffddbb43b51cba223012a11`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921284eb6647f818f95a3f3db77efe9fa3b4c28d2bf2158f08f1c984fe96fef0`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 13.5 KB (13531 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0` - linux; ppc64le

```console
$ docker pull rust@sha256:eb08c0b17cc0c417388189ce35bf4fb1f087a9e6ff51c1bfcec9ff410f2a8733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.2 MB (550221275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3bcff95d0b422fd84f7fcd46bf86991ba30fb41078803b6b6f6722b17322d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:20:52 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Wed, 24 Apr 2024 03:20:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:a6e8bb341b139fa8aae0ba05045cf5f0ef66e8260b98cda6950cadf916ed0f41`  
		Last Modified: Thu, 02 May 2024 18:12:45 GMT  
		Size: 187.1 MB (187143091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0` - unknown; unknown

```console
$ docker pull rust@sha256:7903613b4182abe216e7e36c9ee4ae650fe4a14316160360cdd8f94e459cf946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbc8ff473cd3ae52f9b1427e15706fae4d3d9591a2c8bf3f28b31a19f1a09c4`

```dockerfile
```

-	Layers:
	-	`sha256:6c78d4a4191a65c7af0530480d11f289861eab1ee86584e8133ba9ae8bb2de48`  
		Last Modified: Thu, 02 May 2024 18:12:41 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef473a7f3ff3cbb5e5bff01f89d91164174143787bc52b54999cd47006cd918`  
		Last Modified: Thu, 02 May 2024 18:12:40 GMT  
		Size: 13.0 KB (12979 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0` - linux; s390x

```console
$ docker pull rust@sha256:35a2f27aa7b8300d5a2e4aed602e03edcc950d6dcfbd9d7f8b8a86be19752041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578756361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008c354d831f826547ccd2d2a946c706ca40e6916ef33806ecaa916a21041dd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:42:45 GMT
ADD file:6b0e091009ac95d80973222b4f56557fc521253f20bb18eea1c9da2b61ed5cc2 in / 
# Wed, 24 Apr 2024 03:42:53 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea1cd174fa855055f0cc0296260c9e987dbd4cddfc8655fe48891b91e5af95b7`  
		Last Modified: Wed, 24 Apr 2024 03:48:59 GMT  
		Size: 47.9 MB (47942206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e212650b3684bdd95eb8c4cd55ad81ca7f992455cbcc5c126d1aac521b5399`  
		Last Modified: Wed, 24 Apr 2024 04:23:04 GMT  
		Size: 24.0 MB (24047036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5049d590d068e07d3557ef371a6ccc2fc96ffadeabbf0c1115204536ff84b`  
		Last Modified: Wed, 24 Apr 2024 04:23:21 GMT  
		Size: 63.1 MB (63130514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74409f156b70503c3e2227e45d964aec57dadc484e6492078584c8cad2e0884f`  
		Last Modified: Wed, 24 Apr 2024 04:23:50 GMT  
		Size: 183.2 MB (183208845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0a40d21a23b6b34012eaf7b342b43911c5d236a2f478d1df55a213f5b8247d`  
		Last Modified: Thu, 02 May 2024 18:17:05 GMT  
		Size: 260.4 MB (260427760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0` - unknown; unknown

```console
$ docker pull rust@sha256:70d0ae53ab927ca2824b1543a39761aaa621f8f640351e84e30c9cffcdada927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e4231ef234646dcaa8923b11a5a42334f73cdcc3a2467a2ef8ea47342e8f4`

```dockerfile
```

-	Layers:
	-	`sha256:2d98932b6c77d39b088f5fb17d27824d35fa3db3a89f0dc9677db81f3f0b219b`  
		Last Modified: Thu, 02 May 2024 18:17:02 GMT  
		Size: 15.2 MB (15185203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9bb7ba18a7a3be562faf0170f9215c5065bafb098b5bf71c12feccc9dce19c`  
		Last Modified: Thu, 02 May 2024 18:17:01 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78.0-alpine`

```console
$ docker pull rust@sha256:d4d3f81f3111991353bd7c7fa513ad3725a27027575fd82e24fb7babcd8f26f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.78.0-alpine` - linux; amd64

```console
$ docker pull rust@sha256:41bf7d335c39fd25bb73f3183713b1fdcb77f0fc70def6634e40992e66119292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276648359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9be41f0a10e18d4183096b0d91821b4f93cd1eb4e4884a8fd5fdc8b7ee34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c6c611323bdd864b20f293097226e373d0e34b9108e12e65481c955804c26`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 55.3 MB (55346841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245c9984f45dd6d2464604e214a0391a1b399705f140a8b96469f84d6e1f61e`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 217.9 MB (217892789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:8be526e7cb5aa9bc6b6d8c73fb8ee6e81a9c8164a4c5bfa97533ab5bfc0b6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcc214e8f56925c61fb2680fb60504b652116af551962b9d82c4683a88dc59`

```dockerfile
```

-	Layers:
	-	`sha256:f47a0d5a9bacd02cd11840d2f1a2adc07cd5bdb00e97770f9c417e49c8d49f29`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 710.6 KB (710621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232259c5160cb554f445085a6e5765832b7c088ca5c17fa09d0fb5f2a2dda48`  
		Last Modified: Thu, 02 May 2024 17:53:11 GMT  
		Size: 11.8 KB (11794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b7075f2ddfde9ede284e71e74bade0576f8ea97e0f49b2c8a4ead2a101a1cc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282899712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ab7c4bfc7646c65e0a623ab2551468819a7e5047057601317c046321a3c6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1475e7bc8776b6a5d5098e107869ccf04a61b48d632658ab4bf934b5340337c2`  
		Last Modified: Thu, 02 May 2024 18:30:18 GMT  
		Size: 53.0 MB (52995527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3cbfb4539306a5cd558b71b91000e4f05d22445cf79e04281bf881f3bfd22`  
		Last Modified: Thu, 02 May 2024 18:30:21 GMT  
		Size: 226.6 MB (226556470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f02f381f9fa338bae9204fb7e52a19b44779316d227092aa2fb77ea0a62cea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.2 KB (758219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e2876b12a57c6260b8a220b6a82f40ccb6b3f85bced4f5e908a46f1175e9c`

```dockerfile
```

-	Layers:
	-	`sha256:0f5adf947b65a86f48dfa44a9462e156913eca4be72ad307f8b70e63904defcc`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 746.6 KB (746571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd319de530a5221d01b41f952f79922b81a42473dd697d14646929354af7f96c`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 11.6 KB (11648 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78.0-alpine3.18`

```console
$ docker pull rust@sha256:34f1c35f62e192f39cd0c809982bf90c354f7e5746682a2f4c9e4c43bd516dbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.78.0-alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:909cfdd11b0a96aa82d86c96c17cddf3864bca150a6228d18ab6a658e7006d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272829333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787b53dee543c9d07c38258423856c4ce44a7bb0e10dd80b6ce8d3d6be6d688b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d8cca761111b3832e2234b2a7c144570d1ceaa6a6eab4447a39633b2a0c9e6`  
		Last Modified: Thu, 02 May 2024 17:53:03 GMT  
		Size: 51.5 MB (51534006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94392fe86146798eeda301677559c748ac0525075773894cb651ef44b47f89cf`  
		Last Modified: Thu, 02 May 2024 17:53:06 GMT  
		Size: 217.9 MB (217892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:828ea566785e422ca858dcd98738715dc31eb43e85aa4ac91f75e0f3c0d1a46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13ead6d1e1a8601c572bfe57d56165b246d74fecdc009ab88410fe102fdb904`

```dockerfile
```

-	Layers:
	-	`sha256:022a488b72ff619b6be7c5b9d74e5a88f50c0e8179a478751063a2baa139c1ca`  
		Last Modified: Thu, 02 May 2024 17:53:02 GMT  
		Size: 701.9 KB (701890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d53ac36334ec5e522ca13debbc666b6df6ad9bb97c9efa7639b75bec875183c`  
		Last Modified: Thu, 02 May 2024 17:53:02 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ee1d16c1cc031559875424b27cb090136df31c18dd9e97966cf12391b59ba403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (275971039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0325d780023f87c7f06c8d7e4ee3aadb87e82528ad4b2da06a341cc8e42438bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecadc98c87cbba10a8cd3e79aee52d2aa3670ae6272cc2b29b27128e710a536`  
		Last Modified: Thu, 02 May 2024 18:29:15 GMT  
		Size: 46.1 MB (46081224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688cf2745b0216764a0d813aa9bf3d0c02af25fae1ef4c9bfce32c558a0d640f`  
		Last Modified: Thu, 02 May 2024 18:29:18 GMT  
		Size: 226.6 MB (226556454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:a6e2823b379b899207fbbdc6d8f2181cb7668892e2f31ce8f272302781d6a274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.1 KB (752144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa78da9cdd7dc3787e280f8a86f29faba9f60305898cf6d9486dc01fdc2def2`

```dockerfile
```

-	Layers:
	-	`sha256:2508e1ec9f010359afe8d8e516417a297aa32d170c071185c0be86d2c697cb2f`  
		Last Modified: Thu, 02 May 2024 18:29:13 GMT  
		Size: 741.7 KB (741708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af17300661fa62bda831f09a0938360f387b14cb172b980a435cff240801bee8`  
		Last Modified: Thu, 02 May 2024 18:29:13 GMT  
		Size: 10.4 KB (10436 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78.0-alpine3.19`

```console
$ docker pull rust@sha256:d4d3f81f3111991353bd7c7fa513ad3725a27027575fd82e24fb7babcd8f26f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:1.78.0-alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:41bf7d335c39fd25bb73f3183713b1fdcb77f0fc70def6634e40992e66119292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276648359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9be41f0a10e18d4183096b0d91821b4f93cd1eb4e4884a8fd5fdc8b7ee34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c6c611323bdd864b20f293097226e373d0e34b9108e12e65481c955804c26`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 55.3 MB (55346841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245c9984f45dd6d2464604e214a0391a1b399705f140a8b96469f84d6e1f61e`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 217.9 MB (217892789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:8be526e7cb5aa9bc6b6d8c73fb8ee6e81a9c8164a4c5bfa97533ab5bfc0b6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcc214e8f56925c61fb2680fb60504b652116af551962b9d82c4683a88dc59`

```dockerfile
```

-	Layers:
	-	`sha256:f47a0d5a9bacd02cd11840d2f1a2adc07cd5bdb00e97770f9c417e49c8d49f29`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 710.6 KB (710621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232259c5160cb554f445085a6e5765832b7c088ca5c17fa09d0fb5f2a2dda48`  
		Last Modified: Thu, 02 May 2024 17:53:11 GMT  
		Size: 11.8 KB (11794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b7075f2ddfde9ede284e71e74bade0576f8ea97e0f49b2c8a4ead2a101a1cc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282899712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ab7c4bfc7646c65e0a623ab2551468819a7e5047057601317c046321a3c6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1475e7bc8776b6a5d5098e107869ccf04a61b48d632658ab4bf934b5340337c2`  
		Last Modified: Thu, 02 May 2024 18:30:18 GMT  
		Size: 53.0 MB (52995527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3cbfb4539306a5cd558b71b91000e4f05d22445cf79e04281bf881f3bfd22`  
		Last Modified: Thu, 02 May 2024 18:30:21 GMT  
		Size: 226.6 MB (226556470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:f02f381f9fa338bae9204fb7e52a19b44779316d227092aa2fb77ea0a62cea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.2 KB (758219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e2876b12a57c6260b8a220b6a82f40ccb6b3f85bced4f5e908a46f1175e9c`

```dockerfile
```

-	Layers:
	-	`sha256:0f5adf947b65a86f48dfa44a9462e156913eca4be72ad307f8b70e63904defcc`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 746.6 KB (746571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd319de530a5221d01b41f952f79922b81a42473dd697d14646929354af7f96c`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 11.6 KB (11648 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78.0-bookworm`

```console
$ docker pull rust@sha256:0dd183faf7bc5b9b8efe81cfd42701a5283577520b185b511e322e5bf52f8fc7
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

### `rust:1.78.0-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:d50e312c75fbd66f5cc7b1ab6d76892529751526629c294f34ca217016fe0425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526535638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d8eec96e0ea00b3ec3c6c2e03ef8a15113d8dd0682170d3757c06a78e73dce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:6b9f9d886ac307c9982286da0ae1d85ad364df502e05f2c5c14c9505f30a4feb`  
		Last Modified: Thu, 02 May 2024 17:53:26 GMT  
		Size: 177.6 MB (177591491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9d352cd5f6a779bed1be7057ea6557c8de8f96c40e26e555b469d2c2f8405643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15384104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511f0cc56710400a858b2b313a1fb6c554e2ca7debcdcfd5d6ae3ac4870e716f`

```dockerfile
```

-	Layers:
	-	`sha256:f4420d9292d76286420dd7187c5b08b956041f3a4d90ecee23f7d1f91f3638ac`  
		Last Modified: Thu, 02 May 2024 17:53:24 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6daf94a67a74ecaca457f9fc6812857963aae03a4bdf69ffece0604d2d071e2c`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 13.6 KB (13580 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:225556750412cc8f6f468fd8c3bd1176e9b06c90153acb0e045b500c21265bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514307156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d9947ff3490d7e91dbee0aade813ded906312a29924c5226904b76432127e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07170ec327fa1117b5289697e5555f4c3ba76d00200d7c7cc5c143086856f`  
		Last Modified: Wed, 24 Apr 2024 05:03:03 GMT  
		Size: 59.2 MB (59216995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937bd8fccb438207fe0e77a48873de07dbe1fbea251206222298b72dbd2b3d8`  
		Last Modified: Wed, 24 Apr 2024 05:03:45 GMT  
		Size: 175.1 MB (175141109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499a6710f841b95850a0e6c3589a558408d5ecdb1efe2d461015241a86667d9`  
		Last Modified: Thu, 02 May 2024 18:16:14 GMT  
		Size: 212.8 MB (212820090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a8d872088f3bc18ac36bb4ee06e93eac69f16897387344fcfd238be07505d19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15189426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f357e10dda11cec2f915422dbbb7f4dc9ef73032fc8aa82efe6609b3de03843`

```dockerfile
```

-	Layers:
	-	`sha256:67f172e545903f27510fe2841e22b7f07947e3314640824e648cc35a5e4af23c`  
		Last Modified: Thu, 02 May 2024 18:16:09 GMT  
		Size: 15.2 MB (15176407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becad9a5634f77e5e49e5e8f1bda8454cd92e0059d86c4ae3e43d13bba5c36d9`  
		Last Modified: Thu, 02 May 2024 18:16:08 GMT  
		Size: 13.0 KB (13019 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cb3fe1b45243325da5aaafb59bc75f8541697bfd9acbfedc914c0f132c7949ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.0 MB (586021653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b44c56b25c83977fc9ebfdf243d37b0b15ab1a4fcf0c647f0878847949cf84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476478a1e1450b999421118cb8f193aa62f1816e0cadd988a084385cf0a5696`  
		Last Modified: Wed, 24 Apr 2024 08:42:20 GMT  
		Size: 202.6 MB (202575289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ab2e8f65d41c1e5e2c493944dc3f6ca456b65a5275ac05e12bc31af0b697d`  
		Last Modified: Thu, 02 May 2024 18:26:37 GMT  
		Size: 246.3 MB (246251422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9562e2467c5e3f2f6ee0ccff2633f57a5ff3cd388a582fca74510f46aba072bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6aaf4016fa5c395bc612fd990fc2d7422e8623e54ebe02b7b2625e179f7920`

```dockerfile
```

-	Layers:
	-	`sha256:1c4d0653a7e064d93a08cf2e3cb73351a07d67c388a1a2590326a06812bff5f3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 15.4 MB (15399046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790e84f88528ef27e0f653b5aeba1fafd203db38ba551366c785a778180828b3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 12.9 KB (12935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-bookworm` - linux; 386

```console
$ docker pull rust@sha256:d1f3c3a8b571383507c4e76f99678f065d5a03aa90eea84693c767e32fc869c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542180953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009dec677b8280c20069beef31c3fbbbc461bc0ab36f0558b2ec40439a5f6079`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:48 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Wed, 24 Apr 2024 03:38:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:29:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:30:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:1614889c1e665cd335548134ca677fb6f9f1910d4ab6488c04424418a97f495a`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 190.6 MB (190599211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:de08ac7a06b5af621f4e0fb99dabf08168a533017d45b6ff2510485f17d0b355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15363096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc533d073cc58cb332d3410a63a6c6f32d775b9febedb13c3c8b78a6d6079a9`

```dockerfile
```

-	Layers:
	-	`sha256:64ac9f5f1c25c9fffc99c099a79689856019c48dfffddbb43b51cba223012a11`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921284eb6647f818f95a3f3db77efe9fa3b4c28d2bf2158f08f1c984fe96fef0`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 13.5 KB (13531 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:eb08c0b17cc0c417388189ce35bf4fb1f087a9e6ff51c1bfcec9ff410f2a8733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.2 MB (550221275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3bcff95d0b422fd84f7fcd46bf86991ba30fb41078803b6b6f6722b17322d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:20:52 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Wed, 24 Apr 2024 03:20:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:a6e8bb341b139fa8aae0ba05045cf5f0ef66e8260b98cda6950cadf916ed0f41`  
		Last Modified: Thu, 02 May 2024 18:12:45 GMT  
		Size: 187.1 MB (187143091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7903613b4182abe216e7e36c9ee4ae650fe4a14316160360cdd8f94e459cf946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbc8ff473cd3ae52f9b1427e15706fae4d3d9591a2c8bf3f28b31a19f1a09c4`

```dockerfile
```

-	Layers:
	-	`sha256:6c78d4a4191a65c7af0530480d11f289861eab1ee86584e8133ba9ae8bb2de48`  
		Last Modified: Thu, 02 May 2024 18:12:41 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef473a7f3ff3cbb5e5bff01f89d91164174143787bc52b54999cd47006cd918`  
		Last Modified: Thu, 02 May 2024 18:12:40 GMT  
		Size: 13.0 KB (12979 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:35a2f27aa7b8300d5a2e4aed602e03edcc950d6dcfbd9d7f8b8a86be19752041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578756361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008c354d831f826547ccd2d2a946c706ca40e6916ef33806ecaa916a21041dd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:42:45 GMT
ADD file:6b0e091009ac95d80973222b4f56557fc521253f20bb18eea1c9da2b61ed5cc2 in / 
# Wed, 24 Apr 2024 03:42:53 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea1cd174fa855055f0cc0296260c9e987dbd4cddfc8655fe48891b91e5af95b7`  
		Last Modified: Wed, 24 Apr 2024 03:48:59 GMT  
		Size: 47.9 MB (47942206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e212650b3684bdd95eb8c4cd55ad81ca7f992455cbcc5c126d1aac521b5399`  
		Last Modified: Wed, 24 Apr 2024 04:23:04 GMT  
		Size: 24.0 MB (24047036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5049d590d068e07d3557ef371a6ccc2fc96ffadeabbf0c1115204536ff84b`  
		Last Modified: Wed, 24 Apr 2024 04:23:21 GMT  
		Size: 63.1 MB (63130514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74409f156b70503c3e2227e45d964aec57dadc484e6492078584c8cad2e0884f`  
		Last Modified: Wed, 24 Apr 2024 04:23:50 GMT  
		Size: 183.2 MB (183208845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0a40d21a23b6b34012eaf7b342b43911c5d236a2f478d1df55a213f5b8247d`  
		Last Modified: Thu, 02 May 2024 18:17:05 GMT  
		Size: 260.4 MB (260427760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:70d0ae53ab927ca2824b1543a39761aaa621f8f640351e84e30c9cffcdada927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e4231ef234646dcaa8923b11a5a42334f73cdcc3a2467a2ef8ea47342e8f4`

```dockerfile
```

-	Layers:
	-	`sha256:2d98932b6c77d39b088f5fb17d27824d35fa3db3a89f0dc9677db81f3f0b219b`  
		Last Modified: Thu, 02 May 2024 18:17:02 GMT  
		Size: 15.2 MB (15185203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9bb7ba18a7a3be562faf0170f9215c5065bafb098b5bf71c12feccc9dce19c`  
		Last Modified: Thu, 02 May 2024 18:17:01 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78.0-bullseye`

```console
$ docker pull rust@sha256:2552dc030938db6be68061470bb1d06a614e2523bc28aca5ae3db334fe4b3476
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

### `rust:1.78.0-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:e6d6b30cc542e783d7c99f59c4981a1dfc16854065004dd2031731c1f39bde8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.0 MB (500031479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcad364931eede82edf28ce9a8b0d641d449dfc7c66a5409117906b6b6b8b4ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:13:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:534d57e3d7c23ea864729859cd9639d95758dc80d3fae7c2f1a781369374f72c`  
		Last Modified: Thu, 02 May 2024 17:53:19 GMT  
		Size: 177.6 MB (177591486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:394674afd531ba7ba75772c582acf4520d9dfde25713860cf929548250230b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14987362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd227c9c6937e47e8c7124353322fb9c95d173d5e40454385bc62a5de0a4d204`

```dockerfile
```

-	Layers:
	-	`sha256:5175f4542d292457f1a4530967191286a12c21391a2bb9a183579ff56267c300`  
		Last Modified: Thu, 02 May 2024 17:53:17 GMT  
		Size: 15.0 MB (14974944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da52b512eddefa1c1ecbaaa573257018e0b1790c5832c459900ce53606e1b2a`  
		Last Modified: Thu, 02 May 2024 17:53:16 GMT  
		Size: 12.4 KB (12418 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:04d28c769d11d7e8647f2cb4abc12e4772bf7ac447fdc05e7a6713bf8619ec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.8 MB (495758778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021e7713c700cad89a3873cd2bcb165eeda0cba39d5eac5e6c0ceb0433e2015f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:15 GMT
ADD file:59046a1e0987059e779fff5a0f35e03203c109d778a75058e9474705d3fcfdff in / 
# Wed, 24 Apr 2024 04:07:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:51:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:53:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:853e2341066ebc3a07d3c44ebac8c3ce40daf429fb9cc3f49f2d35115e9cc93f`  
		Last Modified: Wed, 24 Apr 2024 04:11:34 GMT  
		Size: 50.3 MB (50255574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d5c1aa98981d0ab503d79e97e4eeed8435372346757065a98c291d66c74df`  
		Last Modified: Wed, 24 Apr 2024 05:03:57 GMT  
		Size: 14.9 MB (14880390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94741efe025699cbcd617a32ea95a4fea8cfaeedfa3b93bd9cbc7ed02063a74a`  
		Last Modified: Wed, 24 Apr 2024 05:04:17 GMT  
		Size: 50.4 MB (50359575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba251a5fa80ede4ef9bfae4161563b58236318c68e2a17d1cbd5afa4ba9a2c68`  
		Last Modified: Wed, 24 Apr 2024 05:04:53 GMT  
		Size: 167.4 MB (167442932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5d2b6834c7a0899f1680cc6d8cc388f1d0dca62c4f7a8ebe01f44f45352ed7`  
		Last Modified: Thu, 02 May 2024 18:12:01 GMT  
		Size: 212.8 MB (212820307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80b041026f0b46d413060fd8525a3ba151a2eacd151071f8c61fc152cdfd39d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14788669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51b3ef7ff5219f52138329d10cb8348d58ffc8198540c1b328f90fbc8a82ea6`

```dockerfile
```

-	Layers:
	-	`sha256:6c813ccd1a4df3a4bbbbe45bfed024331d0fd2c3308c8a3d7d111ea597aafb5f`  
		Last Modified: Thu, 02 May 2024 18:11:56 GMT  
		Size: 14.8 MB (14776844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19847e3e85938bfccef756d696d053d674fb2f4065a928f39c3451d036e26c9d`  
		Last Modified: Thu, 02 May 2024 18:11:55 GMT  
		Size: 11.8 KB (11825 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:82d27aac8d8758af4166b14ffb1cc316fa08b2fd8cfaf238846ba54bc171e9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.4 MB (560350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423aa11d7bda4aed73983759f01bf96699ace117c8ea8c844c414b738c64bcd7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33008ff0928e624ce22cedd5d004edd66b80372bfd1223e8900206330213ee34`  
		Last Modified: Wed, 24 Apr 2024 08:42:31 GMT  
		Size: 15.8 MB (15750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36972983386f768dbeff5de37af34ed4e2f59541b2e3c43575f29758c3591923`  
		Last Modified: Wed, 24 Apr 2024 08:42:45 GMT  
		Size: 54.7 MB (54696233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3224178d7041e10ec03b66358ce4ba6bb5aeaf26b593f3e8672ca38f7b70769e`  
		Last Modified: Wed, 24 Apr 2024 08:43:09 GMT  
		Size: 189.9 MB (189912094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97275dd0257b83d60c67c3d70971c98640014802ea42bae0e7414eaacf4f365b`  
		Last Modified: Thu, 02 May 2024 18:22:28 GMT  
		Size: 246.3 MB (246251467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cb31ecf48d87fa71df2cb5a2933820e8ecbdd1dbb690d4b5aff13d7fbd87755e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14989175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2aef4675fe30517f9f710edbba6c5a198def25e9b99362e323b7e9b30a6d4d`

```dockerfile
```

-	Layers:
	-	`sha256:eb1b6d19dba8c8c9789a080460223469c5e39861aabf0abb48fe6a856f49572f`  
		Last Modified: Thu, 02 May 2024 18:22:23 GMT  
		Size: 15.0 MB (14977411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed5b26cdc4f076066fac6d6878fca32b53fbe9a0c5bf6b5429bb951a8de7223`  
		Last Modified: Thu, 02 May 2024 18:22:22 GMT  
		Size: 11.8 KB (11764 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-bullseye` - linux; 386

```console
$ docker pull rust@sha256:232c18232dd7076711f3603df35b9bfe483c49663e03b9259edbd30810dfc02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518766287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858075fb8a3b54656c0ee7518ef0b22601a2d1b7d4d1f2fd037699198b2bef9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:08 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
# Wed, 24 Apr 2024 03:39:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:30:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:32:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:df053a23eab4180eece3d17162346216b301343de9fb6226cd226f21702be82f`  
		Last Modified: Thu, 02 May 2024 17:53:36 GMT  
		Size: 190.6 MB (190599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cf1fa86ecf03dd1fbb4dcce34d4a6d575a64d018570476a025626d21108bf3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14976156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0056775c2d4a3ef6fbace0e34ff6db97f0f12ad062f8875c69193a8f497145ad`

```dockerfile
```

-	Layers:
	-	`sha256:189cacbc159513dae1c96778228fcacb8fa5341832b01271f051b1124b140d81`  
		Last Modified: Thu, 02 May 2024 17:53:30 GMT  
		Size: 15.0 MB (14963767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86ac21aeb5f940ce0d749c02477c27d23e1023a107afeb492eedaa85b35f6e8`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 12.4 KB (12389 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:74f6d27411b0fe1655b74893221edde39cc79b5c54f779b8f924d0f94e5b6ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.1 MB (518096210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655131ce8b88722fe88822b0323c0f901ee374ed6e1eb86f90e53c8a0f1031de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:25 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
# Wed, 24 Apr 2024 03:21:30 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:04:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:f315af7fc149bdbb645add44aaef365e14662b9bf33a24ebcdeda2ed49bcef6f`  
		Last Modified: Thu, 02 May 2024 18:07:04 GMT  
		Size: 187.1 MB (187143092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:02041686275df55e6c1cde2ab50a36777b23e5f0bfa0620bcea85ce288d8403d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14954340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c14dc83c058acbfa6bd18b2ba83506e0f719407a324008942f86a2d4dcc87af`

```dockerfile
```

-	Layers:
	-	`sha256:ce1abb7d3006b3e51d88e3b055b4055bbc25212003172c9a9aa9532a8425ad91`  
		Last Modified: Thu, 02 May 2024 18:06:59 GMT  
		Size: 14.9 MB (14942547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c168268955e9148deab9bdffcc4c0a75e9a8cea798c2286a9aab8cdf5599398f`  
		Last Modified: Thu, 02 May 2024 18:06:58 GMT  
		Size: 11.8 KB (11793 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:e3c00ec457a002c90f44ff20936bcfee6bd86f03ab1cc7750785060a7895e5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.5 MB (556478959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3364960915922de42d06974605b4e00f6fc171fd9a6475446ac1f876a6543c0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:33 GMT
ADD file:e0a1fc1de1477cea6fe41bdd15378013c680928cad3988dd16926cc1562c775e in / 
# Wed, 24 Apr 2024 03:43:38 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b57a10abb081ff40e5bb34246c3875a71b8d258f767c4f8384d7054b1bc42725`  
		Last Modified: Wed, 24 Apr 2024 03:49:31 GMT  
		Size: 53.3 MB (53337419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ed92794c4710c20ea615a0e07fe947837768482be7bcd9d1fccb335072a92`  
		Last Modified: Wed, 24 Apr 2024 04:24:03 GMT  
		Size: 15.6 MB (15642846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0318d2197701d71929fa882d8d64bdc0c65ee6bc9abd4bd4063694d92acb7`  
		Last Modified: Wed, 24 Apr 2024 04:24:17 GMT  
		Size: 54.1 MB (54076626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c3f9b4c72abaa52996d64ffc8754f8500b075a8a677c0fe59c310548e9af5c`  
		Last Modified: Wed, 24 Apr 2024 04:24:43 GMT  
		Size: 173.0 MB (172994116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66302c05a1f58a25604176a4b9b6bc0e717fb72ff97e0334ea79fb2895e26df7`  
		Last Modified: Thu, 02 May 2024 18:08:54 GMT  
		Size: 260.4 MB (260427952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:52b39a86a4ea99cb0237d970a10213cddfe8f113046bf4abdd5d3e4a3cda1363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14808368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bec0dfd4f38a0e9dad4996be6db3bacd06333698fa0cae356936fc13be9fd4`

```dockerfile
```

-	Layers:
	-	`sha256:83ce677ca56d4a667f9518ab5babc3e5b9ad1f44c3a5dbd0ff5ba123690f4055`  
		Last Modified: Thu, 02 May 2024 18:08:50 GMT  
		Size: 14.8 MB (14796613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f959e24eefab058ecc036f364b2858652b6977cafed184475b485ec952b32bc`  
		Last Modified: Thu, 02 May 2024 18:08:50 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78.0-buster`

```console
$ docker pull rust@sha256:fcb09007a565e6705c6d49835377d7d18e050b309203edc9e412977e91269257
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

### `rust:1.78.0-buster` - linux; amd64

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

### `rust:1.78.0-buster` - unknown; unknown

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

### `rust:1.78.0-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:47eacf3b5d2efd391224926939f061ff7acd7574beacdbcf721c82b01a65715e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 MB (490711222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bef0c9fda88c0ce49bbbe4e82e4c8d2496752121e8e07c5f59170f61ca0d31d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:33 GMT
ADD file:eea1eb05334cd4d0032909b2c56fc86a54faad563cbc3d2d46e763ce9e8922ab in / 
# Wed, 24 Apr 2024 04:07:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:53:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:54:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:55:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
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
	-	`sha256:fe0f6a4b48afbd61f9ef055b862b89cc5fc3980c4be6d4ccdc4e71eb6bd56d0d`  
		Last Modified: Thu, 02 May 2024 18:07:53 GMT  
		Size: 212.8 MB (212820147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-buster` - unknown; unknown

```console
$ docker pull rust@sha256:752d344513be8e413c08339a72a1696e061067a176479b706f0ae0a0c25048f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15780088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c18d957fb0511cfe9d344a4de14bcc9b40ee6d3bfbc1d980e180ae8df9d7aea`

```dockerfile
```

-	Layers:
	-	`sha256:da347c4aa030e17d6c56379e77bbdc5e28dab4fed5f89adbf67d26f052266c5f`  
		Last Modified: Thu, 02 May 2024 18:07:47 GMT  
		Size: 15.8 MB (15769023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52097463634c6c7d47e034b943ee50d0b5c9c9b3d2a8be616e9ebc076bb95f37`  
		Last Modified: Thu, 02 May 2024 18:07:46 GMT  
		Size: 11.1 KB (11065 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:775daa3419885651f2e284f10b29385f68347c1b99caf12ee7dbf82edc24947f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548916487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5233d262b43ce5dd1ff865b0ee9ac12ae4be5844a39f716b3cd8396774e15b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:00 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
# Wed, 24 Apr 2024 04:11:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:36:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
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
	-	`sha256:af5cdf87e38274705e7b47b4d3a5ccbab3f4bf94894cac0c5b2d82abfcf1989e`  
		Last Modified: Thu, 02 May 2024 18:19:24 GMT  
		Size: 246.3 MB (246251497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-buster` - unknown; unknown

```console
$ docker pull rust@sha256:dac6fc781e375c3f98871b1045ea01bd75fc62f126ba52697ba0c6b38a1f4aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15969386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2c1d63305c600acd748d5093b508df829037b295ab55b92bcc3998cf8ce8aa`

```dockerfile
```

-	Layers:
	-	`sha256:65b7feb61540a8b5987675be790620a8a6a102d1c29faafbb53fc91011a7161d`  
		Last Modified: Thu, 02 May 2024 18:19:19 GMT  
		Size: 16.0 MB (15957718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccd3a895875d4cbfb484b9fb55f5e778d710cf340062cd3a9484aadb5c29130`  
		Last Modified: Thu, 02 May 2024 18:19:19 GMT  
		Size: 11.7 KB (11668 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-buster` - linux; 386

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

### `rust:1.78.0-buster` - unknown; unknown

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

## `rust:1.78.0-slim`

```console
$ docker pull rust@sha256:517c6272b328bc51c87e099ef4adfbc7ab4558af2d757e8d423c7c3f1cbbf9d5
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

### `rust:1.78.0-slim` - linux; amd64

```console
$ docker pull rust@sha256:144edf7af2e5e374afdee02fd458df5bad41aba4cae314ace9d43f7933d44c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277315532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036d20da216ad2e94545e4e82700ee8c8ee3ad79fa0e2dca1261f8a69a87a937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8f9fca3e1073639d97fde71b99e2ef803078e36ed1cd97b74ce545ee7b17`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 248.2 MB (248165053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:a10481a084e247a58cb63c17b394d4e65463e3c8369e21bcfc769abbdfffb9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911a63093a97a45bdf3e678240c96fe3b7f81befc1871a5542db741b9b51a7d`

```dockerfile
```

-	Layers:
	-	`sha256:371755c5d7b19c0c727d6c961f8c6528bc0cbd0b3d2c7067a40ddd1f9eaa4e74`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6556d0382c9b778b94f7cc91b1d3f7659518e567fab6462da86ebe4ac90c6382`  
		Last Modified: Thu, 02 May 2024 17:53:22 GMT  
		Size: 13.2 KB (13172 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:ffc8f22bbcaf9c443db0c997aba6a8f0773d989e29a5865d0f164a36f15e8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285223017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d69dbc41e535f1c4657a7b35fe40a346dce9c4f07b392370b716e1c4ea8c45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f060f4605d55cb88006aa78ea1433f0129af80557306aa6ef11d728ad8c15`  
		Last Modified: Thu, 02 May 2024 18:18:12 GMT  
		Size: 260.5 MB (260482575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:8ee1faa28bc0f8ec0e92ba67f71be26d4570984f23660ad77c52f9cdaf0e4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14586c5fd8ae352e99facffdc8e47f2ffe4a171ae426fa7163a3033099714f4d`

```dockerfile
```

-	Layers:
	-	`sha256:f920b7810ae2eb89611842b3c8d00f4e763ddaa0dbb6dc67bc77bc0979211af2`  
		Last Modified: Thu, 02 May 2024 18:18:06 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6070f226a82471804b25ddfcd5994dfb20c75710288cb8fa305eeecbc9689a`  
		Last Modified: Thu, 02 May 2024 18:18:05 GMT  
		Size: 13.1 KB (13107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:701d523927f60aa6594b6b639e16b2872b090efd77b38206eb07f8a5ab5f4b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341067862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d7c8b33fff18a1de7a58bd9764df34dcb7689471c8332703ef166a3be91dbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b6ff75fe73e0b624033411b211e30ab65a0dfe2f196bc831afaa3f262ad40`  
		Last Modified: Thu, 02 May 2024 18:28:13 GMT  
		Size: 311.9 MB (311887927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:3068c80cfcc050b7d2f84d2daa26eb1bb6646dbef2cdc889b4706d0ecec10c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94192de4d427019b53f8d6f476258f84f6c701b7cc313fbe20aac8356c685388`

```dockerfile
```

-	Layers:
	-	`sha256:fe0470bf526cfabeeff81d8175f1ad542787eb63d46eac59584aa0c9700cb865`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 3.9 MB (3941462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e741b4e2feaf42a20f56bbcccb528e05e69b28f20a30f471dab96b02dd26885d`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 13.0 KB (13023 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim` - linux; 386

```console
$ docker pull rust@sha256:9a0ff69ac63b29617f2772d8af475f42b17376ae675690bd4b6ffbd6fa013a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288155332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730521317992ca457b5e32b681e5c2fc6a9985f74b26c05ab75a898d70063efd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be463c23e962e7814d7269dd918a3abf7fe7480f3491260b6939bc093b40232`  
		Last Modified: Thu, 02 May 2024 17:53:34 GMT  
		Size: 258.0 MB (257992149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:406577ad4a920a84505e527616fcb1f008cff2e259737b980109d6586c441132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94959a9ba35ac8e7aa52d2c9634583789f540a6ce1cdf8970c1aeafbeb383266`

```dockerfile
```

-	Layers:
	-	`sha256:5fccb080d41ea034eca85abe7287cd6513b3fcf1304c5b0ab744b5e4f7604ee2`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5ee26d72cca7cd34f6faa2688b32a264613f3b88beb239a82737e7a7bdd0b8`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim` - linux; ppc64le

```console
$ docker pull rust@sha256:ea7984b98ee3317d77412b9077362d5f7934cbed7f5d5ce18a977f899e9386c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288845524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a166a0772dcf6517a472407901b610b01b80c50d7487fd756971dc08ca26d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bdd5b65845940ee92c4225121c6b04def8a421d1c550f7d8d65db0e37bf19`  
		Last Modified: Thu, 02 May 2024 18:15:05 GMT  
		Size: 255.7 MB (255704323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:b8cf1c2e22630a3fb96504ce4e0109e450e2f91f2338965264da180dffb4be0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e443bda8941eefcf331e18425d4d04513900c67b623379aae5f5c3ba60799f`

```dockerfile
```

-	Layers:
	-	`sha256:57c7d4ef78d8836d083ed51f7584a8611e874b74c989c77cbdaefba43cf9c737`  
		Last Modified: Thu, 02 May 2024 18:14:59 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721e6450ded9a8224165692a227cf32021b20727fa9e27b7eb51b9ee46c98d64`  
		Last Modified: Thu, 02 May 2024 18:14:58 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim` - linux; s390x

```console
$ docker pull rust@sha256:f2f85fb1ee50bb9ddd8312a215bd06ef84d9d8a32ae978df573ac5b9b84ab38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337865924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2db01fe12c831f8b1c810ff63f0059a28b15cebb3fc607f041e7f43ba47394a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c36f802355139032b4b3b2815d90b8684055c93beadd105d203de5c4574421`  
		Last Modified: Thu, 02 May 2024 18:19:38 GMT  
		Size: 310.4 MB (310353569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim` - unknown; unknown

```console
$ docker pull rust@sha256:1d010d6d80dc73fcb8b111939211fe047c868a66965107fe6522c5ac238f2882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67848fc2610daa3a0488587b7d72d3197b8f69b13b8bc20914dec3e53cac68c4`

```dockerfile
```

-	Layers:
	-	`sha256:45465cb45a531518db8458bf81a4591118d814a4fcc27d32e893ed00128240f1`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 3.8 MB (3762075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ba7b0835f73f3eba7b3413925b87bc83556d2ccd55606dfd68c5715cec19c7b`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78.0-slim-bookworm`

```console
$ docker pull rust@sha256:517c6272b328bc51c87e099ef4adfbc7ab4558af2d757e8d423c7c3f1cbbf9d5
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

### `rust:1.78.0-slim-bookworm` - linux; amd64

```console
$ docker pull rust@sha256:144edf7af2e5e374afdee02fd458df5bad41aba4cae314ace9d43f7933d44c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277315532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036d20da216ad2e94545e4e82700ee8c8ee3ad79fa0e2dca1261f8a69a87a937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8f9fca3e1073639d97fde71b99e2ef803078e36ed1cd97b74ce545ee7b17`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 248.2 MB (248165053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a10481a084e247a58cb63c17b394d4e65463e3c8369e21bcfc769abbdfffb9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911a63093a97a45bdf3e678240c96fe3b7f81befc1871a5542db741b9b51a7d`

```dockerfile
```

-	Layers:
	-	`sha256:371755c5d7b19c0c727d6c961f8c6528bc0cbd0b3d2c7067a40ddd1f9eaa4e74`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6556d0382c9b778b94f7cc91b1d3f7659518e567fab6462da86ebe4ac90c6382`  
		Last Modified: Thu, 02 May 2024 17:53:22 GMT  
		Size: 13.2 KB (13172 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ffc8f22bbcaf9c443db0c997aba6a8f0773d989e29a5865d0f164a36f15e8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285223017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d69dbc41e535f1c4657a7b35fe40a346dce9c4f07b392370b716e1c4ea8c45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f060f4605d55cb88006aa78ea1433f0129af80557306aa6ef11d728ad8c15`  
		Last Modified: Thu, 02 May 2024 18:18:12 GMT  
		Size: 260.5 MB (260482575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ee1faa28bc0f8ec0e92ba67f71be26d4570984f23660ad77c52f9cdaf0e4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14586c5fd8ae352e99facffdc8e47f2ffe4a171ae426fa7163a3033099714f4d`

```dockerfile
```

-	Layers:
	-	`sha256:f920b7810ae2eb89611842b3c8d00f4e763ddaa0dbb6dc67bc77bc0979211af2`  
		Last Modified: Thu, 02 May 2024 18:18:06 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6070f226a82471804b25ddfcd5994dfb20c75710288cb8fa305eeecbc9689a`  
		Last Modified: Thu, 02 May 2024 18:18:05 GMT  
		Size: 13.1 KB (13107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:701d523927f60aa6594b6b639e16b2872b090efd77b38206eb07f8a5ab5f4b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341067862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d7c8b33fff18a1de7a58bd9764df34dcb7689471c8332703ef166a3be91dbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b6ff75fe73e0b624033411b211e30ab65a0dfe2f196bc831afaa3f262ad40`  
		Last Modified: Thu, 02 May 2024 18:28:13 GMT  
		Size: 311.9 MB (311887927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3068c80cfcc050b7d2f84d2daa26eb1bb6646dbef2cdc889b4706d0ecec10c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94192de4d427019b53f8d6f476258f84f6c701b7cc313fbe20aac8356c685388`

```dockerfile
```

-	Layers:
	-	`sha256:fe0470bf526cfabeeff81d8175f1ad542787eb63d46eac59584aa0c9700cb865`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 3.9 MB (3941462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e741b4e2feaf42a20f56bbcccb528e05e69b28f20a30f471dab96b02dd26885d`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 13.0 KB (13023 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:9a0ff69ac63b29617f2772d8af475f42b17376ae675690bd4b6ffbd6fa013a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288155332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730521317992ca457b5e32b681e5c2fc6a9985f74b26c05ab75a898d70063efd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be463c23e962e7814d7269dd918a3abf7fe7480f3491260b6939bc093b40232`  
		Last Modified: Thu, 02 May 2024 17:53:34 GMT  
		Size: 258.0 MB (257992149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:406577ad4a920a84505e527616fcb1f008cff2e259737b980109d6586c441132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94959a9ba35ac8e7aa52d2c9634583789f540a6ce1cdf8970c1aeafbeb383266`

```dockerfile
```

-	Layers:
	-	`sha256:5fccb080d41ea034eca85abe7287cd6513b3fcf1304c5b0ab744b5e4f7604ee2`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5ee26d72cca7cd34f6faa2688b32a264613f3b88beb239a82737e7a7bdd0b8`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:ea7984b98ee3317d77412b9077362d5f7934cbed7f5d5ce18a977f899e9386c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288845524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a166a0772dcf6517a472407901b610b01b80c50d7487fd756971dc08ca26d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bdd5b65845940ee92c4225121c6b04def8a421d1c550f7d8d65db0e37bf19`  
		Last Modified: Thu, 02 May 2024 18:15:05 GMT  
		Size: 255.7 MB (255704323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b8cf1c2e22630a3fb96504ce4e0109e450e2f91f2338965264da180dffb4be0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e443bda8941eefcf331e18425d4d04513900c67b623379aae5f5c3ba60799f`

```dockerfile
```

-	Layers:
	-	`sha256:57c7d4ef78d8836d083ed51f7584a8611e874b74c989c77cbdaefba43cf9c737`  
		Last Modified: Thu, 02 May 2024 18:14:59 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721e6450ded9a8224165692a227cf32021b20727fa9e27b7eb51b9ee46c98d64`  
		Last Modified: Thu, 02 May 2024 18:14:58 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:f2f85fb1ee50bb9ddd8312a215bd06ef84d9d8a32ae978df573ac5b9b84ab38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337865924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2db01fe12c831f8b1c810ff63f0059a28b15cebb3fc607f041e7f43ba47394a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c36f802355139032b4b3b2815d90b8684055c93beadd105d203de5c4574421`  
		Last Modified: Thu, 02 May 2024 18:19:38 GMT  
		Size: 310.4 MB (310353569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1d010d6d80dc73fcb8b111939211fe047c868a66965107fe6522c5ac238f2882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67848fc2610daa3a0488587b7d72d3197b8f69b13b8bc20914dec3e53cac68c4`

```dockerfile
```

-	Layers:
	-	`sha256:45465cb45a531518db8458bf81a4591118d814a4fcc27d32e893ed00128240f1`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 3.8 MB (3762075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ba7b0835f73f3eba7b3413925b87bc83556d2ccd55606dfd68c5715cec19c7b`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78.0-slim-bullseye`

```console
$ docker pull rust@sha256:33baf245a3be288ec45d6534ebf94de088b834ef9202fd8e1176a3c1a0d9b730
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

### `rust:1.78.0-slim-bullseye` - linux; amd64

```console
$ docker pull rust@sha256:ebd24f6078bcc9f6b23f99a23e450f07d593f570d4bf072b5077added128bf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268954860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0502ee249ca6bfa22cfade789d5296feac6f0928a18703146f522c7cbf7ced10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e70c0d176523de333ba6a5be57344d80ccfba2589ed97a0714e502d2a34ca43`  
		Last Modified: Thu, 02 May 2024 17:53:20 GMT  
		Size: 237.5 MB (237520597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a4dcfa88f53f7b2928efe6b3b835f897d81e20fddd853c43354998e2e042cabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ef9d771e215a52ef1e40b292ede0d829c632e49e4c2367b41dac17ea648ac2`

```dockerfile
```

-	Layers:
	-	`sha256:cef011c9722bb44d4620b4e6bf096623230158399e11cb7d6d6f6c1a1af4bd58`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 4.1 MB (4139833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599c91eec4cbd0f1ff1398eba0b589af02754a51f58dcd99213c8a7b227dac30`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 12.0 KB (11983 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b2d51c493ce70a6df64cc9294f39b991ed51caad0d1b6b4df3aa73ebc0059308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281482631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1845601085edf0de75fa06cb3587d42cc4e40938d1b8a5f3ee758b9356526b5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb88c27c011a0bf4095b4dad73f3b89a8b7d5926dd1b563ef8b60cc2f6c06c3`  
		Last Modified: Thu, 02 May 2024 18:13:56 GMT  
		Size: 254.9 MB (254887889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ede45ee3c4bebfd74b4c54b87023ff6f1af70c483ef9065a07b00b14ba55e7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb61ef780ac05b5018cad0ca9872b446a694f9a1b4446f0d1738749ea277525`

```dockerfile
```

-	Layers:
	-	`sha256:f821ed482f1443a1e918b75b417cb399f4cdb75370c37d86cca0be80d3b3b835`  
		Last Modified: Thu, 02 May 2024 18:13:50 GMT  
		Size: 3.9 MB (3949756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e6fac619e4f33ae52bdc1063f1d01d4404064b385b8d19745a745c85900723`  
		Last Modified: Thu, 02 May 2024 18:13:50 GMT  
		Size: 11.9 KB (11887 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:55184f8e235a387dc47570d3c45c18868da64c7441759ff319bb02b00a30dd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331830874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2efb3db0f1f86b252af2ac6422352121d26077fc46501dc669c95b75f8b7e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a148bfdb5477b5b28e8af64d0d2c9d4cd738688d1ec0104833fc0685436c0c3`  
		Last Modified: Thu, 02 May 2024 18:23:57 GMT  
		Size: 301.7 MB (301743538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:47addcc74cfa8ab7f351d70c100db444ad71814d83f6c96928b852f42598e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0390a7297d4caf490960ab4c3265747cbbd92e4748bed00b3c994f72c02f2`

```dockerfile
```

-	Layers:
	-	`sha256:0508b7e94192ab544e987c54492b371e546f31d0f9919bc0c8cc1c452aa454c4`  
		Last Modified: Thu, 02 May 2024 18:23:49 GMT  
		Size: 4.1 MB (4136713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dccf37e519bcea3696ecfb195e4a0b38348a412004399eb8308b338effdba8b`  
		Last Modified: Thu, 02 May 2024 18:23:48 GMT  
		Size: 11.8 KB (11827 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b189e96e3c85ca97178eb44feb77efb715773ecfe115c08226820247f7cd4371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283597724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d042e33fb45d8dbb5ab9375e1f445cca9f0842403742ac8e16e14a492d1379b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:20 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Wed, 24 Apr 2024 03:39:20 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d994d194bfa3acf9a46df705316048a9e421612eb43dc8e67d2fc7c4b47dc8cd`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 251.2 MB (251172951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:23c07842a4cfddec1e1f1e230639073243847f2eb36626a93f578ed729e42f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9ef9f2ac9c96e93217e0d144744e8d8278050716ca0834c70afa220c7c8939`

```dockerfile
```

-	Layers:
	-	`sha256:80add452afc9acafbae3ebdaf81b51e772270d4168261abc531caa3d40d6f8f2`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 4.1 MB (4131887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9032987821a421011b12f5c932db84722ec77469e7d51d50c7f52fc9d678ac72`  
		Last Modified: Thu, 02 May 2024 17:53:17 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:f231b14bfd93102c404e608edce59336c32bbf5bc5b16dde3b83c3b3058aa530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277263350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6022c77c11237120364d8daebc5e4a7f79b239f345aadfe10e08162f3991d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a8be3c69cc41100693d385b45a719b06420c1a8633ddefd2cd065116e4a80f`  
		Last Modified: Thu, 02 May 2024 18:10:20 GMT  
		Size: 242.0 MB (241951625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1bb874168defcf306f4d12a18fa1d1a431164a64175ab74ccc234d19145dafe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf50d0079f8c3085c91f49970a4c034af187ead7b500a47212bad01b95a54c4`

```dockerfile
```

-	Layers:
	-	`sha256:c87e1c0879f136a39e78ff54f5cea16d36b7126d98ada10edad69ab8afe45793`  
		Last Modified: Thu, 02 May 2024 18:10:13 GMT  
		Size: 4.1 MB (4100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee003b3c784435c5aab66ccdc806e9767a27f9edd3cef32418dbc7142a51ac6`  
		Last Modified: Thu, 02 May 2024 18:10:13 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:a4b95ec70b2c183bd9cd02364c93389c429f8ff07d8a86c91e8830923039acc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332291021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08e265a0280e57d06e189c5f7c3e1e12b10bb2d5eb9c7e0f2004ac291a514f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:03 GMT
ADD file:acaea4e054f1ab7ae5cbc8f02c73b546c367aebfcc48c7fb4f0dd9f3628bc25e in / 
# Wed, 24 Apr 2024 03:44:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6f588995519e0e04ef4c150b91ad96c3c85667869db0ad72e5a78d4fab796e70`  
		Last Modified: Wed, 24 Apr 2024 03:49:47 GMT  
		Size: 29.7 MB (29673934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784d1c6d27c0fa82885a8be868f2c1ed573b39823970c4d06846ef9b4058af1e`  
		Last Modified: Thu, 02 May 2024 18:12:25 GMT  
		Size: 302.6 MB (302617087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ee3b2c41de9bf97e7b05b8905fb5d0e70b4d8b48dcdbd11a87197a0e8af288de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fa73fb55843e1fc73565ef3eb0db89dd88c65c76748308419e9a61dddb5569`

```dockerfile
```

-	Layers:
	-	`sha256:8de35856b398f950ff03181d5960ac2487203d9e917fd71ab33559d927b58a50`  
		Last Modified: Thu, 02 May 2024 18:12:20 GMT  
		Size: 4.0 MB (3972037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad823fcf4f244656c879ab7e131ca3a63d49fb60f964019942d1d0722a7aef41`  
		Last Modified: Thu, 02 May 2024 18:12:19 GMT  
		Size: 11.8 KB (11817 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:1.78.0-slim-buster`

```console
$ docker pull rust@sha256:d30c7ad62c2044e0d1174d742f0efbc02c1e43aea988193b6686ee8aaaf79170
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

### `rust:1.78.0-slim-buster` - linux; amd64

```console
$ docker pull rust@sha256:562d6f211888cbd784790e7fb47d3cea4b20480634543579297832b7fd1c25a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250335520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6261cf21c8a87571e9f4b502375b16f30e624d67d46e199388cdf0bc36235`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906e6ed35d183754f56330a654a033329ee5826a5608612dde75a12c80dfbda`  
		Last Modified: Thu, 02 May 2024 17:53:08 GMT  
		Size: 223.0 MB (222997945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e7b9c6cdb9dc891a721e37b31279d12f59a2aeaa33d3a50cd04c15ed9fdac0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a326d7714ebb85020a2b5bc3eb2f017a246b9349e259e29adf9cf787cd097`

```dockerfile
```

-	Layers:
	-	`sha256:3d7cefbfd3006121cdf982e776f479a01d0119707b7d9103dd24cdb58f580975`  
		Last Modified: Thu, 02 May 2024 17:53:05 GMT  
		Size: 3.9 MB (3941693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca2968425f2c6d21765305834771a5c51369246bdfafc5ca52300a944a9f50d`  
		Last Modified: Thu, 02 May 2024 17:53:05 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:94dda1ea419d69d0e38543407f33117c87a59c53c8e45b2fa3729496d76462c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268702412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb522a78fe20e96dd37a3094bd8201f8bc75d59d78c8672653761f8389e82b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab99a29678006ca048ee3cec2a39dd336045cbef1f173b20313118c42dcc53f3`  
		Last Modified: Thu, 02 May 2024 18:09:45 GMT  
		Size: 245.8 MB (245757348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:870cd6eb7305f07b9e0a9384fb585ac261058d1821c291dae7d3e76c80bb744a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4231130c9d88f75df6ed09cac4d31aa678269b42aa3df4dabb3e9675ce564037`

```dockerfile
```

-	Layers:
	-	`sha256:2dc32a76ad84dbf82ef236a5ee11a01cd7c24687433eb86f7be3f1cfa7568a9b`  
		Last Modified: Thu, 02 May 2024 18:09:40 GMT  
		Size: 3.7 MB (3749343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cd37df8a47dfdf9952876a899f07158606f3fe042c2c85d5825fd83d506bf7`  
		Last Modified: Thu, 02 May 2024 18:09:39 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:489aac5b79003a727f4571932d0a03b2aa17db922cca485942fe79de33c5cb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312574944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fc5383529ef82de9ea2eb11d095ad1d1f517c836bc95f1ecc709194a04799d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:06 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
# Wed, 24 Apr 2024 04:11:07 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62497221c4fce50e070a112fde5ee41270ed6a3a085e7b1825fd24a956f1f4c7`  
		Last Modified: Thu, 02 May 2024 18:20:54 GMT  
		Size: 286.5 MB (286465114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:612bde9c6fe77167e879e6f3787a339655d4b7a1cbfa4ce1d3731711d4aa5508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6441cb64ca635d2e44dba773323ae3d87e7f6d0d4f4aee982365fa0652812d06`

```dockerfile
```

-	Layers:
	-	`sha256:e2fb474d4ff49f24441eccc92c2f1c16d30efe46b4c082a210ed49e145d5e5ee`  
		Last Modified: Thu, 02 May 2024 18:20:47 GMT  
		Size: 3.9 MB (3930985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80129d72be4749680a0777a4fb88afb3ad6bfae867c9ae93c316ad94e7112176`  
		Last Modified: Thu, 02 May 2024 18:20:47 GMT  
		Size: 11.2 KB (11234 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:1.78.0-slim-buster` - linux; 386

```console
$ docker pull rust@sha256:862f761b55bdfb9b687ccd73c39ea5db75ab570112ac0d7d9da5f5c5196dc67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268610066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12d3e0efa5e20f2dffb6cca638c9d030e51183e0ed6dea06200bb6fa61abb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:39 GMT
ADD file:32f0f06baa0e4f10bff55aaa215b511838432ecc5fe547373d9ac99494556801 in / 
# Wed, 24 Apr 2024 03:39:40 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:204b51fc41806ed93b4ccb6ce8272fa49b5f0b099ba6e3b5a940a9e7cd3ce202`  
		Last Modified: Wed, 24 Apr 2024 03:45:03 GMT  
		Size: 28.0 MB (27994678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3981a552b28468ee69108184598097965a5265b74ad064e8e657f3897f599f3`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 240.6 MB (240615388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:1.78.0-slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:4a7ce102abb3a846743437756ea063f781583ab5bea6f40c2612550634e10222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb6026b631db1e909e1f420b7086445db95e1f00ef7bc7c365ad507c9a54fdb`

```dockerfile
```

-	Layers:
	-	`sha256:2e03fc3bfe125dba62e18faebb42c04d798624900a87a5dc953c3be75072510d`  
		Last Modified: Thu, 02 May 2024 17:53:10 GMT  
		Size: 3.9 MB (3948318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e394e2a792e8d275adc332b5b935d4c9db65a83fe54fda94e7437645d5b02114`  
		Last Modified: Thu, 02 May 2024 17:53:10 GMT  
		Size: 11.2 KB (11195 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine`

```console
$ docker pull rust@sha256:d4d3f81f3111991353bd7c7fa513ad3725a27027575fd82e24fb7babcd8f26f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine` - linux; amd64

```console
$ docker pull rust@sha256:41bf7d335c39fd25bb73f3183713b1fdcb77f0fc70def6634e40992e66119292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276648359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9be41f0a10e18d4183096b0d91821b4f93cd1eb4e4884a8fd5fdc8b7ee34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c6c611323bdd864b20f293097226e373d0e34b9108e12e65481c955804c26`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 55.3 MB (55346841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245c9984f45dd6d2464604e214a0391a1b399705f140a8b96469f84d6e1f61e`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 217.9 MB (217892789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:8be526e7cb5aa9bc6b6d8c73fb8ee6e81a9c8164a4c5bfa97533ab5bfc0b6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcc214e8f56925c61fb2680fb60504b652116af551962b9d82c4683a88dc59`

```dockerfile
```

-	Layers:
	-	`sha256:f47a0d5a9bacd02cd11840d2f1a2adc07cd5bdb00e97770f9c417e49c8d49f29`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 710.6 KB (710621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232259c5160cb554f445085a6e5765832b7c088ca5c17fa09d0fb5f2a2dda48`  
		Last Modified: Thu, 02 May 2024 17:53:11 GMT  
		Size: 11.8 KB (11794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b7075f2ddfde9ede284e71e74bade0576f8ea97e0f49b2c8a4ead2a101a1cc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282899712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ab7c4bfc7646c65e0a623ab2551468819a7e5047057601317c046321a3c6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1475e7bc8776b6a5d5098e107869ccf04a61b48d632658ab4bf934b5340337c2`  
		Last Modified: Thu, 02 May 2024 18:30:18 GMT  
		Size: 53.0 MB (52995527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3cbfb4539306a5cd558b71b91000e4f05d22445cf79e04281bf881f3bfd22`  
		Last Modified: Thu, 02 May 2024 18:30:21 GMT  
		Size: 226.6 MB (226556470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine` - unknown; unknown

```console
$ docker pull rust@sha256:f02f381f9fa338bae9204fb7e52a19b44779316d227092aa2fb77ea0a62cea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.2 KB (758219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e2876b12a57c6260b8a220b6a82f40ccb6b3f85bced4f5e908a46f1175e9c`

```dockerfile
```

-	Layers:
	-	`sha256:0f5adf947b65a86f48dfa44a9462e156913eca4be72ad307f8b70e63904defcc`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 746.6 KB (746571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd319de530a5221d01b41f952f79922b81a42473dd697d14646929354af7f96c`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 11.6 KB (11648 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.18`

```console
$ docker pull rust@sha256:34f1c35f62e192f39cd0c809982bf90c354f7e5746682a2f4c9e4c43bd516dbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.18` - linux; amd64

```console
$ docker pull rust@sha256:909cfdd11b0a96aa82d86c96c17cddf3864bca150a6228d18ab6a658e7006d07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.8 MB (272829333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787b53dee543c9d07c38258423856c4ce44a7bb0e10dd80b6ce8d3d6be6d688b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d8cca761111b3832e2234b2a7c144570d1ceaa6a6eab4447a39633b2a0c9e6`  
		Last Modified: Thu, 02 May 2024 17:53:03 GMT  
		Size: 51.5 MB (51534006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94392fe86146798eeda301677559c748ac0525075773894cb651ef44b47f89cf`  
		Last Modified: Thu, 02 May 2024 17:53:06 GMT  
		Size: 217.9 MB (217892785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:828ea566785e422ca858dcd98738715dc31eb43e85aa4ac91f75e0f3c0d1a46f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.5 KB (712482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13ead6d1e1a8601c572bfe57d56165b246d74fecdc009ab88410fe102fdb904`

```dockerfile
```

-	Layers:
	-	`sha256:022a488b72ff619b6be7c5b9d74e5a88f50c0e8179a478751063a2baa139c1ca`  
		Last Modified: Thu, 02 May 2024 17:53:02 GMT  
		Size: 701.9 KB (701890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d53ac36334ec5e522ca13debbc666b6df6ad9bb97c9efa7639b75bec875183c`  
		Last Modified: Thu, 02 May 2024 17:53:02 GMT  
		Size: 10.6 KB (10592 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:ee1d16c1cc031559875424b27cb090136df31c18dd9e97966cf12391b59ba403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.0 MB (275971039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0325d780023f87c7f06c8d7e4ee3aadb87e82528ad4b2da06a341cc8e42438bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ecadc98c87cbba10a8cd3e79aee52d2aa3670ae6272cc2b29b27128e710a536`  
		Last Modified: Thu, 02 May 2024 18:29:15 GMT  
		Size: 46.1 MB (46081224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688cf2745b0216764a0d813aa9bf3d0c02af25fae1ef4c9bfce32c558a0d640f`  
		Last Modified: Thu, 02 May 2024 18:29:18 GMT  
		Size: 226.6 MB (226556454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.18` - unknown; unknown

```console
$ docker pull rust@sha256:a6e2823b379b899207fbbdc6d8f2181cb7668892e2f31ce8f272302781d6a274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.1 KB (752144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa78da9cdd7dc3787e280f8a86f29faba9f60305898cf6d9486dc01fdc2def2`

```dockerfile
```

-	Layers:
	-	`sha256:2508e1ec9f010359afe8d8e516417a297aa32d170c071185c0be86d2c697cb2f`  
		Last Modified: Thu, 02 May 2024 18:29:13 GMT  
		Size: 741.7 KB (741708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af17300661fa62bda831f09a0938360f387b14cb172b980a435cff240801bee8`  
		Last Modified: Thu, 02 May 2024 18:29:13 GMT  
		Size: 10.4 KB (10436 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:alpine3.19`

```console
$ docker pull rust@sha256:d4d3f81f3111991353bd7c7fa513ad3725a27027575fd82e24fb7babcd8f26f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `rust:alpine3.19` - linux; amd64

```console
$ docker pull rust@sha256:41bf7d335c39fd25bb73f3183713b1fdcb77f0fc70def6634e40992e66119292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276648359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec9be41f0a10e18d4183096b0d91821b4f93cd1eb4e4884a8fd5fdc8b7ee34a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4c6c611323bdd864b20f293097226e373d0e34b9108e12e65481c955804c26`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 55.3 MB (55346841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7245c9984f45dd6d2464604e214a0391a1b399705f140a8b96469f84d6e1f61e`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 217.9 MB (217892789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:8be526e7cb5aa9bc6b6d8c73fb8ee6e81a9c8164a4c5bfa97533ab5bfc0b6592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.4 KB (722415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9bcc214e8f56925c61fb2680fb60504b652116af551962b9d82c4683a88dc59`

```dockerfile
```

-	Layers:
	-	`sha256:f47a0d5a9bacd02cd11840d2f1a2adc07cd5bdb00e97770f9c417e49c8d49f29`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 710.6 KB (710621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232259c5160cb554f445085a6e5765832b7c088ca5c17fa09d0fb5f2a2dda48`  
		Last Modified: Thu, 02 May 2024 17:53:11 GMT  
		Size: 11.8 KB (11794 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:b7075f2ddfde9ede284e71e74bade0576f8ea97e0f49b2c8a4ead2a101a1cc5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282899712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ab7c4bfc7646c65e0a623ab2551468819a7e5047057601317c046321a3c6f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
RUN apk add --no-cache         ca-certificates         gcc # buildkit
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apkArch="$(apk --print-arch)";     case "$apkArch" in         x86_64) rustArch='x86_64-unknown-linux-musl'; rustupSha256='b9d84cbba1ed29d11c534406a1839d64274d29805041e0e096d5293ae6390dd0' ;;         aarch64) rustArch='aarch64-unknown-linux-musl'; rustupSha256='841513f7599fcf89c71a62dea332337dfd4332216b60c17648d6effbeefe66a9' ;;         *) echo >&2 "unsupported architecture: $apkArch"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1475e7bc8776b6a5d5098e107869ccf04a61b48d632658ab4bf934b5340337c2`  
		Last Modified: Thu, 02 May 2024 18:30:18 GMT  
		Size: 53.0 MB (52995527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab3cbfb4539306a5cd558b71b91000e4f05d22445cf79e04281bf881f3bfd22`  
		Last Modified: Thu, 02 May 2024 18:30:21 GMT  
		Size: 226.6 MB (226556470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:alpine3.19` - unknown; unknown

```console
$ docker pull rust@sha256:f02f381f9fa338bae9204fb7e52a19b44779316d227092aa2fb77ea0a62cea28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **758.2 KB (758219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698e2876b12a57c6260b8a220b6a82f40ccb6b3f85bced4f5e908a46f1175e9c`

```dockerfile
```

-	Layers:
	-	`sha256:0f5adf947b65a86f48dfa44a9462e156913eca4be72ad307f8b70e63904defcc`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 746.6 KB (746571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd319de530a5221d01b41f952f79922b81a42473dd697d14646929354af7f96c`  
		Last Modified: Thu, 02 May 2024 18:30:16 GMT  
		Size: 11.6 KB (11648 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bookworm`

```console
$ docker pull rust@sha256:0dd183faf7bc5b9b8efe81cfd42701a5283577520b185b511e322e5bf52f8fc7
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
$ docker pull rust@sha256:d50e312c75fbd66f5cc7b1ab6d76892529751526629c294f34ca217016fe0425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526535638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d8eec96e0ea00b3ec3c6c2e03ef8a15113d8dd0682170d3757c06a78e73dce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:6b9f9d886ac307c9982286da0ae1d85ad364df502e05f2c5c14c9505f30a4feb`  
		Last Modified: Thu, 02 May 2024 17:53:26 GMT  
		Size: 177.6 MB (177591491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9d352cd5f6a779bed1be7057ea6557c8de8f96c40e26e555b469d2c2f8405643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15384104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511f0cc56710400a858b2b313a1fb6c554e2ca7debcdcfd5d6ae3ac4870e716f`

```dockerfile
```

-	Layers:
	-	`sha256:f4420d9292d76286420dd7187c5b08b956041f3a4d90ecee23f7d1f91f3638ac`  
		Last Modified: Thu, 02 May 2024 17:53:24 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6daf94a67a74ecaca457f9fc6812857963aae03a4bdf69ffece0604d2d071e2c`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 13.6 KB (13580 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:225556750412cc8f6f468fd8c3bd1176e9b06c90153acb0e045b500c21265bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514307156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d9947ff3490d7e91dbee0aade813ded906312a29924c5226904b76432127e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07170ec327fa1117b5289697e5555f4c3ba76d00200d7c7cc5c143086856f`  
		Last Modified: Wed, 24 Apr 2024 05:03:03 GMT  
		Size: 59.2 MB (59216995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937bd8fccb438207fe0e77a48873de07dbe1fbea251206222298b72dbd2b3d8`  
		Last Modified: Wed, 24 Apr 2024 05:03:45 GMT  
		Size: 175.1 MB (175141109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499a6710f841b95850a0e6c3589a558408d5ecdb1efe2d461015241a86667d9`  
		Last Modified: Thu, 02 May 2024 18:16:14 GMT  
		Size: 212.8 MB (212820090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a8d872088f3bc18ac36bb4ee06e93eac69f16897387344fcfd238be07505d19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15189426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f357e10dda11cec2f915422dbbb7f4dc9ef73032fc8aa82efe6609b3de03843`

```dockerfile
```

-	Layers:
	-	`sha256:67f172e545903f27510fe2841e22b7f07947e3314640824e648cc35a5e4af23c`  
		Last Modified: Thu, 02 May 2024 18:16:09 GMT  
		Size: 15.2 MB (15176407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becad9a5634f77e5e49e5e8f1bda8454cd92e0059d86c4ae3e43d13bba5c36d9`  
		Last Modified: Thu, 02 May 2024 18:16:08 GMT  
		Size: 13.0 KB (13019 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cb3fe1b45243325da5aaafb59bc75f8541697bfd9acbfedc914c0f132c7949ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.0 MB (586021653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b44c56b25c83977fc9ebfdf243d37b0b15ab1a4fcf0c647f0878847949cf84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476478a1e1450b999421118cb8f193aa62f1816e0cadd988a084385cf0a5696`  
		Last Modified: Wed, 24 Apr 2024 08:42:20 GMT  
		Size: 202.6 MB (202575289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ab2e8f65d41c1e5e2c493944dc3f6ca456b65a5275ac05e12bc31af0b697d`  
		Last Modified: Thu, 02 May 2024 18:26:37 GMT  
		Size: 246.3 MB (246251422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:9562e2467c5e3f2f6ee0ccff2633f57a5ff3cd388a582fca74510f46aba072bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6aaf4016fa5c395bc612fd990fc2d7422e8623e54ebe02b7b2625e179f7920`

```dockerfile
```

-	Layers:
	-	`sha256:1c4d0653a7e064d93a08cf2e3cb73351a07d67c388a1a2590326a06812bff5f3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 15.4 MB (15399046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790e84f88528ef27e0f653b5aeba1fafd203db38ba551366c785a778180828b3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 12.9 KB (12935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; 386

```console
$ docker pull rust@sha256:d1f3c3a8b571383507c4e76f99678f065d5a03aa90eea84693c767e32fc869c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542180953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009dec677b8280c20069beef31c3fbbbc461bc0ab36f0558b2ec40439a5f6079`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:48 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Wed, 24 Apr 2024 03:38:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:29:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:30:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:1614889c1e665cd335548134ca677fb6f9f1910d4ab6488c04424418a97f495a`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 190.6 MB (190599211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:de08ac7a06b5af621f4e0fb99dabf08168a533017d45b6ff2510485f17d0b355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15363096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc533d073cc58cb332d3410a63a6c6f32d775b9febedb13c3c8b78a6d6079a9`

```dockerfile
```

-	Layers:
	-	`sha256:64ac9f5f1c25c9fffc99c099a79689856019c48dfffddbb43b51cba223012a11`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921284eb6647f818f95a3f3db77efe9fa3b4c28d2bf2158f08f1c984fe96fef0`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 13.5 KB (13531 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:eb08c0b17cc0c417388189ce35bf4fb1f087a9e6ff51c1bfcec9ff410f2a8733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.2 MB (550221275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3bcff95d0b422fd84f7fcd46bf86991ba30fb41078803b6b6f6722b17322d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:20:52 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Wed, 24 Apr 2024 03:20:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:a6e8bb341b139fa8aae0ba05045cf5f0ef66e8260b98cda6950cadf916ed0f41`  
		Last Modified: Thu, 02 May 2024 18:12:45 GMT  
		Size: 187.1 MB (187143091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:7903613b4182abe216e7e36c9ee4ae650fe4a14316160360cdd8f94e459cf946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbc8ff473cd3ae52f9b1427e15706fae4d3d9591a2c8bf3f28b31a19f1a09c4`

```dockerfile
```

-	Layers:
	-	`sha256:6c78d4a4191a65c7af0530480d11f289861eab1ee86584e8133ba9ae8bb2de48`  
		Last Modified: Thu, 02 May 2024 18:12:41 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef473a7f3ff3cbb5e5bff01f89d91164174143787bc52b54999cd47006cd918`  
		Last Modified: Thu, 02 May 2024 18:12:40 GMT  
		Size: 13.0 KB (12979 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bookworm` - linux; s390x

```console
$ docker pull rust@sha256:35a2f27aa7b8300d5a2e4aed602e03edcc950d6dcfbd9d7f8b8a86be19752041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578756361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008c354d831f826547ccd2d2a946c706ca40e6916ef33806ecaa916a21041dd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:42:45 GMT
ADD file:6b0e091009ac95d80973222b4f56557fc521253f20bb18eea1c9da2b61ed5cc2 in / 
# Wed, 24 Apr 2024 03:42:53 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea1cd174fa855055f0cc0296260c9e987dbd4cddfc8655fe48891b91e5af95b7`  
		Last Modified: Wed, 24 Apr 2024 03:48:59 GMT  
		Size: 47.9 MB (47942206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e212650b3684bdd95eb8c4cd55ad81ca7f992455cbcc5c126d1aac521b5399`  
		Last Modified: Wed, 24 Apr 2024 04:23:04 GMT  
		Size: 24.0 MB (24047036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5049d590d068e07d3557ef371a6ccc2fc96ffadeabbf0c1115204536ff84b`  
		Last Modified: Wed, 24 Apr 2024 04:23:21 GMT  
		Size: 63.1 MB (63130514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74409f156b70503c3e2227e45d964aec57dadc484e6492078584c8cad2e0884f`  
		Last Modified: Wed, 24 Apr 2024 04:23:50 GMT  
		Size: 183.2 MB (183208845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0a40d21a23b6b34012eaf7b342b43911c5d236a2f478d1df55a213f5b8247d`  
		Last Modified: Thu, 02 May 2024 18:17:05 GMT  
		Size: 260.4 MB (260427760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:70d0ae53ab927ca2824b1543a39761aaa621f8f640351e84e30c9cffcdada927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e4231ef234646dcaa8923b11a5a42334f73cdcc3a2467a2ef8ea47342e8f4`

```dockerfile
```

-	Layers:
	-	`sha256:2d98932b6c77d39b088f5fb17d27824d35fa3db3a89f0dc9677db81f3f0b219b`  
		Last Modified: Thu, 02 May 2024 18:17:02 GMT  
		Size: 15.2 MB (15185203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9bb7ba18a7a3be562faf0170f9215c5065bafb098b5bf71c12feccc9dce19c`  
		Last Modified: Thu, 02 May 2024 18:17:01 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:bullseye`

```console
$ docker pull rust@sha256:2552dc030938db6be68061470bb1d06a614e2523bc28aca5ae3db334fe4b3476
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
$ docker pull rust@sha256:e6d6b30cc542e783d7c99f59c4981a1dfc16854065004dd2031731c1f39bde8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **500.0 MB (500031479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcad364931eede82edf28ce9a8b0d641d449dfc7c66a5409117906b6b6b8b4ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:19 GMT
ADD file:d9efaba9e396cd5732f1689338ef5f1fbb66667806efe9c6938ca7169b305496 in / 
# Wed, 24 Apr 2024 03:28:19 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:13:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:534d57e3d7c23ea864729859cd9639d95758dc80d3fae7c2f1a781369374f72c`  
		Last Modified: Thu, 02 May 2024 17:53:19 GMT  
		Size: 177.6 MB (177591486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:394674afd531ba7ba75772c582acf4520d9dfde25713860cf929548250230b39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14987362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd227c9c6937e47e8c7124353322fb9c95d173d5e40454385bc62a5de0a4d204`

```dockerfile
```

-	Layers:
	-	`sha256:5175f4542d292457f1a4530967191286a12c21391a2bb9a183579ff56267c300`  
		Last Modified: Thu, 02 May 2024 17:53:17 GMT  
		Size: 15.0 MB (14974944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6da52b512eddefa1c1ecbaaa573257018e0b1790c5832c459900ce53606e1b2a`  
		Last Modified: Thu, 02 May 2024 17:53:16 GMT  
		Size: 12.4 KB (12418 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:04d28c769d11d7e8647f2cb4abc12e4772bf7ac447fdc05e7a6713bf8619ec59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.8 MB (495758778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:021e7713c700cad89a3873cd2bcb165eeda0cba39d5eac5e6c0ceb0433e2015f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:15 GMT
ADD file:59046a1e0987059e779fff5a0f35e03203c109d778a75058e9474705d3fcfdff in / 
# Wed, 24 Apr 2024 04:07:15 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:51:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:52:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:53:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:853e2341066ebc3a07d3c44ebac8c3ce40daf429fb9cc3f49f2d35115e9cc93f`  
		Last Modified: Wed, 24 Apr 2024 04:11:34 GMT  
		Size: 50.3 MB (50255574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5d5c1aa98981d0ab503d79e97e4eeed8435372346757065a98c291d66c74df`  
		Last Modified: Wed, 24 Apr 2024 05:03:57 GMT  
		Size: 14.9 MB (14880390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94741efe025699cbcd617a32ea95a4fea8cfaeedfa3b93bd9cbc7ed02063a74a`  
		Last Modified: Wed, 24 Apr 2024 05:04:17 GMT  
		Size: 50.4 MB (50359575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba251a5fa80ede4ef9bfae4161563b58236318c68e2a17d1cbd5afa4ba9a2c68`  
		Last Modified: Wed, 24 Apr 2024 05:04:53 GMT  
		Size: 167.4 MB (167442932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5d2b6834c7a0899f1680cc6d8cc388f1d0dca62c4f7a8ebe01f44f45352ed7`  
		Last Modified: Thu, 02 May 2024 18:12:01 GMT  
		Size: 212.8 MB (212820307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:80b041026f0b46d413060fd8525a3ba151a2eacd151071f8c61fc152cdfd39d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14788669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51b3ef7ff5219f52138329d10cb8348d58ffc8198540c1b328f90fbc8a82ea6`

```dockerfile
```

-	Layers:
	-	`sha256:6c813ccd1a4df3a4bbbbe45bfed024331d0fd2c3308c8a3d7d111ea597aafb5f`  
		Last Modified: Thu, 02 May 2024 18:11:56 GMT  
		Size: 14.8 MB (14776844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19847e3e85938bfccef756d696d053d674fb2f4065a928f39c3451d036e26c9d`  
		Last Modified: Thu, 02 May 2024 18:11:55 GMT  
		Size: 11.8 KB (11825 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:82d27aac8d8758af4166b14ffb1cc316fa08b2fd8cfaf238846ba54bc171e9f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **560.4 MB (560350376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423aa11d7bda4aed73983759f01bf96699ace117c8ea8c844c414b738c64bcd7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33008ff0928e624ce22cedd5d004edd66b80372bfd1223e8900206330213ee34`  
		Last Modified: Wed, 24 Apr 2024 08:42:31 GMT  
		Size: 15.8 MB (15750623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36972983386f768dbeff5de37af34ed4e2f59541b2e3c43575f29758c3591923`  
		Last Modified: Wed, 24 Apr 2024 08:42:45 GMT  
		Size: 54.7 MB (54696233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3224178d7041e10ec03b66358ce4ba6bb5aeaf26b593f3e8672ca38f7b70769e`  
		Last Modified: Wed, 24 Apr 2024 08:43:09 GMT  
		Size: 189.9 MB (189912094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97275dd0257b83d60c67c3d70971c98640014802ea42bae0e7414eaacf4f365b`  
		Last Modified: Thu, 02 May 2024 18:22:28 GMT  
		Size: 246.3 MB (246251467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cb31ecf48d87fa71df2cb5a2933820e8ecbdd1dbb690d4b5aff13d7fbd87755e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14989175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec2aef4675fe30517f9f710edbba6c5a198def25e9b99362e323b7e9b30a6d4d`

```dockerfile
```

-	Layers:
	-	`sha256:eb1b6d19dba8c8c9789a080460223469c5e39861aabf0abb48fe6a856f49572f`  
		Last Modified: Thu, 02 May 2024 18:22:23 GMT  
		Size: 15.0 MB (14977411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ed5b26cdc4f076066fac6d6878fca32b53fbe9a0c5bf6b5429bb951a8de7223`  
		Last Modified: Thu, 02 May 2024 18:22:22 GMT  
		Size: 11.8 KB (11764 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; 386

```console
$ docker pull rust@sha256:232c18232dd7076711f3603df35b9bfe483c49663e03b9259edbd30810dfc02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.8 MB (518766287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:858075fb8a3b54656c0ee7518ef0b22601a2d1b7d4d1f2fd037699198b2bef9a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:08 GMT
ADD file:f45ff600062e56788dec8eb7a1a4eb58c56391243efecfc62b3f911f35ce7517 in / 
# Wed, 24 Apr 2024 03:39:09 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:30:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:31:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:32:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:df053a23eab4180eece3d17162346216b301343de9fb6226cd226f21702be82f`  
		Last Modified: Thu, 02 May 2024 17:53:36 GMT  
		Size: 190.6 MB (190599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:cf1fa86ecf03dd1fbb4dcce34d4a6d575a64d018570476a025626d21108bf3e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14976156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0056775c2d4a3ef6fbace0e34ff6db97f0f12ad062f8875c69193a8f497145ad`

```dockerfile
```

-	Layers:
	-	`sha256:189cacbc159513dae1c96778228fcacb8fa5341832b01271f051b1124b140d81`  
		Last Modified: Thu, 02 May 2024 17:53:30 GMT  
		Size: 15.0 MB (14963767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e86ac21aeb5f940ce0d749c02477c27d23e1023a107afeb492eedaa85b35f6e8`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 12.4 KB (12389 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:74f6d27411b0fe1655b74893221edde39cc79b5c54f779b8f924d0f94e5b6ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **518.1 MB (518096210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:655131ce8b88722fe88822b0323c0f901ee374ed6e1eb86f90e53c8a0f1031de`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:25 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
# Wed, 24 Apr 2024 03:21:30 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:04:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:f315af7fc149bdbb645add44aaef365e14662b9bf33a24ebcdeda2ed49bcef6f`  
		Last Modified: Thu, 02 May 2024 18:07:04 GMT  
		Size: 187.1 MB (187143092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:02041686275df55e6c1cde2ab50a36777b23e5f0bfa0620bcea85ce288d8403d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (14954340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c14dc83c058acbfa6bd18b2ba83506e0f719407a324008942f86a2d4dcc87af`

```dockerfile
```

-	Layers:
	-	`sha256:ce1abb7d3006b3e51d88e3b055b4055bbc25212003172c9a9aa9532a8425ad91`  
		Last Modified: Thu, 02 May 2024 18:06:59 GMT  
		Size: 14.9 MB (14942547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c168268955e9148deab9bdffcc4c0a75e9a8cea798c2286a9aab8cdf5599398f`  
		Last Modified: Thu, 02 May 2024 18:06:58 GMT  
		Size: 11.8 KB (11793 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:bullseye` - linux; s390x

```console
$ docker pull rust@sha256:e3c00ec457a002c90f44ff20936bcfee6bd86f03ab1cc7750785060a7895e5d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **556.5 MB (556478959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3364960915922de42d06974605b4e00f6fc171fd9a6475446ac1f876a6543c0f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:33 GMT
ADD file:e0a1fc1de1477cea6fe41bdd15378013c680928cad3988dd16926cc1562c775e in / 
# Wed, 24 Apr 2024 03:43:38 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:b57a10abb081ff40e5bb34246c3875a71b8d258f767c4f8384d7054b1bc42725`  
		Last Modified: Wed, 24 Apr 2024 03:49:31 GMT  
		Size: 53.3 MB (53337419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293ed92794c4710c20ea615a0e07fe947837768482be7bcd9d1fccb335072a92`  
		Last Modified: Wed, 24 Apr 2024 04:24:03 GMT  
		Size: 15.6 MB (15642846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede0318d2197701d71929fa882d8d64bdc0c65ee6bc9abd4bd4063694d92acb7`  
		Last Modified: Wed, 24 Apr 2024 04:24:17 GMT  
		Size: 54.1 MB (54076626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c3f9b4c72abaa52996d64ffc8754f8500b075a8a677c0fe59c310548e9af5c`  
		Last Modified: Wed, 24 Apr 2024 04:24:43 GMT  
		Size: 173.0 MB (172994116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66302c05a1f58a25604176a4b9b6bc0e717fb72ff97e0334ea79fb2895e26df7`  
		Last Modified: Thu, 02 May 2024 18:08:54 GMT  
		Size: 260.4 MB (260427952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:52b39a86a4ea99cb0237d970a10213cddfe8f113046bf4abdd5d3e4a3cda1363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.8 MB (14808368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bec0dfd4f38a0e9dad4996be6db3bacd06333698fa0cae356936fc13be9fd4`

```dockerfile
```

-	Layers:
	-	`sha256:83ce677ca56d4a667f9518ab5babc3e5b9ad1f44c3a5dbd0ff5ba123690f4055`  
		Last Modified: Thu, 02 May 2024 18:08:50 GMT  
		Size: 14.8 MB (14796613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f959e24eefab058ecc036f364b2858652b6977cafed184475b485ec952b32bc`  
		Last Modified: Thu, 02 May 2024 18:08:50 GMT  
		Size: 11.8 KB (11755 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:buster`

```console
$ docker pull rust@sha256:fcb09007a565e6705c6d49835377d7d18e050b309203edc9e412977e91269257
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
$ docker pull rust@sha256:47eacf3b5d2efd391224926939f061ff7acd7574beacdbcf721c82b01a65715e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 MB (490711222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bef0c9fda88c0ce49bbbe4e82e4c8d2496752121e8e07c5f59170f61ca0d31d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:33 GMT
ADD file:eea1eb05334cd4d0032909b2c56fc86a54faad563cbc3d2d46e763ce9e8922ab in / 
# Wed, 24 Apr 2024 04:07:34 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:53:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:54:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:55:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
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
	-	`sha256:fe0f6a4b48afbd61f9ef055b862b89cc5fc3980c4be6d4ccdc4e71eb6bd56d0d`  
		Last Modified: Thu, 02 May 2024 18:07:53 GMT  
		Size: 212.8 MB (212820147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:752d344513be8e413c08339a72a1696e061067a176479b706f0ae0a0c25048f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15780088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c18d957fb0511cfe9d344a4de14bcc9b40ee6d3bfbc1d980e180ae8df9d7aea`

```dockerfile
```

-	Layers:
	-	`sha256:da347c4aa030e17d6c56379e77bbdc5e28dab4fed5f89adbf67d26f052266c5f`  
		Last Modified: Thu, 02 May 2024 18:07:47 GMT  
		Size: 15.8 MB (15769023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52097463634c6c7d47e034b943ee50d0b5c9c9b3d2a8be616e9ebc076bb95f37`  
		Last Modified: Thu, 02 May 2024 18:07:46 GMT  
		Size: 11.1 KB (11065 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:775daa3419885651f2e284f10b29385f68347c1b99caf12ee7dbf82edc24947f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **548.9 MB (548916487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee5233d262b43ce5dd1ff865b0ee9ac12ae4be5844a39f716b3cd8396774e15b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:00 GMT
ADD file:5a7db8f66ffc46a108f386106163b47bdb4a3bcbe5341a94d47988b259039067 in / 
# Wed, 24 Apr 2024 04:11:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:34:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:35:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:36:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
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
	-	`sha256:af5cdf87e38274705e7b47b4d3a5ccbab3f4bf94894cac0c5b2d82abfcf1989e`  
		Last Modified: Thu, 02 May 2024 18:19:24 GMT  
		Size: 246.3 MB (246251497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:buster` - unknown; unknown

```console
$ docker pull rust@sha256:dac6fc781e375c3f98871b1045ea01bd75fc62f126ba52697ba0c6b38a1f4aa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (15969386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2c1d63305c600acd748d5093b508df829037b295ab55b92bcc3998cf8ce8aa`

```dockerfile
```

-	Layers:
	-	`sha256:65b7feb61540a8b5987675be790620a8a6a102d1c29faafbb53fc91011a7161d`  
		Last Modified: Thu, 02 May 2024 18:19:19 GMT  
		Size: 16.0 MB (15957718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eccd3a895875d4cbfb484b9fb55f5e778d710cf340062cd3a9484aadb5c29130`  
		Last Modified: Thu, 02 May 2024 18:19:19 GMT  
		Size: 11.7 KB (11668 bytes)  
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

## `rust:latest`

```console
$ docker pull rust@sha256:0dd183faf7bc5b9b8efe81cfd42701a5283577520b185b511e322e5bf52f8fc7
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
$ docker pull rust@sha256:d50e312c75fbd66f5cc7b1ab6d76892529751526629c294f34ca217016fe0425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **526.5 MB (526535638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d8eec96e0ea00b3ec3c6c2e03ef8a15113d8dd0682170d3757c06a78e73dce`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:27:57 GMT
ADD file:2cc4cba2834c189d0dc41b5d79e1236770862c38452517fcbbb28015b88ab5cf in / 
# Wed, 24 Apr 2024 03:27:57 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:10:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:6b9f9d886ac307c9982286da0ae1d85ad364df502e05f2c5c14c9505f30a4feb`  
		Last Modified: Thu, 02 May 2024 17:53:26 GMT  
		Size: 177.6 MB (177591491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:9d352cd5f6a779bed1be7057ea6557c8de8f96c40e26e555b469d2c2f8405643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15384104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511f0cc56710400a858b2b313a1fb6c554e2ca7debcdcfd5d6ae3ac4870e716f`

```dockerfile
```

-	Layers:
	-	`sha256:f4420d9292d76286420dd7187c5b08b956041f3a4d90ecee23f7d1f91f3638ac`  
		Last Modified: Thu, 02 May 2024 17:53:24 GMT  
		Size: 15.4 MB (15370524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6daf94a67a74ecaca457f9fc6812857963aae03a4bdf69ffece0604d2d071e2c`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 13.6 KB (13580 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm variant v7

```console
$ docker pull rust@sha256:225556750412cc8f6f468fd8c3bd1176e9b06c90153acb0e045b500c21265bdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **514.3 MB (514307156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16d9947ff3490d7e91dbee0aade813ded906312a29924c5226904b76432127e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:06:51 GMT
ADD file:b6d26ef7cfc03fe202f7a5ac219566bc37f382ffadc9acdad685f2dd318cf0e4 in / 
# Wed, 24 Apr 2024 04:06:52 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:50:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:51:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:80e84b3257949a283234599e3906626cfb4ff482d06fa4dc3eaf1dd36551dafa`  
		Last Modified: Wed, 24 Apr 2024 04:10:48 GMT  
		Size: 45.2 MB (45174994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52886721ea5a8a8bac2b197dccd42a74948b88bedcfe0fdf8b24e234c0a660d0`  
		Last Modified: Wed, 24 Apr 2024 05:02:39 GMT  
		Size: 22.0 MB (21953968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d07170ec327fa1117b5289697e5555f4c3ba76d00200d7c7cc5c143086856f`  
		Last Modified: Wed, 24 Apr 2024 05:03:03 GMT  
		Size: 59.2 MB (59216995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937bd8fccb438207fe0e77a48873de07dbe1fbea251206222298b72dbd2b3d8`  
		Last Modified: Wed, 24 Apr 2024 05:03:45 GMT  
		Size: 175.1 MB (175141109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5499a6710f841b95850a0e6c3589a558408d5ecdb1efe2d461015241a86667d9`  
		Last Modified: Thu, 02 May 2024 18:16:14 GMT  
		Size: 212.8 MB (212820090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:a8d872088f3bc18ac36bb4ee06e93eac69f16897387344fcfd238be07505d19d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15189426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f357e10dda11cec2f915422dbbb7f4dc9ef73032fc8aa82efe6609b3de03843`

```dockerfile
```

-	Layers:
	-	`sha256:67f172e545903f27510fe2841e22b7f07947e3314640824e648cc35a5e4af23c`  
		Last Modified: Thu, 02 May 2024 18:16:09 GMT  
		Size: 15.2 MB (15176407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:becad9a5634f77e5e49e5e8f1bda8454cd92e0059d86c4ae3e43d13bba5c36d9`  
		Last Modified: Thu, 02 May 2024 18:16:08 GMT  
		Size: 13.0 KB (13019 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:cb3fe1b45243325da5aaafb59bc75f8541697bfd9acbfedc914c0f132c7949ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.0 MB (586021653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b44c56b25c83977fc9ebfdf243d37b0b15ab1a4fcf0c647f0878847949cf84`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:30 GMT
ADD file:07ae70ad05f39a24007b6bde4418c9934bc3865fe855dfcf62a44d8a30375739 in / 
# Wed, 24 Apr 2024 04:10:31 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:32:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:60bdaf986dbe787297bb85c9f6a28d13ea7b9608b95206ef7ce6cdea50cd5505`  
		Last Modified: Wed, 24 Apr 2024 04:13:43 GMT  
		Size: 49.6 MB (49613341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e100ddc6b415c632410507293430c0fe6bb4228ab320ed59548c6dc030b4e4a`  
		Last Modified: Wed, 24 Apr 2024 08:41:28 GMT  
		Size: 23.6 MB (23586795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9a57bc3c0cb0c1ea5d28dc03fb4451ae05dc271b53941c27edf70eaf70b6e6`  
		Last Modified: Wed, 24 Apr 2024 08:41:47 GMT  
		Size: 64.0 MB (63994806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7476478a1e1450b999421118cb8f193aa62f1816e0cadd988a084385cf0a5696`  
		Last Modified: Wed, 24 Apr 2024 08:42:20 GMT  
		Size: 202.6 MB (202575289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ab2e8f65d41c1e5e2c493944dc3f6ca456b65a5275ac05e12bc31af0b697d`  
		Last Modified: Thu, 02 May 2024 18:26:37 GMT  
		Size: 246.3 MB (246251422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:9562e2467c5e3f2f6ee0ccff2633f57a5ff3cd388a582fca74510f46aba072bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15411981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f6aaf4016fa5c395bc612fd990fc2d7422e8623e54ebe02b7b2625e179f7920`

```dockerfile
```

-	Layers:
	-	`sha256:1c4d0653a7e064d93a08cf2e3cb73351a07d67c388a1a2590326a06812bff5f3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 15.4 MB (15399046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:790e84f88528ef27e0f653b5aeba1fafd203db38ba551366c785a778180828b3`  
		Last Modified: Thu, 02 May 2024 18:26:32 GMT  
		Size: 12.9 KB (12935 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; 386

```console
$ docker pull rust@sha256:d1f3c3a8b571383507c4e76f99678f065d5a03aa90eea84693c767e32fc869c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **542.2 MB (542180953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009dec677b8280c20069beef31c3fbbbc461bc0ab36f0558b2ec40439a5f6079`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:48 GMT
ADD file:f9a006425066d79ec04210dee08da23c9a68df2b7ea7e47b41cbc9d8b7545361 in / 
# Wed, 24 Apr 2024 03:38:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:28:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:29:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:30:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:1614889c1e665cd335548134ca677fb6f9f1910d4ab6488c04424418a97f495a`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 190.6 MB (190599211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:de08ac7a06b5af621f4e0fb99dabf08168a533017d45b6ff2510485f17d0b355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15363096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc533d073cc58cb332d3410a63a6c6f32d775b9febedb13c3c8b78a6d6079a9`

```dockerfile
```

-	Layers:
	-	`sha256:64ac9f5f1c25c9fffc99c099a79689856019c48dfffddbb43b51cba223012a11`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 15.3 MB (15349565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:921284eb6647f818f95a3f3db77efe9fa3b4c28d2bf2158f08f1c984fe96fef0`  
		Last Modified: Thu, 02 May 2024 17:53:25 GMT  
		Size: 13.5 KB (13531 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; ppc64le

```console
$ docker pull rust@sha256:eb08c0b17cc0c417388189ce35bf4fb1f087a9e6ff51c1bfcec9ff410f2a8733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **550.2 MB (550221275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3bcff95d0b422fd84f7fcd46bf86991ba30fb41078803b6b6f6722b17322d9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:20:52 GMT
ADD file:6b48a0374d2bf17058a1ace290a29b25ef9f56d85e94d8cd33ac09dbdc5daddf in / 
# Wed, 24 Apr 2024 03:20:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:48:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:49:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:56:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
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
	-	`sha256:a6e8bb341b139fa8aae0ba05045cf5f0ef66e8260b98cda6950cadf916ed0f41`  
		Last Modified: Thu, 02 May 2024 18:12:45 GMT  
		Size: 187.1 MB (187143091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:7903613b4182abe216e7e36c9ee4ae650fe4a14316160360cdd8f94e459cf946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15358501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfbc8ff473cd3ae52f9b1427e15706fae4d3d9591a2c8bf3f28b31a19f1a09c4`

```dockerfile
```

-	Layers:
	-	`sha256:6c78d4a4191a65c7af0530480d11f289861eab1ee86584e8133ba9ae8bb2de48`  
		Last Modified: Thu, 02 May 2024 18:12:41 GMT  
		Size: 15.3 MB (15345522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef473a7f3ff3cbb5e5bff01f89d91164174143787bc52b54999cd47006cd918`  
		Last Modified: Thu, 02 May 2024 18:12:40 GMT  
		Size: 13.0 KB (12979 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:latest` - linux; s390x

```console
$ docker pull rust@sha256:35a2f27aa7b8300d5a2e4aed602e03edcc950d6dcfbd9d7f8b8a86be19752041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **578.8 MB (578756361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008c354d831f826547ccd2d2a946c706ca40e6916ef33806ecaa916a21041dd6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:42:45 GMT
ADD file:6b0e091009ac95d80973222b4f56557fc521253f20bb18eea1c9da2b61ed5cc2 in / 
# Wed, 24 Apr 2024 03:42:53 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:11:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:12:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version; # buildkit
```

-	Layers:
	-	`sha256:ea1cd174fa855055f0cc0296260c9e987dbd4cddfc8655fe48891b91e5af95b7`  
		Last Modified: Wed, 24 Apr 2024 03:48:59 GMT  
		Size: 47.9 MB (47942206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e212650b3684bdd95eb8c4cd55ad81ca7f992455cbcc5c126d1aac521b5399`  
		Last Modified: Wed, 24 Apr 2024 04:23:04 GMT  
		Size: 24.0 MB (24047036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c5049d590d068e07d3557ef371a6ccc2fc96ffadeabbf0c1115204536ff84b`  
		Last Modified: Wed, 24 Apr 2024 04:23:21 GMT  
		Size: 63.1 MB (63130514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74409f156b70503c3e2227e45d964aec57dadc484e6492078584c8cad2e0884f`  
		Last Modified: Wed, 24 Apr 2024 04:23:50 GMT  
		Size: 183.2 MB (183208845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0a40d21a23b6b34012eaf7b342b43911c5d236a2f478d1df55a213f5b8247d`  
		Last Modified: Thu, 02 May 2024 18:17:05 GMT  
		Size: 260.4 MB (260427760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:latest` - unknown; unknown

```console
$ docker pull rust@sha256:70d0ae53ab927ca2824b1543a39761aaa621f8f640351e84e30c9cffcdada927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15198120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e4231ef234646dcaa8923b11a5a42334f73cdcc3a2467a2ef8ea47342e8f4`

```dockerfile
```

-	Layers:
	-	`sha256:2d98932b6c77d39b088f5fb17d27824d35fa3db3a89f0dc9677db81f3f0b219b`  
		Last Modified: Thu, 02 May 2024 18:17:02 GMT  
		Size: 15.2 MB (15185203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9bb7ba18a7a3be562faf0170f9215c5065bafb098b5bf71c12feccc9dce19c`  
		Last Modified: Thu, 02 May 2024 18:17:01 GMT  
		Size: 12.9 KB (12917 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim`

```console
$ docker pull rust@sha256:517c6272b328bc51c87e099ef4adfbc7ab4558af2d757e8d423c7c3f1cbbf9d5
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
$ docker pull rust@sha256:144edf7af2e5e374afdee02fd458df5bad41aba4cae314ace9d43f7933d44c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277315532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036d20da216ad2e94545e4e82700ee8c8ee3ad79fa0e2dca1261f8a69a87a937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8f9fca3e1073639d97fde71b99e2ef803078e36ed1cd97b74ce545ee7b17`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 248.2 MB (248165053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:a10481a084e247a58cb63c17b394d4e65463e3c8369e21bcfc769abbdfffb9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911a63093a97a45bdf3e678240c96fe3b7f81befc1871a5542db741b9b51a7d`

```dockerfile
```

-	Layers:
	-	`sha256:371755c5d7b19c0c727d6c961f8c6528bc0cbd0b3d2c7067a40ddd1f9eaa4e74`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6556d0382c9b778b94f7cc91b1d3f7659518e567fab6462da86ebe4ac90c6382`  
		Last Modified: Thu, 02 May 2024 17:53:22 GMT  
		Size: 13.2 KB (13172 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm variant v7

```console
$ docker pull rust@sha256:ffc8f22bbcaf9c443db0c997aba6a8f0773d989e29a5865d0f164a36f15e8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285223017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d69dbc41e535f1c4657a7b35fe40a346dce9c4f07b392370b716e1c4ea8c45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f060f4605d55cb88006aa78ea1433f0129af80557306aa6ef11d728ad8c15`  
		Last Modified: Thu, 02 May 2024 18:18:12 GMT  
		Size: 260.5 MB (260482575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:8ee1faa28bc0f8ec0e92ba67f71be26d4570984f23660ad77c52f9cdaf0e4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14586c5fd8ae352e99facffdc8e47f2ffe4a171ae426fa7163a3033099714f4d`

```dockerfile
```

-	Layers:
	-	`sha256:f920b7810ae2eb89611842b3c8d00f4e763ddaa0dbb6dc67bc77bc0979211af2`  
		Last Modified: Thu, 02 May 2024 18:18:06 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6070f226a82471804b25ddfcd5994dfb20c75710288cb8fa305eeecbc9689a`  
		Last Modified: Thu, 02 May 2024 18:18:05 GMT  
		Size: 13.1 KB (13107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:701d523927f60aa6594b6b639e16b2872b090efd77b38206eb07f8a5ab5f4b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341067862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d7c8b33fff18a1de7a58bd9764df34dcb7689471c8332703ef166a3be91dbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b6ff75fe73e0b624033411b211e30ab65a0dfe2f196bc831afaa3f262ad40`  
		Last Modified: Thu, 02 May 2024 18:28:13 GMT  
		Size: 311.9 MB (311887927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:3068c80cfcc050b7d2f84d2daa26eb1bb6646dbef2cdc889b4706d0ecec10c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94192de4d427019b53f8d6f476258f84f6c701b7cc313fbe20aac8356c685388`

```dockerfile
```

-	Layers:
	-	`sha256:fe0470bf526cfabeeff81d8175f1ad542787eb63d46eac59584aa0c9700cb865`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 3.9 MB (3941462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e741b4e2feaf42a20f56bbcccb528e05e69b28f20a30f471dab96b02dd26885d`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 13.0 KB (13023 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; 386

```console
$ docker pull rust@sha256:9a0ff69ac63b29617f2772d8af475f42b17376ae675690bd4b6ffbd6fa013a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288155332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730521317992ca457b5e32b681e5c2fc6a9985f74b26c05ab75a898d70063efd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be463c23e962e7814d7269dd918a3abf7fe7480f3491260b6939bc093b40232`  
		Last Modified: Thu, 02 May 2024 17:53:34 GMT  
		Size: 258.0 MB (257992149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:406577ad4a920a84505e527616fcb1f008cff2e259737b980109d6586c441132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94959a9ba35ac8e7aa52d2c9634583789f540a6ce1cdf8970c1aeafbeb383266`

```dockerfile
```

-	Layers:
	-	`sha256:5fccb080d41ea034eca85abe7287cd6513b3fcf1304c5b0ab744b5e4f7604ee2`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5ee26d72cca7cd34f6faa2688b32a264613f3b88beb239a82737e7a7bdd0b8`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; ppc64le

```console
$ docker pull rust@sha256:ea7984b98ee3317d77412b9077362d5f7934cbed7f5d5ce18a977f899e9386c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288845524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a166a0772dcf6517a472407901b610b01b80c50d7487fd756971dc08ca26d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bdd5b65845940ee92c4225121c6b04def8a421d1c550f7d8d65db0e37bf19`  
		Last Modified: Thu, 02 May 2024 18:15:05 GMT  
		Size: 255.7 MB (255704323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:b8cf1c2e22630a3fb96504ce4e0109e450e2f91f2338965264da180dffb4be0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e443bda8941eefcf331e18425d4d04513900c67b623379aae5f5c3ba60799f`

```dockerfile
```

-	Layers:
	-	`sha256:57c7d4ef78d8836d083ed51f7584a8611e874b74c989c77cbdaefba43cf9c737`  
		Last Modified: Thu, 02 May 2024 18:14:59 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721e6450ded9a8224165692a227cf32021b20727fa9e27b7eb51b9ee46c98d64`  
		Last Modified: Thu, 02 May 2024 18:14:58 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim` - linux; s390x

```console
$ docker pull rust@sha256:f2f85fb1ee50bb9ddd8312a215bd06ef84d9d8a32ae978df573ac5b9b84ab38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337865924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2db01fe12c831f8b1c810ff63f0059a28b15cebb3fc607f041e7f43ba47394a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c36f802355139032b4b3b2815d90b8684055c93beadd105d203de5c4574421`  
		Last Modified: Thu, 02 May 2024 18:19:38 GMT  
		Size: 310.4 MB (310353569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim` - unknown; unknown

```console
$ docker pull rust@sha256:1d010d6d80dc73fcb8b111939211fe047c868a66965107fe6522c5ac238f2882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67848fc2610daa3a0488587b7d72d3197b8f69b13b8bc20914dec3e53cac68c4`

```dockerfile
```

-	Layers:
	-	`sha256:45465cb45a531518db8458bf81a4591118d814a4fcc27d32e893ed00128240f1`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 3.8 MB (3762075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ba7b0835f73f3eba7b3413925b87bc83556d2ccd55606dfd68c5715cec19c7b`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bookworm`

```console
$ docker pull rust@sha256:517c6272b328bc51c87e099ef4adfbc7ab4558af2d757e8d423c7c3f1cbbf9d5
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
$ docker pull rust@sha256:144edf7af2e5e374afdee02fd458df5bad41aba4cae314ace9d43f7933d44c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277315532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:036d20da216ad2e94545e4e82700ee8c8ee3ad79fa0e2dca1261f8a69a87a937`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:09 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Wed, 24 Apr 2024 03:28:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3add8f9fca3e1073639d97fde71b99e2ef803078e36ed1cd97b74ce545ee7b17`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 248.2 MB (248165053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:a10481a084e247a58cb63c17b394d4e65463e3c8369e21bcfc769abbdfffb9a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3932350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7911a63093a97a45bdf3e678240c96fe3b7f81befc1871a5542db741b9b51a7d`

```dockerfile
```

-	Layers:
	-	`sha256:371755c5d7b19c0c727d6c961f8c6528bc0cbd0b3d2c7067a40ddd1f9eaa4e74`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 3.9 MB (3919178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6556d0382c9b778b94f7cc91b1d3f7659518e567fab6462da86ebe4ac90c6382`  
		Last Modified: Thu, 02 May 2024 17:53:22 GMT  
		Size: 13.2 KB (13172 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm variant v7

```console
$ docker pull rust@sha256:ffc8f22bbcaf9c443db0c997aba6a8f0773d989e29a5865d0f164a36f15e8bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285223017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d69dbc41e535f1c4657a7b35fe40a346dce9c4f07b392370b716e1c4ea8c45`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:05 GMT
ADD file:719e14b0eb733543ace336c71543b593f88e2b452e40fb315f5f6e49ebe6af58 in / 
# Wed, 24 Apr 2024 04:07:06 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:77e415c4e7c678efbc2cc774d4bc05f6f2de2a2e04959d7e324ce092026c650e`  
		Last Modified: Wed, 24 Apr 2024 04:11:13 GMT  
		Size: 24.7 MB (24740442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8f060f4605d55cb88006aa78ea1433f0129af80557306aa6ef11d728ad8c15`  
		Last Modified: Thu, 02 May 2024 18:18:12 GMT  
		Size: 260.5 MB (260482575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:8ee1faa28bc0f8ec0e92ba67f71be26d4570984f23660ad77c52f9cdaf0e4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 MB (3749457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14586c5fd8ae352e99facffdc8e47f2ffe4a171ae426fa7163a3033099714f4d`

```dockerfile
```

-	Layers:
	-	`sha256:f920b7810ae2eb89611842b3c8d00f4e763ddaa0dbb6dc67bc77bc0979211af2`  
		Last Modified: Thu, 02 May 2024 18:18:06 GMT  
		Size: 3.7 MB (3736350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf6070f226a82471804b25ddfcd5994dfb20c75710288cb8fa305eeecbc9689a`  
		Last Modified: Thu, 02 May 2024 18:18:05 GMT  
		Size: 13.1 KB (13107 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:701d523927f60aa6594b6b639e16b2872b090efd77b38206eb07f8a5ab5f4b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341067862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d7c8b33fff18a1de7a58bd9764df34dcb7689471c8332703ef166a3be91dbd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:39 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Wed, 24 Apr 2024 04:10:39 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b6ff75fe73e0b624033411b211e30ab65a0dfe2f196bc831afaa3f262ad40`  
		Last Modified: Thu, 02 May 2024 18:28:13 GMT  
		Size: 311.9 MB (311887927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:3068c80cfcc050b7d2f84d2daa26eb1bb6646dbef2cdc889b4706d0ecec10c59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3954485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94192de4d427019b53f8d6f476258f84f6c701b7cc313fbe20aac8356c685388`

```dockerfile
```

-	Layers:
	-	`sha256:fe0470bf526cfabeeff81d8175f1ad542787eb63d46eac59584aa0c9700cb865`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 3.9 MB (3941462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e741b4e2feaf42a20f56bbcccb528e05e69b28f20a30f471dab96b02dd26885d`  
		Last Modified: Thu, 02 May 2024 18:28:07 GMT  
		Size: 13.0 KB (13023 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; 386

```console
$ docker pull rust@sha256:9a0ff69ac63b29617f2772d8af475f42b17376ae675690bd4b6ffbd6fa013a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288155332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:730521317992ca457b5e32b681e5c2fc6a9985f74b26c05ab75a898d70063efd`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:38:57 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
# Wed, 24 Apr 2024 03:38:58 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be463c23e962e7814d7269dd918a3abf7fe7480f3491260b6939bc093b40232`  
		Last Modified: Thu, 02 May 2024 17:53:34 GMT  
		Size: 258.0 MB (257992149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:406577ad4a920a84505e527616fcb1f008cff2e259737b980109d6586c441132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94959a9ba35ac8e7aa52d2c9634583789f540a6ce1cdf8970c1aeafbeb383266`

```dockerfile
```

-	Layers:
	-	`sha256:5fccb080d41ea034eca85abe7287cd6513b3fcf1304c5b0ab744b5e4f7604ee2`  
		Last Modified: Thu, 02 May 2024 17:53:29 GMT  
		Size: 3.9 MB (3900877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd5ee26d72cca7cd34f6faa2688b32a264613f3b88beb239a82737e7a7bdd0b8`  
		Last Modified: Thu, 02 May 2024 17:53:28 GMT  
		Size: 13.1 KB (13122 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; ppc64le

```console
$ docker pull rust@sha256:ea7984b98ee3317d77412b9077362d5f7934cbed7f5d5ce18a977f899e9386c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.8 MB (288845524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5a166a0772dcf6517a472407901b610b01b80c50d7487fd756971dc08ca26d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:13 GMT
ADD file:c7bb343c1806994c9561ecf8d3efa31be5e52ef43e2d7bfa957bafa0a7b4c586 in / 
# Wed, 24 Apr 2024 03:21:15 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6638f5b33adcc7d860acf4acdb1fe172ee2c42fa259745b817b65978748c2788`  
		Last Modified: Wed, 24 Apr 2024 03:26:31 GMT  
		Size: 33.1 MB (33141201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8bdd5b65845940ee92c4225121c6b04def8a421d1c550f7d8d65db0e37bf19`  
		Last Modified: Thu, 02 May 2024 18:15:05 GMT  
		Size: 255.7 MB (255704323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:b8cf1c2e22630a3fb96504ce4e0109e450e2f91f2338965264da180dffb4be0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3904693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1e443bda8941eefcf331e18425d4d04513900c67b623379aae5f5c3ba60799f`

```dockerfile
```

-	Layers:
	-	`sha256:57c7d4ef78d8836d083ed51f7584a8611e874b74c989c77cbdaefba43cf9c737`  
		Last Modified: Thu, 02 May 2024 18:14:59 GMT  
		Size: 3.9 MB (3891626 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721e6450ded9a8224165692a227cf32021b20727fa9e27b7eb51b9ee46c98d64`  
		Last Modified: Thu, 02 May 2024 18:14:58 GMT  
		Size: 13.1 KB (13067 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bookworm` - linux; s390x

```console
$ docker pull rust@sha256:f2f85fb1ee50bb9ddd8312a215bd06ef84d9d8a32ae978df573ac5b9b84ab38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.9 MB (337865924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2db01fe12c831f8b1c810ff63f0059a28b15cebb3fc607f041e7f43ba47394a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:18 GMT
ADD file:8cb22057960ef730bf4b15ce944d70fb8050d356172942041bcdbdb9d2a3a901 in / 
# Wed, 24 Apr 2024 03:43:21 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a0ff905a311848701ed9798adb40b6da9a87d229896e7a643fe00f69142410a8`  
		Last Modified: Wed, 24 Apr 2024 03:49:17 GMT  
		Size: 27.5 MB (27512355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c36f802355139032b4b3b2815d90b8684055c93beadd105d203de5c4574421`  
		Last Modified: Thu, 02 May 2024 18:19:38 GMT  
		Size: 310.4 MB (310353569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bookworm` - unknown; unknown

```console
$ docker pull rust@sha256:1d010d6d80dc73fcb8b111939211fe047c868a66965107fe6522c5ac238f2882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3775080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67848fc2610daa3a0488587b7d72d3197b8f69b13b8bc20914dec3e53cac68c4`

```dockerfile
```

-	Layers:
	-	`sha256:45465cb45a531518db8458bf81a4591118d814a4fcc27d32e893ed00128240f1`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 3.8 MB (3762075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ba7b0835f73f3eba7b3413925b87bc83556d2ccd55606dfd68c5715cec19c7b`  
		Last Modified: Thu, 02 May 2024 18:19:33 GMT  
		Size: 13.0 KB (13005 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-bullseye`

```console
$ docker pull rust@sha256:33baf245a3be288ec45d6534ebf94de088b834ef9202fd8e1176a3c1a0d9b730
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
$ docker pull rust@sha256:ebd24f6078bcc9f6b23f99a23e450f07d593f570d4bf072b5077added128bf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268954860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0502ee249ca6bfa22cfade789d5296feac6f0928a18703146f522c7cbf7ced10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e70c0d176523de333ba6a5be57344d80ccfba2589ed97a0714e502d2a34ca43`  
		Last Modified: Thu, 02 May 2024 17:53:20 GMT  
		Size: 237.5 MB (237520597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:a4dcfa88f53f7b2928efe6b3b835f897d81e20fddd853c43354998e2e042cabe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4151816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ef9d771e215a52ef1e40b292ede0d829c632e49e4c2367b41dac17ea648ac2`

```dockerfile
```

-	Layers:
	-	`sha256:cef011c9722bb44d4620b4e6bf096623230158399e11cb7d6d6f6c1a1af4bd58`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 4.1 MB (4139833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:599c91eec4cbd0f1ff1398eba0b589af02754a51f58dcd99213c8a7b227dac30`  
		Last Modified: Thu, 02 May 2024 17:53:14 GMT  
		Size: 12.0 KB (11983 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm variant v7

```console
$ docker pull rust@sha256:b2d51c493ce70a6df64cc9294f39b991ed51caad0d1b6b4df3aa73ebc0059308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.5 MB (281482631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1845601085edf0de75fa06cb3587d42cc4e40938d1b8a5f3ee758b9356526b5e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:25 GMT
ADD file:83a77ac4b262a896dbca1f6974e4401639b3e4d4ca432d88a933c7983e8ccf10 in / 
# Wed, 24 Apr 2024 04:07:25 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:913a7319952754f0a4a369ee846fb9ecf15cbbead6a1be0f4bdf4a7cbeb1d33c`  
		Last Modified: Wed, 24 Apr 2024 04:11:56 GMT  
		Size: 26.6 MB (26594742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb88c27c011a0bf4095b4dad73f3b89a8b7d5926dd1b563ef8b60cc2f6c06c3`  
		Last Modified: Thu, 02 May 2024 18:13:56 GMT  
		Size: 254.9 MB (254887889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ede45ee3c4bebfd74b4c54b87023ff6f1af70c483ef9065a07b00b14ba55e7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3961643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fb61ef780ac05b5018cad0ca9872b446a694f9a1b4446f0d1738749ea277525`

```dockerfile
```

-	Layers:
	-	`sha256:f821ed482f1443a1e918b75b417cb399f4cdb75370c37d86cca0be80d3b3b835`  
		Last Modified: Thu, 02 May 2024 18:13:50 GMT  
		Size: 3.9 MB (3949756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1e6fac619e4f33ae52bdc1063f1d01d4404064b385b8d19745a745c85900723`  
		Last Modified: Thu, 02 May 2024 18:13:50 GMT  
		Size: 11.9 KB (11887 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:55184f8e235a387dc47570d3c45c18868da64c7441759ff319bb02b00a30dd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.8 MB (331830874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2efb3db0f1f86b252af2ac6422352121d26077fc46501dc669c95b75f8b7e6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:54 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
# Wed, 24 Apr 2024 04:10:54 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a148bfdb5477b5b28e8af64d0d2c9d4cd738688d1ec0104833fc0685436c0c3`  
		Last Modified: Thu, 02 May 2024 18:23:57 GMT  
		Size: 301.7 MB (301743538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:47addcc74cfa8ab7f351d70c100db444ad71814d83f6c96928b852f42598e829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4148540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a0390a7297d4caf490960ab4c3265747cbbd92e4748bed00b3c994f72c02f2`

```dockerfile
```

-	Layers:
	-	`sha256:0508b7e94192ab544e987c54492b371e546f31d0f9919bc0c8cc1c452aa454c4`  
		Last Modified: Thu, 02 May 2024 18:23:49 GMT  
		Size: 4.1 MB (4136713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9dccf37e519bcea3696ecfb195e4a0b38348a412004399eb8308b338effdba8b`  
		Last Modified: Thu, 02 May 2024 18:23:48 GMT  
		Size: 11.8 KB (11827 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; 386

```console
$ docker pull rust@sha256:b189e96e3c85ca97178eb44feb77efb715773ecfe115c08226820247f7cd4371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283597724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d042e33fb45d8dbb5ab9375e1f445cca9f0842403742ac8e16e14a492d1379b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:20 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Wed, 24 Apr 2024 03:39:20 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d994d194bfa3acf9a46df705316048a9e421612eb43dc8e67d2fc7c4b47dc8cd`  
		Last Modified: Thu, 02 May 2024 17:53:23 GMT  
		Size: 251.2 MB (251172951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:23c07842a4cfddec1e1f1e230639073243847f2eb36626a93f578ed729e42f74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4143842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9ef9f2ac9c96e93217e0d144744e8d8278050716ca0834c70afa220c7c8939`

```dockerfile
```

-	Layers:
	-	`sha256:80add452afc9acafbae3ebdaf81b51e772270d4168261abc531caa3d40d6f8f2`  
		Last Modified: Thu, 02 May 2024 17:53:18 GMT  
		Size: 4.1 MB (4131887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9032987821a421011b12f5c932db84722ec77469e7d51d50c7f52fc9d678ac72`  
		Last Modified: Thu, 02 May 2024 17:53:17 GMT  
		Size: 12.0 KB (11955 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; ppc64le

```console
$ docker pull rust@sha256:f231b14bfd93102c404e608edce59336c32bbf5bc5b16dde3b83c3b3058aa530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277263350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6022c77c11237120364d8daebc5e4a7f79b239f345aadfe10e08162f3991d2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:44 GMT
ADD file:19695f701b790b512ac412bc124ed3ccf6357f5d22743aa24dcfb6767ccbb2c7 in / 
# Wed, 24 Apr 2024 03:21:47 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:fa4abeac727fcd70f1806e99adfdd8ed879ac1ffc30990e111f5169e9a451eaf`  
		Last Modified: Wed, 24 Apr 2024 03:27:40 GMT  
		Size: 35.3 MB (35311725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a8be3c69cc41100693d385b45a719b06420c1a8633ddefd2cd065116e4a80f`  
		Last Modified: Thu, 02 May 2024 18:10:20 GMT  
		Size: 242.0 MB (241951625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:1bb874168defcf306f4d12a18fa1d1a431164a64175ab74ccc234d19145dafe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4112769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf50d0079f8c3085c91f49970a4c034af187ead7b500a47212bad01b95a54c4`

```dockerfile
```

-	Layers:
	-	`sha256:c87e1c0879f136a39e78ff54f5cea16d36b7126d98ada10edad69ab8afe45793`  
		Last Modified: Thu, 02 May 2024 18:10:13 GMT  
		Size: 4.1 MB (4100914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ee003b3c784435c5aab66ccdc806e9767a27f9edd3cef32418dbc7142a51ac6`  
		Last Modified: Thu, 02 May 2024 18:10:13 GMT  
		Size: 11.9 KB (11855 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-bullseye` - linux; s390x

```console
$ docker pull rust@sha256:a4b95ec70b2c183bd9cd02364c93389c429f8ff07d8a86c91e8830923039acc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.3 MB (332291021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08e265a0280e57d06e189c5f7c3e1e12b10bb2d5eb9c7e0f2004ac291a514f5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:44:03 GMT
ADD file:acaea4e054f1ab7ae5cbc8f02c73b546c367aebfcc48c7fb4f0dd9f3628bc25e in / 
# Wed, 24 Apr 2024 03:44:09 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         ppc64el) rustArch='powerpc64le-unknown-linux-gnu'; rustupSha256='b152711fb15fd629f0d4c2731cbf9167e6352da0ffcb2210447d80c010180f96' ;;         s390x) rustArch='s390x-unknown-linux-gnu'; rustupSha256='4ff9e7963ed0457e64cbb29d2b5a37496d1fa303f9300adc5251ee3c16bd3b30' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:6f588995519e0e04ef4c150b91ad96c3c85667869db0ad72e5a78d4fab796e70`  
		Last Modified: Wed, 24 Apr 2024 03:49:47 GMT  
		Size: 29.7 MB (29673934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784d1c6d27c0fa82885a8be868f2c1ed573b39823970c4d06846ef9b4058af1e`  
		Last Modified: Thu, 02 May 2024 18:12:25 GMT  
		Size: 302.6 MB (302617087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-bullseye` - unknown; unknown

```console
$ docker pull rust@sha256:ee3b2c41de9bf97e7b05b8905fb5d0e70b4d8b48dcdbd11a87197a0e8af288de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3983854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63fa73fb55843e1fc73565ef3eb0db89dd88c65c76748308419e9a61dddb5569`

```dockerfile
```

-	Layers:
	-	`sha256:8de35856b398f950ff03181d5960ac2487203d9e917fd71ab33559d927b58a50`  
		Last Modified: Thu, 02 May 2024 18:12:20 GMT  
		Size: 4.0 MB (3972037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad823fcf4f244656c879ab7e131ca3a63d49fb60f964019942d1d0722a7aef41`  
		Last Modified: Thu, 02 May 2024 18:12:19 GMT  
		Size: 11.8 KB (11817 bytes)  
		MIME: application/vnd.in-toto+json

## `rust:slim-buster`

```console
$ docker pull rust@sha256:d30c7ad62c2044e0d1174d742f0efbc02c1e43aea988193b6686ee8aaaf79170
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
$ docker pull rust@sha256:562d6f211888cbd784790e7fb47d3cea4b20480634543579297832b7fd1c25a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.3 MB (250335520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe6261cf21c8a87571e9f4b502375b16f30e624d67d46e199388cdf0bc36235`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3906e6ed35d183754f56330a654a033329ee5826a5608612dde75a12c80dfbda`  
		Last Modified: Thu, 02 May 2024 17:53:08 GMT  
		Size: 223.0 MB (222997945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:e7b9c6cdb9dc891a721e37b31279d12f59a2aeaa33d3a50cd04c15ed9fdac0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3952917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e28a326d7714ebb85020a2b5bc3eb2f017a246b9349e259e29adf9cf787cd097`

```dockerfile
```

-	Layers:
	-	`sha256:3d7cefbfd3006121cdf982e776f479a01d0119707b7d9103dd24cdb58f580975`  
		Last Modified: Thu, 02 May 2024 17:53:05 GMT  
		Size: 3.9 MB (3941693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ca2968425f2c6d21765305834771a5c51369246bdfafc5ca52300a944a9f50d`  
		Last Modified: Thu, 02 May 2024 17:53:05 GMT  
		Size: 11.2 KB (11224 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; arm variant v7

```console
$ docker pull rust@sha256:94dda1ea419d69d0e38543407f33117c87a59c53c8e45b2fa3729496d76462c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.7 MB (268702412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb522a78fe20e96dd37a3094bd8201f8bc75d59d78c8672653761f8389e82b8`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:41 GMT
ADD file:985460a24e46cb6fd38e9ecdf21565547413f5f50d7c5c96d367b89aa94b91fa in / 
# Wed, 24 Apr 2024 04:07:41 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:a26123864d4d41f3f97e44b15f7ae2ecb9a15cbc37d6085d418a129976773e32`  
		Last Modified: Wed, 24 Apr 2024 04:12:31 GMT  
		Size: 22.9 MB (22945064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab99a29678006ca048ee3cec2a39dd336045cbef1f173b20313118c42dcc53f3`  
		Last Modified: Thu, 02 May 2024 18:09:45 GMT  
		Size: 245.8 MB (245757348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:870cd6eb7305f07b9e0a9384fb585ac261058d1821c291dae7d3e76c80bb744a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3760470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4231130c9d88f75df6ed09cac4d31aa678269b42aa3df4dabb3e9675ce564037`

```dockerfile
```

-	Layers:
	-	`sha256:2dc32a76ad84dbf82ef236a5ee11a01cd7c24687433eb86f7be3f1cfa7568a9b`  
		Last Modified: Thu, 02 May 2024 18:09:40 GMT  
		Size: 3.7 MB (3749343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cd37df8a47dfdf9952876a899f07158606f3fe042c2c85d5825fd83d506bf7`  
		Last Modified: Thu, 02 May 2024 18:09:39 GMT  
		Size: 11.1 KB (11127 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; arm64 variant v8

```console
$ docker pull rust@sha256:489aac5b79003a727f4571932d0a03b2aa17db922cca485942fe79de33c5cb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312574944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6fc5383529ef82de9ea2eb11d095ad1d1f517c836bc95f1ecc709194a04799d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:06 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
# Wed, 24 Apr 2024 04:11:07 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62497221c4fce50e070a112fde5ee41270ed6a3a085e7b1825fd24a956f1f4c7`  
		Last Modified: Thu, 02 May 2024 18:20:54 GMT  
		Size: 286.5 MB (286465114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:612bde9c6fe77167e879e6f3787a339655d4b7a1cbfa4ce1d3731711d4aa5508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3942219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6441cb64ca635d2e44dba773323ae3d87e7f6d0d4f4aee982365fa0652812d06`

```dockerfile
```

-	Layers:
	-	`sha256:e2fb474d4ff49f24441eccc92c2f1c16d30efe46b4c082a210ed49e145d5e5ee`  
		Last Modified: Thu, 02 May 2024 18:20:47 GMT  
		Size: 3.9 MB (3930985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80129d72be4749680a0777a4fb88afb3ad6bfae867c9ae93c316ad94e7112176`  
		Last Modified: Thu, 02 May 2024 18:20:47 GMT  
		Size: 11.2 KB (11234 bytes)  
		MIME: application/vnd.in-toto+json

### `rust:slim-buster` - linux; 386

```console
$ docker pull rust@sha256:862f761b55bdfb9b687ccd73c39ea5db75ab570112ac0d7d9da5f5c5196dc67f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.6 MB (268610066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d12d3e0efa5e20f2dffb6cca638c9d030e51183e0ed6dea06200bb6fa61abb4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:39 GMT
ADD file:32f0f06baa0e4f10bff55aaa215b511838432ecc5fe547373d9ac99494556801 in / 
# Wed, 24 Apr 2024 03:39:40 GMT
CMD ["bash"]
# Thu, 02 May 2024 12:45:44 GMT
LABEL org.opencontainers.image.source=https://github.com/rust-lang/docker-rust
# Thu, 02 May 2024 12:45:44 GMT
ENV RUSTUP_HOME=/usr/local/rustup CARGO_HOME=/usr/local/cargo PATH=/usr/local/cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin RUST_VERSION=1.78.0
# Thu, 02 May 2024 12:45:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends         ca-certificates         gcc         libc6-dev         wget         ;     dpkgArch="$(dpkg --print-architecture)";     case "${dpkgArch##*-}" in         amd64) rustArch='x86_64-unknown-linux-gnu'; rustupSha256='a3d541a5484c8fa2f1c21478a6f6c505a778d473c21d60a18a4df5185d320ef8' ;;         armhf) rustArch='armv7-unknown-linux-gnueabihf'; rustupSha256='7cff34808434a28d5a697593cd7a46cefdf59c4670021debccd4c86afde0ff76' ;;         arm64) rustArch='aarch64-unknown-linux-gnu'; rustupSha256='76cd420cb8a82e540025c5f97bda3c65ceb0b0661d5843e6ef177479813b0367' ;;         i386) rustArch='i686-unknown-linux-gnu'; rustupSha256='cacdd10eb5ec58498cd95dbb7191fdab5fa4343e05daaf0fb7cdcae63be0a272' ;;         *) echo >&2 "unsupported architecture: ${dpkgArch}"; exit 1 ;;     esac;     url="https://static.rust-lang.org/rustup/archive/1.27.0/${rustArch}/rustup-init";     wget "$url";     echo "${rustupSha256} *rustup-init" | sha256sum -c -;     chmod +x rustup-init;     ./rustup-init -y --no-modify-path --profile minimal --default-toolchain $RUST_VERSION --default-host ${rustArch};     rm rustup-init;     chmod -R a+w $RUSTUP_HOME $CARGO_HOME;     rustup --version;     cargo --version;     rustc --version;     apt-get remove -y --auto-remove         wget         ;     rm -rf /var/lib/apt/lists/*; # buildkit
```

-	Layers:
	-	`sha256:204b51fc41806ed93b4ccb6ce8272fa49b5f0b099ba6e3b5a940a9e7cd3ce202`  
		Last Modified: Wed, 24 Apr 2024 03:45:03 GMT  
		Size: 28.0 MB (27994678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3981a552b28468ee69108184598097965a5265b74ad064e8e657f3897f599f3`  
		Last Modified: Thu, 02 May 2024 17:53:15 GMT  
		Size: 240.6 MB (240615388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `rust:slim-buster` - unknown; unknown

```console
$ docker pull rust@sha256:4a7ce102abb3a846743437756ea063f781583ab5bea6f40c2612550634e10222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3959513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb6026b631db1e909e1f420b7086445db95e1f00ef7bc7c365ad507c9a54fdb`

```dockerfile
```

-	Layers:
	-	`sha256:2e03fc3bfe125dba62e18faebb42c04d798624900a87a5dc953c3be75072510d`  
		Last Modified: Thu, 02 May 2024 17:53:10 GMT  
		Size: 3.9 MB (3948318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e394e2a792e8d275adc332b5b935d4c9db65a83fe54fda94e7437645d5b02114`  
		Last Modified: Thu, 02 May 2024 17:53:10 GMT  
		Size: 11.2 KB (11195 bytes)  
		MIME: application/vnd.in-toto+json
