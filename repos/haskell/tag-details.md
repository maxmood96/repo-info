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
$ docker pull haskell@sha256:9289097b6a630f9e4676b55c517cec338150f4df275c9286c7b072cea01910f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:f20e66216fe57d95c3329c20c4cd58e9a0c8a0a3e2653f8add73d44ddb89a97f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657462230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782e1ef65169600827778cb69a5466aa343b955eb347646a3c781b6c23773263`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:33:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:33:11 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:33:13 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:35:11 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:35:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:35:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533e2a209f7f1132d0afdf989885257f4434723eddd8ae533fc4fa1944f3905`  
		Last Modified: Thu, 17 Oct 2024 04:42:32 GMT  
		Size: 133.7 MB (133667875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c05726d106d3b71751923c64820381a90be1b01981209b9af10ad0b56d1f55`  
		Last Modified: Thu, 17 Oct 2024 04:42:19 GMT  
		Size: 21.6 MB (21635384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5145e73a21b1ec2a9b987c8cdd0ae25bf78a9550e04d9d2f8dc451ab9d12a2`  
		Last Modified: Thu, 17 Oct 2024 04:42:17 GMT  
		Size: 8.0 MB (8004047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1490bd509801f1867561ea786e4e2bffa3a20b6b0fc502a9d9448327a89c82`  
		Last Modified: Thu, 17 Oct 2024 04:43:32 GMT  
		Size: 439.1 MB (439074313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c709da4ddef97cb8908b9076cbc31c7e92c868f29d207f965dfa3133a27228f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.3 MB (663330258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047ae6a523c6133ba89bc6b8850b6a481d682b5095f1b4010bf37976bbf69fde`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:42:00 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:42:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:42:23 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:42:25 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:44:12 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:44:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:44:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71778b6c993471915955cce00cac8c2cc2c7d390e9aeab982a767155e0bb8bf8`  
		Last Modified: Thu, 17 Oct 2024 04:51:41 GMT  
		Size: 129.1 MB (129144009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943c2985ca4521e081a0f8a9bd1fbe7c8b1e2c0da522ca8eb3f2216e07c2ce5`  
		Last Modified: Thu, 17 Oct 2024 04:51:30 GMT  
		Size: 23.9 MB (23858540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4257fb0fcf27cdc7d362396c8f224ef6c530094d6c72cbfe1a87bc13686ae5`  
		Last Modified: Thu, 17 Oct 2024 04:51:29 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0485b3d149db3b54d75f3220ed9665e354df81ee88ffe97ad82d094475225519`  
		Last Modified: Thu, 17 Oct 2024 04:52:34 GMT  
		Size: 446.5 MB (446474548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-bullseye`

```console
$ docker pull haskell@sha256:9289097b6a630f9e4676b55c517cec338150f4df275c9286c7b072cea01910f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f20e66216fe57d95c3329c20c4cd58e9a0c8a0a3e2653f8add73d44ddb89a97f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657462230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782e1ef65169600827778cb69a5466aa343b955eb347646a3c781b6c23773263`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:33:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:33:11 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:33:13 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:35:11 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:35:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:35:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533e2a209f7f1132d0afdf989885257f4434723eddd8ae533fc4fa1944f3905`  
		Last Modified: Thu, 17 Oct 2024 04:42:32 GMT  
		Size: 133.7 MB (133667875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c05726d106d3b71751923c64820381a90be1b01981209b9af10ad0b56d1f55`  
		Last Modified: Thu, 17 Oct 2024 04:42:19 GMT  
		Size: 21.6 MB (21635384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5145e73a21b1ec2a9b987c8cdd0ae25bf78a9550e04d9d2f8dc451ab9d12a2`  
		Last Modified: Thu, 17 Oct 2024 04:42:17 GMT  
		Size: 8.0 MB (8004047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1490bd509801f1867561ea786e4e2bffa3a20b6b0fc502a9d9448327a89c82`  
		Last Modified: Thu, 17 Oct 2024 04:43:32 GMT  
		Size: 439.1 MB (439074313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c709da4ddef97cb8908b9076cbc31c7e92c868f29d207f965dfa3133a27228f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.3 MB (663330258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047ae6a523c6133ba89bc6b8850b6a481d682b5095f1b4010bf37976bbf69fde`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:42:00 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:42:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:42:23 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:42:25 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:44:12 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:44:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:44:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71778b6c993471915955cce00cac8c2cc2c7d390e9aeab982a767155e0bb8bf8`  
		Last Modified: Thu, 17 Oct 2024 04:51:41 GMT  
		Size: 129.1 MB (129144009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943c2985ca4521e081a0f8a9bd1fbe7c8b1e2c0da522ca8eb3f2216e07c2ce5`  
		Last Modified: Thu, 17 Oct 2024 04:51:30 GMT  
		Size: 23.9 MB (23858540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4257fb0fcf27cdc7d362396c8f224ef6c530094d6c72cbfe1a87bc13686ae5`  
		Last Modified: Thu, 17 Oct 2024 04:51:29 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0485b3d149db3b54d75f3220ed9665e354df81ee88ffe97ad82d094475225519`  
		Last Modified: Thu, 17 Oct 2024 04:52:34 GMT  
		Size: 446.5 MB (446474548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:b54e8944575a100879f489ef270a7111d2698609a327f70c8c861fab87ee800f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:76a334d11f696e1e0b7c944021fe40a76253cf54cefe4ebddba3613ce48db081
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606507229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614e867b9ab57c06746ad709710f00ac1d118eb8e8ea5458325daddfe929c81`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:35:23 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:35:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:35:48 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:35:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:37:47 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:37:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:37:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6853f8064ec51113b4645a988f1bdc942c5c3694bb5d90cd96a95859d6b26053`  
		Last Modified: Thu, 17 Oct 2024 04:44:01 GMT  
		Size: 106.4 MB (106365300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b58b2064b9890c49b8c5020ffbde0cf3c1066142f17363d58326fcbd7e6152`  
		Last Modified: Thu, 17 Oct 2024 04:43:50 GMT  
		Size: 21.6 MB (21635387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba790bc30420d4462ef8f3efed9213829bdf63fb0ce3eee2305cfb824f37478`  
		Last Modified: Thu, 17 Oct 2024 04:43:48 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1c65660167fbd58d254ed1434e87c48e6a1baddec615135ffe6ea09597178c`  
		Last Modified: Thu, 17 Oct 2024 04:45:02 GMT  
		Size: 439.1 MB (439073694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:997dddb457c9712d96cb6ac719adce04aa93db4404953861e9298b12edbd1526
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.4 MB (612380863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b761a049ff58b72ee18bb8173ecb18e0fde91a590e5a56d4fa9b6801845d02d0`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:44:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:45:00 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:45:02 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:46:51 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:47:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:47:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f3c53d7fd04a3d7c59254dfc2c251f01e10e4e270cee01a62ccc378dd5fa2`  
		Last Modified: Thu, 17 Oct 2024 04:52:58 GMT  
		Size: 101.9 MB (101852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b39c59cb56b844c7697a89fba53c8211ac9d9afe62a6d84bb852cc0ec0a198`  
		Last Modified: Thu, 17 Oct 2024 04:52:51 GMT  
		Size: 23.9 MB (23858505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d3be321a1df021cb7bdd6dda46673f5c7a355fb5acea251db7638b702ef7c`  
		Last Modified: Thu, 17 Oct 2024 04:52:49 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03169dc144345133bd6bcdc887b59c7cfca72e1e1f89b254fd33b2e865a42cd5`  
		Last Modified: Thu, 17 Oct 2024 04:53:54 GMT  
		Size: 446.5 MB (446475928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-slim-bullseye`

```console
$ docker pull haskell@sha256:b54e8944575a100879f489ef270a7111d2698609a327f70c8c861fab87ee800f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:76a334d11f696e1e0b7c944021fe40a76253cf54cefe4ebddba3613ce48db081
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606507229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614e867b9ab57c06746ad709710f00ac1d118eb8e8ea5458325daddfe929c81`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:35:23 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:35:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:35:48 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:35:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:37:47 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:37:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:37:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6853f8064ec51113b4645a988f1bdc942c5c3694bb5d90cd96a95859d6b26053`  
		Last Modified: Thu, 17 Oct 2024 04:44:01 GMT  
		Size: 106.4 MB (106365300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b58b2064b9890c49b8c5020ffbde0cf3c1066142f17363d58326fcbd7e6152`  
		Last Modified: Thu, 17 Oct 2024 04:43:50 GMT  
		Size: 21.6 MB (21635387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba790bc30420d4462ef8f3efed9213829bdf63fb0ce3eee2305cfb824f37478`  
		Last Modified: Thu, 17 Oct 2024 04:43:48 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1c65660167fbd58d254ed1434e87c48e6a1baddec615135ffe6ea09597178c`  
		Last Modified: Thu, 17 Oct 2024 04:45:02 GMT  
		Size: 439.1 MB (439073694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:997dddb457c9712d96cb6ac719adce04aa93db4404953861e9298b12edbd1526
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.4 MB (612380863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b761a049ff58b72ee18bb8173ecb18e0fde91a590e5a56d4fa9b6801845d02d0`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:44:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:45:00 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:45:02 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:46:51 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:47:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:47:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f3c53d7fd04a3d7c59254dfc2c251f01e10e4e270cee01a62ccc378dd5fa2`  
		Last Modified: Thu, 17 Oct 2024 04:52:58 GMT  
		Size: 101.9 MB (101852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b39c59cb56b844c7697a89fba53c8211ac9d9afe62a6d84bb852cc0ec0a198`  
		Last Modified: Thu, 17 Oct 2024 04:52:51 GMT  
		Size: 23.9 MB (23858505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d3be321a1df021cb7bdd6dda46673f5c7a355fb5acea251db7638b702ef7c`  
		Last Modified: Thu, 17 Oct 2024 04:52:49 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03169dc144345133bd6bcdc887b59c7cfca72e1e1f89b254fd33b2e865a42cd5`  
		Last Modified: Thu, 17 Oct 2024 04:53:54 GMT  
		Size: 446.5 MB (446475928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10-bullseye`

```console
$ docker pull haskell@sha256:9289097b6a630f9e4676b55c517cec338150f4df275c9286c7b072cea01910f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f20e66216fe57d95c3329c20c4cd58e9a0c8a0a3e2653f8add73d44ddb89a97f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657462230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782e1ef65169600827778cb69a5466aa343b955eb347646a3c781b6c23773263`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:33:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:33:11 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:33:13 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:35:11 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:35:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:35:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533e2a209f7f1132d0afdf989885257f4434723eddd8ae533fc4fa1944f3905`  
		Last Modified: Thu, 17 Oct 2024 04:42:32 GMT  
		Size: 133.7 MB (133667875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c05726d106d3b71751923c64820381a90be1b01981209b9af10ad0b56d1f55`  
		Last Modified: Thu, 17 Oct 2024 04:42:19 GMT  
		Size: 21.6 MB (21635384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5145e73a21b1ec2a9b987c8cdd0ae25bf78a9550e04d9d2f8dc451ab9d12a2`  
		Last Modified: Thu, 17 Oct 2024 04:42:17 GMT  
		Size: 8.0 MB (8004047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1490bd509801f1867561ea786e4e2bffa3a20b6b0fc502a9d9448327a89c82`  
		Last Modified: Thu, 17 Oct 2024 04:43:32 GMT  
		Size: 439.1 MB (439074313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c709da4ddef97cb8908b9076cbc31c7e92c868f29d207f965dfa3133a27228f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.3 MB (663330258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047ae6a523c6133ba89bc6b8850b6a481d682b5095f1b4010bf37976bbf69fde`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:42:00 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:42:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:42:23 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:42:25 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:44:12 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:44:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:44:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71778b6c993471915955cce00cac8c2cc2c7d390e9aeab982a767155e0bb8bf8`  
		Last Modified: Thu, 17 Oct 2024 04:51:41 GMT  
		Size: 129.1 MB (129144009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943c2985ca4521e081a0f8a9bd1fbe7c8b1e2c0da522ca8eb3f2216e07c2ce5`  
		Last Modified: Thu, 17 Oct 2024 04:51:30 GMT  
		Size: 23.9 MB (23858540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4257fb0fcf27cdc7d362396c8f224ef6c530094d6c72cbfe1a87bc13686ae5`  
		Last Modified: Thu, 17 Oct 2024 04:51:29 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0485b3d149db3b54d75f3220ed9665e354df81ee88ffe97ad82d094475225519`  
		Last Modified: Thu, 17 Oct 2024 04:52:34 GMT  
		Size: 446.5 MB (446474548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10-slim-bullseye`

```console
$ docker pull haskell@sha256:b54e8944575a100879f489ef270a7111d2698609a327f70c8c861fab87ee800f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:76a334d11f696e1e0b7c944021fe40a76253cf54cefe4ebddba3613ce48db081
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606507229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614e867b9ab57c06746ad709710f00ac1d118eb8e8ea5458325daddfe929c81`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:35:23 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:35:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:35:48 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:35:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:37:47 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:37:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:37:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6853f8064ec51113b4645a988f1bdc942c5c3694bb5d90cd96a95859d6b26053`  
		Last Modified: Thu, 17 Oct 2024 04:44:01 GMT  
		Size: 106.4 MB (106365300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b58b2064b9890c49b8c5020ffbde0cf3c1066142f17363d58326fcbd7e6152`  
		Last Modified: Thu, 17 Oct 2024 04:43:50 GMT  
		Size: 21.6 MB (21635387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba790bc30420d4462ef8f3efed9213829bdf63fb0ce3eee2305cfb824f37478`  
		Last Modified: Thu, 17 Oct 2024 04:43:48 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1c65660167fbd58d254ed1434e87c48e6a1baddec615135ffe6ea09597178c`  
		Last Modified: Thu, 17 Oct 2024 04:45:02 GMT  
		Size: 439.1 MB (439073694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:997dddb457c9712d96cb6ac719adce04aa93db4404953861e9298b12edbd1526
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.4 MB (612380863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b761a049ff58b72ee18bb8173ecb18e0fde91a590e5a56d4fa9b6801845d02d0`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:44:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:45:00 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:45:02 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:46:51 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:47:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:47:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f3c53d7fd04a3d7c59254dfc2c251f01e10e4e270cee01a62ccc378dd5fa2`  
		Last Modified: Thu, 17 Oct 2024 04:52:58 GMT  
		Size: 101.9 MB (101852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b39c59cb56b844c7697a89fba53c8211ac9d9afe62a6d84bb852cc0ec0a198`  
		Last Modified: Thu, 17 Oct 2024 04:52:51 GMT  
		Size: 23.9 MB (23858505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d3be321a1df021cb7bdd6dda46673f5c7a355fb5acea251db7638b702ef7c`  
		Last Modified: Thu, 17 Oct 2024 04:52:49 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03169dc144345133bd6bcdc887b59c7cfca72e1e1f89b254fd33b2e865a42cd5`  
		Last Modified: Thu, 17 Oct 2024 04:53:54 GMT  
		Size: 446.5 MB (446475928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10.1-bullseye`

```console
$ docker pull haskell@sha256:9289097b6a630f9e4676b55c517cec338150f4df275c9286c7b072cea01910f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10.1-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f20e66216fe57d95c3329c20c4cd58e9a0c8a0a3e2653f8add73d44ddb89a97f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657462230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782e1ef65169600827778cb69a5466aa343b955eb347646a3c781b6c23773263`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:33:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:33:11 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:33:13 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:35:11 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:35:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:35:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533e2a209f7f1132d0afdf989885257f4434723eddd8ae533fc4fa1944f3905`  
		Last Modified: Thu, 17 Oct 2024 04:42:32 GMT  
		Size: 133.7 MB (133667875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c05726d106d3b71751923c64820381a90be1b01981209b9af10ad0b56d1f55`  
		Last Modified: Thu, 17 Oct 2024 04:42:19 GMT  
		Size: 21.6 MB (21635384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5145e73a21b1ec2a9b987c8cdd0ae25bf78a9550e04d9d2f8dc451ab9d12a2`  
		Last Modified: Thu, 17 Oct 2024 04:42:17 GMT  
		Size: 8.0 MB (8004047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1490bd509801f1867561ea786e4e2bffa3a20b6b0fc502a9d9448327a89c82`  
		Last Modified: Thu, 17 Oct 2024 04:43:32 GMT  
		Size: 439.1 MB (439074313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c709da4ddef97cb8908b9076cbc31c7e92c868f29d207f965dfa3133a27228f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.3 MB (663330258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047ae6a523c6133ba89bc6b8850b6a481d682b5095f1b4010bf37976bbf69fde`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:42:00 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:42:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:42:23 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:42:25 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:44:12 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:44:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:44:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71778b6c993471915955cce00cac8c2cc2c7d390e9aeab982a767155e0bb8bf8`  
		Last Modified: Thu, 17 Oct 2024 04:51:41 GMT  
		Size: 129.1 MB (129144009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943c2985ca4521e081a0f8a9bd1fbe7c8b1e2c0da522ca8eb3f2216e07c2ce5`  
		Last Modified: Thu, 17 Oct 2024 04:51:30 GMT  
		Size: 23.9 MB (23858540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4257fb0fcf27cdc7d362396c8f224ef6c530094d6c72cbfe1a87bc13686ae5`  
		Last Modified: Thu, 17 Oct 2024 04:51:29 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0485b3d149db3b54d75f3220ed9665e354df81ee88ffe97ad82d094475225519`  
		Last Modified: Thu, 17 Oct 2024 04:52:34 GMT  
		Size: 446.5 MB (446474548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.10.1-slim-bullseye`

```console
$ docker pull haskell@sha256:b54e8944575a100879f489ef270a7111d2698609a327f70c8c861fab87ee800f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.10.1-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:76a334d11f696e1e0b7c944021fe40a76253cf54cefe4ebddba3613ce48db081
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606507229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614e867b9ab57c06746ad709710f00ac1d118eb8e8ea5458325daddfe929c81`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:35:23 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:35:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:35:48 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:35:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:37:47 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:37:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:37:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6853f8064ec51113b4645a988f1bdc942c5c3694bb5d90cd96a95859d6b26053`  
		Last Modified: Thu, 17 Oct 2024 04:44:01 GMT  
		Size: 106.4 MB (106365300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b58b2064b9890c49b8c5020ffbde0cf3c1066142f17363d58326fcbd7e6152`  
		Last Modified: Thu, 17 Oct 2024 04:43:50 GMT  
		Size: 21.6 MB (21635387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba790bc30420d4462ef8f3efed9213829bdf63fb0ce3eee2305cfb824f37478`  
		Last Modified: Thu, 17 Oct 2024 04:43:48 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1c65660167fbd58d254ed1434e87c48e6a1baddec615135ffe6ea09597178c`  
		Last Modified: Thu, 17 Oct 2024 04:45:02 GMT  
		Size: 439.1 MB (439073694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.10.1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:997dddb457c9712d96cb6ac719adce04aa93db4404953861e9298b12edbd1526
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.4 MB (612380863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b761a049ff58b72ee18bb8173ecb18e0fde91a590e5a56d4fa9b6801845d02d0`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:44:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:45:00 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:45:02 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:46:51 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:47:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:47:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f3c53d7fd04a3d7c59254dfc2c251f01e10e4e270cee01a62ccc378dd5fa2`  
		Last Modified: Thu, 17 Oct 2024 04:52:58 GMT  
		Size: 101.9 MB (101852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b39c59cb56b844c7697a89fba53c8211ac9d9afe62a6d84bb852cc0ec0a198`  
		Last Modified: Thu, 17 Oct 2024 04:52:51 GMT  
		Size: 23.9 MB (23858505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d3be321a1df021cb7bdd6dda46673f5c7a355fb5acea251db7638b702ef7c`  
		Last Modified: Thu, 17 Oct 2024 04:52:49 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03169dc144345133bd6bcdc887b59c7cfca72e1e1f89b254fd33b2e865a42cd5`  
		Last Modified: Thu, 17 Oct 2024 04:53:54 GMT  
		Size: 446.5 MB (446475928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6`

```console
$ docker pull haskell@sha256:3df3bd88b676c166cb52a6d405cc4b6c03530220c6f29fe6735451596fc15449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6` - linux; amd64

```console
$ docker pull haskell@sha256:f9f5fe06630d91b6fcc094b2a8cbdfe62e704e3c2ded401ebb57fcfd22df11e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.6 MB (635555701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc3a90b5dfad24fefc0a80b1410b82ffacdab384cd86da5351992751d86f707`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:33:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:33:11 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:33:13 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:38:02 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:38:02 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:39:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:39:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533e2a209f7f1132d0afdf989885257f4434723eddd8ae533fc4fa1944f3905`  
		Last Modified: Thu, 17 Oct 2024 04:42:32 GMT  
		Size: 133.7 MB (133667875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c05726d106d3b71751923c64820381a90be1b01981209b9af10ad0b56d1f55`  
		Last Modified: Thu, 17 Oct 2024 04:42:19 GMT  
		Size: 21.6 MB (21635384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5145e73a21b1ec2a9b987c8cdd0ae25bf78a9550e04d9d2f8dc451ab9d12a2`  
		Last Modified: Thu, 17 Oct 2024 04:42:17 GMT  
		Size: 8.0 MB (8004047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5bc01411405a10adf8fedcc7fdc1dfdedd0b640bd6df129e75f4063ce1eebd`  
		Last Modified: Thu, 17 Oct 2024 04:46:27 GMT  
		Size: 417.2 MB (417167784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f638fa283017b233b2e8210701d06b93b5a246cdf0db7394cef73632abda1a0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.0 MB (647991426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a581e9ee5f07d38ab26d849dd18a3574f55e5520cf918fb9a76373160760cd8`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:42:00 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:42:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:42:23 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:42:25 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:47:16 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:47:16 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:48:56 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:49:11 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:49:11 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71778b6c993471915955cce00cac8c2cc2c7d390e9aeab982a767155e0bb8bf8`  
		Last Modified: Thu, 17 Oct 2024 04:51:41 GMT  
		Size: 129.1 MB (129144009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943c2985ca4521e081a0f8a9bd1fbe7c8b1e2c0da522ca8eb3f2216e07c2ce5`  
		Last Modified: Thu, 17 Oct 2024 04:51:30 GMT  
		Size: 23.9 MB (23858540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4257fb0fcf27cdc7d362396c8f224ef6c530094d6c72cbfe1a87bc13686ae5`  
		Last Modified: Thu, 17 Oct 2024 04:51:29 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9964fa23196f78fa920bd22eb2260512b0a26d0fd29a8dfca3aeff8d957aa841`  
		Last Modified: Thu, 17 Oct 2024 04:55:13 GMT  
		Size: 431.1 MB (431135716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-bullseye`

```console
$ docker pull haskell@sha256:3df3bd88b676c166cb52a6d405cc4b6c03530220c6f29fe6735451596fc15449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f9f5fe06630d91b6fcc094b2a8cbdfe62e704e3c2ded401ebb57fcfd22df11e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.6 MB (635555701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc3a90b5dfad24fefc0a80b1410b82ffacdab384cd86da5351992751d86f707`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:33:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:33:11 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:33:13 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:38:02 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:38:02 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:39:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:39:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533e2a209f7f1132d0afdf989885257f4434723eddd8ae533fc4fa1944f3905`  
		Last Modified: Thu, 17 Oct 2024 04:42:32 GMT  
		Size: 133.7 MB (133667875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c05726d106d3b71751923c64820381a90be1b01981209b9af10ad0b56d1f55`  
		Last Modified: Thu, 17 Oct 2024 04:42:19 GMT  
		Size: 21.6 MB (21635384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5145e73a21b1ec2a9b987c8cdd0ae25bf78a9550e04d9d2f8dc451ab9d12a2`  
		Last Modified: Thu, 17 Oct 2024 04:42:17 GMT  
		Size: 8.0 MB (8004047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5bc01411405a10adf8fedcc7fdc1dfdedd0b640bd6df129e75f4063ce1eebd`  
		Last Modified: Thu, 17 Oct 2024 04:46:27 GMT  
		Size: 417.2 MB (417167784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f638fa283017b233b2e8210701d06b93b5a246cdf0db7394cef73632abda1a0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.0 MB (647991426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a581e9ee5f07d38ab26d849dd18a3574f55e5520cf918fb9a76373160760cd8`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:42:00 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:42:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:42:23 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:42:25 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:47:16 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:47:16 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:48:56 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:49:11 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:49:11 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71778b6c993471915955cce00cac8c2cc2c7d390e9aeab982a767155e0bb8bf8`  
		Last Modified: Thu, 17 Oct 2024 04:51:41 GMT  
		Size: 129.1 MB (129144009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943c2985ca4521e081a0f8a9bd1fbe7c8b1e2c0da522ca8eb3f2216e07c2ce5`  
		Last Modified: Thu, 17 Oct 2024 04:51:30 GMT  
		Size: 23.9 MB (23858540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4257fb0fcf27cdc7d362396c8f224ef6c530094d6c72cbfe1a87bc13686ae5`  
		Last Modified: Thu, 17 Oct 2024 04:51:29 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9964fa23196f78fa920bd22eb2260512b0a26d0fd29a8dfca3aeff8d957aa841`  
		Last Modified: Thu, 17 Oct 2024 04:55:13 GMT  
		Size: 431.1 MB (431135716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-slim`

```console
$ docker pull haskell@sha256:3e3088ee88b1b1ff731c7e1a29a7b02d89c22f31587053444e7d207e4c933376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:b45395bb20d4559f4caae5d28d2e5eb7383697569bf0b0b8bb983c009feca83c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.8 MB (446807819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee3b3fe0512d6e050914af9c2168741596bde7d5b8bc3260ef62083c268da0a`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:35:23 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:35:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:35:48 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:35:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:40:11 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:40:11 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:41:54 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:42:00 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:42:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6853f8064ec51113b4645a988f1bdc942c5c3694bb5d90cd96a95859d6b26053`  
		Last Modified: Thu, 17 Oct 2024 04:44:01 GMT  
		Size: 106.4 MB (106365300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b58b2064b9890c49b8c5020ffbde0cf3c1066142f17363d58326fcbd7e6152`  
		Last Modified: Thu, 17 Oct 2024 04:43:50 GMT  
		Size: 21.6 MB (21635387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba790bc30420d4462ef8f3efed9213829bdf63fb0ce3eee2305cfb824f37478`  
		Last Modified: Thu, 17 Oct 2024 04:43:48 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e4114d6e8bdb5752b03b60d5e65dca567c1af2d4f9944b5f69208e3d4ce5a5`  
		Last Modified: Thu, 17 Oct 2024 04:47:25 GMT  
		Size: 279.4 MB (279374284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:2d91a28995d2470fa5b00d0e3095f30478963724c80639d318255ce4dcbaf20b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.6 MB (455640232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d21e39f0f8776f22d54334faf74dd2cd4f8a50bcfd0296ec13346c1f7b8f7ed`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:44:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:45:00 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:45:02 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:49:24 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:49:24 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:50:59 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:51:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:51:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f3c53d7fd04a3d7c59254dfc2c251f01e10e4e270cee01a62ccc378dd5fa2`  
		Last Modified: Thu, 17 Oct 2024 04:52:58 GMT  
		Size: 101.9 MB (101852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b39c59cb56b844c7697a89fba53c8211ac9d9afe62a6d84bb852cc0ec0a198`  
		Last Modified: Thu, 17 Oct 2024 04:52:51 GMT  
		Size: 23.9 MB (23858505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d3be321a1df021cb7bdd6dda46673f5c7a355fb5acea251db7638b702ef7c`  
		Last Modified: Thu, 17 Oct 2024 04:52:49 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02ca30649a87ab29a0dd6825326f7b54c96668241f18b457cae71195d99bfdb`  
		Last Modified: Thu, 17 Oct 2024 04:56:07 GMT  
		Size: 289.7 MB (289735297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6-slim-bullseye`

```console
$ docker pull haskell@sha256:3e3088ee88b1b1ff731c7e1a29a7b02d89c22f31587053444e7d207e4c933376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:b45395bb20d4559f4caae5d28d2e5eb7383697569bf0b0b8bb983c009feca83c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.8 MB (446807819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee3b3fe0512d6e050914af9c2168741596bde7d5b8bc3260ef62083c268da0a`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:35:23 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:35:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:35:48 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:35:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:40:11 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:40:11 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:41:54 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:42:00 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:42:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6853f8064ec51113b4645a988f1bdc942c5c3694bb5d90cd96a95859d6b26053`  
		Last Modified: Thu, 17 Oct 2024 04:44:01 GMT  
		Size: 106.4 MB (106365300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b58b2064b9890c49b8c5020ffbde0cf3c1066142f17363d58326fcbd7e6152`  
		Last Modified: Thu, 17 Oct 2024 04:43:50 GMT  
		Size: 21.6 MB (21635387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba790bc30420d4462ef8f3efed9213829bdf63fb0ce3eee2305cfb824f37478`  
		Last Modified: Thu, 17 Oct 2024 04:43:48 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e4114d6e8bdb5752b03b60d5e65dca567c1af2d4f9944b5f69208e3d4ce5a5`  
		Last Modified: Thu, 17 Oct 2024 04:47:25 GMT  
		Size: 279.4 MB (279374284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:2d91a28995d2470fa5b00d0e3095f30478963724c80639d318255ce4dcbaf20b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.6 MB (455640232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d21e39f0f8776f22d54334faf74dd2cd4f8a50bcfd0296ec13346c1f7b8f7ed`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:44:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:45:00 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:45:02 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:49:24 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:49:24 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:50:59 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:51:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:51:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f3c53d7fd04a3d7c59254dfc2c251f01e10e4e270cee01a62ccc378dd5fa2`  
		Last Modified: Thu, 17 Oct 2024 04:52:58 GMT  
		Size: 101.9 MB (101852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b39c59cb56b844c7697a89fba53c8211ac9d9afe62a6d84bb852cc0ec0a198`  
		Last Modified: Thu, 17 Oct 2024 04:52:51 GMT  
		Size: 23.9 MB (23858505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d3be321a1df021cb7bdd6dda46673f5c7a355fb5acea251db7638b702ef7c`  
		Last Modified: Thu, 17 Oct 2024 04:52:49 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02ca30649a87ab29a0dd6825326f7b54c96668241f18b457cae71195d99bfdb`  
		Last Modified: Thu, 17 Oct 2024 04:56:07 GMT  
		Size: 289.7 MB (289735297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.6`

```console
$ docker pull haskell@sha256:3df3bd88b676c166cb52a6d405cc4b6c03530220c6f29fe6735451596fc15449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.6` - linux; amd64

```console
$ docker pull haskell@sha256:f9f5fe06630d91b6fcc094b2a8cbdfe62e704e3c2ded401ebb57fcfd22df11e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.6 MB (635555701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc3a90b5dfad24fefc0a80b1410b82ffacdab384cd86da5351992751d86f707`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:33:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:33:11 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:33:13 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:38:02 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:38:02 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:39:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:39:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533e2a209f7f1132d0afdf989885257f4434723eddd8ae533fc4fa1944f3905`  
		Last Modified: Thu, 17 Oct 2024 04:42:32 GMT  
		Size: 133.7 MB (133667875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c05726d106d3b71751923c64820381a90be1b01981209b9af10ad0b56d1f55`  
		Last Modified: Thu, 17 Oct 2024 04:42:19 GMT  
		Size: 21.6 MB (21635384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5145e73a21b1ec2a9b987c8cdd0ae25bf78a9550e04d9d2f8dc451ab9d12a2`  
		Last Modified: Thu, 17 Oct 2024 04:42:17 GMT  
		Size: 8.0 MB (8004047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5bc01411405a10adf8fedcc7fdc1dfdedd0b640bd6df129e75f4063ce1eebd`  
		Last Modified: Thu, 17 Oct 2024 04:46:27 GMT  
		Size: 417.2 MB (417167784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f638fa283017b233b2e8210701d06b93b5a246cdf0db7394cef73632abda1a0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.0 MB (647991426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a581e9ee5f07d38ab26d849dd18a3574f55e5520cf918fb9a76373160760cd8`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:42:00 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:42:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:42:23 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:42:25 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:47:16 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:47:16 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:48:56 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:49:11 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:49:11 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71778b6c993471915955cce00cac8c2cc2c7d390e9aeab982a767155e0bb8bf8`  
		Last Modified: Thu, 17 Oct 2024 04:51:41 GMT  
		Size: 129.1 MB (129144009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943c2985ca4521e081a0f8a9bd1fbe7c8b1e2c0da522ca8eb3f2216e07c2ce5`  
		Last Modified: Thu, 17 Oct 2024 04:51:30 GMT  
		Size: 23.9 MB (23858540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4257fb0fcf27cdc7d362396c8f224ef6c530094d6c72cbfe1a87bc13686ae5`  
		Last Modified: Thu, 17 Oct 2024 04:51:29 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9964fa23196f78fa920bd22eb2260512b0a26d0fd29a8dfca3aeff8d957aa841`  
		Last Modified: Thu, 17 Oct 2024 04:55:13 GMT  
		Size: 431.1 MB (431135716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.6-bullseye`

```console
$ docker pull haskell@sha256:3df3bd88b676c166cb52a6d405cc4b6c03530220c6f29fe6735451596fc15449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.6-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f9f5fe06630d91b6fcc094b2a8cbdfe62e704e3c2ded401ebb57fcfd22df11e5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.6 MB (635555701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc3a90b5dfad24fefc0a80b1410b82ffacdab384cd86da5351992751d86f707`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:33:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:33:11 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:33:13 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:38:02 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:38:02 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:39:48 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:39:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:39:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533e2a209f7f1132d0afdf989885257f4434723eddd8ae533fc4fa1944f3905`  
		Last Modified: Thu, 17 Oct 2024 04:42:32 GMT  
		Size: 133.7 MB (133667875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c05726d106d3b71751923c64820381a90be1b01981209b9af10ad0b56d1f55`  
		Last Modified: Thu, 17 Oct 2024 04:42:19 GMT  
		Size: 21.6 MB (21635384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5145e73a21b1ec2a9b987c8cdd0ae25bf78a9550e04d9d2f8dc451ab9d12a2`  
		Last Modified: Thu, 17 Oct 2024 04:42:17 GMT  
		Size: 8.0 MB (8004047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5bc01411405a10adf8fedcc7fdc1dfdedd0b640bd6df129e75f4063ce1eebd`  
		Last Modified: Thu, 17 Oct 2024 04:46:27 GMT  
		Size: 417.2 MB (417167784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f638fa283017b233b2e8210701d06b93b5a246cdf0db7394cef73632abda1a0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.0 MB (647991426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a581e9ee5f07d38ab26d849dd18a3574f55e5520cf918fb9a76373160760cd8`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:42:00 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:42:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:42:23 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:42:25 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:47:16 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:47:16 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:48:56 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:49:11 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:49:11 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71778b6c993471915955cce00cac8c2cc2c7d390e9aeab982a767155e0bb8bf8`  
		Last Modified: Thu, 17 Oct 2024 04:51:41 GMT  
		Size: 129.1 MB (129144009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943c2985ca4521e081a0f8a9bd1fbe7c8b1e2c0da522ca8eb3f2216e07c2ce5`  
		Last Modified: Thu, 17 Oct 2024 04:51:30 GMT  
		Size: 23.9 MB (23858540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4257fb0fcf27cdc7d362396c8f224ef6c530094d6c72cbfe1a87bc13686ae5`  
		Last Modified: Thu, 17 Oct 2024 04:51:29 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9964fa23196f78fa920bd22eb2260512b0a26d0fd29a8dfca3aeff8d957aa841`  
		Last Modified: Thu, 17 Oct 2024 04:55:13 GMT  
		Size: 431.1 MB (431135716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.6-slim`

```console
$ docker pull haskell@sha256:3e3088ee88b1b1ff731c7e1a29a7b02d89c22f31587053444e7d207e4c933376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:b45395bb20d4559f4caae5d28d2e5eb7383697569bf0b0b8bb983c009feca83c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.8 MB (446807819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee3b3fe0512d6e050914af9c2168741596bde7d5b8bc3260ef62083c268da0a`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:35:23 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:35:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:35:48 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:35:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:40:11 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:40:11 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:41:54 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:42:00 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:42:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6853f8064ec51113b4645a988f1bdc942c5c3694bb5d90cd96a95859d6b26053`  
		Last Modified: Thu, 17 Oct 2024 04:44:01 GMT  
		Size: 106.4 MB (106365300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b58b2064b9890c49b8c5020ffbde0cf3c1066142f17363d58326fcbd7e6152`  
		Last Modified: Thu, 17 Oct 2024 04:43:50 GMT  
		Size: 21.6 MB (21635387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba790bc30420d4462ef8f3efed9213829bdf63fb0ce3eee2305cfb824f37478`  
		Last Modified: Thu, 17 Oct 2024 04:43:48 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e4114d6e8bdb5752b03b60d5e65dca567c1af2d4f9944b5f69208e3d4ce5a5`  
		Last Modified: Thu, 17 Oct 2024 04:47:25 GMT  
		Size: 279.4 MB (279374284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:2d91a28995d2470fa5b00d0e3095f30478963724c80639d318255ce4dcbaf20b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.6 MB (455640232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d21e39f0f8776f22d54334faf74dd2cd4f8a50bcfd0296ec13346c1f7b8f7ed`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:44:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:45:00 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:45:02 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:49:24 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:49:24 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:50:59 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:51:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:51:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f3c53d7fd04a3d7c59254dfc2c251f01e10e4e270cee01a62ccc378dd5fa2`  
		Last Modified: Thu, 17 Oct 2024 04:52:58 GMT  
		Size: 101.9 MB (101852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b39c59cb56b844c7697a89fba53c8211ac9d9afe62a6d84bb852cc0ec0a198`  
		Last Modified: Thu, 17 Oct 2024 04:52:51 GMT  
		Size: 23.9 MB (23858505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d3be321a1df021cb7bdd6dda46673f5c7a355fb5acea251db7638b702ef7c`  
		Last Modified: Thu, 17 Oct 2024 04:52:49 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02ca30649a87ab29a0dd6825326f7b54c96668241f18b457cae71195d99bfdb`  
		Last Modified: Thu, 17 Oct 2024 04:56:07 GMT  
		Size: 289.7 MB (289735297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.6.6-slim-bullseye`

```console
$ docker pull haskell@sha256:3e3088ee88b1b1ff731c7e1a29a7b02d89c22f31587053444e7d207e4c933376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9.6.6-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:b45395bb20d4559f4caae5d28d2e5eb7383697569bf0b0b8bb983c009feca83c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.8 MB (446807819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee3b3fe0512d6e050914af9c2168741596bde7d5b8bc3260ef62083c268da0a`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:35:23 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:35:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:35:48 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:35:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:40:11 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:40:11 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:41:54 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:42:00 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:42:00 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6853f8064ec51113b4645a988f1bdc942c5c3694bb5d90cd96a95859d6b26053`  
		Last Modified: Thu, 17 Oct 2024 04:44:01 GMT  
		Size: 106.4 MB (106365300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b58b2064b9890c49b8c5020ffbde0cf3c1066142f17363d58326fcbd7e6152`  
		Last Modified: Thu, 17 Oct 2024 04:43:50 GMT  
		Size: 21.6 MB (21635387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba790bc30420d4462ef8f3efed9213829bdf63fb0ce3eee2305cfb824f37478`  
		Last Modified: Thu, 17 Oct 2024 04:43:48 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e4114d6e8bdb5752b03b60d5e65dca567c1af2d4f9944b5f69208e3d4ce5a5`  
		Last Modified: Thu, 17 Oct 2024 04:47:25 GMT  
		Size: 279.4 MB (279374284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9.6.6-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:2d91a28995d2470fa5b00d0e3095f30478963724c80639d318255ce4dcbaf20b
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.6 MB (455640232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d21e39f0f8776f22d54334faf74dd2cd4f8a50bcfd0296ec13346c1f7b8f7ed`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:44:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:45:00 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:45:02 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:49:24 GMT
ARG GHC=9.6.6
# Thu, 17 Oct 2024 04:49:24 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 17 Oct 2024 04:50:59 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:51:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:51:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f3c53d7fd04a3d7c59254dfc2c251f01e10e4e270cee01a62ccc378dd5fa2`  
		Last Modified: Thu, 17 Oct 2024 04:52:58 GMT  
		Size: 101.9 MB (101852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b39c59cb56b844c7697a89fba53c8211ac9d9afe62a6d84bb852cc0ec0a198`  
		Last Modified: Thu, 17 Oct 2024 04:52:51 GMT  
		Size: 23.9 MB (23858505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d3be321a1df021cb7bdd6dda46673f5c7a355fb5acea251db7638b702ef7c`  
		Last Modified: Thu, 17 Oct 2024 04:52:49 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02ca30649a87ab29a0dd6825326f7b54c96668241f18b457cae71195d99bfdb`  
		Last Modified: Thu, 17 Oct 2024 04:56:07 GMT  
		Size: 289.7 MB (289735297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:bullseye`

```console
$ docker pull haskell@sha256:9289097b6a630f9e4676b55c517cec338150f4df275c9286c7b072cea01910f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f20e66216fe57d95c3329c20c4cd58e9a0c8a0a3e2653f8add73d44ddb89a97f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657462230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782e1ef65169600827778cb69a5466aa343b955eb347646a3c781b6c23773263`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:33:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:33:11 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:33:13 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:35:11 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:35:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:35:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533e2a209f7f1132d0afdf989885257f4434723eddd8ae533fc4fa1944f3905`  
		Last Modified: Thu, 17 Oct 2024 04:42:32 GMT  
		Size: 133.7 MB (133667875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c05726d106d3b71751923c64820381a90be1b01981209b9af10ad0b56d1f55`  
		Last Modified: Thu, 17 Oct 2024 04:42:19 GMT  
		Size: 21.6 MB (21635384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5145e73a21b1ec2a9b987c8cdd0ae25bf78a9550e04d9d2f8dc451ab9d12a2`  
		Last Modified: Thu, 17 Oct 2024 04:42:17 GMT  
		Size: 8.0 MB (8004047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1490bd509801f1867561ea786e4e2bffa3a20b6b0fc502a9d9448327a89c82`  
		Last Modified: Thu, 17 Oct 2024 04:43:32 GMT  
		Size: 439.1 MB (439074313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c709da4ddef97cb8908b9076cbc31c7e92c868f29d207f965dfa3133a27228f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.3 MB (663330258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047ae6a523c6133ba89bc6b8850b6a481d682b5095f1b4010bf37976bbf69fde`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:42:00 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:42:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:42:23 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:42:25 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:44:12 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:44:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:44:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71778b6c993471915955cce00cac8c2cc2c7d390e9aeab982a767155e0bb8bf8`  
		Last Modified: Thu, 17 Oct 2024 04:51:41 GMT  
		Size: 129.1 MB (129144009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943c2985ca4521e081a0f8a9bd1fbe7c8b1e2c0da522ca8eb3f2216e07c2ce5`  
		Last Modified: Thu, 17 Oct 2024 04:51:30 GMT  
		Size: 23.9 MB (23858540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4257fb0fcf27cdc7d362396c8f224ef6c530094d6c72cbfe1a87bc13686ae5`  
		Last Modified: Thu, 17 Oct 2024 04:51:29 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0485b3d149db3b54d75f3220ed9665e354df81ee88ffe97ad82d094475225519`  
		Last Modified: Thu, 17 Oct 2024 04:52:34 GMT  
		Size: 446.5 MB (446474548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:9289097b6a630f9e4676b55c517cec338150f4df275c9286c7b072cea01910f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:f20e66216fe57d95c3329c20c4cd58e9a0c8a0a3e2653f8add73d44ddb89a97f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.5 MB (657462230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:782e1ef65169600827778cb69a5466aa343b955eb347646a3c781b6c23773263`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:39 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 17 Oct 2024 00:20:39 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:32:44 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:33:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:33:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:33:11 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:33:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:33:13 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:33:14 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:35:11 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:35:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:35:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9533e2a209f7f1132d0afdf989885257f4434723eddd8ae533fc4fa1944f3905`  
		Last Modified: Thu, 17 Oct 2024 04:42:32 GMT  
		Size: 133.7 MB (133667875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c05726d106d3b71751923c64820381a90be1b01981209b9af10ad0b56d1f55`  
		Last Modified: Thu, 17 Oct 2024 04:42:19 GMT  
		Size: 21.6 MB (21635384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5145e73a21b1ec2a9b987c8cdd0ae25bf78a9550e04d9d2f8dc451ab9d12a2`  
		Last Modified: Thu, 17 Oct 2024 04:42:17 GMT  
		Size: 8.0 MB (8004047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d1490bd509801f1867561ea786e4e2bffa3a20b6b0fc502a9d9448327a89c82`  
		Last Modified: Thu, 17 Oct 2024 04:43:32 GMT  
		Size: 439.1 MB (439074313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:c709da4ddef97cb8908b9076cbc31c7e92c868f29d207f965dfa3133a27228f9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.3 MB (663330258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047ae6a523c6133ba89bc6b8850b6a481d682b5095f1b4010bf37976bbf69fde`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:05 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 17 Oct 2024 01:12:06 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:42:00 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:42:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:42:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:42:23 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:42:23 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:42:25 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:42:25 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:44:12 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:44:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:44:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71778b6c993471915955cce00cac8c2cc2c7d390e9aeab982a767155e0bb8bf8`  
		Last Modified: Thu, 17 Oct 2024 04:51:41 GMT  
		Size: 129.1 MB (129144009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c943c2985ca4521e081a0f8a9bd1fbe7c8b1e2c0da522ca8eb3f2216e07c2ce5`  
		Last Modified: Thu, 17 Oct 2024 04:51:30 GMT  
		Size: 23.9 MB (23858540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4257fb0fcf27cdc7d362396c8f224ef6c530094d6c72cbfe1a87bc13686ae5`  
		Last Modified: Thu, 17 Oct 2024 04:51:29 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0485b3d149db3b54d75f3220ed9665e354df81ee88ffe97ad82d094475225519`  
		Last Modified: Thu, 17 Oct 2024 04:52:34 GMT  
		Size: 446.5 MB (446474548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim`

```console
$ docker pull haskell@sha256:b54e8944575a100879f489ef270a7111d2698609a327f70c8c861fab87ee800f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:76a334d11f696e1e0b7c944021fe40a76253cf54cefe4ebddba3613ce48db081
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606507229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614e867b9ab57c06746ad709710f00ac1d118eb8e8ea5458325daddfe929c81`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:35:23 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:35:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:35:48 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:35:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:37:47 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:37:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:37:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6853f8064ec51113b4645a988f1bdc942c5c3694bb5d90cd96a95859d6b26053`  
		Last Modified: Thu, 17 Oct 2024 04:44:01 GMT  
		Size: 106.4 MB (106365300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b58b2064b9890c49b8c5020ffbde0cf3c1066142f17363d58326fcbd7e6152`  
		Last Modified: Thu, 17 Oct 2024 04:43:50 GMT  
		Size: 21.6 MB (21635387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba790bc30420d4462ef8f3efed9213829bdf63fb0ce3eee2305cfb824f37478`  
		Last Modified: Thu, 17 Oct 2024 04:43:48 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1c65660167fbd58d254ed1434e87c48e6a1baddec615135ffe6ea09597178c`  
		Last Modified: Thu, 17 Oct 2024 04:45:02 GMT  
		Size: 439.1 MB (439073694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:997dddb457c9712d96cb6ac719adce04aa93db4404953861e9298b12edbd1526
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.4 MB (612380863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b761a049ff58b72ee18bb8173ecb18e0fde91a590e5a56d4fa9b6801845d02d0`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:44:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:45:00 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:45:02 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:46:51 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:47:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:47:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f3c53d7fd04a3d7c59254dfc2c251f01e10e4e270cee01a62ccc378dd5fa2`  
		Last Modified: Thu, 17 Oct 2024 04:52:58 GMT  
		Size: 101.9 MB (101852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b39c59cb56b844c7697a89fba53c8211ac9d9afe62a6d84bb852cc0ec0a198`  
		Last Modified: Thu, 17 Oct 2024 04:52:51 GMT  
		Size: 23.9 MB (23858505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d3be321a1df021cb7bdd6dda46673f5c7a355fb5acea251db7638b702ef7c`  
		Last Modified: Thu, 17 Oct 2024 04:52:49 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03169dc144345133bd6bcdc887b59c7cfca72e1e1f89b254fd33b2e865a42cd5`  
		Last Modified: Thu, 17 Oct 2024 04:53:54 GMT  
		Size: 446.5 MB (446475928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:slim-bullseye`

```console
$ docker pull haskell@sha256:b54e8944575a100879f489ef270a7111d2698609a327f70c8c861fab87ee800f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:76a334d11f696e1e0b7c944021fe40a76253cf54cefe4ebddba3613ce48db081
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.5 MB (606507229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5614e867b9ab57c06746ad709710f00ac1d118eb8e8ea5458325daddfe929c81`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 00:20:51 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 17 Oct 2024 00:20:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:35:23 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:35:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:35:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:35:48 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:35:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:35:50 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:35:50 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:37:47 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:37:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:37:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6853f8064ec51113b4645a988f1bdc942c5c3694bb5d90cd96a95859d6b26053`  
		Last Modified: Thu, 17 Oct 2024 04:44:01 GMT  
		Size: 106.4 MB (106365300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b58b2064b9890c49b8c5020ffbde0cf3c1066142f17363d58326fcbd7e6152`  
		Last Modified: Thu, 17 Oct 2024 04:43:50 GMT  
		Size: 21.6 MB (21635387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba790bc30420d4462ef8f3efed9213829bdf63fb0ce3eee2305cfb824f37478`  
		Last Modified: Thu, 17 Oct 2024 04:43:48 GMT  
		Size: 8.0 MB (8004048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1c65660167fbd58d254ed1434e87c48e6a1baddec615135ffe6ea09597178c`  
		Last Modified: Thu, 17 Oct 2024 04:45:02 GMT  
		Size: 439.1 MB (439073694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:997dddb457c9712d96cb6ac719adce04aa93db4404953861e9298b12edbd1526
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.4 MB (612380863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b761a049ff58b72ee18bb8173ecb18e0fde91a590e5a56d4fa9b6801845d02d0`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 17 Oct 2024 01:12:13 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 17 Oct 2024 01:12:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 04:44:38 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2024 04:44:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK=3.1.1
# Thu, 17 Oct 2024 04:44:56 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 17 Oct 2024 04:45:00 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 17 Oct 2024 04:45:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 17 Oct 2024 04:45:02 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC=9.10.1
# Thu, 17 Oct 2024 04:45:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 17 Oct 2024 04:46:51 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Thu, 17 Oct 2024 04:47:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2024 04:47:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f01f3c53d7fd04a3d7c59254dfc2c251f01e10e4e270cee01a62ccc378dd5fa2`  
		Last Modified: Thu, 17 Oct 2024 04:52:58 GMT  
		Size: 101.9 MB (101852407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48b39c59cb56b844c7697a89fba53c8211ac9d9afe62a6d84bb852cc0ec0a198`  
		Last Modified: Thu, 17 Oct 2024 04:52:51 GMT  
		Size: 23.9 MB (23858505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115d3be321a1df021cb7bdd6dda46673f5c7a355fb5acea251db7638b702ef7c`  
		Last Modified: Thu, 17 Oct 2024 04:52:49 GMT  
		Size: 10.1 MB (10118266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03169dc144345133bd6bcdc887b59c7cfca72e1e1f89b254fd33b2e865a42cd5`  
		Last Modified: Thu, 17 Oct 2024 04:53:54 GMT  
		Size: 446.5 MB (446475928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
