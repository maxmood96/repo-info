<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:9`](#haskell9)
-	[`haskell:9-bullseye`](#haskell9-bullseye)
-	[`haskell:9-slim`](#haskell9-slim)
-	[`haskell:9-slim-bullseye`](#haskell9-slim-bullseye)
-	[`haskell:9.10-bullseye`](#haskell910-bullseye)
-	[`haskell:9.10-slim-bullseye`](#haskell910-slim-bullseye)
-	[`haskell:9.10.1-bullseye`](#haskell9101-bullseye)
-	[`haskell:9.10.1-slim-bullseye`](#haskell9101-slim-bullseye)
-	[`haskell:bullseye`](#haskellbullseye)
-	[`haskell:latest`](#haskelllatest)
-	[`haskell:slim`](#haskellslim)
-	[`haskell:slim-bullseye`](#haskellslim-bullseye)

## `haskell:9`

```console
$ docker pull haskell@sha256:76f045024b949c01aadc18a75430de171517a7ee42521a855cc8fb99d684f701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:b249e3c9bb6630e4afde592350b7e061cb0857ea3b6838ae1f21be7ad20930fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657469957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f1321f867c36deae5b01c2f23459db8932ab8412f27c84fd3a95ecc75f9dec`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:19:40 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:20:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:20:07 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:20:10 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:22:04 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:22:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:22:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75b0fdeafbb9aeaefe9ef7d1a65a592cdd314b40c2691bb70195683adf6bdf`  
		Last Modified: Fri, 09 Aug 2024 18:25:26 GMT  
		Size: 133.5 MB (133517024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413fbf9c62ffb025608142af38c18a9887e2d082b2f521ab49a8a82fc39a5c9c`  
		Last Modified: Fri, 09 Aug 2024 18:25:12 GMT  
		Size: 21.8 MB (21787165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d282b4bfd6f53fcb2278eaac3bab6665563fe191166a1cf5fdfe746afa74ec01`  
		Last Modified: Fri, 09 Aug 2024 18:25:10 GMT  
		Size: 8.0 MB (8004054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45fe090366505717409423f4073d51af743a646caad4baae760e0ee692b247f`  
		Last Modified: Fri, 09 Aug 2024 18:26:24 GMT  
		Size: 439.1 MB (439077136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6d91a487465ad3119956db03d669fec6e2ed2791c496d414918e674ce35b904
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.4 MB (663432585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9317913eebe3238d376e65ef199a64eec15861ebff3aab36c67581a94df48f60`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:39:33 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:39:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:40:00 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:40:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:40:01 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:40:03 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:42:09 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:42:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:42:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e063bbde2822160b94073c7f78bd03283c1c1061a2097599ed50ec0ac7dc4`  
		Last Modified: Fri, 09 Aug 2024 17:45:30 GMT  
		Size: 129.0 MB (128956709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd73e95142122aff8caa967dc00ea46a79b9d7caa4fa8c36cd19353049f351d7`  
		Last Modified: Fri, 09 Aug 2024 17:45:19 GMT  
		Size: 24.2 MB (24152217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eb7472e89262a9d22769faa271e0c300b858d6607deb276b8ca7a4e4e3b59f`  
		Last Modified: Fri, 09 Aug 2024 17:45:17 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f555c703d4044c860bc7930d4bbe0906e21de4718336bcf6f01507eb1038db`  
		Last Modified: Fri, 09 Aug 2024 17:46:24 GMT  
		Size: 446.5 MB (446475402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-bullseye`

```console
$ docker pull haskell@sha256:76f045024b949c01aadc18a75430de171517a7ee42521a855cc8fb99d684f701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:b249e3c9bb6630e4afde592350b7e061cb0857ea3b6838ae1f21be7ad20930fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657469957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f1321f867c36deae5b01c2f23459db8932ab8412f27c84fd3a95ecc75f9dec`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:19:40 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:20:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:20:07 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:20:10 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:22:04 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:22:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:22:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75b0fdeafbb9aeaefe9ef7d1a65a592cdd314b40c2691bb70195683adf6bdf`  
		Last Modified: Fri, 09 Aug 2024 18:25:26 GMT  
		Size: 133.5 MB (133517024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413fbf9c62ffb025608142af38c18a9887e2d082b2f521ab49a8a82fc39a5c9c`  
		Last Modified: Fri, 09 Aug 2024 18:25:12 GMT  
		Size: 21.8 MB (21787165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d282b4bfd6f53fcb2278eaac3bab6665563fe191166a1cf5fdfe746afa74ec01`  
		Last Modified: Fri, 09 Aug 2024 18:25:10 GMT  
		Size: 8.0 MB (8004054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45fe090366505717409423f4073d51af743a646caad4baae760e0ee692b247f`  
		Last Modified: Fri, 09 Aug 2024 18:26:24 GMT  
		Size: 439.1 MB (439077136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6d91a487465ad3119956db03d669fec6e2ed2791c496d414918e674ce35b904
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.4 MB (663432585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9317913eebe3238d376e65ef199a64eec15861ebff3aab36c67581a94df48f60`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:39:33 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:39:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:40:00 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:40:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:40:01 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:40:03 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:42:09 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:42:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:42:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e063bbde2822160b94073c7f78bd03283c1c1061a2097599ed50ec0ac7dc4`  
		Last Modified: Fri, 09 Aug 2024 17:45:30 GMT  
		Size: 129.0 MB (128956709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd73e95142122aff8caa967dc00ea46a79b9d7caa4fa8c36cd19353049f351d7`  
		Last Modified: Fri, 09 Aug 2024 17:45:19 GMT  
		Size: 24.2 MB (24152217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eb7472e89262a9d22769faa271e0c300b858d6607deb276b8ca7a4e4e3b59f`  
		Last Modified: Fri, 09 Aug 2024 17:45:17 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f555c703d4044c860bc7930d4bbe0906e21de4718336bcf6f01507eb1038db`  
		Last Modified: Fri, 09 Aug 2024 17:46:24 GMT  
		Size: 446.5 MB (446475402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:1190eda9cebded656d239dd64838f62d53682ac29a73e5609daaefb5fafd5608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:c585499c3c56b194049b6de0467852f439eb78dc520b9bf5ac676bf11d5ec046
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606526478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cd87d1856d7bbc83f6b74f8ba1589f640516092d66774980839184eddbeca5`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:22:19 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:22:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:22:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:22:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:24:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:24:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:24:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6c5ef0c83e940ea8ac47bdf9b49015b0c1624823fbf78835110d528cc5f73`  
		Last Modified: Fri, 09 Aug 2024 18:26:55 GMT  
		Size: 106.2 MB (106233423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7e31582c41f348984f32faf302fede73cd3b18f93080e047be1b0036560de1`  
		Last Modified: Fri, 09 Aug 2024 18:26:44 GMT  
		Size: 21.8 MB (21787180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49965f76730a003b0900a294c870c7723abb9f8292df5ec69c6fff5e83b4150`  
		Last Modified: Fri, 09 Aug 2024 18:26:42 GMT  
		Size: 8.0 MB (8004059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9a4b221a8f8da67330a4639ee5507d49183c41c778bde7fa9a2e590ccf004a`  
		Last Modified: Fri, 09 Aug 2024 18:27:56 GMT  
		Size: 439.1 MB (439073486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:82ecddff03b38b21bf2ece6a2e22a0e7a38182bdc8241c02bddab8b1a12b4c24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.5 MB (612519706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6737a4f023bb53436dcf62da9fd4921e5f04fc93aeece3e97f4001812b1820be`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:42:26 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:42:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:42:47 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:42:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:44:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:44:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:44:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6db991b4b9c69d70836d73be5dc678feb8ec707994e2f477bda8b524056b1d`  
		Last Modified: Fri, 09 Aug 2024 17:46:51 GMT  
		Size: 101.7 MB (101696063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c29115546044fc1d3ca4337c9ba179ec6cd09ef92f531df832c68f6dce09dd`  
		Last Modified: Fri, 09 Aug 2024 17:46:43 GMT  
		Size: 24.2 MB (24152215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66fc49b8bcab6efeea5c0ad6543714013724cf78bdc7d05148f1ca2fd221b63`  
		Last Modified: Fri, 09 Aug 2024 17:46:41 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336824a5080379e691550929e893c80b62d96ecd6bb89e437c1a967c7beff0ec`  
		Last Modified: Fri, 09 Aug 2024 17:47:43 GMT  
		Size: 446.5 MB (446477075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim-bullseye`

```console
$ docker pull haskell@sha256:1190eda9cebded656d239dd64838f62d53682ac29a73e5609daaefb5fafd5608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:c585499c3c56b194049b6de0467852f439eb78dc520b9bf5ac676bf11d5ec046
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606526478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cd87d1856d7bbc83f6b74f8ba1589f640516092d66774980839184eddbeca5`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:22:19 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:22:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:22:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:22:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:24:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:24:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:24:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6c5ef0c83e940ea8ac47bdf9b49015b0c1624823fbf78835110d528cc5f73`  
		Last Modified: Fri, 09 Aug 2024 18:26:55 GMT  
		Size: 106.2 MB (106233423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7e31582c41f348984f32faf302fede73cd3b18f93080e047be1b0036560de1`  
		Last Modified: Fri, 09 Aug 2024 18:26:44 GMT  
		Size: 21.8 MB (21787180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49965f76730a003b0900a294c870c7723abb9f8292df5ec69c6fff5e83b4150`  
		Last Modified: Fri, 09 Aug 2024 18:26:42 GMT  
		Size: 8.0 MB (8004059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9a4b221a8f8da67330a4639ee5507d49183c41c778bde7fa9a2e590ccf004a`  
		Last Modified: Fri, 09 Aug 2024 18:27:56 GMT  
		Size: 439.1 MB (439073486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:82ecddff03b38b21bf2ece6a2e22a0e7a38182bdc8241c02bddab8b1a12b4c24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.5 MB (612519706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6737a4f023bb53436dcf62da9fd4921e5f04fc93aeece3e97f4001812b1820be`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:42:26 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:42:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:42:47 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:42:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:44:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:44:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:44:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6db991b4b9c69d70836d73be5dc678feb8ec707994e2f477bda8b524056b1d`  
		Last Modified: Fri, 09 Aug 2024 17:46:51 GMT  
		Size: 101.7 MB (101696063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c29115546044fc1d3ca4337c9ba179ec6cd09ef92f531df832c68f6dce09dd`  
		Last Modified: Fri, 09 Aug 2024 17:46:43 GMT  
		Size: 24.2 MB (24152215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66fc49b8bcab6efeea5c0ad6543714013724cf78bdc7d05148f1ca2fd221b63`  
		Last Modified: Fri, 09 Aug 2024 17:46:41 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336824a5080379e691550929e893c80b62d96ecd6bb89e437c1a967c7beff0ec`  
		Last Modified: Fri, 09 Aug 2024 17:47:43 GMT  
		Size: 446.5 MB (446477075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10-bullseye`

```console
$ docker pull haskell@sha256:76f045024b949c01aadc18a75430de171517a7ee42521a855cc8fb99d684f701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:b249e3c9bb6630e4afde592350b7e061cb0857ea3b6838ae1f21be7ad20930fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657469957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f1321f867c36deae5b01c2f23459db8932ab8412f27c84fd3a95ecc75f9dec`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:19:40 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:20:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:20:07 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:20:10 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:22:04 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:22:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:22:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75b0fdeafbb9aeaefe9ef7d1a65a592cdd314b40c2691bb70195683adf6bdf`  
		Last Modified: Fri, 09 Aug 2024 18:25:26 GMT  
		Size: 133.5 MB (133517024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413fbf9c62ffb025608142af38c18a9887e2d082b2f521ab49a8a82fc39a5c9c`  
		Last Modified: Fri, 09 Aug 2024 18:25:12 GMT  
		Size: 21.8 MB (21787165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d282b4bfd6f53fcb2278eaac3bab6665563fe191166a1cf5fdfe746afa74ec01`  
		Last Modified: Fri, 09 Aug 2024 18:25:10 GMT  
		Size: 8.0 MB (8004054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45fe090366505717409423f4073d51af743a646caad4baae760e0ee692b247f`  
		Last Modified: Fri, 09 Aug 2024 18:26:24 GMT  
		Size: 439.1 MB (439077136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6d91a487465ad3119956db03d669fec6e2ed2791c496d414918e674ce35b904
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.4 MB (663432585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9317913eebe3238d376e65ef199a64eec15861ebff3aab36c67581a94df48f60`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:39:33 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:39:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:40:00 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:40:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:40:01 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:40:03 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:42:09 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:42:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:42:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e063bbde2822160b94073c7f78bd03283c1c1061a2097599ed50ec0ac7dc4`  
		Last Modified: Fri, 09 Aug 2024 17:45:30 GMT  
		Size: 129.0 MB (128956709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd73e95142122aff8caa967dc00ea46a79b9d7caa4fa8c36cd19353049f351d7`  
		Last Modified: Fri, 09 Aug 2024 17:45:19 GMT  
		Size: 24.2 MB (24152217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eb7472e89262a9d22769faa271e0c300b858d6607deb276b8ca7a4e4e3b59f`  
		Last Modified: Fri, 09 Aug 2024 17:45:17 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f555c703d4044c860bc7930d4bbe0906e21de4718336bcf6f01507eb1038db`  
		Last Modified: Fri, 09 Aug 2024 17:46:24 GMT  
		Size: 446.5 MB (446475402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10-slim-bullseye`

```console
$ docker pull haskell@sha256:1190eda9cebded656d239dd64838f62d53682ac29a73e5609daaefb5fafd5608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:c585499c3c56b194049b6de0467852f439eb78dc520b9bf5ac676bf11d5ec046
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606526478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cd87d1856d7bbc83f6b74f8ba1589f640516092d66774980839184eddbeca5`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:22:19 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:22:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:22:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:22:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:24:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:24:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:24:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6c5ef0c83e940ea8ac47bdf9b49015b0c1624823fbf78835110d528cc5f73`  
		Last Modified: Fri, 09 Aug 2024 18:26:55 GMT  
		Size: 106.2 MB (106233423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7e31582c41f348984f32faf302fede73cd3b18f93080e047be1b0036560de1`  
		Last Modified: Fri, 09 Aug 2024 18:26:44 GMT  
		Size: 21.8 MB (21787180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49965f76730a003b0900a294c870c7723abb9f8292df5ec69c6fff5e83b4150`  
		Last Modified: Fri, 09 Aug 2024 18:26:42 GMT  
		Size: 8.0 MB (8004059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9a4b221a8f8da67330a4639ee5507d49183c41c778bde7fa9a2e590ccf004a`  
		Last Modified: Fri, 09 Aug 2024 18:27:56 GMT  
		Size: 439.1 MB (439073486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:82ecddff03b38b21bf2ece6a2e22a0e7a38182bdc8241c02bddab8b1a12b4c24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.5 MB (612519706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6737a4f023bb53436dcf62da9fd4921e5f04fc93aeece3e97f4001812b1820be`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:42:26 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:42:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:42:47 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:42:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:44:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:44:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:44:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6db991b4b9c69d70836d73be5dc678feb8ec707994e2f477bda8b524056b1d`  
		Last Modified: Fri, 09 Aug 2024 17:46:51 GMT  
		Size: 101.7 MB (101696063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c29115546044fc1d3ca4337c9ba179ec6cd09ef92f531df832c68f6dce09dd`  
		Last Modified: Fri, 09 Aug 2024 17:46:43 GMT  
		Size: 24.2 MB (24152215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66fc49b8bcab6efeea5c0ad6543714013724cf78bdc7d05148f1ca2fd221b63`  
		Last Modified: Fri, 09 Aug 2024 17:46:41 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336824a5080379e691550929e893c80b62d96ecd6bb89e437c1a967c7beff0ec`  
		Last Modified: Fri, 09 Aug 2024 17:47:43 GMT  
		Size: 446.5 MB (446477075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10.1-bullseye`

```console
$ docker pull haskell@sha256:76f045024b949c01aadc18a75430de171517a7ee42521a855cc8fb99d684f701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10.1-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:b249e3c9bb6630e4afde592350b7e061cb0857ea3b6838ae1f21be7ad20930fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657469957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f1321f867c36deae5b01c2f23459db8932ab8412f27c84fd3a95ecc75f9dec`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:19:40 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:20:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:20:07 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:20:10 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:22:04 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:22:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:22:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75b0fdeafbb9aeaefe9ef7d1a65a592cdd314b40c2691bb70195683adf6bdf`  
		Last Modified: Fri, 09 Aug 2024 18:25:26 GMT  
		Size: 133.5 MB (133517024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413fbf9c62ffb025608142af38c18a9887e2d082b2f521ab49a8a82fc39a5c9c`  
		Last Modified: Fri, 09 Aug 2024 18:25:12 GMT  
		Size: 21.8 MB (21787165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d282b4bfd6f53fcb2278eaac3bab6665563fe191166a1cf5fdfe746afa74ec01`  
		Last Modified: Fri, 09 Aug 2024 18:25:10 GMT  
		Size: 8.0 MB (8004054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45fe090366505717409423f4073d51af743a646caad4baae760e0ee692b247f`  
		Last Modified: Fri, 09 Aug 2024 18:26:24 GMT  
		Size: 439.1 MB (439077136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6d91a487465ad3119956db03d669fec6e2ed2791c496d414918e674ce35b904
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.4 MB (663432585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9317913eebe3238d376e65ef199a64eec15861ebff3aab36c67581a94df48f60`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:39:33 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:39:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:40:00 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:40:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:40:01 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:40:03 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:42:09 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:42:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:42:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e063bbde2822160b94073c7f78bd03283c1c1061a2097599ed50ec0ac7dc4`  
		Last Modified: Fri, 09 Aug 2024 17:45:30 GMT  
		Size: 129.0 MB (128956709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd73e95142122aff8caa967dc00ea46a79b9d7caa4fa8c36cd19353049f351d7`  
		Last Modified: Fri, 09 Aug 2024 17:45:19 GMT  
		Size: 24.2 MB (24152217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eb7472e89262a9d22769faa271e0c300b858d6607deb276b8ca7a4e4e3b59f`  
		Last Modified: Fri, 09 Aug 2024 17:45:17 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f555c703d4044c860bc7930d4bbe0906e21de4718336bcf6f01507eb1038db`  
		Last Modified: Fri, 09 Aug 2024 17:46:24 GMT  
		Size: 446.5 MB (446475402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10.1-slim-bullseye`

```console
$ docker pull haskell@sha256:1190eda9cebded656d239dd64838f62d53682ac29a73e5609daaefb5fafd5608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10.1-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:c585499c3c56b194049b6de0467852f439eb78dc520b9bf5ac676bf11d5ec046
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606526478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cd87d1856d7bbc83f6b74f8ba1589f640516092d66774980839184eddbeca5`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:22:19 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:22:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:22:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:22:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:24:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:24:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:24:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6c5ef0c83e940ea8ac47bdf9b49015b0c1624823fbf78835110d528cc5f73`  
		Last Modified: Fri, 09 Aug 2024 18:26:55 GMT  
		Size: 106.2 MB (106233423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7e31582c41f348984f32faf302fede73cd3b18f93080e047be1b0036560de1`  
		Last Modified: Fri, 09 Aug 2024 18:26:44 GMT  
		Size: 21.8 MB (21787180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49965f76730a003b0900a294c870c7723abb9f8292df5ec69c6fff5e83b4150`  
		Last Modified: Fri, 09 Aug 2024 18:26:42 GMT  
		Size: 8.0 MB (8004059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9a4b221a8f8da67330a4639ee5507d49183c41c778bde7fa9a2e590ccf004a`  
		Last Modified: Fri, 09 Aug 2024 18:27:56 GMT  
		Size: 439.1 MB (439073486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10.1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:82ecddff03b38b21bf2ece6a2e22a0e7a38182bdc8241c02bddab8b1a12b4c24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.5 MB (612519706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6737a4f023bb53436dcf62da9fd4921e5f04fc93aeece3e97f4001812b1820be`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:42:26 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:42:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:42:47 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:42:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:44:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:44:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:44:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6db991b4b9c69d70836d73be5dc678feb8ec707994e2f477bda8b524056b1d`  
		Last Modified: Fri, 09 Aug 2024 17:46:51 GMT  
		Size: 101.7 MB (101696063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c29115546044fc1d3ca4337c9ba179ec6cd09ef92f531df832c68f6dce09dd`  
		Last Modified: Fri, 09 Aug 2024 17:46:43 GMT  
		Size: 24.2 MB (24152215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66fc49b8bcab6efeea5c0ad6543714013724cf78bdc7d05148f1ca2fd221b63`  
		Last Modified: Fri, 09 Aug 2024 17:46:41 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336824a5080379e691550929e893c80b62d96ecd6bb89e437c1a967c7beff0ec`  
		Last Modified: Fri, 09 Aug 2024 17:47:43 GMT  
		Size: 446.5 MB (446477075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:bullseye`

```console
$ docker pull haskell@sha256:76f045024b949c01aadc18a75430de171517a7ee42521a855cc8fb99d684f701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:b249e3c9bb6630e4afde592350b7e061cb0857ea3b6838ae1f21be7ad20930fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657469957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f1321f867c36deae5b01c2f23459db8932ab8412f27c84fd3a95ecc75f9dec`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:19:40 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:20:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:20:07 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:20:10 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:22:04 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:22:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:22:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75b0fdeafbb9aeaefe9ef7d1a65a592cdd314b40c2691bb70195683adf6bdf`  
		Last Modified: Fri, 09 Aug 2024 18:25:26 GMT  
		Size: 133.5 MB (133517024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413fbf9c62ffb025608142af38c18a9887e2d082b2f521ab49a8a82fc39a5c9c`  
		Last Modified: Fri, 09 Aug 2024 18:25:12 GMT  
		Size: 21.8 MB (21787165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d282b4bfd6f53fcb2278eaac3bab6665563fe191166a1cf5fdfe746afa74ec01`  
		Last Modified: Fri, 09 Aug 2024 18:25:10 GMT  
		Size: 8.0 MB (8004054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45fe090366505717409423f4073d51af743a646caad4baae760e0ee692b247f`  
		Last Modified: Fri, 09 Aug 2024 18:26:24 GMT  
		Size: 439.1 MB (439077136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6d91a487465ad3119956db03d669fec6e2ed2791c496d414918e674ce35b904
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.4 MB (663432585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9317913eebe3238d376e65ef199a64eec15861ebff3aab36c67581a94df48f60`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:39:33 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:39:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:40:00 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:40:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:40:01 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:40:03 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:42:09 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:42:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:42:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e063bbde2822160b94073c7f78bd03283c1c1061a2097599ed50ec0ac7dc4`  
		Last Modified: Fri, 09 Aug 2024 17:45:30 GMT  
		Size: 129.0 MB (128956709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd73e95142122aff8caa967dc00ea46a79b9d7caa4fa8c36cd19353049f351d7`  
		Last Modified: Fri, 09 Aug 2024 17:45:19 GMT  
		Size: 24.2 MB (24152217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eb7472e89262a9d22769faa271e0c300b858d6607deb276b8ca7a4e4e3b59f`  
		Last Modified: Fri, 09 Aug 2024 17:45:17 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f555c703d4044c860bc7930d4bbe0906e21de4718336bcf6f01507eb1038db`  
		Last Modified: Fri, 09 Aug 2024 17:46:24 GMT  
		Size: 446.5 MB (446475402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:76f045024b949c01aadc18a75430de171517a7ee42521a855cc8fb99d684f701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:b249e3c9bb6630e4afde592350b7e061cb0857ea3b6838ae1f21be7ad20930fd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657469957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60f1321f867c36deae5b01c2f23459db8932ab8412f27c84fd3a95ecc75f9dec`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:25 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Tue, 23 Jul 2024 05:24:25 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:19:40 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:20:02 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:20:03 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:20:07 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:20:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:20:10 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:20:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:22:04 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:22:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:22:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a75b0fdeafbb9aeaefe9ef7d1a65a592cdd314b40c2691bb70195683adf6bdf`  
		Last Modified: Fri, 09 Aug 2024 18:25:26 GMT  
		Size: 133.5 MB (133517024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413fbf9c62ffb025608142af38c18a9887e2d082b2f521ab49a8a82fc39a5c9c`  
		Last Modified: Fri, 09 Aug 2024 18:25:12 GMT  
		Size: 21.8 MB (21787165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d282b4bfd6f53fcb2278eaac3bab6665563fe191166a1cf5fdfe746afa74ec01`  
		Last Modified: Fri, 09 Aug 2024 18:25:10 GMT  
		Size: 8.0 MB (8004054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b45fe090366505717409423f4073d51af743a646caad4baae760e0ee692b247f`  
		Last Modified: Fri, 09 Aug 2024 18:26:24 GMT  
		Size: 439.1 MB (439077136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c6d91a487465ad3119956db03d669fec6e2ed2791c496d414918e674ce35b904
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.4 MB (663432585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9317913eebe3238d376e65ef199a64eec15861ebff3aab36c67581a94df48f60`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:58 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Tue, 23 Jul 2024 04:17:59 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:39:33 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:39:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:39:55 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:40:00 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:40:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:40:01 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:40:03 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:40:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:42:09 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:42:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:42:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094e063bbde2822160b94073c7f78bd03283c1c1061a2097599ed50ec0ac7dc4`  
		Last Modified: Fri, 09 Aug 2024 17:45:30 GMT  
		Size: 129.0 MB (128956709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd73e95142122aff8caa967dc00ea46a79b9d7caa4fa8c36cd19353049f351d7`  
		Last Modified: Fri, 09 Aug 2024 17:45:19 GMT  
		Size: 24.2 MB (24152217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eb7472e89262a9d22769faa271e0c300b858d6607deb276b8ca7a4e4e3b59f`  
		Last Modified: Fri, 09 Aug 2024 17:45:17 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f555c703d4044c860bc7930d4bbe0906e21de4718336bcf6f01507eb1038db`  
		Last Modified: Fri, 09 Aug 2024 17:46:24 GMT  
		Size: 446.5 MB (446475402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim`

```console
$ docker pull haskell@sha256:1190eda9cebded656d239dd64838f62d53682ac29a73e5609daaefb5fafd5608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:c585499c3c56b194049b6de0467852f439eb78dc520b9bf5ac676bf11d5ec046
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606526478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cd87d1856d7bbc83f6b74f8ba1589f640516092d66774980839184eddbeca5`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:22:19 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:22:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:22:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:22:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:24:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:24:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:24:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6c5ef0c83e940ea8ac47bdf9b49015b0c1624823fbf78835110d528cc5f73`  
		Last Modified: Fri, 09 Aug 2024 18:26:55 GMT  
		Size: 106.2 MB (106233423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7e31582c41f348984f32faf302fede73cd3b18f93080e047be1b0036560de1`  
		Last Modified: Fri, 09 Aug 2024 18:26:44 GMT  
		Size: 21.8 MB (21787180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49965f76730a003b0900a294c870c7723abb9f8292df5ec69c6fff5e83b4150`  
		Last Modified: Fri, 09 Aug 2024 18:26:42 GMT  
		Size: 8.0 MB (8004059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9a4b221a8f8da67330a4639ee5507d49183c41c778bde7fa9a2e590ccf004a`  
		Last Modified: Fri, 09 Aug 2024 18:27:56 GMT  
		Size: 439.1 MB (439073486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:82ecddff03b38b21bf2ece6a2e22a0e7a38182bdc8241c02bddab8b1a12b4c24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.5 MB (612519706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6737a4f023bb53436dcf62da9fd4921e5f04fc93aeece3e97f4001812b1820be`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:42:26 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:42:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:42:47 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:42:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:44:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:44:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:44:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6db991b4b9c69d70836d73be5dc678feb8ec707994e2f477bda8b524056b1d`  
		Last Modified: Fri, 09 Aug 2024 17:46:51 GMT  
		Size: 101.7 MB (101696063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c29115546044fc1d3ca4337c9ba179ec6cd09ef92f531df832c68f6dce09dd`  
		Last Modified: Fri, 09 Aug 2024 17:46:43 GMT  
		Size: 24.2 MB (24152215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66fc49b8bcab6efeea5c0ad6543714013724cf78bdc7d05148f1ca2fd221b63`  
		Last Modified: Fri, 09 Aug 2024 17:46:41 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336824a5080379e691550929e893c80b62d96ecd6bb89e437c1a967c7beff0ec`  
		Last Modified: Fri, 09 Aug 2024 17:47:43 GMT  
		Size: 446.5 MB (446477075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim-bullseye`

```console
$ docker pull haskell@sha256:1190eda9cebded656d239dd64838f62d53682ac29a73e5609daaefb5fafd5608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:c585499c3c56b194049b6de0467852f439eb78dc520b9bf5ac676bf11d5ec046
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606526478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78cd87d1856d7bbc83f6b74f8ba1589f640516092d66774980839184eddbeca5`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 05:24:37 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Tue, 23 Jul 2024 05:24:38 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 18:22:19 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 18:22:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 18:22:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 18:22:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 18:22:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 18:22:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 18:22:47 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 18:24:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 18:24:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 18:24:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f6c5ef0c83e940ea8ac47bdf9b49015b0c1624823fbf78835110d528cc5f73`  
		Last Modified: Fri, 09 Aug 2024 18:26:55 GMT  
		Size: 106.2 MB (106233423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7e31582c41f348984f32faf302fede73cd3b18f93080e047be1b0036560de1`  
		Last Modified: Fri, 09 Aug 2024 18:26:44 GMT  
		Size: 21.8 MB (21787180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49965f76730a003b0900a294c870c7723abb9f8292df5ec69c6fff5e83b4150`  
		Last Modified: Fri, 09 Aug 2024 18:26:42 GMT  
		Size: 8.0 MB (8004059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9a4b221a8f8da67330a4639ee5507d49183c41c778bde7fa9a2e590ccf004a`  
		Last Modified: Fri, 09 Aug 2024 18:27:56 GMT  
		Size: 439.1 MB (439073486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:82ecddff03b38b21bf2ece6a2e22a0e7a38182bdc8241c02bddab8b1a12b4c24
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.5 MB (612519706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6737a4f023bb53436dcf62da9fd4921e5f04fc93aeece3e97f4001812b1820be`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Fri, 09 Aug 2024 17:42:26 GMT
ENV LANG=C.UTF-8
# Fri, 09 Aug 2024 17:42:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK=2.15.7
# Fri, 09 Aug 2024 17:42:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 09 Aug 2024 17:42:47 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 09 Aug 2024 17:42:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 09 Aug 2024 17:42:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC=9.10.1
# Fri, 09 Aug 2024 17:42:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 09 Aug 2024 17:44:42 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 09 Aug 2024 17:44:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Aug 2024 17:44:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6db991b4b9c69d70836d73be5dc678feb8ec707994e2f477bda8b524056b1d`  
		Last Modified: Fri, 09 Aug 2024 17:46:51 GMT  
		Size: 101.7 MB (101696063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c29115546044fc1d3ca4337c9ba179ec6cd09ef92f531df832c68f6dce09dd`  
		Last Modified: Fri, 09 Aug 2024 17:46:43 GMT  
		Size: 24.2 MB (24152215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e66fc49b8bcab6efeea5c0ad6543714013724cf78bdc7d05148f1ca2fd221b63`  
		Last Modified: Fri, 09 Aug 2024 17:46:41 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336824a5080379e691550929e893c80b62d96ecd6bb89e437c1a967c7beff0ec`  
		Last Modified: Fri, 09 Aug 2024 17:47:43 GMT  
		Size: 446.5 MB (446477075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
