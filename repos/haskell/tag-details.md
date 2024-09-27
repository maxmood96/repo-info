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
-	[`haskell:9.6`](#haskell96)
-	[`haskell:9.6-bullseye`](#haskell96-bullseye)
-	[`haskell:9.6-slim`](#haskell96-slim)
-	[`haskell:9.6-slim-bullseye`](#haskell96-slim-bullseye)
-	[`haskell:9.6.6`](#haskell966)
-	[`haskell:9.6.6-bullseye`](#haskell966-bullseye)
-	[`haskell:9.6.6-slim`](#haskell966-slim)
-	[`haskell:9.6.6-slim-bullseye`](#haskell966-slim-bullseye)
-	[`haskell:bullseye`](#haskellbullseye)
-	[`haskell:latest`](#haskelllatest)
-	[`haskell:slim`](#haskellslim)
-	[`haskell:slim-bullseye`](#haskellslim-bullseye)

## `haskell:9`

```console
$ docker pull haskell@sha256:ce32b18e6632c88e7cc8a6bc9794f7fe113f1d264bfa0afa2b09cb0d96205999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:fb29c7606018a77dc5c0c1d4ac42de3e6825f60792fb04a07ce29f49b637102a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.6 MB (657598673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae5faef0f33e1092e73a2289a962c65c3d0ba241bb634cf88e1530d654c1e8`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:52:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:52:51 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:52:51 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:52:52 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:52:54 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:54:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:54:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:54:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f5843f387f57f6777d24c4f557db58bdbd22e9967f0ff5c5e8d5a5ce528eac`  
		Last Modified: Fri, 27 Sep 2024 05:02:28 GMT  
		Size: 133.7 MB (133650612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ead6b6435258fab2fa2a7f938064be6f7ce00e94cf6bcd32cc41f14f44acb38`  
		Last Modified: Fri, 27 Sep 2024 05:02:14 GMT  
		Size: 21.8 MB (21787178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940bd95f92241cad88e341b6110d7527c3da3b0c8ca2a8ae619d5beb2510137`  
		Last Modified: Fri, 27 Sep 2024 05:02:12 GMT  
		Size: 8.0 MB (8004053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8f8983e4c9592ca9fa443ce6556e8111298891dc4b6ab9c6911793c6665685`  
		Last Modified: Fri, 27 Sep 2024 05:03:27 GMT  
		Size: 439.1 MB (439075439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fca3c9d0707ebb820875d8ef2c2a3050c1cb32bb7f629159915acfb293520540
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.6 MB (663605182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e17fb6a75abeab897ec3a7e5a1213b43a817156eaa4037f48bde70c2b1addf`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:02:30 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:02:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:02:50 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:02:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:02:55 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:02:57 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:04:56 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:05:09 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:05:09 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac14519460f6aeee1cf11e3dbd8aebc1dcdea50c13319f9ff02f648f1fd740`  
		Last Modified: Fri, 27 Sep 2024 05:12:26 GMT  
		Size: 129.1 MB (129124944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426810c71c4327fd5994e8c2f0d0ac9bfa50f9b1c031b64e6a6ac5610faa529c`  
		Last Modified: Fri, 27 Sep 2024 05:12:14 GMT  
		Size: 24.2 MB (24152211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5757b580d898c36f1ffcbbf038034341302aa7b60c5720cd1111b4d13f102e7`  
		Last Modified: Fri, 27 Sep 2024 05:12:13 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8a227d00ea335cdd832eeb24c1babe4f5686947e7e24585cd0c4d28b206496`  
		Last Modified: Fri, 27 Sep 2024 05:13:21 GMT  
		Size: 446.5 MB (446475893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-bullseye`

```console
$ docker pull haskell@sha256:ce32b18e6632c88e7cc8a6bc9794f7fe113f1d264bfa0afa2b09cb0d96205999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:fb29c7606018a77dc5c0c1d4ac42de3e6825f60792fb04a07ce29f49b637102a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.6 MB (657598673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae5faef0f33e1092e73a2289a962c65c3d0ba241bb634cf88e1530d654c1e8`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:52:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:52:51 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:52:51 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:52:52 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:52:54 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:54:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:54:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:54:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f5843f387f57f6777d24c4f557db58bdbd22e9967f0ff5c5e8d5a5ce528eac`  
		Last Modified: Fri, 27 Sep 2024 05:02:28 GMT  
		Size: 133.7 MB (133650612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ead6b6435258fab2fa2a7f938064be6f7ce00e94cf6bcd32cc41f14f44acb38`  
		Last Modified: Fri, 27 Sep 2024 05:02:14 GMT  
		Size: 21.8 MB (21787178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940bd95f92241cad88e341b6110d7527c3da3b0c8ca2a8ae619d5beb2510137`  
		Last Modified: Fri, 27 Sep 2024 05:02:12 GMT  
		Size: 8.0 MB (8004053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8f8983e4c9592ca9fa443ce6556e8111298891dc4b6ab9c6911793c6665685`  
		Last Modified: Fri, 27 Sep 2024 05:03:27 GMT  
		Size: 439.1 MB (439075439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fca3c9d0707ebb820875d8ef2c2a3050c1cb32bb7f629159915acfb293520540
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.6 MB (663605182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e17fb6a75abeab897ec3a7e5a1213b43a817156eaa4037f48bde70c2b1addf`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:02:30 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:02:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:02:50 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:02:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:02:55 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:02:57 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:04:56 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:05:09 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:05:09 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac14519460f6aeee1cf11e3dbd8aebc1dcdea50c13319f9ff02f648f1fd740`  
		Last Modified: Fri, 27 Sep 2024 05:12:26 GMT  
		Size: 129.1 MB (129124944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426810c71c4327fd5994e8c2f0d0ac9bfa50f9b1c031b64e6a6ac5610faa529c`  
		Last Modified: Fri, 27 Sep 2024 05:12:14 GMT  
		Size: 24.2 MB (24152211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5757b580d898c36f1ffcbbf038034341302aa7b60c5720cd1111b4d13f102e7`  
		Last Modified: Fri, 27 Sep 2024 05:12:13 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8a227d00ea335cdd832eeb24c1babe4f5686947e7e24585cd0c4d28b206496`  
		Last Modified: Fri, 27 Sep 2024 05:13:21 GMT  
		Size: 446.5 MB (446475893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:345e44e48cc55ad24dbc5ece5a07a68dc2bb3934ef65c983a197ec125347bb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:5bed54236eb27f560768d786d577bcd6223faa66bf331199215593036c522cf7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.7 MB (606666993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887cc905f0ab30764b21351acdcb5208f535a2dd6496782eec3579747850e012`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:55:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:55:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:55:27 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:55:30 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:57:29 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:57:38 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:57:38 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4245851650f9e4807c8be2c401467280707ac3062ec457080c43e56f02113`  
		Last Modified: Fri, 27 Sep 2024 05:03:57 GMT  
		Size: 106.4 MB (106364856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3afccb50c76122edb47d85d04e1183c7293a9f1283c764093750331cb6bdcb7`  
		Last Modified: Fri, 27 Sep 2024 05:03:46 GMT  
		Size: 21.8 MB (21787158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ef6d5c5e7643717a714595ecdf3194398742a95ed9a628595d3b0ddbadb24c`  
		Last Modified: Fri, 27 Sep 2024 05:03:44 GMT  
		Size: 8.0 MB (8004055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe6cfc0abe0e26b662cd1ddb441e88750a5e4866eea530060ff6428c1b042ca`  
		Last Modified: Fri, 27 Sep 2024 05:04:58 GMT  
		Size: 439.1 MB (439082325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a9abe2be4fafbef93cec98290689750d90b255918d8e412c1a0a74940fa7f276
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.7 MB (612676788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3113aee132ea737150aae8db4360d32b04a1cc189bc159489603225eb625218f`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:05:22 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:05:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:05:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:05:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:07:34 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:07:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:07:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b2ab68b28e6ef33b48bde65f6282b649027a6efd43f6c0ad6e0492c9540809`  
		Last Modified: Fri, 27 Sep 2024 05:13:47 GMT  
		Size: 101.9 MB (101852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ff235fab3eb8bc0cb5466deb71f17e3b45ce5b30dd85ee353397fa5b4740e5`  
		Last Modified: Fri, 27 Sep 2024 05:13:38 GMT  
		Size: 24.2 MB (24152199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c86239d91041fdf1ae6f460f763662091472cd4e8094d6b6cc2c428e3c1368`  
		Last Modified: Fri, 27 Sep 2024 05:13:37 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8edc6cddf1140cdfb9bc3f1b3d044980e2e483e2b7acd9a92ae056bc475dbc`  
		Last Modified: Fri, 27 Sep 2024 05:14:45 GMT  
		Size: 446.5 MB (446478613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim-bullseye`

```console
$ docker pull haskell@sha256:345e44e48cc55ad24dbc5ece5a07a68dc2bb3934ef65c983a197ec125347bb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:5bed54236eb27f560768d786d577bcd6223faa66bf331199215593036c522cf7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.7 MB (606666993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887cc905f0ab30764b21351acdcb5208f535a2dd6496782eec3579747850e012`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:55:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:55:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:55:27 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:55:30 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:57:29 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:57:38 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:57:38 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4245851650f9e4807c8be2c401467280707ac3062ec457080c43e56f02113`  
		Last Modified: Fri, 27 Sep 2024 05:03:57 GMT  
		Size: 106.4 MB (106364856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3afccb50c76122edb47d85d04e1183c7293a9f1283c764093750331cb6bdcb7`  
		Last Modified: Fri, 27 Sep 2024 05:03:46 GMT  
		Size: 21.8 MB (21787158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ef6d5c5e7643717a714595ecdf3194398742a95ed9a628595d3b0ddbadb24c`  
		Last Modified: Fri, 27 Sep 2024 05:03:44 GMT  
		Size: 8.0 MB (8004055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe6cfc0abe0e26b662cd1ddb441e88750a5e4866eea530060ff6428c1b042ca`  
		Last Modified: Fri, 27 Sep 2024 05:04:58 GMT  
		Size: 439.1 MB (439082325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a9abe2be4fafbef93cec98290689750d90b255918d8e412c1a0a74940fa7f276
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.7 MB (612676788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3113aee132ea737150aae8db4360d32b04a1cc189bc159489603225eb625218f`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:05:22 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:05:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:05:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:05:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:07:34 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:07:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:07:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b2ab68b28e6ef33b48bde65f6282b649027a6efd43f6c0ad6e0492c9540809`  
		Last Modified: Fri, 27 Sep 2024 05:13:47 GMT  
		Size: 101.9 MB (101852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ff235fab3eb8bc0cb5466deb71f17e3b45ce5b30dd85ee353397fa5b4740e5`  
		Last Modified: Fri, 27 Sep 2024 05:13:38 GMT  
		Size: 24.2 MB (24152199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c86239d91041fdf1ae6f460f763662091472cd4e8094d6b6cc2c428e3c1368`  
		Last Modified: Fri, 27 Sep 2024 05:13:37 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8edc6cddf1140cdfb9bc3f1b3d044980e2e483e2b7acd9a92ae056bc475dbc`  
		Last Modified: Fri, 27 Sep 2024 05:14:45 GMT  
		Size: 446.5 MB (446478613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10-bullseye`

```console
$ docker pull haskell@sha256:ce32b18e6632c88e7cc8a6bc9794f7fe113f1d264bfa0afa2b09cb0d96205999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:fb29c7606018a77dc5c0c1d4ac42de3e6825f60792fb04a07ce29f49b637102a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.6 MB (657598673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae5faef0f33e1092e73a2289a962c65c3d0ba241bb634cf88e1530d654c1e8`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:52:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:52:51 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:52:51 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:52:52 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:52:54 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:54:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:54:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:54:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f5843f387f57f6777d24c4f557db58bdbd22e9967f0ff5c5e8d5a5ce528eac`  
		Last Modified: Fri, 27 Sep 2024 05:02:28 GMT  
		Size: 133.7 MB (133650612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ead6b6435258fab2fa2a7f938064be6f7ce00e94cf6bcd32cc41f14f44acb38`  
		Last Modified: Fri, 27 Sep 2024 05:02:14 GMT  
		Size: 21.8 MB (21787178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940bd95f92241cad88e341b6110d7527c3da3b0c8ca2a8ae619d5beb2510137`  
		Last Modified: Fri, 27 Sep 2024 05:02:12 GMT  
		Size: 8.0 MB (8004053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8f8983e4c9592ca9fa443ce6556e8111298891dc4b6ab9c6911793c6665685`  
		Last Modified: Fri, 27 Sep 2024 05:03:27 GMT  
		Size: 439.1 MB (439075439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fca3c9d0707ebb820875d8ef2c2a3050c1cb32bb7f629159915acfb293520540
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.6 MB (663605182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e17fb6a75abeab897ec3a7e5a1213b43a817156eaa4037f48bde70c2b1addf`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:02:30 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:02:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:02:50 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:02:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:02:55 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:02:57 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:04:56 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:05:09 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:05:09 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac14519460f6aeee1cf11e3dbd8aebc1dcdea50c13319f9ff02f648f1fd740`  
		Last Modified: Fri, 27 Sep 2024 05:12:26 GMT  
		Size: 129.1 MB (129124944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426810c71c4327fd5994e8c2f0d0ac9bfa50f9b1c031b64e6a6ac5610faa529c`  
		Last Modified: Fri, 27 Sep 2024 05:12:14 GMT  
		Size: 24.2 MB (24152211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5757b580d898c36f1ffcbbf038034341302aa7b60c5720cd1111b4d13f102e7`  
		Last Modified: Fri, 27 Sep 2024 05:12:13 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8a227d00ea335cdd832eeb24c1babe4f5686947e7e24585cd0c4d28b206496`  
		Last Modified: Fri, 27 Sep 2024 05:13:21 GMT  
		Size: 446.5 MB (446475893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10-slim-bullseye`

```console
$ docker pull haskell@sha256:345e44e48cc55ad24dbc5ece5a07a68dc2bb3934ef65c983a197ec125347bb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:5bed54236eb27f560768d786d577bcd6223faa66bf331199215593036c522cf7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.7 MB (606666993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887cc905f0ab30764b21351acdcb5208f535a2dd6496782eec3579747850e012`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:55:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:55:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:55:27 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:55:30 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:57:29 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:57:38 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:57:38 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4245851650f9e4807c8be2c401467280707ac3062ec457080c43e56f02113`  
		Last Modified: Fri, 27 Sep 2024 05:03:57 GMT  
		Size: 106.4 MB (106364856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3afccb50c76122edb47d85d04e1183c7293a9f1283c764093750331cb6bdcb7`  
		Last Modified: Fri, 27 Sep 2024 05:03:46 GMT  
		Size: 21.8 MB (21787158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ef6d5c5e7643717a714595ecdf3194398742a95ed9a628595d3b0ddbadb24c`  
		Last Modified: Fri, 27 Sep 2024 05:03:44 GMT  
		Size: 8.0 MB (8004055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe6cfc0abe0e26b662cd1ddb441e88750a5e4866eea530060ff6428c1b042ca`  
		Last Modified: Fri, 27 Sep 2024 05:04:58 GMT  
		Size: 439.1 MB (439082325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a9abe2be4fafbef93cec98290689750d90b255918d8e412c1a0a74940fa7f276
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.7 MB (612676788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3113aee132ea737150aae8db4360d32b04a1cc189bc159489603225eb625218f`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:05:22 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:05:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:05:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:05:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:07:34 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:07:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:07:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b2ab68b28e6ef33b48bde65f6282b649027a6efd43f6c0ad6e0492c9540809`  
		Last Modified: Fri, 27 Sep 2024 05:13:47 GMT  
		Size: 101.9 MB (101852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ff235fab3eb8bc0cb5466deb71f17e3b45ce5b30dd85ee353397fa5b4740e5`  
		Last Modified: Fri, 27 Sep 2024 05:13:38 GMT  
		Size: 24.2 MB (24152199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c86239d91041fdf1ae6f460f763662091472cd4e8094d6b6cc2c428e3c1368`  
		Last Modified: Fri, 27 Sep 2024 05:13:37 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8edc6cddf1140cdfb9bc3f1b3d044980e2e483e2b7acd9a92ae056bc475dbc`  
		Last Modified: Fri, 27 Sep 2024 05:14:45 GMT  
		Size: 446.5 MB (446478613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10.1-bullseye`

```console
$ docker pull haskell@sha256:ce32b18e6632c88e7cc8a6bc9794f7fe113f1d264bfa0afa2b09cb0d96205999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10.1-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:fb29c7606018a77dc5c0c1d4ac42de3e6825f60792fb04a07ce29f49b637102a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.6 MB (657598673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae5faef0f33e1092e73a2289a962c65c3d0ba241bb634cf88e1530d654c1e8`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:52:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:52:51 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:52:51 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:52:52 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:52:54 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:54:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:54:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:54:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f5843f387f57f6777d24c4f557db58bdbd22e9967f0ff5c5e8d5a5ce528eac`  
		Last Modified: Fri, 27 Sep 2024 05:02:28 GMT  
		Size: 133.7 MB (133650612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ead6b6435258fab2fa2a7f938064be6f7ce00e94cf6bcd32cc41f14f44acb38`  
		Last Modified: Fri, 27 Sep 2024 05:02:14 GMT  
		Size: 21.8 MB (21787178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940bd95f92241cad88e341b6110d7527c3da3b0c8ca2a8ae619d5beb2510137`  
		Last Modified: Fri, 27 Sep 2024 05:02:12 GMT  
		Size: 8.0 MB (8004053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8f8983e4c9592ca9fa443ce6556e8111298891dc4b6ab9c6911793c6665685`  
		Last Modified: Fri, 27 Sep 2024 05:03:27 GMT  
		Size: 439.1 MB (439075439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fca3c9d0707ebb820875d8ef2c2a3050c1cb32bb7f629159915acfb293520540
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.6 MB (663605182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e17fb6a75abeab897ec3a7e5a1213b43a817156eaa4037f48bde70c2b1addf`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:02:30 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:02:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:02:50 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:02:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:02:55 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:02:57 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:04:56 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:05:09 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:05:09 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac14519460f6aeee1cf11e3dbd8aebc1dcdea50c13319f9ff02f648f1fd740`  
		Last Modified: Fri, 27 Sep 2024 05:12:26 GMT  
		Size: 129.1 MB (129124944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426810c71c4327fd5994e8c2f0d0ac9bfa50f9b1c031b64e6a6ac5610faa529c`  
		Last Modified: Fri, 27 Sep 2024 05:12:14 GMT  
		Size: 24.2 MB (24152211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5757b580d898c36f1ffcbbf038034341302aa7b60c5720cd1111b4d13f102e7`  
		Last Modified: Fri, 27 Sep 2024 05:12:13 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8a227d00ea335cdd832eeb24c1babe4f5686947e7e24585cd0c4d28b206496`  
		Last Modified: Fri, 27 Sep 2024 05:13:21 GMT  
		Size: 446.5 MB (446475893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10.1-slim-bullseye`

```console
$ docker pull haskell@sha256:345e44e48cc55ad24dbc5ece5a07a68dc2bb3934ef65c983a197ec125347bb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10.1-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:5bed54236eb27f560768d786d577bcd6223faa66bf331199215593036c522cf7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.7 MB (606666993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887cc905f0ab30764b21351acdcb5208f535a2dd6496782eec3579747850e012`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:55:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:55:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:55:27 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:55:30 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:57:29 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:57:38 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:57:38 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4245851650f9e4807c8be2c401467280707ac3062ec457080c43e56f02113`  
		Last Modified: Fri, 27 Sep 2024 05:03:57 GMT  
		Size: 106.4 MB (106364856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3afccb50c76122edb47d85d04e1183c7293a9f1283c764093750331cb6bdcb7`  
		Last Modified: Fri, 27 Sep 2024 05:03:46 GMT  
		Size: 21.8 MB (21787158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ef6d5c5e7643717a714595ecdf3194398742a95ed9a628595d3b0ddbadb24c`  
		Last Modified: Fri, 27 Sep 2024 05:03:44 GMT  
		Size: 8.0 MB (8004055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe6cfc0abe0e26b662cd1ddb441e88750a5e4866eea530060ff6428c1b042ca`  
		Last Modified: Fri, 27 Sep 2024 05:04:58 GMT  
		Size: 439.1 MB (439082325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10.1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a9abe2be4fafbef93cec98290689750d90b255918d8e412c1a0a74940fa7f276
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.7 MB (612676788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3113aee132ea737150aae8db4360d32b04a1cc189bc159489603225eb625218f`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:05:22 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:05:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:05:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:05:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:07:34 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:07:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:07:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b2ab68b28e6ef33b48bde65f6282b649027a6efd43f6c0ad6e0492c9540809`  
		Last Modified: Fri, 27 Sep 2024 05:13:47 GMT  
		Size: 101.9 MB (101852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ff235fab3eb8bc0cb5466deb71f17e3b45ce5b30dd85ee353397fa5b4740e5`  
		Last Modified: Fri, 27 Sep 2024 05:13:38 GMT  
		Size: 24.2 MB (24152199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c86239d91041fdf1ae6f460f763662091472cd4e8094d6b6cc2c428e3c1368`  
		Last Modified: Fri, 27 Sep 2024 05:13:37 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8edc6cddf1140cdfb9bc3f1b3d044980e2e483e2b7acd9a92ae056bc475dbc`  
		Last Modified: Fri, 27 Sep 2024 05:14:45 GMT  
		Size: 446.5 MB (446478613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6`

```console
$ docker pull haskell@sha256:ff87472c659a8e381e4a54b1da445c74fe2ac5aab0ce2935cafc2fa4d79cff52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6` - linux; amd64

```console
$ docker pull haskell@sha256:55688aa378c8e79d14f38ec5c2705c42937bfd65b5e8b652f742325d4f9f69a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.3 MB (635349067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a903988fe07128415f9c7247fb968e48b4ebe28b6f92a90ddd64ffe30d41bdf6`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:52:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:57:42 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 04:57:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:57:46 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:57:47 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:57:47 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:57:49 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:57:49 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 04:57:49 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 04:59:34 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:59:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:59:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f5843f387f57f6777d24c4f557db58bdbd22e9967f0ff5c5e8d5a5ce528eac`  
		Last Modified: Fri, 27 Sep 2024 05:02:28 GMT  
		Size: 133.7 MB (133650612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8baec99a4c31d49b250a24e45d24aacc2fe5cdfa9a3798be37ca8868a787826`  
		Last Modified: Fri, 27 Sep 2024 05:05:17 GMT  
		Size: 21.4 MB (21443349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44dafce3bcb5825ad89ebf0584fc52545428e437b43292fc2b6ab939747a9aa`  
		Last Modified: Fri, 27 Sep 2024 05:05:15 GMT  
		Size: 8.0 MB (8004054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2567065a0f83d2ab372cf646e725fb4429e4becc558982a5e357304801cfe0af`  
		Last Modified: Fri, 27 Sep 2024 05:06:25 GMT  
		Size: 417.2 MB (417169661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b7a69b6b04d913dc9e9fd224927a0983dc54a9c28d3138804aad97324ea57b17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647871425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398c513837f84a92ae93b48024c44712e577cb8e031d5de5e5ceebff6168949f`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:02:30 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:02:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:00 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 05:08:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:08:05 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:08:05 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:08:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:08:07 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:08:07 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 05:08:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:09:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:10:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:10:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac14519460f6aeee1cf11e3dbd8aebc1dcdea50c13319f9ff02f648f1fd740`  
		Last Modified: Fri, 27 Sep 2024 05:12:26 GMT  
		Size: 129.1 MB (129124944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f470e04b4265d2ba8ff4d626c904c3e1b0b61fa56489d6114aa0d957a0126e5`  
		Last Modified: Fri, 27 Sep 2024 05:15:02 GMT  
		Size: 23.7 MB (23749360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c72e61443c05b575be756d581ee18d99c0cb05d4b54fdae38e875b61a959fac`  
		Last Modified: Fri, 27 Sep 2024 05:15:01 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2808a38c02a904bb9acd7a1a9fa12fe4163eb6272bbd74c21f2896608f5a09b`  
		Last Modified: Fri, 27 Sep 2024 05:16:06 GMT  
		Size: 431.1 MB (431144987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-bullseye`

```console
$ docker pull haskell@sha256:ff87472c659a8e381e4a54b1da445c74fe2ac5aab0ce2935cafc2fa4d79cff52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:55688aa378c8e79d14f38ec5c2705c42937bfd65b5e8b652f742325d4f9f69a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.3 MB (635349067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a903988fe07128415f9c7247fb968e48b4ebe28b6f92a90ddd64ffe30d41bdf6`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:52:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:57:42 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 04:57:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:57:46 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:57:47 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:57:47 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:57:49 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:57:49 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 04:57:49 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 04:59:34 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:59:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:59:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f5843f387f57f6777d24c4f557db58bdbd22e9967f0ff5c5e8d5a5ce528eac`  
		Last Modified: Fri, 27 Sep 2024 05:02:28 GMT  
		Size: 133.7 MB (133650612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8baec99a4c31d49b250a24e45d24aacc2fe5cdfa9a3798be37ca8868a787826`  
		Last Modified: Fri, 27 Sep 2024 05:05:17 GMT  
		Size: 21.4 MB (21443349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44dafce3bcb5825ad89ebf0584fc52545428e437b43292fc2b6ab939747a9aa`  
		Last Modified: Fri, 27 Sep 2024 05:05:15 GMT  
		Size: 8.0 MB (8004054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2567065a0f83d2ab372cf646e725fb4429e4becc558982a5e357304801cfe0af`  
		Last Modified: Fri, 27 Sep 2024 05:06:25 GMT  
		Size: 417.2 MB (417169661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b7a69b6b04d913dc9e9fd224927a0983dc54a9c28d3138804aad97324ea57b17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647871425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398c513837f84a92ae93b48024c44712e577cb8e031d5de5e5ceebff6168949f`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:02:30 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:02:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:00 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 05:08:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:08:05 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:08:05 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:08:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:08:07 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:08:07 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 05:08:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:09:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:10:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:10:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac14519460f6aeee1cf11e3dbd8aebc1dcdea50c13319f9ff02f648f1fd740`  
		Last Modified: Fri, 27 Sep 2024 05:12:26 GMT  
		Size: 129.1 MB (129124944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f470e04b4265d2ba8ff4d626c904c3e1b0b61fa56489d6114aa0d957a0126e5`  
		Last Modified: Fri, 27 Sep 2024 05:15:02 GMT  
		Size: 23.7 MB (23749360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c72e61443c05b575be756d581ee18d99c0cb05d4b54fdae38e875b61a959fac`  
		Last Modified: Fri, 27 Sep 2024 05:15:01 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2808a38c02a904bb9acd7a1a9fa12fe4163eb6272bbd74c21f2896608f5a09b`  
		Last Modified: Fri, 27 Sep 2024 05:16:06 GMT  
		Size: 431.1 MB (431144987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-slim`

```console
$ docker pull haskell@sha256:71c6097bfa2ae58f3d745097eafa4356d3186903055c6810302c40b928d4f061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:9b74f66c4a1ce6f3a3054eb03958559ed601fda80eadf7c4d3300d5a2137b170
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446617847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e909ca4e6a4697f8e8b733047b7fd5010dd5e91d5ea2a61ea81df2fb6a44d0c5`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:55:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:55:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:59:51 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 04:59:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:59:54 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:59:55 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:59:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:59:57 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:59:57 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 04:59:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:01:39 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:01:45 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:01:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4245851650f9e4807c8be2c401467280707ac3062ec457080c43e56f02113`  
		Last Modified: Fri, 27 Sep 2024 05:03:57 GMT  
		Size: 106.4 MB (106364856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd2dc5e0505900f5c66ae11b065cc9cae53ae159e957a6c78aee31b8500e6a4`  
		Last Modified: Fri, 27 Sep 2024 05:06:40 GMT  
		Size: 21.4 MB (21443348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf70e1a888ea9e17ccc5adbe5d1e32fb1e9d7018edbcdd21b817dfb4a49d991e`  
		Last Modified: Fri, 27 Sep 2024 05:06:38 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc7317b1edf8b83f52af61da79b56db4d9efbedc0ea280da6adc313b6e94e7e`  
		Last Modified: Fri, 27 Sep 2024 05:07:23 GMT  
		Size: 279.4 MB (279376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:cf2150c3ab37ec35e12a18ff811bd7eddeaaf3e99541b6ad309fffc612fd1790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455529932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ecc7063e7a888960d5b6b812fb2dcad35a6ebf1138cc2605b686a06993b586`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:05:22 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:05:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:10:08 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 05:10:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:10:12 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:10:12 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:10:12 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:10:14 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:10:14 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 05:10:14 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:11:47 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:11:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:11:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b2ab68b28e6ef33b48bde65f6282b649027a6efd43f6c0ad6e0492c9540809`  
		Last Modified: Fri, 27 Sep 2024 05:13:47 GMT  
		Size: 101.9 MB (101852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d210823e86bf393f2115294bf0489052ecc4e33cb5c2c4ff93335e902466630`  
		Last Modified: Fri, 27 Sep 2024 05:16:20 GMT  
		Size: 23.7 MB (23749360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9aed38395a35dfcd8bb6c1d3220bef3e66ddd25deb181382a455f5e6051de7`  
		Last Modified: Fri, 27 Sep 2024 05:16:19 GMT  
		Size: 10.1 MB (10118267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fad95f153123630ad265b659e919385a7c8f63a1b6d4f9bd49ea643844df07a`  
		Last Modified: Fri, 27 Sep 2024 05:17:00 GMT  
		Size: 289.7 MB (289734599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-slim-bullseye`

```console
$ docker pull haskell@sha256:71c6097bfa2ae58f3d745097eafa4356d3186903055c6810302c40b928d4f061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:9b74f66c4a1ce6f3a3054eb03958559ed601fda80eadf7c4d3300d5a2137b170
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446617847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e909ca4e6a4697f8e8b733047b7fd5010dd5e91d5ea2a61ea81df2fb6a44d0c5`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:55:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:55:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:59:51 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 04:59:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:59:54 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:59:55 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:59:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:59:57 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:59:57 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 04:59:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:01:39 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:01:45 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:01:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4245851650f9e4807c8be2c401467280707ac3062ec457080c43e56f02113`  
		Last Modified: Fri, 27 Sep 2024 05:03:57 GMT  
		Size: 106.4 MB (106364856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd2dc5e0505900f5c66ae11b065cc9cae53ae159e957a6c78aee31b8500e6a4`  
		Last Modified: Fri, 27 Sep 2024 05:06:40 GMT  
		Size: 21.4 MB (21443348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf70e1a888ea9e17ccc5adbe5d1e32fb1e9d7018edbcdd21b817dfb4a49d991e`  
		Last Modified: Fri, 27 Sep 2024 05:06:38 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc7317b1edf8b83f52af61da79b56db4d9efbedc0ea280da6adc313b6e94e7e`  
		Last Modified: Fri, 27 Sep 2024 05:07:23 GMT  
		Size: 279.4 MB (279376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:cf2150c3ab37ec35e12a18ff811bd7eddeaaf3e99541b6ad309fffc612fd1790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455529932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ecc7063e7a888960d5b6b812fb2dcad35a6ebf1138cc2605b686a06993b586`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:05:22 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:05:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:10:08 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 05:10:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:10:12 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:10:12 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:10:12 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:10:14 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:10:14 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 05:10:14 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:11:47 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:11:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:11:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b2ab68b28e6ef33b48bde65f6282b649027a6efd43f6c0ad6e0492c9540809`  
		Last Modified: Fri, 27 Sep 2024 05:13:47 GMT  
		Size: 101.9 MB (101852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d210823e86bf393f2115294bf0489052ecc4e33cb5c2c4ff93335e902466630`  
		Last Modified: Fri, 27 Sep 2024 05:16:20 GMT  
		Size: 23.7 MB (23749360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9aed38395a35dfcd8bb6c1d3220bef3e66ddd25deb181382a455f5e6051de7`  
		Last Modified: Fri, 27 Sep 2024 05:16:19 GMT  
		Size: 10.1 MB (10118267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fad95f153123630ad265b659e919385a7c8f63a1b6d4f9bd49ea643844df07a`  
		Last Modified: Fri, 27 Sep 2024 05:17:00 GMT  
		Size: 289.7 MB (289734599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.6`

```console
$ docker pull haskell@sha256:ff87472c659a8e381e4a54b1da445c74fe2ac5aab0ce2935cafc2fa4d79cff52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.6` - linux; amd64

```console
$ docker pull haskell@sha256:55688aa378c8e79d14f38ec5c2705c42937bfd65b5e8b652f742325d4f9f69a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.3 MB (635349067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a903988fe07128415f9c7247fb968e48b4ebe28b6f92a90ddd64ffe30d41bdf6`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:52:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:57:42 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 04:57:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:57:46 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:57:47 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:57:47 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:57:49 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:57:49 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 04:57:49 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 04:59:34 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:59:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:59:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f5843f387f57f6777d24c4f557db58bdbd22e9967f0ff5c5e8d5a5ce528eac`  
		Last Modified: Fri, 27 Sep 2024 05:02:28 GMT  
		Size: 133.7 MB (133650612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8baec99a4c31d49b250a24e45d24aacc2fe5cdfa9a3798be37ca8868a787826`  
		Last Modified: Fri, 27 Sep 2024 05:05:17 GMT  
		Size: 21.4 MB (21443349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44dafce3bcb5825ad89ebf0584fc52545428e437b43292fc2b6ab939747a9aa`  
		Last Modified: Fri, 27 Sep 2024 05:05:15 GMT  
		Size: 8.0 MB (8004054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2567065a0f83d2ab372cf646e725fb4429e4becc558982a5e357304801cfe0af`  
		Last Modified: Fri, 27 Sep 2024 05:06:25 GMT  
		Size: 417.2 MB (417169661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b7a69b6b04d913dc9e9fd224927a0983dc54a9c28d3138804aad97324ea57b17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647871425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398c513837f84a92ae93b48024c44712e577cb8e031d5de5e5ceebff6168949f`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:02:30 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:02:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:00 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 05:08:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:08:05 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:08:05 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:08:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:08:07 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:08:07 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 05:08:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:09:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:10:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:10:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac14519460f6aeee1cf11e3dbd8aebc1dcdea50c13319f9ff02f648f1fd740`  
		Last Modified: Fri, 27 Sep 2024 05:12:26 GMT  
		Size: 129.1 MB (129124944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f470e04b4265d2ba8ff4d626c904c3e1b0b61fa56489d6114aa0d957a0126e5`  
		Last Modified: Fri, 27 Sep 2024 05:15:02 GMT  
		Size: 23.7 MB (23749360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c72e61443c05b575be756d581ee18d99c0cb05d4b54fdae38e875b61a959fac`  
		Last Modified: Fri, 27 Sep 2024 05:15:01 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2808a38c02a904bb9acd7a1a9fa12fe4163eb6272bbd74c21f2896608f5a09b`  
		Last Modified: Fri, 27 Sep 2024 05:16:06 GMT  
		Size: 431.1 MB (431144987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.6-bullseye`

```console
$ docker pull haskell@sha256:ff87472c659a8e381e4a54b1da445c74fe2ac5aab0ce2935cafc2fa4d79cff52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.6-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:55688aa378c8e79d14f38ec5c2705c42937bfd65b5e8b652f742325d4f9f69a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.3 MB (635349067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a903988fe07128415f9c7247fb968e48b4ebe28b6f92a90ddd64ffe30d41bdf6`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:52:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:57:42 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 04:57:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:57:46 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:57:47 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:57:47 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:57:49 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:57:49 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 04:57:49 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 04:59:34 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:59:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:59:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f5843f387f57f6777d24c4f557db58bdbd22e9967f0ff5c5e8d5a5ce528eac`  
		Last Modified: Fri, 27 Sep 2024 05:02:28 GMT  
		Size: 133.7 MB (133650612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8baec99a4c31d49b250a24e45d24aacc2fe5cdfa9a3798be37ca8868a787826`  
		Last Modified: Fri, 27 Sep 2024 05:05:17 GMT  
		Size: 21.4 MB (21443349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44dafce3bcb5825ad89ebf0584fc52545428e437b43292fc2b6ab939747a9aa`  
		Last Modified: Fri, 27 Sep 2024 05:05:15 GMT  
		Size: 8.0 MB (8004054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2567065a0f83d2ab372cf646e725fb4429e4becc558982a5e357304801cfe0af`  
		Last Modified: Fri, 27 Sep 2024 05:06:25 GMT  
		Size: 417.2 MB (417169661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b7a69b6b04d913dc9e9fd224927a0983dc54a9c28d3138804aad97324ea57b17
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.9 MB (647871425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398c513837f84a92ae93b48024c44712e577cb8e031d5de5e5ceebff6168949f`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:02:30 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:02:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:00 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 05:08:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:08:05 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:08:05 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:08:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:08:07 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:08:07 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 05:08:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:09:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:10:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:10:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac14519460f6aeee1cf11e3dbd8aebc1dcdea50c13319f9ff02f648f1fd740`  
		Last Modified: Fri, 27 Sep 2024 05:12:26 GMT  
		Size: 129.1 MB (129124944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f470e04b4265d2ba8ff4d626c904c3e1b0b61fa56489d6114aa0d957a0126e5`  
		Last Modified: Fri, 27 Sep 2024 05:15:02 GMT  
		Size: 23.7 MB (23749360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c72e61443c05b575be756d581ee18d99c0cb05d4b54fdae38e875b61a959fac`  
		Last Modified: Fri, 27 Sep 2024 05:15:01 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2808a38c02a904bb9acd7a1a9fa12fe4163eb6272bbd74c21f2896608f5a09b`  
		Last Modified: Fri, 27 Sep 2024 05:16:06 GMT  
		Size: 431.1 MB (431144987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.6-slim`

```console
$ docker pull haskell@sha256:71c6097bfa2ae58f3d745097eafa4356d3186903055c6810302c40b928d4f061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:9b74f66c4a1ce6f3a3054eb03958559ed601fda80eadf7c4d3300d5a2137b170
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446617847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e909ca4e6a4697f8e8b733047b7fd5010dd5e91d5ea2a61ea81df2fb6a44d0c5`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:55:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:55:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:59:51 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 04:59:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:59:54 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:59:55 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:59:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:59:57 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:59:57 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 04:59:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:01:39 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:01:45 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:01:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4245851650f9e4807c8be2c401467280707ac3062ec457080c43e56f02113`  
		Last Modified: Fri, 27 Sep 2024 05:03:57 GMT  
		Size: 106.4 MB (106364856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd2dc5e0505900f5c66ae11b065cc9cae53ae159e957a6c78aee31b8500e6a4`  
		Last Modified: Fri, 27 Sep 2024 05:06:40 GMT  
		Size: 21.4 MB (21443348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf70e1a888ea9e17ccc5adbe5d1e32fb1e9d7018edbcdd21b817dfb4a49d991e`  
		Last Modified: Fri, 27 Sep 2024 05:06:38 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc7317b1edf8b83f52af61da79b56db4d9efbedc0ea280da6adc313b6e94e7e`  
		Last Modified: Fri, 27 Sep 2024 05:07:23 GMT  
		Size: 279.4 MB (279376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:cf2150c3ab37ec35e12a18ff811bd7eddeaaf3e99541b6ad309fffc612fd1790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455529932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ecc7063e7a888960d5b6b812fb2dcad35a6ebf1138cc2605b686a06993b586`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:05:22 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:05:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:10:08 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 05:10:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:10:12 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:10:12 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:10:12 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:10:14 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:10:14 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 05:10:14 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:11:47 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:11:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:11:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b2ab68b28e6ef33b48bde65f6282b649027a6efd43f6c0ad6e0492c9540809`  
		Last Modified: Fri, 27 Sep 2024 05:13:47 GMT  
		Size: 101.9 MB (101852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d210823e86bf393f2115294bf0489052ecc4e33cb5c2c4ff93335e902466630`  
		Last Modified: Fri, 27 Sep 2024 05:16:20 GMT  
		Size: 23.7 MB (23749360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9aed38395a35dfcd8bb6c1d3220bef3e66ddd25deb181382a455f5e6051de7`  
		Last Modified: Fri, 27 Sep 2024 05:16:19 GMT  
		Size: 10.1 MB (10118267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fad95f153123630ad265b659e919385a7c8f63a1b6d4f9bd49ea643844df07a`  
		Last Modified: Fri, 27 Sep 2024 05:17:00 GMT  
		Size: 289.7 MB (289734599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.6-slim-bullseye`

```console
$ docker pull haskell@sha256:71c6097bfa2ae58f3d745097eafa4356d3186903055c6810302c40b928d4f061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.6-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:9b74f66c4a1ce6f3a3054eb03958559ed601fda80eadf7c4d3300d5a2137b170
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446617847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e909ca4e6a4697f8e8b733047b7fd5010dd5e91d5ea2a61ea81df2fb6a44d0c5`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:55:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:55:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:59:51 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 04:59:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:59:54 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:59:55 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:59:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:59:57 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:59:57 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 04:59:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:01:39 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:01:45 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:01:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4245851650f9e4807c8be2c401467280707ac3062ec457080c43e56f02113`  
		Last Modified: Fri, 27 Sep 2024 05:03:57 GMT  
		Size: 106.4 MB (106364856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd2dc5e0505900f5c66ae11b065cc9cae53ae159e957a6c78aee31b8500e6a4`  
		Last Modified: Fri, 27 Sep 2024 05:06:40 GMT  
		Size: 21.4 MB (21443348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf70e1a888ea9e17ccc5adbe5d1e32fb1e9d7018edbcdd21b817dfb4a49d991e`  
		Last Modified: Fri, 27 Sep 2024 05:06:38 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dc7317b1edf8b83f52af61da79b56db4d9efbedc0ea280da6adc313b6e94e7e`  
		Last Modified: Fri, 27 Sep 2024 05:07:23 GMT  
		Size: 279.4 MB (279376996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.6-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:cf2150c3ab37ec35e12a18ff811bd7eddeaaf3e99541b6ad309fffc612fd1790
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455529932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ecc7063e7a888960d5b6b812fb2dcad35a6ebf1138cc2605b686a06993b586`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:05:22 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:05:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:10:08 GMT
ARG STACK=2.15.5
# Fri, 27 Sep 2024 05:10:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:10:12 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:10:12 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:10:12 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:10:14 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:10:14 GMT
ARG GHC=9.6.6
# Fri, 27 Sep 2024 05:10:14 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 27 Sep 2024 05:11:47 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:11:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:11:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b2ab68b28e6ef33b48bde65f6282b649027a6efd43f6c0ad6e0492c9540809`  
		Last Modified: Fri, 27 Sep 2024 05:13:47 GMT  
		Size: 101.9 MB (101852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d210823e86bf393f2115294bf0489052ecc4e33cb5c2c4ff93335e902466630`  
		Last Modified: Fri, 27 Sep 2024 05:16:20 GMT  
		Size: 23.7 MB (23749360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9aed38395a35dfcd8bb6c1d3220bef3e66ddd25deb181382a455f5e6051de7`  
		Last Modified: Fri, 27 Sep 2024 05:16:19 GMT  
		Size: 10.1 MB (10118267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fad95f153123630ad265b659e919385a7c8f63a1b6d4f9bd49ea643844df07a`  
		Last Modified: Fri, 27 Sep 2024 05:17:00 GMT  
		Size: 289.7 MB (289734599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:bullseye`

```console
$ docker pull haskell@sha256:ce32b18e6632c88e7cc8a6bc9794f7fe113f1d264bfa0afa2b09cb0d96205999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:fb29c7606018a77dc5c0c1d4ac42de3e6825f60792fb04a07ce29f49b637102a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.6 MB (657598673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae5faef0f33e1092e73a2289a962c65c3d0ba241bb634cf88e1530d654c1e8`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:52:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:52:51 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:52:51 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:52:52 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:52:54 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:54:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:54:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:54:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f5843f387f57f6777d24c4f557db58bdbd22e9967f0ff5c5e8d5a5ce528eac`  
		Last Modified: Fri, 27 Sep 2024 05:02:28 GMT  
		Size: 133.7 MB (133650612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ead6b6435258fab2fa2a7f938064be6f7ce00e94cf6bcd32cc41f14f44acb38`  
		Last Modified: Fri, 27 Sep 2024 05:02:14 GMT  
		Size: 21.8 MB (21787178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940bd95f92241cad88e341b6110d7527c3da3b0c8ca2a8ae619d5beb2510137`  
		Last Modified: Fri, 27 Sep 2024 05:02:12 GMT  
		Size: 8.0 MB (8004053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8f8983e4c9592ca9fa443ce6556e8111298891dc4b6ab9c6911793c6665685`  
		Last Modified: Fri, 27 Sep 2024 05:03:27 GMT  
		Size: 439.1 MB (439075439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fca3c9d0707ebb820875d8ef2c2a3050c1cb32bb7f629159915acfb293520540
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.6 MB (663605182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e17fb6a75abeab897ec3a7e5a1213b43a817156eaa4037f48bde70c2b1addf`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:02:30 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:02:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:02:50 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:02:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:02:55 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:02:57 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:04:56 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:05:09 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:05:09 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac14519460f6aeee1cf11e3dbd8aebc1dcdea50c13319f9ff02f648f1fd740`  
		Last Modified: Fri, 27 Sep 2024 05:12:26 GMT  
		Size: 129.1 MB (129124944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426810c71c4327fd5994e8c2f0d0ac9bfa50f9b1c031b64e6a6ac5610faa529c`  
		Last Modified: Fri, 27 Sep 2024 05:12:14 GMT  
		Size: 24.2 MB (24152211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5757b580d898c36f1ffcbbf038034341302aa7b60c5720cd1111b4d13f102e7`  
		Last Modified: Fri, 27 Sep 2024 05:12:13 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8a227d00ea335cdd832eeb24c1babe4f5686947e7e24585cd0c4d28b206496`  
		Last Modified: Fri, 27 Sep 2024 05:13:21 GMT  
		Size: 446.5 MB (446475893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:ce32b18e6632c88e7cc8a6bc9794f7fe113f1d264bfa0afa2b09cb0d96205999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:fb29c7606018a77dc5c0c1d4ac42de3e6825f60792fb04a07ce29f49b637102a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.6 MB (657598673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ae5faef0f33e1092e73a2289a962c65c3d0ba241bb634cf88e1530d654c1e8`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:52:24 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:52:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:52:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:52:51 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:52:51 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:52:52 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:52:54 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:52:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:54:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:54:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:54:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f5843f387f57f6777d24c4f557db58bdbd22e9967f0ff5c5e8d5a5ce528eac`  
		Last Modified: Fri, 27 Sep 2024 05:02:28 GMT  
		Size: 133.7 MB (133650612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ead6b6435258fab2fa2a7f938064be6f7ce00e94cf6bcd32cc41f14f44acb38`  
		Last Modified: Fri, 27 Sep 2024 05:02:14 GMT  
		Size: 21.8 MB (21787178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e940bd95f92241cad88e341b6110d7527c3da3b0c8ca2a8ae619d5beb2510137`  
		Last Modified: Fri, 27 Sep 2024 05:02:12 GMT  
		Size: 8.0 MB (8004053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8f8983e4c9592ca9fa443ce6556e8111298891dc4b6ab9c6911793c6665685`  
		Last Modified: Fri, 27 Sep 2024 05:03:27 GMT  
		Size: 439.1 MB (439075439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:fca3c9d0707ebb820875d8ef2c2a3050c1cb32bb7f629159915acfb293520540
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.6 MB (663605182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e17fb6a75abeab897ec3a7e5a1213b43a817156eaa4037f48bde70c2b1addf`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:02:30 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:02:48 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:02:50 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:02:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:02:55 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:02:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:02:57 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:02:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:04:56 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:05:09 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:05:09 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ac14519460f6aeee1cf11e3dbd8aebc1dcdea50c13319f9ff02f648f1fd740`  
		Last Modified: Fri, 27 Sep 2024 05:12:26 GMT  
		Size: 129.1 MB (129124944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:426810c71c4327fd5994e8c2f0d0ac9bfa50f9b1c031b64e6a6ac5610faa529c`  
		Last Modified: Fri, 27 Sep 2024 05:12:14 GMT  
		Size: 24.2 MB (24152211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5757b580d898c36f1ffcbbf038034341302aa7b60c5720cd1111b4d13f102e7`  
		Last Modified: Fri, 27 Sep 2024 05:12:13 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8a227d00ea335cdd832eeb24c1babe4f5686947e7e24585cd0c4d28b206496`  
		Last Modified: Fri, 27 Sep 2024 05:13:21 GMT  
		Size: 446.5 MB (446475893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim`

```console
$ docker pull haskell@sha256:345e44e48cc55ad24dbc5ece5a07a68dc2bb3934ef65c983a197ec125347bb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:5bed54236eb27f560768d786d577bcd6223faa66bf331199215593036c522cf7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.7 MB (606666993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887cc905f0ab30764b21351acdcb5208f535a2dd6496782eec3579747850e012`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:55:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:55:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:55:27 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:55:30 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:57:29 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:57:38 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:57:38 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4245851650f9e4807c8be2c401467280707ac3062ec457080c43e56f02113`  
		Last Modified: Fri, 27 Sep 2024 05:03:57 GMT  
		Size: 106.4 MB (106364856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3afccb50c76122edb47d85d04e1183c7293a9f1283c764093750331cb6bdcb7`  
		Last Modified: Fri, 27 Sep 2024 05:03:46 GMT  
		Size: 21.8 MB (21787158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ef6d5c5e7643717a714595ecdf3194398742a95ed9a628595d3b0ddbadb24c`  
		Last Modified: Fri, 27 Sep 2024 05:03:44 GMT  
		Size: 8.0 MB (8004055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe6cfc0abe0e26b662cd1ddb441e88750a5e4866eea530060ff6428c1b042ca`  
		Last Modified: Fri, 27 Sep 2024 05:04:58 GMT  
		Size: 439.1 MB (439082325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a9abe2be4fafbef93cec98290689750d90b255918d8e412c1a0a74940fa7f276
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.7 MB (612676788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3113aee132ea737150aae8db4360d32b04a1cc189bc159489603225eb625218f`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:05:22 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:05:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:05:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:05:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:07:34 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:07:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:07:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b2ab68b28e6ef33b48bde65f6282b649027a6efd43f6c0ad6e0492c9540809`  
		Last Modified: Fri, 27 Sep 2024 05:13:47 GMT  
		Size: 101.9 MB (101852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ff235fab3eb8bc0cb5466deb71f17e3b45ce5b30dd85ee353397fa5b4740e5`  
		Last Modified: Fri, 27 Sep 2024 05:13:38 GMT  
		Size: 24.2 MB (24152199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c86239d91041fdf1ae6f460f763662091472cd4e8094d6b6cc2c428e3c1368`  
		Last Modified: Fri, 27 Sep 2024 05:13:37 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8edc6cddf1140cdfb9bc3f1b3d044980e2e483e2b7acd9a92ae056bc475dbc`  
		Last Modified: Fri, 27 Sep 2024 05:14:45 GMT  
		Size: 446.5 MB (446478613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim-bullseye`

```console
$ docker pull haskell@sha256:345e44e48cc55ad24dbc5ece5a07a68dc2bb3934ef65c983a197ec125347bb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:5bed54236eb27f560768d786d577bcd6223faa66bf331199215593036c522cf7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.7 MB (606666993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887cc905f0ab30764b21351acdcb5208f535a2dd6496782eec3579747850e012`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 04:55:03 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 04:55:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 04:55:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 04:55:27 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 04:55:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 04:55:30 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 04:55:30 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 04:57:29 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 04:57:38 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 04:57:38 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae4245851650f9e4807c8be2c401467280707ac3062ec457080c43e56f02113`  
		Last Modified: Fri, 27 Sep 2024 05:03:57 GMT  
		Size: 106.4 MB (106364856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3afccb50c76122edb47d85d04e1183c7293a9f1283c764093750331cb6bdcb7`  
		Last Modified: Fri, 27 Sep 2024 05:03:46 GMT  
		Size: 21.8 MB (21787158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ef6d5c5e7643717a714595ecdf3194398742a95ed9a628595d3b0ddbadb24c`  
		Last Modified: Fri, 27 Sep 2024 05:03:44 GMT  
		Size: 8.0 MB (8004055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe6cfc0abe0e26b662cd1ddb441e88750a5e4866eea530060ff6428c1b042ca`  
		Last Modified: Fri, 27 Sep 2024 05:04:58 GMT  
		Size: 439.1 MB (439082325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a9abe2be4fafbef93cec98290689750d90b255918d8e412c1a0a74940fa7f276
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.7 MB (612676788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3113aee132ea737150aae8db4360d32b04a1cc189bc159489603225eb625218f`
-	Default Command: `["ghci"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:05:22 GMT
ENV LANG=C.UTF-8
# Fri, 27 Sep 2024 05:05:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK=2.15.7
# Fri, 27 Sep 2024 05:05:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Fri, 27 Sep 2024 05:05:44 GMT
# ARGS: STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='f0c4b038c7e895902e133a2f4c4c217e03c4be44aa5da48aec9f7947f4af090b';             ;;         'x86_64')             STACK_SHA256='4e635d6168f7578a5694a0d473c980c3c7ed35d971acae969de1fd48ef14e030';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 27 Sep 2024 05:05:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 27 Sep 2024 05:05:46 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC=9.10.1
# Fri, 27 Sep 2024 05:05:46 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Fri, 27 Sep 2024 05:07:34 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=2.15.7 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 27 Sep 2024 05:07:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 27 Sep 2024 05:07:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b2ab68b28e6ef33b48bde65f6282b649027a6efd43f6c0ad6e0492c9540809`  
		Last Modified: Fri, 27 Sep 2024 05:13:47 GMT  
		Size: 101.9 MB (101852548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ff235fab3eb8bc0cb5466deb71f17e3b45ce5b30dd85ee353397fa5b4740e5`  
		Last Modified: Fri, 27 Sep 2024 05:13:38 GMT  
		Size: 24.2 MB (24152199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c86239d91041fdf1ae6f460f763662091472cd4e8094d6b6cc2c428e3c1368`  
		Last Modified: Fri, 27 Sep 2024 05:13:37 GMT  
		Size: 10.1 MB (10118270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8edc6cddf1140cdfb9bc3f1b3d044980e2e483e2b7acd9a92ae056bc475dbc`  
		Last Modified: Fri, 27 Sep 2024 05:14:45 GMT  
		Size: 446.5 MB (446478613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
