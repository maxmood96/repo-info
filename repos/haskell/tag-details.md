<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:9`](#haskell9)
-	[`haskell:9-buster`](#haskell9-buster)
-	[`haskell:9-slim`](#haskell9-slim)
-	[`haskell:9-slim-buster`](#haskell9-slim-buster)
-	[`haskell:9.0`](#haskell90)
-	[`haskell:9.0-buster`](#haskell90-buster)
-	[`haskell:9.0-slim`](#haskell90-slim)
-	[`haskell:9.0-slim-buster`](#haskell90-slim-buster)
-	[`haskell:9.0.2`](#haskell902)
-	[`haskell:9.0.2-buster`](#haskell902-buster)
-	[`haskell:9.0.2-slim`](#haskell902-slim)
-	[`haskell:9.0.2-slim-buster`](#haskell902-slim-buster)
-	[`haskell:9.2`](#haskell92)
-	[`haskell:9.2-buster`](#haskell92-buster)
-	[`haskell:9.2-slim`](#haskell92-slim)
-	[`haskell:9.2-slim-buster`](#haskell92-slim-buster)
-	[`haskell:9.2.8`](#haskell928)
-	[`haskell:9.2.8-buster`](#haskell928-buster)
-	[`haskell:9.2.8-slim`](#haskell928-slim)
-	[`haskell:9.2.8-slim-buster`](#haskell928-slim-buster)
-	[`haskell:9.4`](#haskell94)
-	[`haskell:9.4-buster`](#haskell94-buster)
-	[`haskell:9.4-slim`](#haskell94-slim)
-	[`haskell:9.4-slim-buster`](#haskell94-slim-buster)
-	[`haskell:9.4.8`](#haskell948)
-	[`haskell:9.4.8-buster`](#haskell948-buster)
-	[`haskell:9.4.8-slim`](#haskell948-slim)
-	[`haskell:9.4.8-slim-buster`](#haskell948-slim-buster)
-	[`haskell:9.6`](#haskell96)
-	[`haskell:9.6-buster`](#haskell96-buster)
-	[`haskell:9.6-slim`](#haskell96-slim)
-	[`haskell:9.6-slim-buster`](#haskell96-slim-buster)
-	[`haskell:9.6.5`](#haskell965)
-	[`haskell:9.6.5-buster`](#haskell965-buster)
-	[`haskell:9.6.5-slim`](#haskell965-slim)
-	[`haskell:9.6.5-slim-buster`](#haskell965-slim-buster)
-	[`haskell:9.8`](#haskell98)
-	[`haskell:9.8-buster`](#haskell98-buster)
-	[`haskell:9.8-slim`](#haskell98-slim)
-	[`haskell:9.8-slim-buster`](#haskell98-slim-buster)
-	[`haskell:9.8.2`](#haskell982)
-	[`haskell:9.8.2-buster`](#haskell982-buster)
-	[`haskell:9.8.2-slim`](#haskell982-slim)
-	[`haskell:9.8.2-slim-buster`](#haskell982-slim-buster)
-	[`haskell:buster`](#haskellbuster)
-	[`haskell:latest`](#haskelllatest)
-	[`haskell:slim`](#haskellslim)
-	[`haskell:slim-buster`](#haskellslim-buster)

## `haskell:9`

```console
$ docker pull haskell@sha256:96705a005edc39eac637e2b4f70752c9a1a01745c06d005a19dd3e42e9b1100f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:b9fd4cc3cbe521e329bec346bbb89470f092643341344a11c7f087a3cc235b3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783698500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d3ef7825ce4866b834fe4b88177fff3e2eaedaa8147cc0ccf70494b9325fc`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:21:09 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:21:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:21:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7dba5e179f52cb2cd009e95da4e8c307e4251a8879195c46bfc0d256fa311`  
		Last Modified: Wed, 10 Apr 2024 09:38:42 GMT  
		Size: 441.8 MB (441811327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8f31b5d663813e79e76f4b8bcdb59f2e0d8d8e584119d0e3293802f4478f03a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.8 MB (785788047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9a82b985960bf46356702aedcb3095179824a4bb0d3c87cffd4edffd807f9d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:55:46 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:55:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:56:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b0b8f4f36bb81ea21877b9df9bdeb276a41701999be87deff93362c2ef98ed`  
		Last Modified: Wed, 10 Apr 2024 07:13:06 GMT  
		Size: 448.9 MB (448904259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-buster`

```console
$ docker pull haskell@sha256:96705a005edc39eac637e2b4f70752c9a1a01745c06d005a19dd3e42e9b1100f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-buster` - linux; amd64

```console
$ docker pull haskell@sha256:b9fd4cc3cbe521e329bec346bbb89470f092643341344a11c7f087a3cc235b3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783698500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d3ef7825ce4866b834fe4b88177fff3e2eaedaa8147cc0ccf70494b9325fc`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:21:09 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:21:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:21:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7dba5e179f52cb2cd009e95da4e8c307e4251a8879195c46bfc0d256fa311`  
		Last Modified: Wed, 10 Apr 2024 09:38:42 GMT  
		Size: 441.8 MB (441811327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8f31b5d663813e79e76f4b8bcdb59f2e0d8d8e584119d0e3293802f4478f03a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.8 MB (785788047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9a82b985960bf46356702aedcb3095179824a4bb0d3c87cffd4edffd807f9d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:55:46 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:55:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:56:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b0b8f4f36bb81ea21877b9df9bdeb276a41701999be87deff93362c2ef98ed`  
		Last Modified: Wed, 10 Apr 2024 07:13:06 GMT  
		Size: 448.9 MB (448904259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:bbf9006351ecf54bb5668e37c4bdb17a78072c1022755aecc4648fe1e49ec8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:5dd55cd8aae5c0ee893306470874a6dd568dab348fa575c1e007e8416bafe24c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447662209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770ce30215bba6c99b3d9bf85038fc346f7e92f394355a585f167f491fcb253a`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:23:35 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:23:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:23:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a711823476076f81c4c9eaa538aa7c8406459afaf56831da6e241829561a06`  
		Last Modified: Wed, 10 Apr 2024 09:39:59 GMT  
		Size: 297.0 MB (296984261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6aa0434cb4a41447a13c28bb8b965ff3a5ccb67086f8a534d96c4b0bc1928d71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451489042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65baf4086cd897d7bf6241d06b7e7d60568ae55b9ce6b24862c36ee98ba3dff7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:58:01 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:58:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:58:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d890e4e955f93af0fa46b7bbddf91a7470650dc50f05cc748dc9781d006fd5`  
		Last Modified: Wed, 10 Apr 2024 07:14:12 GMT  
		Size: 303.6 MB (303605843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim-buster`

```console
$ docker pull haskell@sha256:bbf9006351ecf54bb5668e37c4bdb17a78072c1022755aecc4648fe1e49ec8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5dd55cd8aae5c0ee893306470874a6dd568dab348fa575c1e007e8416bafe24c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447662209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770ce30215bba6c99b3d9bf85038fc346f7e92f394355a585f167f491fcb253a`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:23:35 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:23:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:23:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a711823476076f81c4c9eaa538aa7c8406459afaf56831da6e241829561a06`  
		Last Modified: Wed, 10 Apr 2024 09:39:59 GMT  
		Size: 297.0 MB (296984261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6aa0434cb4a41447a13c28bb8b965ff3a5ccb67086f8a534d96c4b0bc1928d71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451489042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65baf4086cd897d7bf6241d06b7e7d60568ae55b9ce6b24862c36ee98ba3dff7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:58:01 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:58:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:58:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d890e4e955f93af0fa46b7bbddf91a7470650dc50f05cc748dc9781d006fd5`  
		Last Modified: Wed, 10 Apr 2024 07:14:12 GMT  
		Size: 303.6 MB (303605843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0`

```console
$ docker pull haskell@sha256:ccaa4dfef350755d7db3e464b4482c080649def0d36e0abbb55d97f150c7f09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0` - linux; amd64

```console
$ docker pull haskell@sha256:d357b3d5f7b49e23f79ac03dbf643db0fc2e39ae81a5079d352f3ba5776bbce6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.3 MB (723281841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9f0e9a19be959b775e2459cd94832bbfe46b4e458a7443742da419e1890c4c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:34:09 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 09:34:09 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 09:34:09 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 09:34:09 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 09:34:09 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:35:22 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:35:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:35:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd63675a672c111f2bdbfbcc973f21d6bc5903441c5268dd998aab2be90c12`  
		Last Modified: Wed, 10 Apr 2024 09:45:21 GMT  
		Size: 7.8 MB (7838363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac255a52b7e74dd83c3afd2b5842f7370db637fdf5d794ae9313c029cde4b527`  
		Last Modified: Wed, 10 Apr 2024 09:49:06 GMT  
		Size: 381.6 MB (381555756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b4e7c81dbe17a557ddab307edbb8b9fcf807c743e1821958b7d3b2609bba76d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.4 MB (648354435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8017f7302e5ff418a2d2167c88094e00aa4409fcaaae3b86309625143e5518`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:05:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:09:17 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 07:09:17 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 07:09:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 07:09:27 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 07:09:27 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:10:11 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:10:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:10:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cb2b13c41d84b27ddbfb3c8b95470c93ef9e2d9a96e025aa6a8b7fd553ef8`  
		Last Modified: Wed, 10 Apr 2024 07:19:06 GMT  
		Size: 12.4 MB (12373187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f563f3da2878a618ba5b0adb61bd69c400872446d7f2e389924eceb98d278fe2`  
		Last Modified: Wed, 10 Apr 2024 07:21:43 GMT  
		Size: 45.9 MB (45889804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a41bb361d3f70c477a0cfd008495eaf4bb242e0a53bb1d6aae1627e95789eb0`  
		Last Modified: Wed, 10 Apr 2024 07:22:23 GMT  
		Size: 263.3 MB (263320643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-buster`

```console
$ docker pull haskell@sha256:ccaa4dfef350755d7db3e464b4482c080649def0d36e0abbb55d97f150c7f09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-buster` - linux; amd64

```console
$ docker pull haskell@sha256:d357b3d5f7b49e23f79ac03dbf643db0fc2e39ae81a5079d352f3ba5776bbce6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.3 MB (723281841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9f0e9a19be959b775e2459cd94832bbfe46b4e458a7443742da419e1890c4c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:34:09 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 09:34:09 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 09:34:09 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 09:34:09 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 09:34:09 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:35:22 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:35:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:35:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd63675a672c111f2bdbfbcc973f21d6bc5903441c5268dd998aab2be90c12`  
		Last Modified: Wed, 10 Apr 2024 09:45:21 GMT  
		Size: 7.8 MB (7838363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac255a52b7e74dd83c3afd2b5842f7370db637fdf5d794ae9313c029cde4b527`  
		Last Modified: Wed, 10 Apr 2024 09:49:06 GMT  
		Size: 381.6 MB (381555756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b4e7c81dbe17a557ddab307edbb8b9fcf807c743e1821958b7d3b2609bba76d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.4 MB (648354435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8017f7302e5ff418a2d2167c88094e00aa4409fcaaae3b86309625143e5518`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:05:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:09:17 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 07:09:17 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 07:09:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 07:09:27 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 07:09:27 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:10:11 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:10:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:10:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cb2b13c41d84b27ddbfb3c8b95470c93ef9e2d9a96e025aa6a8b7fd553ef8`  
		Last Modified: Wed, 10 Apr 2024 07:19:06 GMT  
		Size: 12.4 MB (12373187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f563f3da2878a618ba5b0adb61bd69c400872446d7f2e389924eceb98d278fe2`  
		Last Modified: Wed, 10 Apr 2024 07:21:43 GMT  
		Size: 45.9 MB (45889804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a41bb361d3f70c477a0cfd008495eaf4bb242e0a53bb1d6aae1627e95789eb0`  
		Last Modified: Wed, 10 Apr 2024 07:22:23 GMT  
		Size: 263.3 MB (263320643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-slim`

```console
$ docker pull haskell@sha256:0791caee22e8d10fac4a39af0a665ad9b1cde1f6a6846199d0a64f7747f1ce40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-slim` - linux; amd64

```console
$ docker pull haskell@sha256:73d50f445fd2f7cbd074836ba888bb1431f4055e357ceaccbb172388b06e9688
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.6 MB (415639278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2986dfa79398dba0f9f69d9080c59cbfe48d621dd3cc4a8dc7e50115314f5253`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:32:47 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:35:32 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 09:35:33 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 09:35:33 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 09:35:34 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 09:35:34 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:36:43 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:36:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:36:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18323aa33942f4ce38900edb6e6ce5600a98e3f0c2bc7844d7de11c90f245f`  
		Last Modified: Wed, 10 Apr 2024 09:46:49 GMT  
		Size: 7.8 MB (7838391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bef2a49b4dc373d79e03f905ecef4110a2dcdda530d1ec14b95f006cd0c461f`  
		Last Modified: Wed, 10 Apr 2024 09:50:10 GMT  
		Size: 265.1 MB (265122400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:292b07354b9b92b173dad66cd3e7c1decf3e19cdaa0a17d79b30fdd975039af0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.3 MB (473297448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102a13820f1f2254f3cb716044d6446fb91fa6dcbe9e4587f8fb5efe2083f8f8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:07:41 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:10:26 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 07:10:26 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 07:10:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 07:10:35 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 07:10:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:11:21 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:11:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:11:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f330562a7cbe256af1662b6f7102221fd87de0d9c2655959f17910e2678219`  
		Last Modified: Wed, 10 Apr 2024 07:20:35 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bea3a236a5f954ce95673cc81899e0c18923b1288fa6fa1ab3ff41ed719bc`  
		Last Modified: Wed, 10 Apr 2024 07:22:41 GMT  
		Size: 59.8 MB (59836024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2c7f961ee023505240037b67b4e3358589b4496e6c8c6fcb58ff32d1e6509`  
		Last Modified: Wed, 10 Apr 2024 07:23:21 GMT  
		Size: 263.3 MB (263318017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-slim-buster`

```console
$ docker pull haskell@sha256:0791caee22e8d10fac4a39af0a665ad9b1cde1f6a6846199d0a64f7747f1ce40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:73d50f445fd2f7cbd074836ba888bb1431f4055e357ceaccbb172388b06e9688
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.6 MB (415639278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2986dfa79398dba0f9f69d9080c59cbfe48d621dd3cc4a8dc7e50115314f5253`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:32:47 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:35:32 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 09:35:33 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 09:35:33 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 09:35:34 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 09:35:34 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:36:43 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:36:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:36:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18323aa33942f4ce38900edb6e6ce5600a98e3f0c2bc7844d7de11c90f245f`  
		Last Modified: Wed, 10 Apr 2024 09:46:49 GMT  
		Size: 7.8 MB (7838391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bef2a49b4dc373d79e03f905ecef4110a2dcdda530d1ec14b95f006cd0c461f`  
		Last Modified: Wed, 10 Apr 2024 09:50:10 GMT  
		Size: 265.1 MB (265122400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:292b07354b9b92b173dad66cd3e7c1decf3e19cdaa0a17d79b30fdd975039af0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.3 MB (473297448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102a13820f1f2254f3cb716044d6446fb91fa6dcbe9e4587f8fb5efe2083f8f8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:07:41 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:10:26 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 07:10:26 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 07:10:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 07:10:35 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 07:10:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:11:21 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:11:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:11:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f330562a7cbe256af1662b6f7102221fd87de0d9c2655959f17910e2678219`  
		Last Modified: Wed, 10 Apr 2024 07:20:35 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bea3a236a5f954ce95673cc81899e0c18923b1288fa6fa1ab3ff41ed719bc`  
		Last Modified: Wed, 10 Apr 2024 07:22:41 GMT  
		Size: 59.8 MB (59836024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2c7f961ee023505240037b67b4e3358589b4496e6c8c6fcb58ff32d1e6509`  
		Last Modified: Wed, 10 Apr 2024 07:23:21 GMT  
		Size: 263.3 MB (263318017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2`

```console
$ docker pull haskell@sha256:ccaa4dfef350755d7db3e464b4482c080649def0d36e0abbb55d97f150c7f09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2` - linux; amd64

```console
$ docker pull haskell@sha256:d357b3d5f7b49e23f79ac03dbf643db0fc2e39ae81a5079d352f3ba5776bbce6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.3 MB (723281841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9f0e9a19be959b775e2459cd94832bbfe46b4e458a7443742da419e1890c4c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:34:09 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 09:34:09 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 09:34:09 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 09:34:09 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 09:34:09 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:35:22 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:35:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:35:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd63675a672c111f2bdbfbcc973f21d6bc5903441c5268dd998aab2be90c12`  
		Last Modified: Wed, 10 Apr 2024 09:45:21 GMT  
		Size: 7.8 MB (7838363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac255a52b7e74dd83c3afd2b5842f7370db637fdf5d794ae9313c029cde4b527`  
		Last Modified: Wed, 10 Apr 2024 09:49:06 GMT  
		Size: 381.6 MB (381555756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b4e7c81dbe17a557ddab307edbb8b9fcf807c743e1821958b7d3b2609bba76d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.4 MB (648354435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8017f7302e5ff418a2d2167c88094e00aa4409fcaaae3b86309625143e5518`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:05:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:09:17 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 07:09:17 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 07:09:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 07:09:27 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 07:09:27 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:10:11 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:10:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:10:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cb2b13c41d84b27ddbfb3c8b95470c93ef9e2d9a96e025aa6a8b7fd553ef8`  
		Last Modified: Wed, 10 Apr 2024 07:19:06 GMT  
		Size: 12.4 MB (12373187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f563f3da2878a618ba5b0adb61bd69c400872446d7f2e389924eceb98d278fe2`  
		Last Modified: Wed, 10 Apr 2024 07:21:43 GMT  
		Size: 45.9 MB (45889804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a41bb361d3f70c477a0cfd008495eaf4bb242e0a53bb1d6aae1627e95789eb0`  
		Last Modified: Wed, 10 Apr 2024 07:22:23 GMT  
		Size: 263.3 MB (263320643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-buster`

```console
$ docker pull haskell@sha256:ccaa4dfef350755d7db3e464b4482c080649def0d36e0abbb55d97f150c7f09c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:d357b3d5f7b49e23f79ac03dbf643db0fc2e39ae81a5079d352f3ba5776bbce6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **723.3 MB (723281841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9f0e9a19be959b775e2459cd94832bbfe46b4e458a7443742da419e1890c4c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:34:09 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 09:34:09 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 09:34:09 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 09:34:09 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 09:34:09 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:35:22 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:35:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:35:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd63675a672c111f2bdbfbcc973f21d6bc5903441c5268dd998aab2be90c12`  
		Last Modified: Wed, 10 Apr 2024 09:45:21 GMT  
		Size: 7.8 MB (7838363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac255a52b7e74dd83c3afd2b5842f7370db637fdf5d794ae9313c029cde4b527`  
		Last Modified: Wed, 10 Apr 2024 09:49:06 GMT  
		Size: 381.6 MB (381555756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b4e7c81dbe17a557ddab307edbb8b9fcf807c743e1821958b7d3b2609bba76d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.4 MB (648354435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8017f7302e5ff418a2d2167c88094e00aa4409fcaaae3b86309625143e5518`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:05:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:09:17 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 07:09:17 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 07:09:27 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 07:09:27 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 07:09:27 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:10:11 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:10:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:10:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cb2b13c41d84b27ddbfb3c8b95470c93ef9e2d9a96e025aa6a8b7fd553ef8`  
		Last Modified: Wed, 10 Apr 2024 07:19:06 GMT  
		Size: 12.4 MB (12373187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f563f3da2878a618ba5b0adb61bd69c400872446d7f2e389924eceb98d278fe2`  
		Last Modified: Wed, 10 Apr 2024 07:21:43 GMT  
		Size: 45.9 MB (45889804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a41bb361d3f70c477a0cfd008495eaf4bb242e0a53bb1d6aae1627e95789eb0`  
		Last Modified: Wed, 10 Apr 2024 07:22:23 GMT  
		Size: 263.3 MB (263320643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-slim`

```console
$ docker pull haskell@sha256:0791caee22e8d10fac4a39af0a665ad9b1cde1f6a6846199d0a64f7747f1ce40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:73d50f445fd2f7cbd074836ba888bb1431f4055e357ceaccbb172388b06e9688
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.6 MB (415639278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2986dfa79398dba0f9f69d9080c59cbfe48d621dd3cc4a8dc7e50115314f5253`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:32:47 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:35:32 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 09:35:33 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 09:35:33 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 09:35:34 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 09:35:34 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:36:43 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:36:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:36:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18323aa33942f4ce38900edb6e6ce5600a98e3f0c2bc7844d7de11c90f245f`  
		Last Modified: Wed, 10 Apr 2024 09:46:49 GMT  
		Size: 7.8 MB (7838391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bef2a49b4dc373d79e03f905ecef4110a2dcdda530d1ec14b95f006cd0c461f`  
		Last Modified: Wed, 10 Apr 2024 09:50:10 GMT  
		Size: 265.1 MB (265122400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:292b07354b9b92b173dad66cd3e7c1decf3e19cdaa0a17d79b30fdd975039af0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.3 MB (473297448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102a13820f1f2254f3cb716044d6446fb91fa6dcbe9e4587f8fb5efe2083f8f8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:07:41 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:10:26 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 07:10:26 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 07:10:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 07:10:35 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 07:10:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:11:21 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:11:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:11:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f330562a7cbe256af1662b6f7102221fd87de0d9c2655959f17910e2678219`  
		Last Modified: Wed, 10 Apr 2024 07:20:35 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bea3a236a5f954ce95673cc81899e0c18923b1288fa6fa1ab3ff41ed719bc`  
		Last Modified: Wed, 10 Apr 2024 07:22:41 GMT  
		Size: 59.8 MB (59836024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2c7f961ee023505240037b67b4e3358589b4496e6c8c6fcb58ff32d1e6509`  
		Last Modified: Wed, 10 Apr 2024 07:23:21 GMT  
		Size: 263.3 MB (263318017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-slim-buster`

```console
$ docker pull haskell@sha256:0791caee22e8d10fac4a39af0a665ad9b1cde1f6a6846199d0a64f7747f1ce40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:73d50f445fd2f7cbd074836ba888bb1431f4055e357ceaccbb172388b06e9688
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.6 MB (415639278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2986dfa79398dba0f9f69d9080c59cbfe48d621dd3cc4a8dc7e50115314f5253`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:32:47 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:35:32 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 09:35:33 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 09:35:33 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 09:35:34 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 09:35:34 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:36:43 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:36:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:36:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18323aa33942f4ce38900edb6e6ce5600a98e3f0c2bc7844d7de11c90f245f`  
		Last Modified: Wed, 10 Apr 2024 09:46:49 GMT  
		Size: 7.8 MB (7838391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bef2a49b4dc373d79e03f905ecef4110a2dcdda530d1ec14b95f006cd0c461f`  
		Last Modified: Wed, 10 Apr 2024 09:50:10 GMT  
		Size: 265.1 MB (265122400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:292b07354b9b92b173dad66cd3e7c1decf3e19cdaa0a17d79b30fdd975039af0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **473.3 MB (473297448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:102a13820f1f2254f3cb716044d6446fb91fa6dcbe9e4587f8fb5efe2083f8f8`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:07:41 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:10:26 GMT
ARG LLVM_VERSION=12
# Wed, 10 Apr 2024 07:10:26 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 10 Apr 2024 07:10:34 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 10 Apr 2024 07:10:35 GMT
ARG GHC=9.0.2
# Wed, 10 Apr 2024 07:10:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:11:21 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:11:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:11:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f330562a7cbe256af1662b6f7102221fd87de0d9c2655959f17910e2678219`  
		Last Modified: Wed, 10 Apr 2024 07:20:35 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bea3a236a5f954ce95673cc81899e0c18923b1288fa6fa1ab3ff41ed719bc`  
		Last Modified: Wed, 10 Apr 2024 07:22:41 GMT  
		Size: 59.8 MB (59836024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dab2c7f961ee023505240037b67b4e3358589b4496e6c8c6fcb58ff32d1e6509`  
		Last Modified: Wed, 10 Apr 2024 07:23:21 GMT  
		Size: 263.3 MB (263318017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2`

```console
$ docker pull haskell@sha256:2ad9d51b2814cd9f67f38bd06a7ab8b78d615fc5fad53a08dc15b785e0606643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2` - linux; amd64

```console
$ docker pull haskell@sha256:440e93e53537ac42ac7cc85d8a297380307f89378b8b47c0aa735a9b5e42f9c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.9 MB (741939540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65627e52f5ee0a51a800b27ec834d398df75e9131fad5e6640ee1d42569bee7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:31:08 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 09:31:09 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:32:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:32:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:32:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd63675a672c111f2bdbfbcc973f21d6bc5903441c5268dd998aab2be90c12`  
		Last Modified: Wed, 10 Apr 2024 09:45:21 GMT  
		Size: 7.8 MB (7838363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6a12d9cb7ab197972f9ab5f18e6877095c82730e0dee30653834f0d5ce74ae`  
		Last Modified: Wed, 10 Apr 2024 09:46:35 GMT  
		Size: 400.2 MB (400213455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc64d2a8bbe9218464ade145fe28a41826347610e7d00cf85bb02addebf0ed4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.6 MB (804605406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df2867f4365b0464c28863d1e687860a273ab6f0b684eb526c71d5c64ef4454`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:05:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:05:49 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 07:05:49 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:07:16 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:07:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:07:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cb2b13c41d84b27ddbfb3c8b95470c93ef9e2d9a96e025aa6a8b7fd553ef8`  
		Last Modified: Wed, 10 Apr 2024 07:19:06 GMT  
		Size: 12.4 MB (12373187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599cac09e37dc881c2ddac5b015963a4ea78ecbaa53db2e03ebfd304b41346c0`  
		Last Modified: Wed, 10 Apr 2024 07:20:21 GMT  
		Size: 465.5 MB (465461418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-buster`

```console
$ docker pull haskell@sha256:2ad9d51b2814cd9f67f38bd06a7ab8b78d615fc5fad53a08dc15b785e0606643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:440e93e53537ac42ac7cc85d8a297380307f89378b8b47c0aa735a9b5e42f9c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.9 MB (741939540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65627e52f5ee0a51a800b27ec834d398df75e9131fad5e6640ee1d42569bee7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:31:08 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 09:31:09 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:32:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:32:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:32:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd63675a672c111f2bdbfbcc973f21d6bc5903441c5268dd998aab2be90c12`  
		Last Modified: Wed, 10 Apr 2024 09:45:21 GMT  
		Size: 7.8 MB (7838363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6a12d9cb7ab197972f9ab5f18e6877095c82730e0dee30653834f0d5ce74ae`  
		Last Modified: Wed, 10 Apr 2024 09:46:35 GMT  
		Size: 400.2 MB (400213455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc64d2a8bbe9218464ade145fe28a41826347610e7d00cf85bb02addebf0ed4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.6 MB (804605406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df2867f4365b0464c28863d1e687860a273ab6f0b684eb526c71d5c64ef4454`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:05:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:05:49 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 07:05:49 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:07:16 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:07:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:07:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cb2b13c41d84b27ddbfb3c8b95470c93ef9e2d9a96e025aa6a8b7fd553ef8`  
		Last Modified: Wed, 10 Apr 2024 07:19:06 GMT  
		Size: 12.4 MB (12373187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599cac09e37dc881c2ddac5b015963a4ea78ecbaa53db2e03ebfd304b41346c0`  
		Last Modified: Wed, 10 Apr 2024 07:20:21 GMT  
		Size: 465.5 MB (465461418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-slim`

```console
$ docker pull haskell@sha256:f3a17a959888ec5c9391ca2e26b2c9f70b45f293f86d1ae541e1808b1254ddaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:900165e7e04e084ee8ce981c60aa95fba32a01d27a875952150e4cae8ce8a968
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428479087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8242dadea9b4e9b8a2d780d0f5e0d7881d45f4a42c05a83f6a7a19d44b21b6`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:32:47 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:32:47 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 09:32:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:33:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:34:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:34:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18323aa33942f4ce38900edb6e6ce5600a98e3f0c2bc7844d7de11c90f245f`  
		Last Modified: Wed, 10 Apr 2024 09:46:49 GMT  
		Size: 7.8 MB (7838391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07825fee56074c1f3b6ece14439e881b544167cdeaa32ebd93e8fa62446c3275`  
		Last Modified: Wed, 10 Apr 2024 09:47:41 GMT  
		Size: 278.0 MB (277962209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3cb69fa8b28395f5d54a54632cfdd79b5eb1d2eb3f6ea5e0faf3282ed2314c97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.3 MB (470328876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cebe65edfabd188590224a4c6063f5fca03ad40252e3ec923e0ae3758e97e3`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:07:41 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:07:41 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 07:07:41 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:09:00 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:09:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:09:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f330562a7cbe256af1662b6f7102221fd87de0d9c2655959f17910e2678219`  
		Last Modified: Wed, 10 Apr 2024 07:20:35 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949007b382393df630444de3c0e0cb309b27bbc1bd1edf7d30506dc2c68914f6`  
		Last Modified: Wed, 10 Apr 2024 07:21:27 GMT  
		Size: 320.2 MB (320185469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-slim-buster`

```console
$ docker pull haskell@sha256:f3a17a959888ec5c9391ca2e26b2c9f70b45f293f86d1ae541e1808b1254ddaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:900165e7e04e084ee8ce981c60aa95fba32a01d27a875952150e4cae8ce8a968
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428479087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8242dadea9b4e9b8a2d780d0f5e0d7881d45f4a42c05a83f6a7a19d44b21b6`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:32:47 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:32:47 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 09:32:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:33:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:34:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:34:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18323aa33942f4ce38900edb6e6ce5600a98e3f0c2bc7844d7de11c90f245f`  
		Last Modified: Wed, 10 Apr 2024 09:46:49 GMT  
		Size: 7.8 MB (7838391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07825fee56074c1f3b6ece14439e881b544167cdeaa32ebd93e8fa62446c3275`  
		Last Modified: Wed, 10 Apr 2024 09:47:41 GMT  
		Size: 278.0 MB (277962209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3cb69fa8b28395f5d54a54632cfdd79b5eb1d2eb3f6ea5e0faf3282ed2314c97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.3 MB (470328876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cebe65edfabd188590224a4c6063f5fca03ad40252e3ec923e0ae3758e97e3`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:07:41 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:07:41 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 07:07:41 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:09:00 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:09:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:09:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f330562a7cbe256af1662b6f7102221fd87de0d9c2655959f17910e2678219`  
		Last Modified: Wed, 10 Apr 2024 07:20:35 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949007b382393df630444de3c0e0cb309b27bbc1bd1edf7d30506dc2c68914f6`  
		Last Modified: Wed, 10 Apr 2024 07:21:27 GMT  
		Size: 320.2 MB (320185469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.8`

```console
$ docker pull haskell@sha256:2ad9d51b2814cd9f67f38bd06a7ab8b78d615fc5fad53a08dc15b785e0606643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.8` - linux; amd64

```console
$ docker pull haskell@sha256:440e93e53537ac42ac7cc85d8a297380307f89378b8b47c0aa735a9b5e42f9c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.9 MB (741939540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65627e52f5ee0a51a800b27ec834d398df75e9131fad5e6640ee1d42569bee7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:31:08 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 09:31:09 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:32:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:32:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:32:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd63675a672c111f2bdbfbcc973f21d6bc5903441c5268dd998aab2be90c12`  
		Last Modified: Wed, 10 Apr 2024 09:45:21 GMT  
		Size: 7.8 MB (7838363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6a12d9cb7ab197972f9ab5f18e6877095c82730e0dee30653834f0d5ce74ae`  
		Last Modified: Wed, 10 Apr 2024 09:46:35 GMT  
		Size: 400.2 MB (400213455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc64d2a8bbe9218464ade145fe28a41826347610e7d00cf85bb02addebf0ed4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.6 MB (804605406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df2867f4365b0464c28863d1e687860a273ab6f0b684eb526c71d5c64ef4454`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:05:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:05:49 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 07:05:49 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:07:16 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:07:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:07:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cb2b13c41d84b27ddbfb3c8b95470c93ef9e2d9a96e025aa6a8b7fd553ef8`  
		Last Modified: Wed, 10 Apr 2024 07:19:06 GMT  
		Size: 12.4 MB (12373187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599cac09e37dc881c2ddac5b015963a4ea78ecbaa53db2e03ebfd304b41346c0`  
		Last Modified: Wed, 10 Apr 2024 07:20:21 GMT  
		Size: 465.5 MB (465461418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.8-buster`

```console
$ docker pull haskell@sha256:2ad9d51b2814cd9f67f38bd06a7ab8b78d615fc5fad53a08dc15b785e0606643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:440e93e53537ac42ac7cc85d8a297380307f89378b8b47c0aa735a9b5e42f9c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **741.9 MB (741939540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65627e52f5ee0a51a800b27ec834d398df75e9131fad5e6640ee1d42569bee7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:31:06 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:31:08 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:31:08 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 09:31:09 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:32:24 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:32:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:32:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd63675a672c111f2bdbfbcc973f21d6bc5903441c5268dd998aab2be90c12`  
		Last Modified: Wed, 10 Apr 2024 09:45:21 GMT  
		Size: 7.8 MB (7838363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6a12d9cb7ab197972f9ab5f18e6877095c82730e0dee30653834f0d5ce74ae`  
		Last Modified: Wed, 10 Apr 2024 09:46:35 GMT  
		Size: 400.2 MB (400213455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.8-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc64d2a8bbe9218464ade145fe28a41826347610e7d00cf85bb02addebf0ed4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **804.6 MB (804605406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df2867f4365b0464c28863d1e687860a273ab6f0b684eb526c71d5c64ef4454`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:05:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:05:48 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:05:49 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 07:05:49 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:07:16 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:07:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:07:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5cb2b13c41d84b27ddbfb3c8b95470c93ef9e2d9a96e025aa6a8b7fd553ef8`  
		Last Modified: Wed, 10 Apr 2024 07:19:06 GMT  
		Size: 12.4 MB (12373187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:599cac09e37dc881c2ddac5b015963a4ea78ecbaa53db2e03ebfd304b41346c0`  
		Last Modified: Wed, 10 Apr 2024 07:20:21 GMT  
		Size: 465.5 MB (465461418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.8-slim`

```console
$ docker pull haskell@sha256:f3a17a959888ec5c9391ca2e26b2c9f70b45f293f86d1ae541e1808b1254ddaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:900165e7e04e084ee8ce981c60aa95fba32a01d27a875952150e4cae8ce8a968
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428479087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8242dadea9b4e9b8a2d780d0f5e0d7881d45f4a42c05a83f6a7a19d44b21b6`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:32:47 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:32:47 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 09:32:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:33:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:34:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:34:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18323aa33942f4ce38900edb6e6ce5600a98e3f0c2bc7844d7de11c90f245f`  
		Last Modified: Wed, 10 Apr 2024 09:46:49 GMT  
		Size: 7.8 MB (7838391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07825fee56074c1f3b6ece14439e881b544167cdeaa32ebd93e8fa62446c3275`  
		Last Modified: Wed, 10 Apr 2024 09:47:41 GMT  
		Size: 278.0 MB (277962209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3cb69fa8b28395f5d54a54632cfdd79b5eb1d2eb3f6ea5e0faf3282ed2314c97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.3 MB (470328876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cebe65edfabd188590224a4c6063f5fca03ad40252e3ec923e0ae3758e97e3`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:07:41 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:07:41 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 07:07:41 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:09:00 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:09:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:09:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f330562a7cbe256af1662b6f7102221fd87de0d9c2655959f17910e2678219`  
		Last Modified: Wed, 10 Apr 2024 07:20:35 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949007b382393df630444de3c0e0cb309b27bbc1bd1edf7d30506dc2c68914f6`  
		Last Modified: Wed, 10 Apr 2024 07:21:27 GMT  
		Size: 320.2 MB (320185469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.8-slim-buster`

```console
$ docker pull haskell@sha256:f3a17a959888ec5c9391ca2e26b2c9f70b45f293f86d1ae541e1808b1254ddaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.8-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:900165e7e04e084ee8ce981c60aa95fba32a01d27a875952150e4cae8ce8a968
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428479087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8242dadea9b4e9b8a2d780d0f5e0d7881d45f4a42c05a83f6a7a19d44b21b6`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 09:32:45 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 09:32:47 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:32:47 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 09:32:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:33:59 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:34:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:34:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e18323aa33942f4ce38900edb6e6ce5600a98e3f0c2bc7844d7de11c90f245f`  
		Last Modified: Wed, 10 Apr 2024 09:46:49 GMT  
		Size: 7.8 MB (7838391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07825fee56074c1f3b6ece14439e881b544167cdeaa32ebd93e8fa62446c3275`  
		Last Modified: Wed, 10 Apr 2024 09:47:41 GMT  
		Size: 278.0 MB (277962209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.8-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3cb69fa8b28395f5d54a54632cfdd79b5eb1d2eb3f6ea5e0faf3282ed2314c97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **470.3 MB (470328876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42cebe65edfabd188590224a4c6063f5fca03ad40252e3ec923e0ae3758e97e3`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 10 Apr 2024 07:07:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 10 Apr 2024 07:07:41 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:07:41 GMT
ARG GHC=9.2.8
# Wed, 10 Apr 2024 07:07:41 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:09:00 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.2.8 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='645433359d8ad9e7b286f85ef5111db1b787ee3712c24c5dfde7c62769aa59a4';             ;;         'x86_64')             GHC_SHA256='10d1be25487bcf99ac8eb77beaa220c85e69f8c1106f4219ce019206ecc0ac51';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:09:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:09:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f330562a7cbe256af1662b6f7102221fd87de0d9c2655959f17910e2678219`  
		Last Modified: Wed, 10 Apr 2024 07:20:35 GMT  
		Size: 12.4 MB (12373194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:949007b382393df630444de3c0e0cb309b27bbc1bd1edf7d30506dc2c68914f6`  
		Last Modified: Wed, 10 Apr 2024 07:21:27 GMT  
		Size: 320.2 MB (320185469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4`

```console
$ docker pull haskell@sha256:7b0be07333727cd2bb74a82e60071317cba58acf4a88f987a0cccceb7b927019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4` - linux; amd64

```console
$ docker pull haskell@sha256:dd8ad57aefd52c5eab8395951607bfaea14a8c11abef87f5f7daa95a5d391745
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.0 MB (769996109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1375d354d190aeff32b9b024aaaa28ff42e8f309422a80b19d759c1877691b73`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:27:32 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 09:27:33 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 09:29:04 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:29:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:29:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441f9905b2e79440fd35dac01ce0620fd8f7c2885b41028e801d4742d3f92ae5`  
		Last Modified: Wed, 10 Apr 2024 09:44:06 GMT  
		Size: 428.1 MB (428108936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:63ffae8ca2c488dd5cdd02385f501c76c2d73901383871e5d6c809ea834ebdc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.0 MB (814027374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833330a18aab963ec0d7e164651a62d7b60ec635827d2d37d9beba5a84088247`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:02:14 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 07:02:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 07:03:43 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:03:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:03:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730af2258961dc5522486b334f42a2a2bfe8606e6750856df7351f55df1ed05a`  
		Last Modified: Wed, 10 Apr 2024 07:17:54 GMT  
		Size: 477.1 MB (477143586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4-buster`

```console
$ docker pull haskell@sha256:7b0be07333727cd2bb74a82e60071317cba58acf4a88f987a0cccceb7b927019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4-buster` - linux; amd64

```console
$ docker pull haskell@sha256:dd8ad57aefd52c5eab8395951607bfaea14a8c11abef87f5f7daa95a5d391745
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.0 MB (769996109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1375d354d190aeff32b9b024aaaa28ff42e8f309422a80b19d759c1877691b73`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:27:32 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 09:27:33 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 09:29:04 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:29:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:29:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441f9905b2e79440fd35dac01ce0620fd8f7c2885b41028e801d4742d3f92ae5`  
		Last Modified: Wed, 10 Apr 2024 09:44:06 GMT  
		Size: 428.1 MB (428108936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:63ffae8ca2c488dd5cdd02385f501c76c2d73901383871e5d6c809ea834ebdc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.0 MB (814027374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833330a18aab963ec0d7e164651a62d7b60ec635827d2d37d9beba5a84088247`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:02:14 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 07:02:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 07:03:43 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:03:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:03:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730af2258961dc5522486b334f42a2a2bfe8606e6750856df7351f55df1ed05a`  
		Last Modified: Wed, 10 Apr 2024 07:17:54 GMT  
		Size: 477.1 MB (477143586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4-slim`

```console
$ docker pull haskell@sha256:41e05a08ddeb6c0900f7973c7cecddc43ab966158322daa1adb59d82f5a192b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4-slim` - linux; amd64

```console
$ docker pull haskell@sha256:0c4c11695f67a68133af64499b16d73e00a437eaa1686a91a72791230b708600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.2 MB (436239263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca5eb4020c41a0e14560335cc45a2434a6efe5e514580fc1c4761bc76bc2d10`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:29:27 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 09:29:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 09:30:53 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:30:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:30:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392cc1d06ef85eb524e05ab6d0852149550aab62d939fb2d3bf08ebf50605715`  
		Last Modified: Wed, 10 Apr 2024 09:45:07 GMT  
		Size: 285.6 MB (285561315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:61741346b669dd2e660a31f53774ec7650d2bc05d4ff5c8f1ff0796b3627681e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.6 MB (458616875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656112bfe02c2dbad4aa7389a42bff05888d4fdfb118856c7cdd10962df1906c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:04:07 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 07:04:08 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 07:05:28 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:05:40 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:05:40 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58ff229b7a70cbedada36c02880bb3b669e2532c8ff1fbf70be9f520ae9d19`  
		Last Modified: Wed, 10 Apr 2024 07:18:53 GMT  
		Size: 310.7 MB (310733676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4-slim-buster`

```console
$ docker pull haskell@sha256:41e05a08ddeb6c0900f7973c7cecddc43ab966158322daa1adb59d82f5a192b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:0c4c11695f67a68133af64499b16d73e00a437eaa1686a91a72791230b708600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.2 MB (436239263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca5eb4020c41a0e14560335cc45a2434a6efe5e514580fc1c4761bc76bc2d10`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:29:27 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 09:29:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 09:30:53 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:30:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:30:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392cc1d06ef85eb524e05ab6d0852149550aab62d939fb2d3bf08ebf50605715`  
		Last Modified: Wed, 10 Apr 2024 09:45:07 GMT  
		Size: 285.6 MB (285561315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:61741346b669dd2e660a31f53774ec7650d2bc05d4ff5c8f1ff0796b3627681e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.6 MB (458616875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656112bfe02c2dbad4aa7389a42bff05888d4fdfb118856c7cdd10962df1906c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:04:07 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 07:04:08 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 07:05:28 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:05:40 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:05:40 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58ff229b7a70cbedada36c02880bb3b669e2532c8ff1fbf70be9f520ae9d19`  
		Last Modified: Wed, 10 Apr 2024 07:18:53 GMT  
		Size: 310.7 MB (310733676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.8`

```console
$ docker pull haskell@sha256:7b0be07333727cd2bb74a82e60071317cba58acf4a88f987a0cccceb7b927019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.8` - linux; amd64

```console
$ docker pull haskell@sha256:dd8ad57aefd52c5eab8395951607bfaea14a8c11abef87f5f7daa95a5d391745
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.0 MB (769996109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1375d354d190aeff32b9b024aaaa28ff42e8f309422a80b19d759c1877691b73`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:27:32 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 09:27:33 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 09:29:04 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:29:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:29:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441f9905b2e79440fd35dac01ce0620fd8f7c2885b41028e801d4742d3f92ae5`  
		Last Modified: Wed, 10 Apr 2024 09:44:06 GMT  
		Size: 428.1 MB (428108936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:63ffae8ca2c488dd5cdd02385f501c76c2d73901383871e5d6c809ea834ebdc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.0 MB (814027374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833330a18aab963ec0d7e164651a62d7b60ec635827d2d37d9beba5a84088247`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:02:14 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 07:02:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 07:03:43 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:03:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:03:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730af2258961dc5522486b334f42a2a2bfe8606e6750856df7351f55df1ed05a`  
		Last Modified: Wed, 10 Apr 2024 07:17:54 GMT  
		Size: 477.1 MB (477143586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.8-buster`

```console
$ docker pull haskell@sha256:7b0be07333727cd2bb74a82e60071317cba58acf4a88f987a0cccceb7b927019
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:dd8ad57aefd52c5eab8395951607bfaea14a8c11abef87f5f7daa95a5d391745
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **770.0 MB (769996109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1375d354d190aeff32b9b024aaaa28ff42e8f309422a80b19d759c1877691b73`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:27:32 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 09:27:33 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 09:29:04 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:29:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:29:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441f9905b2e79440fd35dac01ce0620fd8f7c2885b41028e801d4742d3f92ae5`  
		Last Modified: Wed, 10 Apr 2024 09:44:06 GMT  
		Size: 428.1 MB (428108936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.8-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:63ffae8ca2c488dd5cdd02385f501c76c2d73901383871e5d6c809ea834ebdc7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **814.0 MB (814027374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833330a18aab963ec0d7e164651a62d7b60ec635827d2d37d9beba5a84088247`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:02:14 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 07:02:14 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 07:03:43 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:03:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:03:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730af2258961dc5522486b334f42a2a2bfe8606e6750856df7351f55df1ed05a`  
		Last Modified: Wed, 10 Apr 2024 07:17:54 GMT  
		Size: 477.1 MB (477143586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.8-slim`

```console
$ docker pull haskell@sha256:41e05a08ddeb6c0900f7973c7cecddc43ab966158322daa1adb59d82f5a192b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:0c4c11695f67a68133af64499b16d73e00a437eaa1686a91a72791230b708600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.2 MB (436239263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca5eb4020c41a0e14560335cc45a2434a6efe5e514580fc1c4761bc76bc2d10`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:29:27 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 09:29:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 09:30:53 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:30:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:30:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392cc1d06ef85eb524e05ab6d0852149550aab62d939fb2d3bf08ebf50605715`  
		Last Modified: Wed, 10 Apr 2024 09:45:07 GMT  
		Size: 285.6 MB (285561315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:61741346b669dd2e660a31f53774ec7650d2bc05d4ff5c8f1ff0796b3627681e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.6 MB (458616875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656112bfe02c2dbad4aa7389a42bff05888d4fdfb118856c7cdd10962df1906c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:04:07 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 07:04:08 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 07:05:28 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:05:40 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:05:40 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58ff229b7a70cbedada36c02880bb3b669e2532c8ff1fbf70be9f520ae9d19`  
		Last Modified: Wed, 10 Apr 2024 07:18:53 GMT  
		Size: 310.7 MB (310733676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.4.8-slim-buster`

```console
$ docker pull haskell@sha256:41e05a08ddeb6c0900f7973c7cecddc43ab966158322daa1adb59d82f5a192b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.4.8-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:0c4c11695f67a68133af64499b16d73e00a437eaa1686a91a72791230b708600
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.2 MB (436239263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca5eb4020c41a0e14560335cc45a2434a6efe5e514580fc1c4761bc76bc2d10`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:29:27 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 09:29:27 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 09:30:53 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:30:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:30:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:392cc1d06ef85eb524e05ab6d0852149550aab62d939fb2d3bf08ebf50605715`  
		Last Modified: Wed, 10 Apr 2024 09:45:07 GMT  
		Size: 285.6 MB (285561315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.4.8-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:61741346b669dd2e660a31f53774ec7650d2bc05d4ff5c8f1ff0796b3627681e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.6 MB (458616875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656112bfe02c2dbad4aa7389a42bff05888d4fdfb118856c7cdd10962df1906c`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:04:07 GMT
ARG GHC=9.4.8
# Wed, 10 Apr 2024 07:04:08 GMT
ARG GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4
# Wed, 10 Apr 2024 07:05:28 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.4.8 GHC_RELEASE_KEY=88b57fcf7db53b4db3bfa4b1588764fbe22d19c4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='278e287e1ee624712b9c6d7803d1cf915ca1cce56e013b0a16215eb8dfeb1531';             ;;         'x86_64')             GHC_SHA256='fc77eaae5b89f29177bf159fd95ce438066ec64a46bf69df61b267102afdb10e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:05:40 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.4.8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:05:40 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c58ff229b7a70cbedada36c02880bb3b669e2532c8ff1fbf70be9f520ae9d19`  
		Last Modified: Wed, 10 Apr 2024 07:18:53 GMT  
		Size: 310.7 MB (310733676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6`

```console
$ docker pull haskell@sha256:64cb7a29955a8bd062cb10357690c7aeee4ea85eda3803fedeec208fd475ac62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6` - linux; amd64

```console
$ docker pull haskell@sha256:030753085c272117259be2dab206610ba77bcc701d15d0ea3251adc636fe9fee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.9 MB (766945481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8377070b0019154f012e7de83312d2c524ed5f74cbdbe5c07b62512543fb0ba2`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:23:45 GMT
ARG GHC=9.6.4
# Wed, 10 Apr 2024 09:23:45 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:25:25 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.4 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='d430345a66128c858e09dd9a90e5beabc045a9a3cedf776aea3adb45d1286276';             ;;         'x86_64')             GHC_SHA256='59885c43902110262cda168513dc6a9cc750e3e728dffb0cdb168e44929cb014';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:25:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:25:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f42038142ba07647d650001117a2a7efec95e02aa9741264c0bcdf19f8f9a9`  
		Last Modified: Wed, 10 Apr 2024 09:41:34 GMT  
		Size: 425.1 MB (425058308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fae6875e7af0d477a4f64522d5bdbada9c6f343c6116e7da965000647d050a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.3 MB (769275950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6f08d0f2490084fa4419c7c1b038f906d1ac80b858753ad358ace91e34e313`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:58:28 GMT
ARG GHC=9.6.4
# Wed, 10 Apr 2024 06:58:28 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:00:00 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.4 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='d430345a66128c858e09dd9a90e5beabc045a9a3cedf776aea3adb45d1286276';             ;;         'x86_64')             GHC_SHA256='59885c43902110262cda168513dc6a9cc750e3e728dffb0cdb168e44929cb014';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:00:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:00:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14237655da42be6effb605f8ad66e63e5aadd56143a93f9a7abde800b25c52aa`  
		Last Modified: Wed, 10 Apr 2024 07:15:36 GMT  
		Size: 432.4 MB (432392162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-buster`

```console
$ docker pull haskell@sha256:64cb7a29955a8bd062cb10357690c7aeee4ea85eda3803fedeec208fd475ac62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-buster` - linux; amd64

```console
$ docker pull haskell@sha256:030753085c272117259be2dab206610ba77bcc701d15d0ea3251adc636fe9fee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **766.9 MB (766945481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8377070b0019154f012e7de83312d2c524ed5f74cbdbe5c07b62512543fb0ba2`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:23:45 GMT
ARG GHC=9.6.4
# Wed, 10 Apr 2024 09:23:45 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:25:25 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.4 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='d430345a66128c858e09dd9a90e5beabc045a9a3cedf776aea3adb45d1286276';             ;;         'x86_64')             GHC_SHA256='59885c43902110262cda168513dc6a9cc750e3e728dffb0cdb168e44929cb014';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:25:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:25:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f42038142ba07647d650001117a2a7efec95e02aa9741264c0bcdf19f8f9a9`  
		Last Modified: Wed, 10 Apr 2024 09:41:34 GMT  
		Size: 425.1 MB (425058308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fae6875e7af0d477a4f64522d5bdbada9c6f343c6116e7da965000647d050a3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **769.3 MB (769275950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc6f08d0f2490084fa4419c7c1b038f906d1ac80b858753ad358ace91e34e313`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:58:28 GMT
ARG GHC=9.6.4
# Wed, 10 Apr 2024 06:58:28 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:00:00 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.4 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='d430345a66128c858e09dd9a90e5beabc045a9a3cedf776aea3adb45d1286276';             ;;         'x86_64')             GHC_SHA256='59885c43902110262cda168513dc6a9cc750e3e728dffb0cdb168e44929cb014';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:00:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:00:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14237655da42be6effb605f8ad66e63e5aadd56143a93f9a7abde800b25c52aa`  
		Last Modified: Wed, 10 Apr 2024 07:15:36 GMT  
		Size: 432.4 MB (432392162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-slim`

```console
$ docker pull haskell@sha256:513724207b978a8c98c816110f41810aad660cf482b187432da3733a2891d6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:6a30f3ffdb6569868ce7670b50b3f5bd0dcd9586f4a02ff0dc7a61f046e4e55a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.3 MB (434337230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a93270cceffa3171e328b4075f1972756a0cf24f0fd2389dc8155fa1dff3d9f`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:25:38 GMT
ARG GHC=9.6.4
# Wed, 10 Apr 2024 09:25:39 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:27:13 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.4 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='d430345a66128c858e09dd9a90e5beabc045a9a3cedf776aea3adb45d1286276';             ;;         'x86_64')             GHC_SHA256='59885c43902110262cda168513dc6a9cc750e3e728dffb0cdb168e44929cb014';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:27:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:27:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae4e68252f598dce6c508c9f7f6ea4d700c3b557adc57608f7e6fad606b570d`  
		Last Modified: Wed, 10 Apr 2024 09:42:39 GMT  
		Size: 283.7 MB (283659282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:89d174caaf2ada341449492d1f0911a3494f30076f6b671dd70bab7c509624e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.4 MB (438385347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551130cd00ee4797e89eb0041fb860ca1859f9bf19abcd2674dd254cf39dc2b5`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:00:21 GMT
ARG GHC=9.6.4
# Wed, 10 Apr 2024 07:00:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:01:53 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.4 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='d430345a66128c858e09dd9a90e5beabc045a9a3cedf776aea3adb45d1286276';             ;;         'x86_64')             GHC_SHA256='59885c43902110262cda168513dc6a9cc750e3e728dffb0cdb168e44929cb014';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:02:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:02:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fb4de41186cf81001e7f8f090b835fe069ff80c8a3b1832744053f347eca10`  
		Last Modified: Wed, 10 Apr 2024 07:16:31 GMT  
		Size: 290.5 MB (290502148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-slim-buster`

```console
$ docker pull haskell@sha256:513724207b978a8c98c816110f41810aad660cf482b187432da3733a2891d6c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:6a30f3ffdb6569868ce7670b50b3f5bd0dcd9586f4a02ff0dc7a61f046e4e55a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **434.3 MB (434337230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a93270cceffa3171e328b4075f1972756a0cf24f0fd2389dc8155fa1dff3d9f`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:25:38 GMT
ARG GHC=9.6.4
# Wed, 10 Apr 2024 09:25:39 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:27:13 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.4 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='d430345a66128c858e09dd9a90e5beabc045a9a3cedf776aea3adb45d1286276';             ;;         'x86_64')             GHC_SHA256='59885c43902110262cda168513dc6a9cc750e3e728dffb0cdb168e44929cb014';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:27:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:27:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae4e68252f598dce6c508c9f7f6ea4d700c3b557adc57608f7e6fad606b570d`  
		Last Modified: Wed, 10 Apr 2024 09:42:39 GMT  
		Size: 283.7 MB (283659282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:89d174caaf2ada341449492d1f0911a3494f30076f6b671dd70bab7c509624e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.4 MB (438385347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:551130cd00ee4797e89eb0041fb860ca1859f9bf19abcd2674dd254cf39dc2b5`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 07:00:21 GMT
ARG GHC=9.6.4
# Wed, 10 Apr 2024 07:00:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 07:01:53 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.4 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='d430345a66128c858e09dd9a90e5beabc045a9a3cedf776aea3adb45d1286276';             ;;         'x86_64')             GHC_SHA256='59885c43902110262cda168513dc6a9cc750e3e728dffb0cdb168e44929cb014';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 07:02:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 07:02:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3fb4de41186cf81001e7f8f090b835fe069ff80c8a3b1832744053f347eca10`  
		Last Modified: Wed, 10 Apr 2024 07:16:31 GMT  
		Size: 290.5 MB (290502148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.5`

**does not exist** (yet?)

## `haskell:9.6.5-buster`

**does not exist** (yet?)

## `haskell:9.6.5-slim`

**does not exist** (yet?)

## `haskell:9.6.5-slim-buster`

**does not exist** (yet?)

## `haskell:9.8`

```console
$ docker pull haskell@sha256:96705a005edc39eac637e2b4f70752c9a1a01745c06d005a19dd3e42e9b1100f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8` - linux; amd64

```console
$ docker pull haskell@sha256:b9fd4cc3cbe521e329bec346bbb89470f092643341344a11c7f087a3cc235b3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783698500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d3ef7825ce4866b834fe4b88177fff3e2eaedaa8147cc0ccf70494b9325fc`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:21:09 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:21:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:21:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7dba5e179f52cb2cd009e95da4e8c307e4251a8879195c46bfc0d256fa311`  
		Last Modified: Wed, 10 Apr 2024 09:38:42 GMT  
		Size: 441.8 MB (441811327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8f31b5d663813e79e76f4b8bcdb59f2e0d8d8e584119d0e3293802f4478f03a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.8 MB (785788047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9a82b985960bf46356702aedcb3095179824a4bb0d3c87cffd4edffd807f9d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:55:46 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:55:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:56:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b0b8f4f36bb81ea21877b9df9bdeb276a41701999be87deff93362c2ef98ed`  
		Last Modified: Wed, 10 Apr 2024 07:13:06 GMT  
		Size: 448.9 MB (448904259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8-buster`

```console
$ docker pull haskell@sha256:96705a005edc39eac637e2b4f70752c9a1a01745c06d005a19dd3e42e9b1100f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:b9fd4cc3cbe521e329bec346bbb89470f092643341344a11c7f087a3cc235b3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783698500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d3ef7825ce4866b834fe4b88177fff3e2eaedaa8147cc0ccf70494b9325fc`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:21:09 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:21:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:21:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7dba5e179f52cb2cd009e95da4e8c307e4251a8879195c46bfc0d256fa311`  
		Last Modified: Wed, 10 Apr 2024 09:38:42 GMT  
		Size: 441.8 MB (441811327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8f31b5d663813e79e76f4b8bcdb59f2e0d8d8e584119d0e3293802f4478f03a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.8 MB (785788047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9a82b985960bf46356702aedcb3095179824a4bb0d3c87cffd4edffd807f9d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:55:46 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:55:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:56:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b0b8f4f36bb81ea21877b9df9bdeb276a41701999be87deff93362c2ef98ed`  
		Last Modified: Wed, 10 Apr 2024 07:13:06 GMT  
		Size: 448.9 MB (448904259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8-slim`

```console
$ docker pull haskell@sha256:bbf9006351ecf54bb5668e37c4bdb17a78072c1022755aecc4648fe1e49ec8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:5dd55cd8aae5c0ee893306470874a6dd568dab348fa575c1e007e8416bafe24c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447662209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770ce30215bba6c99b3d9bf85038fc346f7e92f394355a585f167f491fcb253a`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:23:35 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:23:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:23:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a711823476076f81c4c9eaa538aa7c8406459afaf56831da6e241829561a06`  
		Last Modified: Wed, 10 Apr 2024 09:39:59 GMT  
		Size: 297.0 MB (296984261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6aa0434cb4a41447a13c28bb8b965ff3a5ccb67086f8a534d96c4b0bc1928d71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451489042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65baf4086cd897d7bf6241d06b7e7d60568ae55b9ce6b24862c36ee98ba3dff7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:58:01 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:58:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:58:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d890e4e955f93af0fa46b7bbddf91a7470650dc50f05cc748dc9781d006fd5`  
		Last Modified: Wed, 10 Apr 2024 07:14:12 GMT  
		Size: 303.6 MB (303605843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8-slim-buster`

```console
$ docker pull haskell@sha256:bbf9006351ecf54bb5668e37c4bdb17a78072c1022755aecc4648fe1e49ec8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5dd55cd8aae5c0ee893306470874a6dd568dab348fa575c1e007e8416bafe24c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447662209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770ce30215bba6c99b3d9bf85038fc346f7e92f394355a585f167f491fcb253a`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:23:35 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:23:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:23:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a711823476076f81c4c9eaa538aa7c8406459afaf56831da6e241829561a06`  
		Last Modified: Wed, 10 Apr 2024 09:39:59 GMT  
		Size: 297.0 MB (296984261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6aa0434cb4a41447a13c28bb8b965ff3a5ccb67086f8a534d96c4b0bc1928d71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451489042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65baf4086cd897d7bf6241d06b7e7d60568ae55b9ce6b24862c36ee98ba3dff7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:58:01 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:58:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:58:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d890e4e955f93af0fa46b7bbddf91a7470650dc50f05cc748dc9781d006fd5`  
		Last Modified: Wed, 10 Apr 2024 07:14:12 GMT  
		Size: 303.6 MB (303605843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8.2`

```console
$ docker pull haskell@sha256:96705a005edc39eac637e2b4f70752c9a1a01745c06d005a19dd3e42e9b1100f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8.2` - linux; amd64

```console
$ docker pull haskell@sha256:b9fd4cc3cbe521e329bec346bbb89470f092643341344a11c7f087a3cc235b3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783698500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d3ef7825ce4866b834fe4b88177fff3e2eaedaa8147cc0ccf70494b9325fc`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:21:09 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:21:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:21:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7dba5e179f52cb2cd009e95da4e8c307e4251a8879195c46bfc0d256fa311`  
		Last Modified: Wed, 10 Apr 2024 09:38:42 GMT  
		Size: 441.8 MB (441811327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8f31b5d663813e79e76f4b8bcdb59f2e0d8d8e584119d0e3293802f4478f03a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.8 MB (785788047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9a82b985960bf46356702aedcb3095179824a4bb0d3c87cffd4edffd807f9d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:55:46 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:55:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:56:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b0b8f4f36bb81ea21877b9df9bdeb276a41701999be87deff93362c2ef98ed`  
		Last Modified: Wed, 10 Apr 2024 07:13:06 GMT  
		Size: 448.9 MB (448904259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8.2-buster`

```console
$ docker pull haskell@sha256:96705a005edc39eac637e2b4f70752c9a1a01745c06d005a19dd3e42e9b1100f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:b9fd4cc3cbe521e329bec346bbb89470f092643341344a11c7f087a3cc235b3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783698500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d3ef7825ce4866b834fe4b88177fff3e2eaedaa8147cc0ccf70494b9325fc`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:21:09 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:21:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:21:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7dba5e179f52cb2cd009e95da4e8c307e4251a8879195c46bfc0d256fa311`  
		Last Modified: Wed, 10 Apr 2024 09:38:42 GMT  
		Size: 441.8 MB (441811327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8f31b5d663813e79e76f4b8bcdb59f2e0d8d8e584119d0e3293802f4478f03a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.8 MB (785788047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9a82b985960bf46356702aedcb3095179824a4bb0d3c87cffd4edffd807f9d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:55:46 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:55:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:56:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b0b8f4f36bb81ea21877b9df9bdeb276a41701999be87deff93362c2ef98ed`  
		Last Modified: Wed, 10 Apr 2024 07:13:06 GMT  
		Size: 448.9 MB (448904259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8.2-slim`

```console
$ docker pull haskell@sha256:bbf9006351ecf54bb5668e37c4bdb17a78072c1022755aecc4648fe1e49ec8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:5dd55cd8aae5c0ee893306470874a6dd568dab348fa575c1e007e8416bafe24c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447662209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770ce30215bba6c99b3d9bf85038fc346f7e92f394355a585f167f491fcb253a`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:23:35 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:23:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:23:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a711823476076f81c4c9eaa538aa7c8406459afaf56831da6e241829561a06`  
		Last Modified: Wed, 10 Apr 2024 09:39:59 GMT  
		Size: 297.0 MB (296984261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6aa0434cb4a41447a13c28bb8b965ff3a5ccb67086f8a534d96c4b0bc1928d71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451489042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65baf4086cd897d7bf6241d06b7e7d60568ae55b9ce6b24862c36ee98ba3dff7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:58:01 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:58:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:58:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d890e4e955f93af0fa46b7bbddf91a7470650dc50f05cc748dc9781d006fd5`  
		Last Modified: Wed, 10 Apr 2024 07:14:12 GMT  
		Size: 303.6 MB (303605843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.8.2-slim-buster`

```console
$ docker pull haskell@sha256:bbf9006351ecf54bb5668e37c4bdb17a78072c1022755aecc4648fe1e49ec8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.8.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5dd55cd8aae5c0ee893306470874a6dd568dab348fa575c1e007e8416bafe24c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447662209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770ce30215bba6c99b3d9bf85038fc346f7e92f394355a585f167f491fcb253a`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:23:35 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:23:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:23:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a711823476076f81c4c9eaa538aa7c8406459afaf56831da6e241829561a06`  
		Last Modified: Wed, 10 Apr 2024 09:39:59 GMT  
		Size: 297.0 MB (296984261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.8.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6aa0434cb4a41447a13c28bb8b965ff3a5ccb67086f8a534d96c4b0bc1928d71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451489042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65baf4086cd897d7bf6241d06b7e7d60568ae55b9ce6b24862c36ee98ba3dff7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:58:01 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:58:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:58:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d890e4e955f93af0fa46b7bbddf91a7470650dc50f05cc748dc9781d006fd5`  
		Last Modified: Wed, 10 Apr 2024 07:14:12 GMT  
		Size: 303.6 MB (303605843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:buster`

```console
$ docker pull haskell@sha256:96705a005edc39eac637e2b4f70752c9a1a01745c06d005a19dd3e42e9b1100f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:buster` - linux; amd64

```console
$ docker pull haskell@sha256:b9fd4cc3cbe521e329bec346bbb89470f092643341344a11c7f087a3cc235b3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783698500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d3ef7825ce4866b834fe4b88177fff3e2eaedaa8147cc0ccf70494b9325fc`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:21:09 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:21:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:21:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7dba5e179f52cb2cd009e95da4e8c307e4251a8879195c46bfc0d256fa311`  
		Last Modified: Wed, 10 Apr 2024 09:38:42 GMT  
		Size: 441.8 MB (441811327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8f31b5d663813e79e76f4b8bcdb59f2e0d8d8e584119d0e3293802f4478f03a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.8 MB (785788047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9a82b985960bf46356702aedcb3095179824a4bb0d3c87cffd4edffd807f9d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:55:46 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:55:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:56:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b0b8f4f36bb81ea21877b9df9bdeb276a41701999be87deff93362c2ef98ed`  
		Last Modified: Wed, 10 Apr 2024 07:13:06 GMT  
		Size: 448.9 MB (448904259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:96705a005edc39eac637e2b4f70752c9a1a01745c06d005a19dd3e42e9b1100f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:b9fd4cc3cbe521e329bec346bbb89470f092643341344a11c7f087a3cc235b3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **783.7 MB (783698500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6d3ef7825ce4866b834fe4b88177fff3e2eaedaa8147cc0ccf70494b9325fc`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:21 GMT
ADD file:c76ecdf17d2140aebb59f0261fd464e159af74b6489e79a1a10ad55941a63582 in / 
# Wed, 10 Apr 2024 01:51:22 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:27:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:28:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:29:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:12 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:19:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:19:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:19:20 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:19:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:19:23 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:19:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:21:09 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:21:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:21:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:13dc5104e330a0605d2251ca4b7184ca5c05c0c068e626b00515daf54ba1a917`  
		Last Modified: Wed, 10 Apr 2024 01:56:34 GMT  
		Size: 50.5 MB (50504020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a2be0394bca1f01401189d28d39b1fb8bded550d9905f371ad19c22c885f00`  
		Last Modified: Wed, 10 Apr 2024 05:36:56 GMT  
		Size: 17.6 MB (17585819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff192bd22402b8fc49beab8169860334a7e3ed795e392e8146c5ab943a7b5558`  
		Last Modified: Wed, 10 Apr 2024 05:37:12 GMT  
		Size: 51.9 MB (51895071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021d9f9c794a69ecba98598d11f0a7ef02e0a248ee4a7333f38a9e7fdcdf0cb`  
		Last Modified: Wed, 10 Apr 2024 05:37:42 GMT  
		Size: 191.9 MB (191944262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2efeeaff35c6d9702faf8d58ad5036bd5b97d208d91cfceff48580029b3ccb`  
		Last Modified: Wed, 10 Apr 2024 09:37:21 GMT  
		Size: 515.2 KB (515156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f352a0b11ca683a7659f8358a0041153323eee97a80818e1b9409ec67bf1aceb`  
		Last Modified: Wed, 10 Apr 2024 09:37:24 GMT  
		Size: 21.4 MB (21443394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6211943c10e1d768632c4af8973abf9ff3405a3e2ece8fccd9a3f20d5fe88920`  
		Last Modified: Wed, 10 Apr 2024 09:37:22 GMT  
		Size: 8.0 MB (7999451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c7dba5e179f52cb2cd009e95da4e8c307e4251a8879195c46bfc0d256fa311`  
		Last Modified: Wed, 10 Apr 2024 09:38:42 GMT  
		Size: 441.8 MB (441811327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8f31b5d663813e79e76f4b8bcdb59f2e0d8d8e584119d0e3293802f4478f03a6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **785.8 MB (785788047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb9a82b985960bf46356702aedcb3095179824a4bb0d3c87cffd4edffd807f9d`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:45 GMT
ADD file:9b995c280b9e45d7ee0b5a7151b97767f47960ed492e35fd55c5eec6917bde2c in / 
# Wed, 10 Apr 2024 00:40:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:24:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:25:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:26:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:57 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:54:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         libnuma-dev         libtinfo-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:54:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:54:04 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:54:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:54:07 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:54:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:55:46 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:55:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:56:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5173f9984b20306181404de41336884e6153c70a737a933879b7878563fc5bad`  
		Last Modified: Wed, 10 Apr 2024 00:45:06 GMT  
		Size: 49.3 MB (49290826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2fef8d22586d8b400820a7eb103890ffb31484294a394d9d1f6c707a2bb9c`  
		Last Modified: Wed, 10 Apr 2024 04:33:49 GMT  
		Size: 17.5 MB (17456523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f4463add27d4c2d315ca63e2d49c8bfb34a4fdd9015ea40d66f773285375d7`  
		Last Modified: Wed, 10 Apr 2024 04:34:03 GMT  
		Size: 52.2 MB (52231857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8636ccf677873adfe47bae13204f2fe3222b5c3d17e9cad47a51e6e6c67116`  
		Last Modified: Wed, 10 Apr 2024 04:34:28 GMT  
		Size: 183.5 MB (183524834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b20fa36d4a27d58dd8f7af4361d7cc35b3155f7f9e5d7e5323e120b5f81a37`  
		Last Modified: Wed, 10 Apr 2024 07:11:59 GMT  
		Size: 517.4 KB (517399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366649b8450d1306cbc5887a77cfd43636381a6ef968d89072e109975e159f9f`  
		Last Modified: Wed, 10 Apr 2024 07:12:02 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a340dd826f3bb91eb9b9cc728dbdf049935189fe172f2d8a6d3bca0d94c9a74`  
		Last Modified: Wed, 10 Apr 2024 07:12:01 GMT  
		Size: 10.1 MB (10112987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b0b8f4f36bb81ea21877b9df9bdeb276a41701999be87deff93362c2ef98ed`  
		Last Modified: Wed, 10 Apr 2024 07:13:06 GMT  
		Size: 448.9 MB (448904259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim`

```console
$ docker pull haskell@sha256:bbf9006351ecf54bb5668e37c4bdb17a78072c1022755aecc4648fe1e49ec8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:5dd55cd8aae5c0ee893306470874a6dd568dab348fa575c1e007e8416bafe24c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447662209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770ce30215bba6c99b3d9bf85038fc346f7e92f394355a585f167f491fcb253a`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:23:35 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:23:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:23:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a711823476076f81c4c9eaa538aa7c8406459afaf56831da6e241829561a06`  
		Last Modified: Wed, 10 Apr 2024 09:39:59 GMT  
		Size: 297.0 MB (296984261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6aa0434cb4a41447a13c28bb8b965ff3a5ccb67086f8a534d96c4b0bc1928d71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451489042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65baf4086cd897d7bf6241d06b7e7d60568ae55b9ce6b24862c36ee98ba3dff7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:58:01 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:58:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:58:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d890e4e955f93af0fa46b7bbddf91a7470650dc50f05cc748dc9781d006fd5`  
		Last Modified: Wed, 10 Apr 2024 07:14:12 GMT  
		Size: 303.6 MB (303605843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim-buster`

```console
$ docker pull haskell@sha256:bbf9006351ecf54bb5668e37c4bdb17a78072c1022755aecc4648fe1e49ec8cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5dd55cd8aae5c0ee893306470874a6dd568dab348fa575c1e007e8416bafe24c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447662209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770ce30215bba6c99b3d9bf85038fc346f7e92f394355a585f167f491fcb253a`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 01:51:34 GMT
ADD file:e2af322a9017b39b3ef71f2a62c8741e8f586798b9dec008de592186d3d9defc in / 
# Wed, 10 Apr 2024 01:51:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 09:21:21 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 09:21:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 09:21:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 09:21:48 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 09:21:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 09:21:51 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 09:21:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 09:23:35 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 09:23:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 09:23:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:8e208ccce385ccf024f3c96baef3af76333a0ea7b4596b450948bedb5aacb7d7`  
		Last Modified: Wed, 10 Apr 2024 01:56:54 GMT  
		Size: 27.2 MB (27190862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b256c33c886e3c28b6ca1b24709ff2f0a4d3f29a3cbb53307820265a3735d3b3`  
		Last Modified: Wed, 10 Apr 2024 09:39:19 GMT  
		Size: 94.0 MB (94044205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70656a015099a0aa550151e22c7cb18dc778b852e518b0ea9bd8b886d6ff230a`  
		Last Modified: Wed, 10 Apr 2024 09:39:08 GMT  
		Size: 21.4 MB (21443420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0586face6cec01f06f3b4e9f7d9afe82ebfbe2f95956c917db2b7efe499fd6d6`  
		Last Modified: Wed, 10 Apr 2024 09:39:05 GMT  
		Size: 8.0 MB (7999461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a711823476076f81c4c9eaa538aa7c8406459afaf56831da6e241829561a06`  
		Last Modified: Wed, 10 Apr 2024 09:39:59 GMT  
		Size: 297.0 MB (296984261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6aa0434cb4a41447a13c28bb8b965ff3a5ccb67086f8a534d96c4b0bc1928d71
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451489042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65baf4086cd897d7bf6241d06b7e7d60568ae55b9ce6b24862c36ee98ba3dff7`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:53 GMT
ADD file:d292eb4ae4049e9a68a950bea3e24901fefa765657eb1ffca34101cd6126a19b in / 
# Wed, 10 Apr 2024 00:40:54 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:56:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Apr 2024 06:56:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK=2.15.5
# Wed, 10 Apr 2024 06:56:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 10 Apr 2024 06:56:27 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL=3.10.2.0
# Wed, 10 Apr 2024 06:56:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 10 Apr 2024 06:56:30 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC=9.8.2
# Wed, 10 Apr 2024 06:56:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 10 Apr 2024 06:58:01 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 10 Apr 2024 06:58:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Apr 2024 06:58:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bb2cc851f729fd01506e97a9e7a21bdfb1f204260dd392851fb212ad839fc5ea`  
		Last Modified: Wed, 10 Apr 2024 00:45:27 GMT  
		Size: 26.0 MB (25963461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05556e0c26f5525ede197e61df2c47beaebd0cfce6c048a9a9dd4e4022bff913`  
		Last Modified: Wed, 10 Apr 2024 07:13:37 GMT  
		Size: 88.1 MB (88057394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0daa23d221c47495f135661560808abd10e003a600a37ca3a4fbad45505e60`  
		Last Modified: Wed, 10 Apr 2024 07:13:30 GMT  
		Size: 23.7 MB (23749358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82127a467fc0c4a1c94189c4ec6d5a9504473b5cef78c523417e55c81a6f355e`  
		Last Modified: Wed, 10 Apr 2024 07:13:29 GMT  
		Size: 10.1 MB (10112986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d890e4e955f93af0fa46b7bbddf91a7470650dc50f05cc748dc9781d006fd5`  
		Last Modified: Wed, 10 Apr 2024 07:14:12 GMT  
		Size: 303.6 MB (303605843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
