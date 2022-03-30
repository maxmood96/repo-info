<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:8`](#haskell8)
-	[`haskell:8-buster`](#haskell8-buster)
-	[`haskell:8-slim`](#haskell8-slim)
-	[`haskell:8-slim-buster`](#haskell8-slim-buster)
-	[`haskell:8.10`](#haskell810)
-	[`haskell:8.10-buster`](#haskell810-buster)
-	[`haskell:8.10-slim`](#haskell810-slim)
-	[`haskell:8.10-slim-buster`](#haskell810-slim-buster)
-	[`haskell:8.10.7`](#haskell8107)
-	[`haskell:8.10.7-buster`](#haskell8107-buster)
-	[`haskell:8.10.7-slim`](#haskell8107-slim)
-	[`haskell:8.10.7-slim-buster`](#haskell8107-slim-buster)
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
-	[`haskell:9.2.2`](#haskell922)
-	[`haskell:9.2.2-buster`](#haskell922-buster)
-	[`haskell:9.2.2-slim`](#haskell922-slim)
-	[`haskell:9.2.2-slim-buster`](#haskell922-slim-buster)
-	[`haskell:buster`](#haskellbuster)
-	[`haskell:latest`](#haskelllatest)
-	[`haskell:slim`](#haskellslim)
-	[`haskell:slim-buster`](#haskellslim-buster)

## `haskell:8`

```console
$ docker pull haskell@sha256:bc7488627b02c0593c561e37473b5e969ffd652ff52974dbf1183f665920b69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8` - linux; amd64

```console
$ docker pull haskell@sha256:ccd414f347f5830f1f1b007d89e98fa5af8ac33cd00f982fd395a1bc103b75a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529535178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2da59d45daf719c3bd50e1713858fec13a4937b401081a54feeaaf5480bd26`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:51:59 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:52:00 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:52:00 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:55:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:55:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:55:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:55:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1855e5c587bd7717bafdc84ad07dabfbc388ae01b5a0fc852037fb1ce505ac`  
		Last Modified: Tue, 29 Mar 2022 18:03:54 GMT  
		Size: 330.5 MB (330502117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867cacc8d5483d85f6d6b913846c34b5a6ca1bc6ac017647b97ad08d3a350563`  
		Last Modified: Tue, 29 Mar 2022 18:02:51 GMT  
		Size: 17.9 MB (17926646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c01add40faafd1d9d03da731a12aa5a4859dca35200b1aa7e84d595287e0c97c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06229dcda2877d585c64b887d44cee01cbbadb4e854822fd97757276abe4b8b1`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:37:05 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:37:06 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:37:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:39:58 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:39:59 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:41:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:41:20 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:41:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:41:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:41:24 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:41:24 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cacb9b6bf491db5cff4f0e764a4ab3268007be46fcf9507f5e4c897fda3db`  
		Last Modified: Wed, 30 Mar 2022 08:47:35 GMT  
		Size: 59.9 MB (59908205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f433415a942cd03f447929cbc00a28a180115b62d4fad91374496a054714b38d`  
		Last Modified: Wed, 30 Mar 2022 08:51:16 GMT  
		Size: 490.3 MB (490337945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-buster`

```console
$ docker pull haskell@sha256:bc7488627b02c0593c561e37473b5e969ffd652ff52974dbf1183f665920b69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:ccd414f347f5830f1f1b007d89e98fa5af8ac33cd00f982fd395a1bc103b75a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529535178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2da59d45daf719c3bd50e1713858fec13a4937b401081a54feeaaf5480bd26`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:51:59 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:52:00 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:52:00 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:55:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:55:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:55:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:55:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1855e5c587bd7717bafdc84ad07dabfbc388ae01b5a0fc852037fb1ce505ac`  
		Last Modified: Tue, 29 Mar 2022 18:03:54 GMT  
		Size: 330.5 MB (330502117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867cacc8d5483d85f6d6b913846c34b5a6ca1bc6ac017647b97ad08d3a350563`  
		Last Modified: Tue, 29 Mar 2022 18:02:51 GMT  
		Size: 17.9 MB (17926646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c01add40faafd1d9d03da731a12aa5a4859dca35200b1aa7e84d595287e0c97c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06229dcda2877d585c64b887d44cee01cbbadb4e854822fd97757276abe4b8b1`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:37:05 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:37:06 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:37:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:39:58 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:39:59 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:41:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:41:20 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:41:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:41:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:41:24 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:41:24 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cacb9b6bf491db5cff4f0e764a4ab3268007be46fcf9507f5e4c897fda3db`  
		Last Modified: Wed, 30 Mar 2022 08:47:35 GMT  
		Size: 59.9 MB (59908205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f433415a942cd03f447929cbc00a28a180115b62d4fad91374496a054714b38d`  
		Last Modified: Wed, 30 Mar 2022 08:51:16 GMT  
		Size: 490.3 MB (490337945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-slim`

```console
$ docker pull haskell@sha256:2c3addb3c9b5229570985c849e3a452f2d7e5bbb2ffaf9a0fba8007e68cca52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:f134db47505dd08b35ee7c1476f7b0b4cab710b7f8f8b935ff36d2b4ece0e12e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363647792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ae49918a82ca4cae7a3ec9df44ec30a7b66a3f14169b72d98aa95f50c26d11`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:53:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:56:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:56:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:56:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:56:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192755ec96aaaf1973b90766cf7ddc791d9200621b2961fdc4d820c8b36ed8fd`  
		Last Modified: Tue, 29 Mar 2022 18:05:02 GMT  
		Size: 214.5 MB (214534940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a6adc90cf8090280376e27cc74b51010a1031747e7f8e47cf891f2654f2443`  
		Last Modified: Tue, 29 Mar 2022 18:04:21 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:67473826052226d6f8ee8d18c5ca0075abe3ced3284a1841669d3e35a0847ead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515379052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef99f70f318a41c0dfa28955151f06e66e3785910b127b4a2512363be7998cc`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:38:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:41:40 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:41:41 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:42:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:42:58 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:42:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:42:59 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c94d792812ebca8dc9346adac0bae2029f10373b61a9f1633ba83c332e8e70e`  
		Last Modified: Wed, 30 Mar 2022 08:48:39 GMT  
		Size: 59.6 MB (59622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d142ff4a8bac9e9449263ca00498614ef08ab67fd8c6895ed85b6c5be1982d`  
		Last Modified: Wed, 30 Mar 2022 08:52:47 GMT  
		Size: 324.8 MB (324829152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-slim-buster`

```console
$ docker pull haskell@sha256:2c3addb3c9b5229570985c849e3a452f2d7e5bbb2ffaf9a0fba8007e68cca52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:f134db47505dd08b35ee7c1476f7b0b4cab710b7f8f8b935ff36d2b4ece0e12e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363647792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ae49918a82ca4cae7a3ec9df44ec30a7b66a3f14169b72d98aa95f50c26d11`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:53:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:56:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:56:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:56:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:56:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192755ec96aaaf1973b90766cf7ddc791d9200621b2961fdc4d820c8b36ed8fd`  
		Last Modified: Tue, 29 Mar 2022 18:05:02 GMT  
		Size: 214.5 MB (214534940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a6adc90cf8090280376e27cc74b51010a1031747e7f8e47cf891f2654f2443`  
		Last Modified: Tue, 29 Mar 2022 18:04:21 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:67473826052226d6f8ee8d18c5ca0075abe3ced3284a1841669d3e35a0847ead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515379052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef99f70f318a41c0dfa28955151f06e66e3785910b127b4a2512363be7998cc`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:38:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:41:40 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:41:41 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:42:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:42:58 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:42:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:42:59 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c94d792812ebca8dc9346adac0bae2029f10373b61a9f1633ba83c332e8e70e`  
		Last Modified: Wed, 30 Mar 2022 08:48:39 GMT  
		Size: 59.6 MB (59622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d142ff4a8bac9e9449263ca00498614ef08ab67fd8c6895ed85b6c5be1982d`  
		Last Modified: Wed, 30 Mar 2022 08:52:47 GMT  
		Size: 324.8 MB (324829152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10`

```console
$ docker pull haskell@sha256:bc7488627b02c0593c561e37473b5e969ffd652ff52974dbf1183f665920b69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10` - linux; amd64

```console
$ docker pull haskell@sha256:ccd414f347f5830f1f1b007d89e98fa5af8ac33cd00f982fd395a1bc103b75a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529535178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2da59d45daf719c3bd50e1713858fec13a4937b401081a54feeaaf5480bd26`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:51:59 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:52:00 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:52:00 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:55:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:55:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:55:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:55:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1855e5c587bd7717bafdc84ad07dabfbc388ae01b5a0fc852037fb1ce505ac`  
		Last Modified: Tue, 29 Mar 2022 18:03:54 GMT  
		Size: 330.5 MB (330502117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867cacc8d5483d85f6d6b913846c34b5a6ca1bc6ac017647b97ad08d3a350563`  
		Last Modified: Tue, 29 Mar 2022 18:02:51 GMT  
		Size: 17.9 MB (17926646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c01add40faafd1d9d03da731a12aa5a4859dca35200b1aa7e84d595287e0c97c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06229dcda2877d585c64b887d44cee01cbbadb4e854822fd97757276abe4b8b1`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:37:05 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:37:06 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:37:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:39:58 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:39:59 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:41:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:41:20 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:41:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:41:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:41:24 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:41:24 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cacb9b6bf491db5cff4f0e764a4ab3268007be46fcf9507f5e4c897fda3db`  
		Last Modified: Wed, 30 Mar 2022 08:47:35 GMT  
		Size: 59.9 MB (59908205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f433415a942cd03f447929cbc00a28a180115b62d4fad91374496a054714b38d`  
		Last Modified: Wed, 30 Mar 2022 08:51:16 GMT  
		Size: 490.3 MB (490337945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-buster`

```console
$ docker pull haskell@sha256:bc7488627b02c0593c561e37473b5e969ffd652ff52974dbf1183f665920b69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10-buster` - linux; amd64

```console
$ docker pull haskell@sha256:ccd414f347f5830f1f1b007d89e98fa5af8ac33cd00f982fd395a1bc103b75a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529535178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2da59d45daf719c3bd50e1713858fec13a4937b401081a54feeaaf5480bd26`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:51:59 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:52:00 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:52:00 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:55:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:55:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:55:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:55:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1855e5c587bd7717bafdc84ad07dabfbc388ae01b5a0fc852037fb1ce505ac`  
		Last Modified: Tue, 29 Mar 2022 18:03:54 GMT  
		Size: 330.5 MB (330502117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867cacc8d5483d85f6d6b913846c34b5a6ca1bc6ac017647b97ad08d3a350563`  
		Last Modified: Tue, 29 Mar 2022 18:02:51 GMT  
		Size: 17.9 MB (17926646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c01add40faafd1d9d03da731a12aa5a4859dca35200b1aa7e84d595287e0c97c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06229dcda2877d585c64b887d44cee01cbbadb4e854822fd97757276abe4b8b1`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:37:05 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:37:06 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:37:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:39:58 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:39:59 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:41:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:41:20 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:41:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:41:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:41:24 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:41:24 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cacb9b6bf491db5cff4f0e764a4ab3268007be46fcf9507f5e4c897fda3db`  
		Last Modified: Wed, 30 Mar 2022 08:47:35 GMT  
		Size: 59.9 MB (59908205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f433415a942cd03f447929cbc00a28a180115b62d4fad91374496a054714b38d`  
		Last Modified: Wed, 30 Mar 2022 08:51:16 GMT  
		Size: 490.3 MB (490337945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-slim`

```console
$ docker pull haskell@sha256:2c3addb3c9b5229570985c849e3a452f2d7e5bbb2ffaf9a0fba8007e68cca52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10-slim` - linux; amd64

```console
$ docker pull haskell@sha256:f134db47505dd08b35ee7c1476f7b0b4cab710b7f8f8b935ff36d2b4ece0e12e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363647792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ae49918a82ca4cae7a3ec9df44ec30a7b66a3f14169b72d98aa95f50c26d11`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:53:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:56:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:56:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:56:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:56:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192755ec96aaaf1973b90766cf7ddc791d9200621b2961fdc4d820c8b36ed8fd`  
		Last Modified: Tue, 29 Mar 2022 18:05:02 GMT  
		Size: 214.5 MB (214534940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a6adc90cf8090280376e27cc74b51010a1031747e7f8e47cf891f2654f2443`  
		Last Modified: Tue, 29 Mar 2022 18:04:21 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:67473826052226d6f8ee8d18c5ca0075abe3ced3284a1841669d3e35a0847ead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515379052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef99f70f318a41c0dfa28955151f06e66e3785910b127b4a2512363be7998cc`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:38:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:41:40 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:41:41 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:42:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:42:58 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:42:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:42:59 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c94d792812ebca8dc9346adac0bae2029f10373b61a9f1633ba83c332e8e70e`  
		Last Modified: Wed, 30 Mar 2022 08:48:39 GMT  
		Size: 59.6 MB (59622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d142ff4a8bac9e9449263ca00498614ef08ab67fd8c6895ed85b6c5be1982d`  
		Last Modified: Wed, 30 Mar 2022 08:52:47 GMT  
		Size: 324.8 MB (324829152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-slim-buster`

```console
$ docker pull haskell@sha256:2c3addb3c9b5229570985c849e3a452f2d7e5bbb2ffaf9a0fba8007e68cca52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:f134db47505dd08b35ee7c1476f7b0b4cab710b7f8f8b935ff36d2b4ece0e12e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363647792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ae49918a82ca4cae7a3ec9df44ec30a7b66a3f14169b72d98aa95f50c26d11`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:53:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:56:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:56:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:56:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:56:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192755ec96aaaf1973b90766cf7ddc791d9200621b2961fdc4d820c8b36ed8fd`  
		Last Modified: Tue, 29 Mar 2022 18:05:02 GMT  
		Size: 214.5 MB (214534940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a6adc90cf8090280376e27cc74b51010a1031747e7f8e47cf891f2654f2443`  
		Last Modified: Tue, 29 Mar 2022 18:04:21 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:67473826052226d6f8ee8d18c5ca0075abe3ced3284a1841669d3e35a0847ead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515379052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef99f70f318a41c0dfa28955151f06e66e3785910b127b4a2512363be7998cc`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:38:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:41:40 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:41:41 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:42:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:42:58 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:42:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:42:59 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c94d792812ebca8dc9346adac0bae2029f10373b61a9f1633ba83c332e8e70e`  
		Last Modified: Wed, 30 Mar 2022 08:48:39 GMT  
		Size: 59.6 MB (59622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d142ff4a8bac9e9449263ca00498614ef08ab67fd8c6895ed85b6c5be1982d`  
		Last Modified: Wed, 30 Mar 2022 08:52:47 GMT  
		Size: 324.8 MB (324829152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7`

```console
$ docker pull haskell@sha256:bc7488627b02c0593c561e37473b5e969ffd652ff52974dbf1183f665920b69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10.7` - linux; amd64

```console
$ docker pull haskell@sha256:ccd414f347f5830f1f1b007d89e98fa5af8ac33cd00f982fd395a1bc103b75a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529535178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2da59d45daf719c3bd50e1713858fec13a4937b401081a54feeaaf5480bd26`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:51:59 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:52:00 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:52:00 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:55:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:55:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:55:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:55:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1855e5c587bd7717bafdc84ad07dabfbc388ae01b5a0fc852037fb1ce505ac`  
		Last Modified: Tue, 29 Mar 2022 18:03:54 GMT  
		Size: 330.5 MB (330502117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867cacc8d5483d85f6d6b913846c34b5a6ca1bc6ac017647b97ad08d3a350563`  
		Last Modified: Tue, 29 Mar 2022 18:02:51 GMT  
		Size: 17.9 MB (17926646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10.7` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c01add40faafd1d9d03da731a12aa5a4859dca35200b1aa7e84d595287e0c97c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06229dcda2877d585c64b887d44cee01cbbadb4e854822fd97757276abe4b8b1`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:37:05 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:37:06 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:37:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:39:58 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:39:59 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:41:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:41:20 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:41:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:41:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:41:24 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:41:24 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cacb9b6bf491db5cff4f0e764a4ab3268007be46fcf9507f5e4c897fda3db`  
		Last Modified: Wed, 30 Mar 2022 08:47:35 GMT  
		Size: 59.9 MB (59908205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f433415a942cd03f447929cbc00a28a180115b62d4fad91374496a054714b38d`  
		Last Modified: Wed, 30 Mar 2022 08:51:16 GMT  
		Size: 490.3 MB (490337945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7-buster`

```console
$ docker pull haskell@sha256:bc7488627b02c0593c561e37473b5e969ffd652ff52974dbf1183f665920b69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10.7-buster` - linux; amd64

```console
$ docker pull haskell@sha256:ccd414f347f5830f1f1b007d89e98fa5af8ac33cd00f982fd395a1bc103b75a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **529.5 MB (529535178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2da59d45daf719c3bd50e1713858fec13a4937b401081a54feeaaf5480bd26`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:51:59 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:52:00 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:52:00 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:54:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:55:32 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:55:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:55:41 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:55:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:55:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1855e5c587bd7717bafdc84ad07dabfbc388ae01b5a0fc852037fb1ce505ac`  
		Last Modified: Tue, 29 Mar 2022 18:03:54 GMT  
		Size: 330.5 MB (330502117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867cacc8d5483d85f6d6b913846c34b5a6ca1bc6ac017647b97ad08d3a350563`  
		Last Modified: Tue, 29 Mar 2022 18:02:51 GMT  
		Size: 17.9 MB (17926646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10.7-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c01add40faafd1d9d03da731a12aa5a4859dca35200b1aa7e84d595287e0c97c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **731.1 MB (731133582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06229dcda2877d585c64b887d44cee01cbbadb4e854822fd97757276abe4b8b1`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:37:05 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:37:06 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:37:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:39:58 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:39:59 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:41:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:41:20 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:41:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:41:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:41:24 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:41:24 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cacb9b6bf491db5cff4f0e764a4ab3268007be46fcf9507f5e4c897fda3db`  
		Last Modified: Wed, 30 Mar 2022 08:47:35 GMT  
		Size: 59.9 MB (59908205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f433415a942cd03f447929cbc00a28a180115b62d4fad91374496a054714b38d`  
		Last Modified: Wed, 30 Mar 2022 08:51:16 GMT  
		Size: 490.3 MB (490337945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7-slim`

```console
$ docker pull haskell@sha256:2c3addb3c9b5229570985c849e3a452f2d7e5bbb2ffaf9a0fba8007e68cca52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10.7-slim` - linux; amd64

```console
$ docker pull haskell@sha256:f134db47505dd08b35ee7c1476f7b0b4cab710b7f8f8b935ff36d2b4ece0e12e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363647792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ae49918a82ca4cae7a3ec9df44ec30a7b66a3f14169b72d98aa95f50c26d11`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:53:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:56:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:56:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:56:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:56:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192755ec96aaaf1973b90766cf7ddc791d9200621b2961fdc4d820c8b36ed8fd`  
		Last Modified: Tue, 29 Mar 2022 18:05:02 GMT  
		Size: 214.5 MB (214534940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a6adc90cf8090280376e27cc74b51010a1031747e7f8e47cf891f2654f2443`  
		Last Modified: Tue, 29 Mar 2022 18:04:21 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10.7-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:67473826052226d6f8ee8d18c5ca0075abe3ced3284a1841669d3e35a0847ead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515379052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef99f70f318a41c0dfa28955151f06e66e3785910b127b4a2512363be7998cc`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:38:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:41:40 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:41:41 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:42:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:42:58 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:42:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:42:59 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c94d792812ebca8dc9346adac0bae2029f10373b61a9f1633ba83c332e8e70e`  
		Last Modified: Wed, 30 Mar 2022 08:48:39 GMT  
		Size: 59.6 MB (59622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d142ff4a8bac9e9449263ca00498614ef08ab67fd8c6895ed85b6c5be1982d`  
		Last Modified: Wed, 30 Mar 2022 08:52:47 GMT  
		Size: 324.8 MB (324829152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7-slim-buster`

```console
$ docker pull haskell@sha256:2c3addb3c9b5229570985c849e3a452f2d7e5bbb2ffaf9a0fba8007e68cca52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:8.10.7-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:f134db47505dd08b35ee7c1476f7b0b4cab710b7f8f8b935ff36d2b4ece0e12e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.6 MB (363647792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ae49918a82ca4cae7a3ec9df44ec30a7b66a3f14169b72d98aa95f50c26d11`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:53:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC=8.10.7
# Tue, 29 Mar 2022 17:55:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:56:47 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:56:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:56:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:56:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:56:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192755ec96aaaf1973b90766cf7ddc791d9200621b2961fdc4d820c8b36ed8fd`  
		Last Modified: Tue, 29 Mar 2022 18:05:02 GMT  
		Size: 214.5 MB (214534940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a6adc90cf8090280376e27cc74b51010a1031747e7f8e47cf891f2654f2443`  
		Last Modified: Tue, 29 Mar 2022 18:04:21 GMT  
		Size: 17.9 MB (17926649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:8.10.7-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:67473826052226d6f8ee8d18c5ca0075abe3ced3284a1841669d3e35a0847ead
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **515.4 MB (515379052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef99f70f318a41c0dfa28955151f06e66e3785910b127b4a2512363be7998cc`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:38:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:41:40 GMT
ARG GHC=8.10.7
# Wed, 30 Mar 2022 08:41:41 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:42:55 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='fad2417f9b295233bf8ade79c0e6140896359e87be46cb61cd1d35863d9d0e55';             ;;         'x86_64')             GHC_SHA256='a13719bca87a0d3ac0c7d4157a4e60887009a7f1a8dbe95c4759ec413e086d30';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:42:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:42:58 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:42:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:42:59 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c94d792812ebca8dc9346adac0bae2029f10373b61a9f1633ba83c332e8e70e`  
		Last Modified: Wed, 30 Mar 2022 08:48:39 GMT  
		Size: 59.6 MB (59622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8d142ff4a8bac9e9449263ca00498614ef08ab67fd8c6895ed85b6c5be1982d`  
		Last Modified: Wed, 30 Mar 2022 08:52:47 GMT  
		Size: 324.8 MB (324829152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9`

```console
$ docker pull haskell@sha256:fb0cb2a45ef1847921bc7b60496897900185a365f55f0109c849dcfbb649a4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:5df3103025085c4d8b3d42ac918539279de50ee9c2d9f1d98d0b193fac7325a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540047925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa36c0f6009e6b52d88bc3f4df23cafe1274e8b944a01301a258e7a070725f99`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:50:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:50:14 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:50:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:50:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d0017e27e5d1f2421b842d474f8c144627a77c25301ef32a4db06ef18f3842`  
		Last Modified: Tue, 29 Mar 2022 17:58:49 GMT  
		Size: 341.0 MB (341014853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e2d37aaa5c1f5b4c06be64f76d2b740de209330337a8e7caab5d22b2e1f0e9`  
		Last Modified: Tue, 29 Mar 2022 17:57:42 GMT  
		Size: 17.9 MB (17926657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:df671503eea4996c169397f1aad07f3e840ccd2c5ecd952569a6bfc7137401b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.5 MB (586545110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f31b9446ebc9fc0f9b1b5d6b76c6e57b5d01aa268f2a7d1433c55bad4e47dd`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:33:26 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:33:27 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:34:47 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:34:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:34:50 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:34:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:34:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafe4fa00f42681cd7e17079b6b10160786fdd140060f8647ce1096e4363cc6`  
		Last Modified: Wed, 30 Mar 2022 08:45:36 GMT  
		Size: 405.7 MB (405657678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-buster`

```console
$ docker pull haskell@sha256:fb0cb2a45ef1847921bc7b60496897900185a365f55f0109c849dcfbb649a4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5df3103025085c4d8b3d42ac918539279de50ee9c2d9f1d98d0b193fac7325a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540047925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa36c0f6009e6b52d88bc3f4df23cafe1274e8b944a01301a258e7a070725f99`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:50:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:50:14 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:50:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:50:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d0017e27e5d1f2421b842d474f8c144627a77c25301ef32a4db06ef18f3842`  
		Last Modified: Tue, 29 Mar 2022 17:58:49 GMT  
		Size: 341.0 MB (341014853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e2d37aaa5c1f5b4c06be64f76d2b740de209330337a8e7caab5d22b2e1f0e9`  
		Last Modified: Tue, 29 Mar 2022 17:57:42 GMT  
		Size: 17.9 MB (17926657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:df671503eea4996c169397f1aad07f3e840ccd2c5ecd952569a6bfc7137401b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.5 MB (586545110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f31b9446ebc9fc0f9b1b5d6b76c6e57b5d01aa268f2a7d1433c55bad4e47dd`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:33:26 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:33:27 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:34:47 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:34:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:34:50 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:34:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:34:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafe4fa00f42681cd7e17079b6b10160786fdd140060f8647ce1096e4363cc6`  
		Last Modified: Wed, 30 Mar 2022 08:45:36 GMT  
		Size: 405.7 MB (405657678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:4c8dec588c918af065246b417a7f0041636abe31247aff63ef9591fdf0995941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:c7c4a1dbc7d8818719765f10dd6271056d3b374d8be51404be797db548846409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368243193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3205460f1dca64d4dd88bafba8a68e6b0786b7a28e2af709a36109b6bb17a3`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:51:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:51:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:51:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:51:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e7218692fc3e3d9d3dc77b5f85f270f68ab71fda0e290f1182d02a70228d4e`  
		Last Modified: Tue, 29 Mar 2022 18:00:01 GMT  
		Size: 219.1 MB (219130338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928df00ae7823132f2b590610f1d5aa602c0e2eda749a6e7b7f0e534cb52050e`  
		Last Modified: Tue, 29 Mar 2022 17:59:18 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f1d1eb4f1774f8df08311de6ac2896840479047aada32863e723ab2becbadb77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391864302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8cafc711fe4e9128d36ca21eeee82b3df3d7c84e7fdee7775bf2bb78a7ae96`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:35:38 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:35:39 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:36:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:36:54 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:36:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:36:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702a9d31bdee1b93af5524239e3a332acd79d3ff423e6125bcfe218b28cf159`  
		Last Modified: Wed, 30 Mar 2022 08:46:58 GMT  
		Size: 260.9 MB (260937376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim-buster`

```console
$ docker pull haskell@sha256:4c8dec588c918af065246b417a7f0041636abe31247aff63ef9591fdf0995941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c7c4a1dbc7d8818719765f10dd6271056d3b374d8be51404be797db548846409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368243193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3205460f1dca64d4dd88bafba8a68e6b0786b7a28e2af709a36109b6bb17a3`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:51:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:51:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:51:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:51:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e7218692fc3e3d9d3dc77b5f85f270f68ab71fda0e290f1182d02a70228d4e`  
		Last Modified: Tue, 29 Mar 2022 18:00:01 GMT  
		Size: 219.1 MB (219130338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928df00ae7823132f2b590610f1d5aa602c0e2eda749a6e7b7f0e534cb52050e`  
		Last Modified: Tue, 29 Mar 2022 17:59:18 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f1d1eb4f1774f8df08311de6ac2896840479047aada32863e723ab2becbadb77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391864302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8cafc711fe4e9128d36ca21eeee82b3df3d7c84e7fdee7775bf2bb78a7ae96`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:35:38 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:35:39 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:36:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:36:54 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:36:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:36:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702a9d31bdee1b93af5524239e3a332acd79d3ff423e6125bcfe218b28cf159`  
		Last Modified: Wed, 30 Mar 2022 08:46:58 GMT  
		Size: 260.9 MB (260937376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0`

```console
$ docker pull haskell@sha256:529f2746ff81030e1f516454dfc69cd5fd1b21f8d95ee831076ca7ba9bd1b99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0` - linux; amd64

```console
$ docker pull haskell@sha256:f30cfc368b08f166581b64ac7bf2491a8ef6d578843b7832a5549091ad4b825e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525438475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d78316c864bfab43ec1bd1649f007545a49b3593862c6eaeda32e7baa42d9b`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:51:59 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:52:00 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:52:00 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:52:00 GMT
ARG GHC=9.0.2
# Tue, 29 Mar 2022 17:52:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:53:03 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:53:07 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:53:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:53:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:53:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:53:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdee28ca056c13821a2f8f3bd1fa6f7cc385e403ae4185e94ba2d1ecf28f48e0`  
		Last Modified: Tue, 29 Mar 2022 18:01:33 GMT  
		Size: 326.4 MB (326405408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3651525de2e5232547fe732855b1e1f5d01019cc0c10aa00667487c35f7ddce1`  
		Last Modified: Tue, 29 Mar 2022 18:00:30 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a8c2844e711a8d8f6ac34bfe335a238c10d706864b0e6ebf9ae907a4ebcbe9d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.8 MB (471777390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8477413f6f665d5d7acfaed8403ca909f9f5c65664416d85f72bb322e966fd71`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:37:05 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:37:06 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:37:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:37:18 GMT
ARG GHC=9.0.2
# Wed, 30 Mar 2022 08:37:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:38:16 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:38:17 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:38:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:38:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:38:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:38:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cacb9b6bf491db5cff4f0e764a4ab3268007be46fcf9507f5e4c897fda3db`  
		Last Modified: Wed, 30 Mar 2022 08:47:35 GMT  
		Size: 59.9 MB (59908205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae36f2ef5f385c68cb07a0f322dcf9bd7401153258d4aa23ac6819a60011a2f0`  
		Last Modified: Wed, 30 Mar 2022 08:48:14 GMT  
		Size: 231.0 MB (230981753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-buster`

```console
$ docker pull haskell@sha256:529f2746ff81030e1f516454dfc69cd5fd1b21f8d95ee831076ca7ba9bd1b99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-buster` - linux; amd64

```console
$ docker pull haskell@sha256:f30cfc368b08f166581b64ac7bf2491a8ef6d578843b7832a5549091ad4b825e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525438475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d78316c864bfab43ec1bd1649f007545a49b3593862c6eaeda32e7baa42d9b`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:51:59 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:52:00 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:52:00 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:52:00 GMT
ARG GHC=9.0.2
# Tue, 29 Mar 2022 17:52:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:53:03 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:53:07 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:53:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:53:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:53:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:53:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdee28ca056c13821a2f8f3bd1fa6f7cc385e403ae4185e94ba2d1ecf28f48e0`  
		Last Modified: Tue, 29 Mar 2022 18:01:33 GMT  
		Size: 326.4 MB (326405408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3651525de2e5232547fe732855b1e1f5d01019cc0c10aa00667487c35f7ddce1`  
		Last Modified: Tue, 29 Mar 2022 18:00:30 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a8c2844e711a8d8f6ac34bfe335a238c10d706864b0e6ebf9ae907a4ebcbe9d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.8 MB (471777390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8477413f6f665d5d7acfaed8403ca909f9f5c65664416d85f72bb322e966fd71`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:37:05 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:37:06 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:37:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:37:18 GMT
ARG GHC=9.0.2
# Wed, 30 Mar 2022 08:37:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:38:16 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:38:17 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:38:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:38:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:38:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:38:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cacb9b6bf491db5cff4f0e764a4ab3268007be46fcf9507f5e4c897fda3db`  
		Last Modified: Wed, 30 Mar 2022 08:47:35 GMT  
		Size: 59.9 MB (59908205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae36f2ef5f385c68cb07a0f322dcf9bd7401153258d4aa23ac6819a60011a2f0`  
		Last Modified: Wed, 30 Mar 2022 08:48:14 GMT  
		Size: 231.0 MB (230981753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-slim`

```console
$ docker pull haskell@sha256:8088f0da89d9d1810c46b0c738b3e1c189fecf28beb7d3b68a31d56d4551112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-slim` - linux; amd64

```console
$ docker pull haskell@sha256:8d3cc6e46168fb41c1b7bbe02d62ad82f13251984265f026af1237085cbedea7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359085460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa237378686405bae836b167aa4ee2e40689ee2cb798e01716ec1ae54a347002`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:53:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:53:23 GMT
ARG GHC=9.0.2
# Tue, 29 Mar 2022 17:53:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:54:20 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:54:24 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:54:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:54:27 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:54:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:54:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fcf8bac2f4369f26780766b3eeb36b03f53aec9d8a0fd3189a70b1be675732`  
		Last Modified: Tue, 29 Mar 2022 18:02:31 GMT  
		Size: 210.0 MB (209972593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a330344560e0216e1f3f92ffee5f7cf52a2a3b9cbe0d7ed13d9f946e221f9b7a`  
		Last Modified: Tue, 29 Mar 2022 18:01:52 GMT  
		Size: 17.9 MB (17926664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:edec78ec10b910d83fe1cc7d5879c7b63df02e23d711a1c5414f1438405e91fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.5 MB (421534608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5052579595a773bbedc9fc9bab321bae5b82aab4b577a6d5960984cb5b8d0c7`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:38:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:38:42 GMT
ARG GHC=9.0.2
# Wed, 30 Mar 2022 08:38:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:39:39 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:39:39 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:39:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:39:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:39:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:39:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c94d792812ebca8dc9346adac0bae2029f10373b61a9f1633ba83c332e8e70e`  
		Last Modified: Wed, 30 Mar 2022 08:48:39 GMT  
		Size: 59.6 MB (59622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e791e967ae3379633fe2bce4046cb99d518caf6c0768e7d411cabc0f13a0cf`  
		Last Modified: Wed, 30 Mar 2022 08:49:18 GMT  
		Size: 231.0 MB (230984708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-slim-buster`

```console
$ docker pull haskell@sha256:8088f0da89d9d1810c46b0c738b3e1c189fecf28beb7d3b68a31d56d4551112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:8d3cc6e46168fb41c1b7bbe02d62ad82f13251984265f026af1237085cbedea7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359085460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa237378686405bae836b167aa4ee2e40689ee2cb798e01716ec1ae54a347002`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:53:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:53:23 GMT
ARG GHC=9.0.2
# Tue, 29 Mar 2022 17:53:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:54:20 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:54:24 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:54:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:54:27 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:54:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:54:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fcf8bac2f4369f26780766b3eeb36b03f53aec9d8a0fd3189a70b1be675732`  
		Last Modified: Tue, 29 Mar 2022 18:02:31 GMT  
		Size: 210.0 MB (209972593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a330344560e0216e1f3f92ffee5f7cf52a2a3b9cbe0d7ed13d9f946e221f9b7a`  
		Last Modified: Tue, 29 Mar 2022 18:01:52 GMT  
		Size: 17.9 MB (17926664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:edec78ec10b910d83fe1cc7d5879c7b63df02e23d711a1c5414f1438405e91fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.5 MB (421534608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5052579595a773bbedc9fc9bab321bae5b82aab4b577a6d5960984cb5b8d0c7`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:38:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:38:42 GMT
ARG GHC=9.0.2
# Wed, 30 Mar 2022 08:38:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:39:39 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:39:39 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:39:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:39:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:39:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:39:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c94d792812ebca8dc9346adac0bae2029f10373b61a9f1633ba83c332e8e70e`  
		Last Modified: Wed, 30 Mar 2022 08:48:39 GMT  
		Size: 59.6 MB (59622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e791e967ae3379633fe2bce4046cb99d518caf6c0768e7d411cabc0f13a0cf`  
		Last Modified: Wed, 30 Mar 2022 08:49:18 GMT  
		Size: 231.0 MB (230984708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2`

```console
$ docker pull haskell@sha256:529f2746ff81030e1f516454dfc69cd5fd1b21f8d95ee831076ca7ba9bd1b99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2` - linux; amd64

```console
$ docker pull haskell@sha256:f30cfc368b08f166581b64ac7bf2491a8ef6d578843b7832a5549091ad4b825e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525438475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d78316c864bfab43ec1bd1649f007545a49b3593862c6eaeda32e7baa42d9b`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:51:59 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:52:00 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:52:00 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:52:00 GMT
ARG GHC=9.0.2
# Tue, 29 Mar 2022 17:52:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:53:03 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:53:07 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:53:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:53:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:53:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:53:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdee28ca056c13821a2f8f3bd1fa6f7cc385e403ae4185e94ba2d1ecf28f48e0`  
		Last Modified: Tue, 29 Mar 2022 18:01:33 GMT  
		Size: 326.4 MB (326405408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3651525de2e5232547fe732855b1e1f5d01019cc0c10aa00667487c35f7ddce1`  
		Last Modified: Tue, 29 Mar 2022 18:00:30 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a8c2844e711a8d8f6ac34bfe335a238c10d706864b0e6ebf9ae907a4ebcbe9d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.8 MB (471777390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8477413f6f665d5d7acfaed8403ca909f9f5c65664416d85f72bb322e966fd71`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:37:05 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:37:06 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:37:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:37:18 GMT
ARG GHC=9.0.2
# Wed, 30 Mar 2022 08:37:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:38:16 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:38:17 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:38:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:38:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:38:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:38:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cacb9b6bf491db5cff4f0e764a4ab3268007be46fcf9507f5e4c897fda3db`  
		Last Modified: Wed, 30 Mar 2022 08:47:35 GMT  
		Size: 59.9 MB (59908205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae36f2ef5f385c68cb07a0f322dcf9bd7401153258d4aa23ac6819a60011a2f0`  
		Last Modified: Wed, 30 Mar 2022 08:48:14 GMT  
		Size: 231.0 MB (230981753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-buster`

```console
$ docker pull haskell@sha256:529f2746ff81030e1f516454dfc69cd5fd1b21f8d95ee831076ca7ba9bd1b99c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:f30cfc368b08f166581b64ac7bf2491a8ef6d578843b7832a5549091ad4b825e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **525.4 MB (525438475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d78316c864bfab43ec1bd1649f007545a49b3593862c6eaeda32e7baa42d9b`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:51:59 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:52:00 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:52:00 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:52:00 GMT
ARG GHC=9.0.2
# Tue, 29 Mar 2022 17:52:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:53:03 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:53:07 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:53:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:53:12 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:53:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:53:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdee28ca056c13821a2f8f3bd1fa6f7cc385e403ae4185e94ba2d1ecf28f48e0`  
		Last Modified: Tue, 29 Mar 2022 18:01:33 GMT  
		Size: 326.4 MB (326405408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3651525de2e5232547fe732855b1e1f5d01019cc0c10aa00667487c35f7ddce1`  
		Last Modified: Tue, 29 Mar 2022 18:00:30 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a8c2844e711a8d8f6ac34bfe335a238c10d706864b0e6ebf9ae907a4ebcbe9d1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **471.8 MB (471777390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8477413f6f665d5d7acfaed8403ca909f9f5c65664416d85f72bb322e966fd71`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:37:05 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:37:06 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:37:17 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:37:18 GMT
ARG GHC=9.0.2
# Wed, 30 Mar 2022 08:37:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:38:16 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:38:17 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:38:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:38:19 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:38:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:38:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cacb9b6bf491db5cff4f0e764a4ab3268007be46fcf9507f5e4c897fda3db`  
		Last Modified: Wed, 30 Mar 2022 08:47:35 GMT  
		Size: 59.9 MB (59908205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae36f2ef5f385c68cb07a0f322dcf9bd7401153258d4aa23ac6819a60011a2f0`  
		Last Modified: Wed, 30 Mar 2022 08:48:14 GMT  
		Size: 231.0 MB (230981753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-slim`

```console
$ docker pull haskell@sha256:8088f0da89d9d1810c46b0c738b3e1c189fecf28beb7d3b68a31d56d4551112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:8d3cc6e46168fb41c1b7bbe02d62ad82f13251984265f026af1237085cbedea7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359085460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa237378686405bae836b167aa4ee2e40689ee2cb798e01716ec1ae54a347002`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:53:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:53:23 GMT
ARG GHC=9.0.2
# Tue, 29 Mar 2022 17:53:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:54:20 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:54:24 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:54:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:54:27 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:54:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:54:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fcf8bac2f4369f26780766b3eeb36b03f53aec9d8a0fd3189a70b1be675732`  
		Last Modified: Tue, 29 Mar 2022 18:02:31 GMT  
		Size: 210.0 MB (209972593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a330344560e0216e1f3f92ffee5f7cf52a2a3b9cbe0d7ed13d9f946e221f9b7a`  
		Last Modified: Tue, 29 Mar 2022 18:01:52 GMT  
		Size: 17.9 MB (17926664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:edec78ec10b910d83fe1cc7d5879c7b63df02e23d711a1c5414f1438405e91fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.5 MB (421534608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5052579595a773bbedc9fc9bab321bae5b82aab4b577a6d5960984cb5b8d0c7`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:38:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:38:42 GMT
ARG GHC=9.0.2
# Wed, 30 Mar 2022 08:38:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:39:39 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:39:39 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:39:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:39:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:39:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:39:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c94d792812ebca8dc9346adac0bae2029f10373b61a9f1633ba83c332e8e70e`  
		Last Modified: Wed, 30 Mar 2022 08:48:39 GMT  
		Size: 59.6 MB (59622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e791e967ae3379633fe2bce4046cb99d518caf6c0768e7d411cabc0f13a0cf`  
		Last Modified: Wed, 30 Mar 2022 08:49:18 GMT  
		Size: 231.0 MB (230984708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.2-slim-buster`

```console
$ docker pull haskell@sha256:8088f0da89d9d1810c46b0c738b3e1c189fecf28beb7d3b68a31d56d4551112f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.0.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:8d3cc6e46168fb41c1b7bbe02d62ad82f13251984265f026af1237085cbedea7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359085460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa237378686405bae836b167aa4ee2e40689ee2cb798e01716ec1ae54a347002`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_VERSION=12
# Tue, 29 Mar 2022 17:53:22 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Tue, 29 Mar 2022 17:53:23 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Tue, 29 Mar 2022 17:53:23 GMT
ARG GHC=9.0.2
# Tue, 29 Mar 2022 17:53:23 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 29 Mar 2022 17:54:20 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:54:24 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:54:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:54:27 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:54:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:54:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fcf8bac2f4369f26780766b3eeb36b03f53aec9d8a0fd3189a70b1be675732`  
		Last Modified: Tue, 29 Mar 2022 18:02:31 GMT  
		Size: 210.0 MB (209972593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a330344560e0216e1f3f92ffee5f7cf52a2a3b9cbe0d7ed13d9f946e221f9b7a`  
		Last Modified: Tue, 29 Mar 2022 18:01:52 GMT  
		Size: 17.9 MB (17926664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.0.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:edec78ec10b910d83fe1cc7d5879c7b63df02e23d711a1c5414f1438405e91fc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.5 MB (421534608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5052579595a773bbedc9fc9bab321bae5b82aab4b577a6d5960984cb5b8d0c7`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_VERSION=12
# Wed, 30 Mar 2022 08:38:32 GMT
ARG LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421
# Wed, 30 Mar 2022 08:38:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     if [ "$(dpkg-architecture --query DEB_BUILD_GNU_CPU)" = "aarch64" ]; then         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         mkdir -p /usr/local/share/keyrings/;         gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$LLVM_KEY";         gpg --batch --armor --export "$LLVM_KEY" > /usr/local/share/keyrings/apt.llvm.org.gpg.asc;         echo "deb [ signed-by=/usr/local/share/keyrings/apt.llvm.org.gpg.asc ] http://apt.llvm.org/buster/ llvm-toolchain-buster-$LLVM_VERSION main" > /etc/apt/sources.list.d/llvm.list;         apt-get update;         apt-get install -y --no-install-recommends llvm-$LLVM_VERSION;         gpgconf --kill all;         rm -rf "$GNUPGHOME" /var/lib/apt/lists/*;     fi
# Wed, 30 Mar 2022 08:38:42 GMT
ARG GHC=9.0.2
# Wed, 30 Mar 2022 08:38:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 30 Mar 2022 08:39:39 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='cb016344c70a872738a24af60bd15d3b18749087b9905c1b3f1b1549dc01f46d';             ;;         'x86_64')             GHC_SHA256='5d0b9414b10cfb918453bcd01c5ea7a1824fe95948b08498d6780f20ba247afc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:39:39 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:39:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:39:42 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.0.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 LLVM_KEY=6084F3CF814B57C1CF12EFD515CF4D18AF4F7421 LLVM_VERSION=12 STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:39:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:39:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c94d792812ebca8dc9346adac0bae2029f10373b61a9f1633ba83c332e8e70e`  
		Last Modified: Wed, 30 Mar 2022 08:48:39 GMT  
		Size: 59.6 MB (59622974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e791e967ae3379633fe2bce4046cb99d518caf6c0768e7d411cabc0f13a0cf`  
		Last Modified: Wed, 30 Mar 2022 08:49:18 GMT  
		Size: 231.0 MB (230984708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2`

```console
$ docker pull haskell@sha256:fb0cb2a45ef1847921bc7b60496897900185a365f55f0109c849dcfbb649a4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2` - linux; amd64

```console
$ docker pull haskell@sha256:5df3103025085c4d8b3d42ac918539279de50ee9c2d9f1d98d0b193fac7325a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540047925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa36c0f6009e6b52d88bc3f4df23cafe1274e8b944a01301a258e7a070725f99`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:50:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:50:14 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:50:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:50:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d0017e27e5d1f2421b842d474f8c144627a77c25301ef32a4db06ef18f3842`  
		Last Modified: Tue, 29 Mar 2022 17:58:49 GMT  
		Size: 341.0 MB (341014853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e2d37aaa5c1f5b4c06be64f76d2b740de209330337a8e7caab5d22b2e1f0e9`  
		Last Modified: Tue, 29 Mar 2022 17:57:42 GMT  
		Size: 17.9 MB (17926657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:df671503eea4996c169397f1aad07f3e840ccd2c5ecd952569a6bfc7137401b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.5 MB (586545110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f31b9446ebc9fc0f9b1b5d6b76c6e57b5d01aa268f2a7d1433c55bad4e47dd`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:33:26 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:33:27 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:34:47 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:34:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:34:50 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:34:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:34:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafe4fa00f42681cd7e17079b6b10160786fdd140060f8647ce1096e4363cc6`  
		Last Modified: Wed, 30 Mar 2022 08:45:36 GMT  
		Size: 405.7 MB (405657678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-buster`

```console
$ docker pull haskell@sha256:fb0cb2a45ef1847921bc7b60496897900185a365f55f0109c849dcfbb649a4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5df3103025085c4d8b3d42ac918539279de50ee9c2d9f1d98d0b193fac7325a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540047925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa36c0f6009e6b52d88bc3f4df23cafe1274e8b944a01301a258e7a070725f99`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:50:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:50:14 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:50:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:50:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d0017e27e5d1f2421b842d474f8c144627a77c25301ef32a4db06ef18f3842`  
		Last Modified: Tue, 29 Mar 2022 17:58:49 GMT  
		Size: 341.0 MB (341014853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e2d37aaa5c1f5b4c06be64f76d2b740de209330337a8e7caab5d22b2e1f0e9`  
		Last Modified: Tue, 29 Mar 2022 17:57:42 GMT  
		Size: 17.9 MB (17926657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:df671503eea4996c169397f1aad07f3e840ccd2c5ecd952569a6bfc7137401b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.5 MB (586545110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f31b9446ebc9fc0f9b1b5d6b76c6e57b5d01aa268f2a7d1433c55bad4e47dd`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:33:26 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:33:27 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:34:47 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:34:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:34:50 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:34:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:34:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafe4fa00f42681cd7e17079b6b10160786fdd140060f8647ce1096e4363cc6`  
		Last Modified: Wed, 30 Mar 2022 08:45:36 GMT  
		Size: 405.7 MB (405657678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-slim`

```console
$ docker pull haskell@sha256:4c8dec588c918af065246b417a7f0041636abe31247aff63ef9591fdf0995941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:c7c4a1dbc7d8818719765f10dd6271056d3b374d8be51404be797db548846409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368243193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3205460f1dca64d4dd88bafba8a68e6b0786b7a28e2af709a36109b6bb17a3`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:51:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:51:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:51:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:51:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e7218692fc3e3d9d3dc77b5f85f270f68ab71fda0e290f1182d02a70228d4e`  
		Last Modified: Tue, 29 Mar 2022 18:00:01 GMT  
		Size: 219.1 MB (219130338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928df00ae7823132f2b590610f1d5aa602c0e2eda749a6e7b7f0e534cb52050e`  
		Last Modified: Tue, 29 Mar 2022 17:59:18 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f1d1eb4f1774f8df08311de6ac2896840479047aada32863e723ab2becbadb77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391864302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8cafc711fe4e9128d36ca21eeee82b3df3d7c84e7fdee7775bf2bb78a7ae96`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:35:38 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:35:39 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:36:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:36:54 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:36:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:36:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702a9d31bdee1b93af5524239e3a332acd79d3ff423e6125bcfe218b28cf159`  
		Last Modified: Wed, 30 Mar 2022 08:46:58 GMT  
		Size: 260.9 MB (260937376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2-slim-buster`

```console
$ docker pull haskell@sha256:4c8dec588c918af065246b417a7f0041636abe31247aff63ef9591fdf0995941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c7c4a1dbc7d8818719765f10dd6271056d3b374d8be51404be797db548846409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368243193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3205460f1dca64d4dd88bafba8a68e6b0786b7a28e2af709a36109b6bb17a3`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:51:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:51:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:51:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:51:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e7218692fc3e3d9d3dc77b5f85f270f68ab71fda0e290f1182d02a70228d4e`  
		Last Modified: Tue, 29 Mar 2022 18:00:01 GMT  
		Size: 219.1 MB (219130338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928df00ae7823132f2b590610f1d5aa602c0e2eda749a6e7b7f0e534cb52050e`  
		Last Modified: Tue, 29 Mar 2022 17:59:18 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f1d1eb4f1774f8df08311de6ac2896840479047aada32863e723ab2becbadb77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391864302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8cafc711fe4e9128d36ca21eeee82b3df3d7c84e7fdee7775bf2bb78a7ae96`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:35:38 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:35:39 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:36:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:36:54 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:36:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:36:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702a9d31bdee1b93af5524239e3a332acd79d3ff423e6125bcfe218b28cf159`  
		Last Modified: Wed, 30 Mar 2022 08:46:58 GMT  
		Size: 260.9 MB (260937376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.2`

```console
$ docker pull haskell@sha256:fb0cb2a45ef1847921bc7b60496897900185a365f55f0109c849dcfbb649a4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.2` - linux; amd64

```console
$ docker pull haskell@sha256:5df3103025085c4d8b3d42ac918539279de50ee9c2d9f1d98d0b193fac7325a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540047925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa36c0f6009e6b52d88bc3f4df23cafe1274e8b944a01301a258e7a070725f99`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:50:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:50:14 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:50:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:50:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d0017e27e5d1f2421b842d474f8c144627a77c25301ef32a4db06ef18f3842`  
		Last Modified: Tue, 29 Mar 2022 17:58:49 GMT  
		Size: 341.0 MB (341014853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e2d37aaa5c1f5b4c06be64f76d2b740de209330337a8e7caab5d22b2e1f0e9`  
		Last Modified: Tue, 29 Mar 2022 17:57:42 GMT  
		Size: 17.9 MB (17926657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:df671503eea4996c169397f1aad07f3e840ccd2c5ecd952569a6bfc7137401b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.5 MB (586545110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f31b9446ebc9fc0f9b1b5d6b76c6e57b5d01aa268f2a7d1433c55bad4e47dd`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:33:26 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:33:27 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:34:47 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:34:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:34:50 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:34:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:34:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafe4fa00f42681cd7e17079b6b10160786fdd140060f8647ce1096e4363cc6`  
		Last Modified: Wed, 30 Mar 2022 08:45:36 GMT  
		Size: 405.7 MB (405657678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.2-buster`

```console
$ docker pull haskell@sha256:fb0cb2a45ef1847921bc7b60496897900185a365f55f0109c849dcfbb649a4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.2-buster` - linux; amd64

```console
$ docker pull haskell@sha256:5df3103025085c4d8b3d42ac918539279de50ee9c2d9f1d98d0b193fac7325a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540047925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa36c0f6009e6b52d88bc3f4df23cafe1274e8b944a01301a258e7a070725f99`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:50:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:50:14 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:50:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:50:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d0017e27e5d1f2421b842d474f8c144627a77c25301ef32a4db06ef18f3842`  
		Last Modified: Tue, 29 Mar 2022 17:58:49 GMT  
		Size: 341.0 MB (341014853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e2d37aaa5c1f5b4c06be64f76d2b740de209330337a8e7caab5d22b2e1f0e9`  
		Last Modified: Tue, 29 Mar 2022 17:57:42 GMT  
		Size: 17.9 MB (17926657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.2-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:df671503eea4996c169397f1aad07f3e840ccd2c5ecd952569a6bfc7137401b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.5 MB (586545110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f31b9446ebc9fc0f9b1b5d6b76c6e57b5d01aa268f2a7d1433c55bad4e47dd`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:33:26 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:33:27 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:34:47 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:34:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:34:50 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:34:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:34:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafe4fa00f42681cd7e17079b6b10160786fdd140060f8647ce1096e4363cc6`  
		Last Modified: Wed, 30 Mar 2022 08:45:36 GMT  
		Size: 405.7 MB (405657678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.2-slim`

```console
$ docker pull haskell@sha256:4c8dec588c918af065246b417a7f0041636abe31247aff63ef9591fdf0995941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.2-slim` - linux; amd64

```console
$ docker pull haskell@sha256:c7c4a1dbc7d8818719765f10dd6271056d3b374d8be51404be797db548846409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368243193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3205460f1dca64d4dd88bafba8a68e6b0786b7a28e2af709a36109b6bb17a3`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:51:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:51:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:51:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:51:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e7218692fc3e3d9d3dc77b5f85f270f68ab71fda0e290f1182d02a70228d4e`  
		Last Modified: Tue, 29 Mar 2022 18:00:01 GMT  
		Size: 219.1 MB (219130338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928df00ae7823132f2b590610f1d5aa602c0e2eda749a6e7b7f0e534cb52050e`  
		Last Modified: Tue, 29 Mar 2022 17:59:18 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.2-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f1d1eb4f1774f8df08311de6ac2896840479047aada32863e723ab2becbadb77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391864302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8cafc711fe4e9128d36ca21eeee82b3df3d7c84e7fdee7775bf2bb78a7ae96`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:35:38 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:35:39 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:36:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:36:54 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:36:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:36:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702a9d31bdee1b93af5524239e3a332acd79d3ff423e6125bcfe218b28cf159`  
		Last Modified: Wed, 30 Mar 2022 08:46:58 GMT  
		Size: 260.9 MB (260937376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.2.2-slim-buster`

```console
$ docker pull haskell@sha256:4c8dec588c918af065246b417a7f0041636abe31247aff63ef9591fdf0995941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.2.2-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c7c4a1dbc7d8818719765f10dd6271056d3b374d8be51404be797db548846409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368243193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3205460f1dca64d4dd88bafba8a68e6b0786b7a28e2af709a36109b6bb17a3`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:51:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:51:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:51:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:51:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e7218692fc3e3d9d3dc77b5f85f270f68ab71fda0e290f1182d02a70228d4e`  
		Last Modified: Tue, 29 Mar 2022 18:00:01 GMT  
		Size: 219.1 MB (219130338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928df00ae7823132f2b590610f1d5aa602c0e2eda749a6e7b7f0e534cb52050e`  
		Last Modified: Tue, 29 Mar 2022 17:59:18 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.2.2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f1d1eb4f1774f8df08311de6ac2896840479047aada32863e723ab2becbadb77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391864302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8cafc711fe4e9128d36ca21eeee82b3df3d7c84e7fdee7775bf2bb78a7ae96`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:35:38 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:35:39 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:36:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:36:54 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:36:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:36:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702a9d31bdee1b93af5524239e3a332acd79d3ff423e6125bcfe218b28cf159`  
		Last Modified: Wed, 30 Mar 2022 08:46:58 GMT  
		Size: 260.9 MB (260937376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:buster`

```console
$ docker pull haskell@sha256:fb0cb2a45ef1847921bc7b60496897900185a365f55f0109c849dcfbb649a4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:buster` - linux; amd64

```console
$ docker pull haskell@sha256:5df3103025085c4d8b3d42ac918539279de50ee9c2d9f1d98d0b193fac7325a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540047925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa36c0f6009e6b52d88bc3f4df23cafe1274e8b944a01301a258e7a070725f99`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:50:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:50:14 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:50:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:50:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d0017e27e5d1f2421b842d474f8c144627a77c25301ef32a4db06ef18f3842`  
		Last Modified: Tue, 29 Mar 2022 17:58:49 GMT  
		Size: 341.0 MB (341014853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e2d37aaa5c1f5b4c06be64f76d2b740de209330337a8e7caab5d22b2e1f0e9`  
		Last Modified: Tue, 29 Mar 2022 17:57:42 GMT  
		Size: 17.9 MB (17926657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:df671503eea4996c169397f1aad07f3e840ccd2c5ecd952569a6bfc7137401b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.5 MB (586545110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f31b9446ebc9fc0f9b1b5d6b76c6e57b5d01aa268f2a7d1433c55bad4e47dd`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:33:26 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:33:27 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:34:47 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:34:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:34:50 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:34:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:34:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafe4fa00f42681cd7e17079b6b10160786fdd140060f8647ce1096e4363cc6`  
		Last Modified: Wed, 30 Mar 2022 08:45:36 GMT  
		Size: 405.7 MB (405657678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:fb0cb2a45ef1847921bc7b60496897900185a365f55f0109c849dcfbb649a4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:5df3103025085c4d8b3d42ac918539279de50ee9c2d9f1d98d0b193fac7325a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **540.0 MB (540047925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa36c0f6009e6b52d88bc3f4df23cafe1274e8b944a01301a258e7a070725f99`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:28 GMT
ADD file:8c5e9f12fd3b6e830ec0ee1800d8e9dcebf217896148f2dc72c010c8a88d9b8f in / 
# Tue, 29 Mar 2022 00:22:28 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:48:29 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:48:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:48:50 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:48:51 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:48:53 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:48:53 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:50:05 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:50:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:50:14 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:50:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:50:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b281ebec60d2630a225601bd58a4681375a31b7316263b64d3b149f49694c3fe`  
		Last Modified: Tue, 29 Mar 2022 00:27:37 GMT  
		Size: 50.4 MB (50437915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09ae98d29049825f151b492e3ab68ebb47205936d746308c79cc2a6624dfa5`  
		Last Modified: Tue, 29 Mar 2022 17:57:59 GMT  
		Size: 120.6 MB (120636231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7471c88a182c6ebf2bda9da90649af28badadd636933199e469b1392efbeb964`  
		Last Modified: Tue, 29 Mar 2022 17:57:41 GMT  
		Size: 10.0 MB (10032269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d0017e27e5d1f2421b842d474f8c144627a77c25301ef32a4db06ef18f3842`  
		Last Modified: Tue, 29 Mar 2022 17:58:49 GMT  
		Size: 341.0 MB (341014853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e2d37aaa5c1f5b4c06be64f76d2b740de209330337a8e7caab5d22b2e1f0e9`  
		Last Modified: Tue, 29 Mar 2022 17:57:42 GMT  
		Size: 17.9 MB (17926657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:df671503eea4996c169397f1aad07f3e840ccd2c5ecd952569a6bfc7137401b0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **586.5 MB (586545110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f31b9446ebc9fc0f9b1b5d6b76c6e57b5d01aa268f2a7d1433c55bad4e47dd`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:27 GMT
ADD file:7686930f8c48390948992fbe39ce798cc57ee1d8785b3da70f4a3220f6e7b024 in / 
# Tue, 29 Mar 2022 00:43:28 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:32:56 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:33:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:33:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:33:25 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:33:26 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:33:27 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:34:46 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:34:47 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:34:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:34:50 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:34:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:34:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c732c99090fe64466c6911ecfdd8d4d3f6dfb183aab95d7746163bc49ebe35c9`  
		Last Modified: Tue, 29 Mar 2022 00:50:29 GMT  
		Size: 49.2 MB (49225896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c24a07e51b33cdbb01306ed066836a1c9fce4b9a8ce7a74921b2fe54ca70ba0`  
		Last Modified: Wed, 30 Mar 2022 08:44:31 GMT  
		Size: 114.7 MB (114677659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07cd995c2687e188925657e5ee090ad1e6d2cebe70a07514fd4ce6db5462a70`  
		Last Modified: Wed, 30 Mar 2022 08:44:19 GMT  
		Size: 17.0 MB (16983877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcafe4fa00f42681cd7e17079b6b10160786fdd140060f8647ce1096e4363cc6`  
		Last Modified: Wed, 30 Mar 2022 08:45:36 GMT  
		Size: 405.7 MB (405657678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim`

```console
$ docker pull haskell@sha256:4c8dec588c918af065246b417a7f0041636abe31247aff63ef9591fdf0995941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:c7c4a1dbc7d8818719765f10dd6271056d3b374d8be51404be797db548846409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368243193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3205460f1dca64d4dd88bafba8a68e6b0786b7a28e2af709a36109b6bb17a3`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:51:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:51:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:51:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:51:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e7218692fc3e3d9d3dc77b5f85f270f68ab71fda0e290f1182d02a70228d4e`  
		Last Modified: Tue, 29 Mar 2022 18:00:01 GMT  
		Size: 219.1 MB (219130338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928df00ae7823132f2b590610f1d5aa602c0e2eda749a6e7b7f0e534cb52050e`  
		Last Modified: Tue, 29 Mar 2022 17:59:18 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f1d1eb4f1774f8df08311de6ac2896840479047aada32863e723ab2becbadb77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391864302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8cafc711fe4e9128d36ca21eeee82b3df3d7c84e7fdee7775bf2bb78a7ae96`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:35:38 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:35:39 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:36:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:36:54 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:36:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:36:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702a9d31bdee1b93af5524239e3a332acd79d3ff423e6125bcfe218b28cf159`  
		Last Modified: Wed, 30 Mar 2022 08:46:58 GMT  
		Size: 260.9 MB (260937376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim-buster`

```console
$ docker pull haskell@sha256:4c8dec588c918af065246b417a7f0041636abe31247aff63ef9591fdf0995941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:c7c4a1dbc7d8818719765f10dd6271056d3b374d8be51404be797db548846409
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.2 MB (368243193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca3205460f1dca64d4dd88bafba8a68e6b0786b7a28e2af709a36109b6bb17a3`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:38 GMT
ADD file:59187422476c57db46e60f894a4cfd0f243e80230ef9ea75b2d8dd4925d59df3 in / 
# Tue, 29 Mar 2022 00:22:38 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:50:22 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:50:41 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:50:41 GMT
ARG CABAL_INSTALL=3.6.2.0
# Tue, 29 Mar 2022 17:50:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Tue, 29 Mar 2022 17:50:44 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC=9.2.2
# Tue, 29 Mar 2022 17:50:44 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 29 Mar 2022 17:51:43 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK=2.7.5
# Tue, 29 Mar 2022 17:51:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 29 Mar 2022 17:51:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Tue, 29 Mar 2022 17:51:51 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:51:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f003217c5aaebdfee0b9a448fbabd995e5f0159f5b231460c0ecc21baf171953`  
		Last Modified: Tue, 29 Mar 2022 00:28:02 GMT  
		Size: 27.2 MB (27151970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabf8c5045a7884ed40233b09464bb07a0d41d8d39bfea2b76d5d44733c33382`  
		Last Modified: Tue, 29 Mar 2022 17:59:32 GMT  
		Size: 94.0 MB (94001963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21d44f18ad86bd21cca1a52545195d5258517c349277708cefafd2dc0e63dfe`  
		Last Modified: Tue, 29 Mar 2022 17:59:17 GMT  
		Size: 10.0 MB (10032270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e7218692fc3e3d9d3dc77b5f85f270f68ab71fda0e290f1182d02a70228d4e`  
		Last Modified: Tue, 29 Mar 2022 18:00:01 GMT  
		Size: 219.1 MB (219130338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928df00ae7823132f2b590610f1d5aa602c0e2eda749a6e7b7f0e534cb52050e`  
		Last Modified: Tue, 29 Mar 2022 17:59:18 GMT  
		Size: 17.9 MB (17926652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f1d1eb4f1774f8df08311de6ac2896840479047aada32863e723ab2becbadb77
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 MB (391864302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8cafc711fe4e9128d36ca21eeee82b3df3d7c84e7fdee7775bf2bb78a7ae96`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:42 GMT
ADD file:fdc8a5391a75cbf8c121f8f799ca08e94d2b3967b2546b36231c9297f7ce2151 in / 
# Tue, 29 Mar 2022 00:43:43 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 08:35:08 GMT
ENV LANG=C.UTF-8
# Wed, 30 Mar 2022 08:35:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL=3.6.2.0
# Wed, 30 Mar 2022 08:35:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Wed, 30 Mar 2022 08:35:37 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='d9acee67d4308bc5c22d27bee034d388cc4192a25deff9e7e491e2396572b030';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4759b56e9257e02f29fa374a6b25d6cb2f9d80c7e3a55d4f678a8e570925641c';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 30 Mar 2022 08:35:38 GMT
ARG GHC=9.2.2
# Wed, 30 Mar 2022 08:35:39 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 30 Mar 2022 08:36:51 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='f3621ccba7ae48fcd67a9505f61bb5ccfb05c4cbfecd5a6ea65fe3f150af0e98';             ;;         'x86_64')             GHC_SHA256='fb61dea556a2023dc2d50ee61a22144bb23e4229a378e533065124c218f40cfc';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;     rm -rf "/opt/ghc/$GHC/share/";         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK=2.7.5
# Wed, 30 Mar 2022 08:36:52 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 30 Mar 2022 08:36:54 GMT
# ARGS: CABAL_INSTALL=3.6.2.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 GHC=9.2.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.7.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     INSTALL_STACK="true";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             INSTALL_STACK="false";             ;;         'x86_64')             STACK_SHA256='9bcd165358d4dcafd2b33320d4fe98ce72faaf62300cc9b0fb86a27eb670da50';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     if [ "$INSTALL_STACK" = "true" ]; then         curl -sSL "$STACK_URL" -o stack.tar.gz;         echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;                 curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;         gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";         gpg --batch --verify stack.tar.gz.asc stack.tar.gz;         gpgconf --kill all;                 tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";         stack config set system-ghc --global true;         stack config set install-ghc --global false;                 rm -rf /tmp/*;                 stack --version;     fi
# Wed, 30 Mar 2022 08:36:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.2.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 08:36:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5022906f515a0d4ec6bc1d0e5e7a01f47b1fbbb912e7e3f1ace27987169a9a21`  
		Last Modified: Tue, 29 Mar 2022 00:50:58 GMT  
		Size: 25.9 MB (25919777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff07ea0d3bf5f5b9bee460e5c9493797e30001066d9bab142ca0b22308729659`  
		Last Modified: Wed, 30 Mar 2022 08:46:18 GMT  
		Size: 88.0 MB (88023267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37047efe540e4b36e1cb6be3a02a2868b96be0a4bcfa9c57cf28f88d1f422292`  
		Last Modified: Wed, 30 Mar 2022 08:46:09 GMT  
		Size: 17.0 MB (16983882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702a9d31bdee1b93af5524239e3a332acd79d3ff423e6125bcfe218b28cf159`  
		Last Modified: Wed, 30 Mar 2022 08:46:58 GMT  
		Size: 260.9 MB (260937376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
