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
$ docker pull haskell@sha256:5e08516a4fd13c48d22797c951c6e16ffda608da143dd9cbe5815b4ef1011337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:eb21b07abb915d5c68549a1e60b26ea484b40e29ad0f62e018c5a39fd0d78fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.3 MB (657278662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af874785f1fcee41e111c9e05adeded192f15a7a2a99ff51e7de2eed930eb27`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22677557f04c2c5f502453272eb2ddfff5e9987d79def541eba9e4148c3b1788`  
		Last Modified: Tue, 12 Nov 2024 02:05:37 GMT  
		Size: 133.5 MB (133465533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761f03c7787040f4a9084bbd05591f227ea792206e320c0f2132d3cebbb208ff`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd65be81f63555d7214c2ee2f895b5cdc4212c2df77d957f5d793cc3d2c238e`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 8.0 MB (8003993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dacef6f44feb22336740f78724f1360770ddd2cb39fa3c55f737e0a937ab0e`  
		Last Modified: Tue, 12 Nov 2024 02:05:42 GMT  
		Size: 439.1 MB (439065047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9` - unknown; unknown

```console
$ docker pull haskell@sha256:aaa79158007aa6cfb429503b2115ec5ab2f82978d2778507c9370b5984d18568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9247851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25206c1c3999974f6fe38c644cb50280e768122352f482e0b23528dc5cf5999`

```dockerfile
```

-	Layers:
	-	`sha256:2e2d9b1a03fda50b14a8795a02a8d5341a5a9cf99dd0d7ccedc5a73724fb5e78`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 9.2 MB (9221612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c19d26835a02aab0b142dff9d0dc9d809b6f0ac3473f685988f484d88749df`  
		Last Modified: Tue, 12 Nov 2024 02:05:35 GMT  
		Size: 26.2 KB (26239 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e497d749e328bfe91867420976cb49e6c85a1878288a5859677af30ae0616193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.2 MB (663152118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96662e2d295c409dd249fb27d285f6573d1564e0f6d0e1594697bf31e072f18d`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d8d00371e2e7b40542b740d20a4c9e93e348e6fbe9e3aa7eb7a49b9665f21`  
		Last Modified: Tue, 12 Nov 2024 02:56:10 GMT  
		Size: 128.9 MB (128939082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d342905770afdf31d822922383c6ee818f7f7b39f0263bc5bd40c5c60722276`  
		Last Modified: Tue, 12 Nov 2024 02:56:08 GMT  
		Size: 23.9 MB (23858434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0551fcb5fbb4bc0cceb5f416167d16cec945e6b024c41639269a8e134e2e6d7`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 10.1 MB (10118237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb6ab606bf2c5c9bd189cbe7d090cea88527ee92f455a2f3116116e28f684d0`  
		Last Modified: Tue, 12 Nov 2024 02:56:18 GMT  
		Size: 446.5 MB (446479293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9` - unknown; unknown

```console
$ docker pull haskell@sha256:19dc2d860390cd6df5d1fc3ed24f9d366933d7995e629a297580679939604b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9249589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ff21abf28e3e13ced40e808b9bdb9c969187d5166fe303a755772fea74965f`

```dockerfile
```

-	Layers:
	-	`sha256:bf597b52b0e99a2def071aa2d5787b898a4b52c8753c5ef40f7bd42457a83dc9`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 9.2 MB (9223175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba2bb8ee587de7c0e27d08bc14f75e2cc4f82c7e261ecac76478a50bb78dedb`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 26.4 KB (26414 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-bullseye`

```console
$ docker pull haskell@sha256:5e08516a4fd13c48d22797c951c6e16ffda608da143dd9cbe5815b4ef1011337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:eb21b07abb915d5c68549a1e60b26ea484b40e29ad0f62e018c5a39fd0d78fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.3 MB (657278662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af874785f1fcee41e111c9e05adeded192f15a7a2a99ff51e7de2eed930eb27`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22677557f04c2c5f502453272eb2ddfff5e9987d79def541eba9e4148c3b1788`  
		Last Modified: Tue, 12 Nov 2024 02:05:37 GMT  
		Size: 133.5 MB (133465533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761f03c7787040f4a9084bbd05591f227ea792206e320c0f2132d3cebbb208ff`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd65be81f63555d7214c2ee2f895b5cdc4212c2df77d957f5d793cc3d2c238e`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 8.0 MB (8003993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dacef6f44feb22336740f78724f1360770ddd2cb39fa3c55f737e0a937ab0e`  
		Last Modified: Tue, 12 Nov 2024 02:05:42 GMT  
		Size: 439.1 MB (439065047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:aaa79158007aa6cfb429503b2115ec5ab2f82978d2778507c9370b5984d18568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9247851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25206c1c3999974f6fe38c644cb50280e768122352f482e0b23528dc5cf5999`

```dockerfile
```

-	Layers:
	-	`sha256:2e2d9b1a03fda50b14a8795a02a8d5341a5a9cf99dd0d7ccedc5a73724fb5e78`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 9.2 MB (9221612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c19d26835a02aab0b142dff9d0dc9d809b6f0ac3473f685988f484d88749df`  
		Last Modified: Tue, 12 Nov 2024 02:05:35 GMT  
		Size: 26.2 KB (26239 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e497d749e328bfe91867420976cb49e6c85a1878288a5859677af30ae0616193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.2 MB (663152118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96662e2d295c409dd249fb27d285f6573d1564e0f6d0e1594697bf31e072f18d`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d8d00371e2e7b40542b740d20a4c9e93e348e6fbe9e3aa7eb7a49b9665f21`  
		Last Modified: Tue, 12 Nov 2024 02:56:10 GMT  
		Size: 128.9 MB (128939082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d342905770afdf31d822922383c6ee818f7f7b39f0263bc5bd40c5c60722276`  
		Last Modified: Tue, 12 Nov 2024 02:56:08 GMT  
		Size: 23.9 MB (23858434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0551fcb5fbb4bc0cceb5f416167d16cec945e6b024c41639269a8e134e2e6d7`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 10.1 MB (10118237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb6ab606bf2c5c9bd189cbe7d090cea88527ee92f455a2f3116116e28f684d0`  
		Last Modified: Tue, 12 Nov 2024 02:56:18 GMT  
		Size: 446.5 MB (446479293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:19dc2d860390cd6df5d1fc3ed24f9d366933d7995e629a297580679939604b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9249589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ff21abf28e3e13ced40e808b9bdb9c969187d5166fe303a755772fea74965f`

```dockerfile
```

-	Layers:
	-	`sha256:bf597b52b0e99a2def071aa2d5787b898a4b52c8753c5ef40f7bd42457a83dc9`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 9.2 MB (9223175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba2bb8ee587de7c0e27d08bc14f75e2cc4f82c7e261ecac76478a50bb78dedb`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 26.4 KB (26414 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:6b5eef6a067bf18998088bb84710328e738096ae706099f5d4a15590bfd7bdd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:10786f2bc84220ad238b08fde58a2a71d7f14b1a01d9804e1418ac9736174219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.3 MB (606325189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352947a574330c0f506e1d0e268563be282eca5be96bb761dd45b0572a562a1b`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55589ce86d9ab62bee6eb57404aa4d74f66fa19602bfc9a8ff5319ebda246a1`  
		Last Modified: Tue, 12 Nov 2024 02:05:33 GMT  
		Size: 106.2 MB (106165547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca083f05228141441bded503ea2632c5046b643675dfa2281847754f53794bb`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 21.6 MB (21635310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac68d5f112a8a9f40485fe96f7abd6a3e2b173744bedcb065a54d01a4750cf`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 8.0 MB (8003992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb6058904372757735da5db92e2bb91645b5ff1c7a170991bc06cd8fb118db`  
		Last Modified: Tue, 12 Nov 2024 02:05:38 GMT  
		Size: 439.1 MB (439068779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:dcbb1dc816ee3397648a97fc4b949ea13b5a39951d1ed10000a206ef735d1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6601781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7709c014028ddb2d3229e0fcaa6d64419990ba8cfe7784e7fbea64928258f41`

```dockerfile
```

-	Layers:
	-	`sha256:15ceee96e8dd9df6138930490c664fbf6e9fa80b76f5dba0c303d2407bd42772`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 6.6 MB (6575477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9db4cca4e25a569068990bb0bc20ca67504890227de6a7dff32127c68917df`  
		Last Modified: Tue, 12 Nov 2024 02:05:31 GMT  
		Size: 26.3 KB (26304 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:06183701126c89d6fdc8293fc113dd1402a0d954e3e48b36e7bb1b3dfe5ab977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.2 MB (612208868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab1c248ffd50882193ed988a1bdd29e3f6697434d6131180757efa778cdda9`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e8b3f0cc178385a51ad68a206d52bc4b3fcd448831411e23411fd7e80aba0`  
		Last Modified: Tue, 12 Nov 2024 03:00:19 GMT  
		Size: 101.7 MB (101659657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8215a07b8bb8b861a6456ae3ad7292ce133b2099b3cc8696820ad419a7395`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 23.9 MB (23858407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c16122dfefec93c836ac69da5fa70576df559098feecc611cd500d34c3ece2`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 10.1 MB (10118220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11c1871237a126594e5824d2cd67d890b64221a0e9c4801d82b87a38023bb3c`  
		Last Modified: Tue, 12 Nov 2024 03:00:26 GMT  
		Size: 446.5 MB (446480984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:2d5770c5314ecc44ec1b2cae2863ae231c5644ec3ae823882aaf1a1b6e51ee5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6604783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299d49982a4719f297e8a2b6db5cdb6ad25d32c3358542313a27168550b5e627`

```dockerfile
```

-	Layers:
	-	`sha256:646726145ad3515e883dad6b77b4039dd643cffb32a124f169300547511ebf0b`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 6.6 MB (6578304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec3c5cf8f0f2a0e2eb5a15be33a852a4b1b0836194978c3a5f7422de9f16784`  
		Last Modified: Tue, 12 Nov 2024 03:00:16 GMT  
		Size: 26.5 KB (26479 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim-bullseye`

```console
$ docker pull haskell@sha256:6b5eef6a067bf18998088bb84710328e738096ae706099f5d4a15590bfd7bdd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:10786f2bc84220ad238b08fde58a2a71d7f14b1a01d9804e1418ac9736174219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.3 MB (606325189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352947a574330c0f506e1d0e268563be282eca5be96bb761dd45b0572a562a1b`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55589ce86d9ab62bee6eb57404aa4d74f66fa19602bfc9a8ff5319ebda246a1`  
		Last Modified: Tue, 12 Nov 2024 02:05:33 GMT  
		Size: 106.2 MB (106165547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca083f05228141441bded503ea2632c5046b643675dfa2281847754f53794bb`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 21.6 MB (21635310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac68d5f112a8a9f40485fe96f7abd6a3e2b173744bedcb065a54d01a4750cf`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 8.0 MB (8003992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb6058904372757735da5db92e2bb91645b5ff1c7a170991bc06cd8fb118db`  
		Last Modified: Tue, 12 Nov 2024 02:05:38 GMT  
		Size: 439.1 MB (439068779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:dcbb1dc816ee3397648a97fc4b949ea13b5a39951d1ed10000a206ef735d1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6601781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7709c014028ddb2d3229e0fcaa6d64419990ba8cfe7784e7fbea64928258f41`

```dockerfile
```

-	Layers:
	-	`sha256:15ceee96e8dd9df6138930490c664fbf6e9fa80b76f5dba0c303d2407bd42772`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 6.6 MB (6575477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9db4cca4e25a569068990bb0bc20ca67504890227de6a7dff32127c68917df`  
		Last Modified: Tue, 12 Nov 2024 02:05:31 GMT  
		Size: 26.3 KB (26304 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:06183701126c89d6fdc8293fc113dd1402a0d954e3e48b36e7bb1b3dfe5ab977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.2 MB (612208868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab1c248ffd50882193ed988a1bdd29e3f6697434d6131180757efa778cdda9`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e8b3f0cc178385a51ad68a206d52bc4b3fcd448831411e23411fd7e80aba0`  
		Last Modified: Tue, 12 Nov 2024 03:00:19 GMT  
		Size: 101.7 MB (101659657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8215a07b8bb8b861a6456ae3ad7292ce133b2099b3cc8696820ad419a7395`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 23.9 MB (23858407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c16122dfefec93c836ac69da5fa70576df559098feecc611cd500d34c3ece2`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 10.1 MB (10118220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11c1871237a126594e5824d2cd67d890b64221a0e9c4801d82b87a38023bb3c`  
		Last Modified: Tue, 12 Nov 2024 03:00:26 GMT  
		Size: 446.5 MB (446480984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:2d5770c5314ecc44ec1b2cae2863ae231c5644ec3ae823882aaf1a1b6e51ee5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6604783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299d49982a4719f297e8a2b6db5cdb6ad25d32c3358542313a27168550b5e627`

```dockerfile
```

-	Layers:
	-	`sha256:646726145ad3515e883dad6b77b4039dd643cffb32a124f169300547511ebf0b`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 6.6 MB (6578304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec3c5cf8f0f2a0e2eb5a15be33a852a4b1b0836194978c3a5f7422de9f16784`  
		Last Modified: Tue, 12 Nov 2024 03:00:16 GMT  
		Size: 26.5 KB (26479 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-bullseye`

```console
$ docker pull haskell@sha256:5e08516a4fd13c48d22797c951c6e16ffda608da143dd9cbe5815b4ef1011337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:eb21b07abb915d5c68549a1e60b26ea484b40e29ad0f62e018c5a39fd0d78fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.3 MB (657278662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af874785f1fcee41e111c9e05adeded192f15a7a2a99ff51e7de2eed930eb27`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22677557f04c2c5f502453272eb2ddfff5e9987d79def541eba9e4148c3b1788`  
		Last Modified: Tue, 12 Nov 2024 02:05:37 GMT  
		Size: 133.5 MB (133465533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761f03c7787040f4a9084bbd05591f227ea792206e320c0f2132d3cebbb208ff`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd65be81f63555d7214c2ee2f895b5cdc4212c2df77d957f5d793cc3d2c238e`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 8.0 MB (8003993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dacef6f44feb22336740f78724f1360770ddd2cb39fa3c55f737e0a937ab0e`  
		Last Modified: Tue, 12 Nov 2024 02:05:42 GMT  
		Size: 439.1 MB (439065047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:aaa79158007aa6cfb429503b2115ec5ab2f82978d2778507c9370b5984d18568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9247851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25206c1c3999974f6fe38c644cb50280e768122352f482e0b23528dc5cf5999`

```dockerfile
```

-	Layers:
	-	`sha256:2e2d9b1a03fda50b14a8795a02a8d5341a5a9cf99dd0d7ccedc5a73724fb5e78`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 9.2 MB (9221612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c19d26835a02aab0b142dff9d0dc9d809b6f0ac3473f685988f484d88749df`  
		Last Modified: Tue, 12 Nov 2024 02:05:35 GMT  
		Size: 26.2 KB (26239 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e497d749e328bfe91867420976cb49e6c85a1878288a5859677af30ae0616193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.2 MB (663152118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96662e2d295c409dd249fb27d285f6573d1564e0f6d0e1594697bf31e072f18d`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d8d00371e2e7b40542b740d20a4c9e93e348e6fbe9e3aa7eb7a49b9665f21`  
		Last Modified: Tue, 12 Nov 2024 02:56:10 GMT  
		Size: 128.9 MB (128939082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d342905770afdf31d822922383c6ee818f7f7b39f0263bc5bd40c5c60722276`  
		Last Modified: Tue, 12 Nov 2024 02:56:08 GMT  
		Size: 23.9 MB (23858434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0551fcb5fbb4bc0cceb5f416167d16cec945e6b024c41639269a8e134e2e6d7`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 10.1 MB (10118237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb6ab606bf2c5c9bd189cbe7d090cea88527ee92f455a2f3116116e28f684d0`  
		Last Modified: Tue, 12 Nov 2024 02:56:18 GMT  
		Size: 446.5 MB (446479293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:19dc2d860390cd6df5d1fc3ed24f9d366933d7995e629a297580679939604b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9249589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ff21abf28e3e13ced40e808b9bdb9c969187d5166fe303a755772fea74965f`

```dockerfile
```

-	Layers:
	-	`sha256:bf597b52b0e99a2def071aa2d5787b898a4b52c8753c5ef40f7bd42457a83dc9`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 9.2 MB (9223175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba2bb8ee587de7c0e27d08bc14f75e2cc4f82c7e261ecac76478a50bb78dedb`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 26.4 KB (26414 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-slim-bullseye`

```console
$ docker pull haskell@sha256:6b5eef6a067bf18998088bb84710328e738096ae706099f5d4a15590bfd7bdd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:10786f2bc84220ad238b08fde58a2a71d7f14b1a01d9804e1418ac9736174219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.3 MB (606325189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352947a574330c0f506e1d0e268563be282eca5be96bb761dd45b0572a562a1b`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55589ce86d9ab62bee6eb57404aa4d74f66fa19602bfc9a8ff5319ebda246a1`  
		Last Modified: Tue, 12 Nov 2024 02:05:33 GMT  
		Size: 106.2 MB (106165547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca083f05228141441bded503ea2632c5046b643675dfa2281847754f53794bb`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 21.6 MB (21635310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac68d5f112a8a9f40485fe96f7abd6a3e2b173744bedcb065a54d01a4750cf`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 8.0 MB (8003992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb6058904372757735da5db92e2bb91645b5ff1c7a170991bc06cd8fb118db`  
		Last Modified: Tue, 12 Nov 2024 02:05:38 GMT  
		Size: 439.1 MB (439068779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:dcbb1dc816ee3397648a97fc4b949ea13b5a39951d1ed10000a206ef735d1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6601781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7709c014028ddb2d3229e0fcaa6d64419990ba8cfe7784e7fbea64928258f41`

```dockerfile
```

-	Layers:
	-	`sha256:15ceee96e8dd9df6138930490c664fbf6e9fa80b76f5dba0c303d2407bd42772`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 6.6 MB (6575477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9db4cca4e25a569068990bb0bc20ca67504890227de6a7dff32127c68917df`  
		Last Modified: Tue, 12 Nov 2024 02:05:31 GMT  
		Size: 26.3 KB (26304 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:06183701126c89d6fdc8293fc113dd1402a0d954e3e48b36e7bb1b3dfe5ab977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.2 MB (612208868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab1c248ffd50882193ed988a1bdd29e3f6697434d6131180757efa778cdda9`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e8b3f0cc178385a51ad68a206d52bc4b3fcd448831411e23411fd7e80aba0`  
		Last Modified: Tue, 12 Nov 2024 03:00:19 GMT  
		Size: 101.7 MB (101659657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8215a07b8bb8b861a6456ae3ad7292ce133b2099b3cc8696820ad419a7395`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 23.9 MB (23858407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c16122dfefec93c836ac69da5fa70576df559098feecc611cd500d34c3ece2`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 10.1 MB (10118220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11c1871237a126594e5824d2cd67d890b64221a0e9c4801d82b87a38023bb3c`  
		Last Modified: Tue, 12 Nov 2024 03:00:26 GMT  
		Size: 446.5 MB (446480984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:2d5770c5314ecc44ec1b2cae2863ae231c5644ec3ae823882aaf1a1b6e51ee5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6604783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299d49982a4719f297e8a2b6db5cdb6ad25d32c3358542313a27168550b5e627`

```dockerfile
```

-	Layers:
	-	`sha256:646726145ad3515e883dad6b77b4039dd643cffb32a124f169300547511ebf0b`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 6.6 MB (6578304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec3c5cf8f0f2a0e2eb5a15be33a852a4b1b0836194978c3a5f7422de9f16784`  
		Last Modified: Tue, 12 Nov 2024 03:00:16 GMT  
		Size: 26.5 KB (26479 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.1-bullseye`

```console
$ docker pull haskell@sha256:5e08516a4fd13c48d22797c951c6e16ffda608da143dd9cbe5815b4ef1011337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.1-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:eb21b07abb915d5c68549a1e60b26ea484b40e29ad0f62e018c5a39fd0d78fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.3 MB (657278662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af874785f1fcee41e111c9e05adeded192f15a7a2a99ff51e7de2eed930eb27`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22677557f04c2c5f502453272eb2ddfff5e9987d79def541eba9e4148c3b1788`  
		Last Modified: Tue, 12 Nov 2024 02:05:37 GMT  
		Size: 133.5 MB (133465533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761f03c7787040f4a9084bbd05591f227ea792206e320c0f2132d3cebbb208ff`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd65be81f63555d7214c2ee2f895b5cdc4212c2df77d957f5d793cc3d2c238e`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 8.0 MB (8003993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dacef6f44feb22336740f78724f1360770ddd2cb39fa3c55f737e0a937ab0e`  
		Last Modified: Tue, 12 Nov 2024 02:05:42 GMT  
		Size: 439.1 MB (439065047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.1-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:aaa79158007aa6cfb429503b2115ec5ab2f82978d2778507c9370b5984d18568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9247851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25206c1c3999974f6fe38c644cb50280e768122352f482e0b23528dc5cf5999`

```dockerfile
```

-	Layers:
	-	`sha256:2e2d9b1a03fda50b14a8795a02a8d5341a5a9cf99dd0d7ccedc5a73724fb5e78`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 9.2 MB (9221612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c19d26835a02aab0b142dff9d0dc9d809b6f0ac3473f685988f484d88749df`  
		Last Modified: Tue, 12 Nov 2024 02:05:35 GMT  
		Size: 26.2 KB (26239 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.1-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e497d749e328bfe91867420976cb49e6c85a1878288a5859677af30ae0616193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.2 MB (663152118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96662e2d295c409dd249fb27d285f6573d1564e0f6d0e1594697bf31e072f18d`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d8d00371e2e7b40542b740d20a4c9e93e348e6fbe9e3aa7eb7a49b9665f21`  
		Last Modified: Tue, 12 Nov 2024 02:56:10 GMT  
		Size: 128.9 MB (128939082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d342905770afdf31d822922383c6ee818f7f7b39f0263bc5bd40c5c60722276`  
		Last Modified: Tue, 12 Nov 2024 02:56:08 GMT  
		Size: 23.9 MB (23858434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0551fcb5fbb4bc0cceb5f416167d16cec945e6b024c41639269a8e134e2e6d7`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 10.1 MB (10118237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb6ab606bf2c5c9bd189cbe7d090cea88527ee92f455a2f3116116e28f684d0`  
		Last Modified: Tue, 12 Nov 2024 02:56:18 GMT  
		Size: 446.5 MB (446479293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.1-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:19dc2d860390cd6df5d1fc3ed24f9d366933d7995e629a297580679939604b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9249589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ff21abf28e3e13ced40e808b9bdb9c969187d5166fe303a755772fea74965f`

```dockerfile
```

-	Layers:
	-	`sha256:bf597b52b0e99a2def071aa2d5787b898a4b52c8753c5ef40f7bd42457a83dc9`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 9.2 MB (9223175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba2bb8ee587de7c0e27d08bc14f75e2cc4f82c7e261ecac76478a50bb78dedb`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 26.4 KB (26414 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.1-slim-bullseye`

```console
$ docker pull haskell@sha256:6b5eef6a067bf18998088bb84710328e738096ae706099f5d4a15590bfd7bdd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.1-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:10786f2bc84220ad238b08fde58a2a71d7f14b1a01d9804e1418ac9736174219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.3 MB (606325189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352947a574330c0f506e1d0e268563be282eca5be96bb761dd45b0572a562a1b`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55589ce86d9ab62bee6eb57404aa4d74f66fa19602bfc9a8ff5319ebda246a1`  
		Last Modified: Tue, 12 Nov 2024 02:05:33 GMT  
		Size: 106.2 MB (106165547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca083f05228141441bded503ea2632c5046b643675dfa2281847754f53794bb`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 21.6 MB (21635310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac68d5f112a8a9f40485fe96f7abd6a3e2b173744bedcb065a54d01a4750cf`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 8.0 MB (8003992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb6058904372757735da5db92e2bb91645b5ff1c7a170991bc06cd8fb118db`  
		Last Modified: Tue, 12 Nov 2024 02:05:38 GMT  
		Size: 439.1 MB (439068779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.1-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:dcbb1dc816ee3397648a97fc4b949ea13b5a39951d1ed10000a206ef735d1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6601781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7709c014028ddb2d3229e0fcaa6d64419990ba8cfe7784e7fbea64928258f41`

```dockerfile
```

-	Layers:
	-	`sha256:15ceee96e8dd9df6138930490c664fbf6e9fa80b76f5dba0c303d2407bd42772`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 6.6 MB (6575477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9db4cca4e25a569068990bb0bc20ca67504890227de6a7dff32127c68917df`  
		Last Modified: Tue, 12 Nov 2024 02:05:31 GMT  
		Size: 26.3 KB (26304 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.1-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:06183701126c89d6fdc8293fc113dd1402a0d954e3e48b36e7bb1b3dfe5ab977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.2 MB (612208868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab1c248ffd50882193ed988a1bdd29e3f6697434d6131180757efa778cdda9`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e8b3f0cc178385a51ad68a206d52bc4b3fcd448831411e23411fd7e80aba0`  
		Last Modified: Tue, 12 Nov 2024 03:00:19 GMT  
		Size: 101.7 MB (101659657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8215a07b8bb8b861a6456ae3ad7292ce133b2099b3cc8696820ad419a7395`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 23.9 MB (23858407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c16122dfefec93c836ac69da5fa70576df559098feecc611cd500d34c3ece2`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 10.1 MB (10118220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11c1871237a126594e5824d2cd67d890b64221a0e9c4801d82b87a38023bb3c`  
		Last Modified: Tue, 12 Nov 2024 03:00:26 GMT  
		Size: 446.5 MB (446480984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.1-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:2d5770c5314ecc44ec1b2cae2863ae231c5644ec3ae823882aaf1a1b6e51ee5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6604783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299d49982a4719f297e8a2b6db5cdb6ad25d32c3358542313a27168550b5e627`

```dockerfile
```

-	Layers:
	-	`sha256:646726145ad3515e883dad6b77b4039dd643cffb32a124f169300547511ebf0b`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 6.6 MB (6578304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec3c5cf8f0f2a0e2eb5a15be33a852a4b1b0836194978c3a5f7422de9f16784`  
		Last Modified: Tue, 12 Nov 2024 03:00:16 GMT  
		Size: 26.5 KB (26479 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6`

```console
$ docker pull haskell@sha256:832c7a4be4fd64fb7d7a56c70a05500df62face42f9f10b52e30fc7b014fac5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6` - linux; amd64

```console
$ docker pull haskell@sha256:6bd6fd238d717c2e4871f09f7dd6098a82952c0a73aa79c3b237b2afd2fc2a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.4 MB (635381032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83e5723a02846dfdf765483a7df05c642ee3f149b1229f5afbde04b3c48e07f`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6a1660a85018c519774c704b99a2e4c8d1796e14a4eb53021e4d662c5d35d6`  
		Last Modified: Tue, 12 Nov 2024 02:05:22 GMT  
		Size: 133.5 MB (133465517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193950265113a9f7274c76f4354a1db8f4453bf653be99ab71dd852c0bd4a5cd`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42447e33ac8aae9aca4196ad5430470c287e19dc4c8f47f25ece476d4c556f25`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 8.0 MB (8003998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7159363bc8549aae0aa7c2ec967c7c5d048e0ecae3ba606a8b13d156e0c325`  
		Last Modified: Tue, 12 Nov 2024 02:05:26 GMT  
		Size: 417.2 MB (417167428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6` - unknown; unknown

```console
$ docker pull haskell@sha256:8bf94be43de8a40b32f33fbfb6e6bb752c17740f747d4927f67bc0728c2e9972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9248706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e5dfeee4da6dcad35500d3dc25ae0bb485d9723bf92e88fec5befba448040`

```dockerfile
```

-	Layers:
	-	`sha256:ba04c49b941f9652b01075af23cfe0ca5493fbe5d0cec941e4a9cff01b3c31e1`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 9.2 MB (9222403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4337b11222e9533ccebce50551cabd13ae0e0cfcae197393e233d55260aec9ae`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 26.3 KB (26303 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e9db82392b6ec0fefb3abf6fb66ce1f842b8b2a59d548cb3a2794a9ef54ca232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.8 MB (647803312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbce8723f87c58163295464813807de64f12fb420f094f63b1907ba747b5097f`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d8d00371e2e7b40542b740d20a4c9e93e348e6fbe9e3aa7eb7a49b9665f21`  
		Last Modified: Tue, 12 Nov 2024 02:56:10 GMT  
		Size: 128.9 MB (128939082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d342905770afdf31d822922383c6ee818f7f7b39f0263bc5bd40c5c60722276`  
		Last Modified: Tue, 12 Nov 2024 02:56:08 GMT  
		Size: 23.9 MB (23858434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0551fcb5fbb4bc0cceb5f416167d16cec945e6b024c41639269a8e134e2e6d7`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 10.1 MB (10118237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8382f28071094481ce71aa1d752ec9b16ce5aebbacd37ff65927ac40ee53ecb`  
		Last Modified: Tue, 12 Nov 2024 03:03:52 GMT  
		Size: 431.1 MB (431130487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6` - unknown; unknown

```console
$ docker pull haskell@sha256:12c48336d17e6fda4e3a5e8d8bac9ce9092cd1613e9b807a3682deb7355a7e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9250395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e861de1cb896fd02df759f76b6ceaf21f2d99df8c3e82297ffc19ead9bd3bf`

```dockerfile
```

-	Layers:
	-	`sha256:d9e1ababcd3361cd87439f712ccda7cd943bba6d59489fa21c0c3755e1b38624`  
		Last Modified: Tue, 12 Nov 2024 03:03:40 GMT  
		Size: 9.2 MB (9223942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b39e29e625d3ebd253f1d4b5fd1277da700856c82448ee3daaef01a9ba515fb`  
		Last Modified: Tue, 12 Nov 2024 03:03:39 GMT  
		Size: 26.5 KB (26453 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-bullseye`

```console
$ docker pull haskell@sha256:832c7a4be4fd64fb7d7a56c70a05500df62face42f9f10b52e30fc7b014fac5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:6bd6fd238d717c2e4871f09f7dd6098a82952c0a73aa79c3b237b2afd2fc2a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.4 MB (635381032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83e5723a02846dfdf765483a7df05c642ee3f149b1229f5afbde04b3c48e07f`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6a1660a85018c519774c704b99a2e4c8d1796e14a4eb53021e4d662c5d35d6`  
		Last Modified: Tue, 12 Nov 2024 02:05:22 GMT  
		Size: 133.5 MB (133465517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193950265113a9f7274c76f4354a1db8f4453bf653be99ab71dd852c0bd4a5cd`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42447e33ac8aae9aca4196ad5430470c287e19dc4c8f47f25ece476d4c556f25`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 8.0 MB (8003998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7159363bc8549aae0aa7c2ec967c7c5d048e0ecae3ba606a8b13d156e0c325`  
		Last Modified: Tue, 12 Nov 2024 02:05:26 GMT  
		Size: 417.2 MB (417167428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:8bf94be43de8a40b32f33fbfb6e6bb752c17740f747d4927f67bc0728c2e9972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9248706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e5dfeee4da6dcad35500d3dc25ae0bb485d9723bf92e88fec5befba448040`

```dockerfile
```

-	Layers:
	-	`sha256:ba04c49b941f9652b01075af23cfe0ca5493fbe5d0cec941e4a9cff01b3c31e1`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 9.2 MB (9222403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4337b11222e9533ccebce50551cabd13ae0e0cfcae197393e233d55260aec9ae`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 26.3 KB (26303 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e9db82392b6ec0fefb3abf6fb66ce1f842b8b2a59d548cb3a2794a9ef54ca232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.8 MB (647803312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbce8723f87c58163295464813807de64f12fb420f094f63b1907ba747b5097f`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d8d00371e2e7b40542b740d20a4c9e93e348e6fbe9e3aa7eb7a49b9665f21`  
		Last Modified: Tue, 12 Nov 2024 02:56:10 GMT  
		Size: 128.9 MB (128939082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d342905770afdf31d822922383c6ee818f7f7b39f0263bc5bd40c5c60722276`  
		Last Modified: Tue, 12 Nov 2024 02:56:08 GMT  
		Size: 23.9 MB (23858434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0551fcb5fbb4bc0cceb5f416167d16cec945e6b024c41639269a8e134e2e6d7`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 10.1 MB (10118237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8382f28071094481ce71aa1d752ec9b16ce5aebbacd37ff65927ac40ee53ecb`  
		Last Modified: Tue, 12 Nov 2024 03:03:52 GMT  
		Size: 431.1 MB (431130487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:12c48336d17e6fda4e3a5e8d8bac9ce9092cd1613e9b807a3682deb7355a7e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9250395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e861de1cb896fd02df759f76b6ceaf21f2d99df8c3e82297ffc19ead9bd3bf`

```dockerfile
```

-	Layers:
	-	`sha256:d9e1ababcd3361cd87439f712ccda7cd943bba6d59489fa21c0c3755e1b38624`  
		Last Modified: Tue, 12 Nov 2024 03:03:40 GMT  
		Size: 9.2 MB (9223942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b39e29e625d3ebd253f1d4b5fd1277da700856c82448ee3daaef01a9ba515fb`  
		Last Modified: Tue, 12 Nov 2024 03:03:39 GMT  
		Size: 26.5 KB (26453 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-slim`

```console
$ docker pull haskell@sha256:febe870a40e4c9be2f2c76464e00fb1cad6639a784b200cbce57a2b708809458
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:600297cad206b02dde1e82f667b38aaf7b1695410b41204920871c7c2a340f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446635424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695ea5037615d42f19d5016b343ed735ae910dff71544197434bd4a2f89a059a`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4523eb2cb215df95498f6bd77d18c8324a8d388dbff0613b1390d1fa63cc8a6f`  
		Last Modified: Tue, 12 Nov 2024 02:04:57 GMT  
		Size: 106.2 MB (106165469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d45044173027914610270695c4f2125bedea9de906196f1a2518c55885428bb`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42447e33ac8aae9aca4196ad5430470c287e19dc4c8f47f25ece476d4c556f25`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 8.0 MB (8003998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aab8e8a77f533e9d26be7aa3e768245e9e71bff4a638f06c8b751801ea7fbb8`  
		Last Modified: Tue, 12 Nov 2024 02:05:00 GMT  
		Size: 279.4 MB (279379087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:bcc31109e29dce9adc131aba75eb99a401561ab1bab2158c1002d1486e55107f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6602968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebc865fcaf63a9ef644f0cb8f21169ab5562c6faac6f548d6c772bd7ce861f9`

```dockerfile
```

-	Layers:
	-	`sha256:9f021da47d38b7c6db10b8b8589c2081f442c118e301220b054983863234d41f`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 6.6 MB (6576262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3398d3439a12a5dc501157bb971e3b1d79d3144803e5c19542757888512c5afd`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 26.7 KB (26706 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e89f17a5341d7fd358ea4a0c5f8fe047cc416b4ab5e2f1042deaeaf153078b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455461101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b98433a61c659bc6087fd13280d18a21c328571d0f0398d3c66fd5fbe5e188e`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e8b3f0cc178385a51ad68a206d52bc4b3fcd448831411e23411fd7e80aba0`  
		Last Modified: Tue, 12 Nov 2024 03:00:19 GMT  
		Size: 101.7 MB (101659657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8215a07b8bb8b861a6456ae3ad7292ce133b2099b3cc8696820ad419a7395`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 23.9 MB (23858407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c16122dfefec93c836ac69da5fa70576df559098feecc611cd500d34c3ece2`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 10.1 MB (10118220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ae0c2f761c8ed0a9ffb8727eb039896eba838dc87de6929b986104cb337dc9`  
		Last Modified: Tue, 12 Nov 2024 03:07:09 GMT  
		Size: 289.7 MB (289733217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:ba2c957d5520848be324574d5d85cc2c0001a13904365c2e8ef0225e9136788b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6605923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaed3ecb0decc61f950e7e1deacd59a13e74c9efc4d4b09a0c2db137489c19b`

```dockerfile
```

-	Layers:
	-	`sha256:c748dfceeb0b596b92d5e21af9397d87fff2116898553f74f72ccd225c04d89f`  
		Last Modified: Tue, 12 Nov 2024 03:06:58 GMT  
		Size: 6.6 MB (6579065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1e44e3fcdc44dd06bdcb6020d3ab8b03f567f9e761f36ff5a3e5b76adae85f`  
		Last Modified: Tue, 12 Nov 2024 03:06:57 GMT  
		Size: 26.9 KB (26858 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-slim-bullseye`

```console
$ docker pull haskell@sha256:febe870a40e4c9be2f2c76464e00fb1cad6639a784b200cbce57a2b708809458
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:600297cad206b02dde1e82f667b38aaf7b1695410b41204920871c7c2a340f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446635424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695ea5037615d42f19d5016b343ed735ae910dff71544197434bd4a2f89a059a`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4523eb2cb215df95498f6bd77d18c8324a8d388dbff0613b1390d1fa63cc8a6f`  
		Last Modified: Tue, 12 Nov 2024 02:04:57 GMT  
		Size: 106.2 MB (106165469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d45044173027914610270695c4f2125bedea9de906196f1a2518c55885428bb`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42447e33ac8aae9aca4196ad5430470c287e19dc4c8f47f25ece476d4c556f25`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 8.0 MB (8003998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aab8e8a77f533e9d26be7aa3e768245e9e71bff4a638f06c8b751801ea7fbb8`  
		Last Modified: Tue, 12 Nov 2024 02:05:00 GMT  
		Size: 279.4 MB (279379087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:bcc31109e29dce9adc131aba75eb99a401561ab1bab2158c1002d1486e55107f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6602968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebc865fcaf63a9ef644f0cb8f21169ab5562c6faac6f548d6c772bd7ce861f9`

```dockerfile
```

-	Layers:
	-	`sha256:9f021da47d38b7c6db10b8b8589c2081f442c118e301220b054983863234d41f`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 6.6 MB (6576262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3398d3439a12a5dc501157bb971e3b1d79d3144803e5c19542757888512c5afd`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 26.7 KB (26706 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e89f17a5341d7fd358ea4a0c5f8fe047cc416b4ab5e2f1042deaeaf153078b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455461101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b98433a61c659bc6087fd13280d18a21c328571d0f0398d3c66fd5fbe5e188e`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e8b3f0cc178385a51ad68a206d52bc4b3fcd448831411e23411fd7e80aba0`  
		Last Modified: Tue, 12 Nov 2024 03:00:19 GMT  
		Size: 101.7 MB (101659657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8215a07b8bb8b861a6456ae3ad7292ce133b2099b3cc8696820ad419a7395`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 23.9 MB (23858407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c16122dfefec93c836ac69da5fa70576df559098feecc611cd500d34c3ece2`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 10.1 MB (10118220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ae0c2f761c8ed0a9ffb8727eb039896eba838dc87de6929b986104cb337dc9`  
		Last Modified: Tue, 12 Nov 2024 03:07:09 GMT  
		Size: 289.7 MB (289733217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:ba2c957d5520848be324574d5d85cc2c0001a13904365c2e8ef0225e9136788b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6605923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaed3ecb0decc61f950e7e1deacd59a13e74c9efc4d4b09a0c2db137489c19b`

```dockerfile
```

-	Layers:
	-	`sha256:c748dfceeb0b596b92d5e21af9397d87fff2116898553f74f72ccd225c04d89f`  
		Last Modified: Tue, 12 Nov 2024 03:06:58 GMT  
		Size: 6.6 MB (6579065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1e44e3fcdc44dd06bdcb6020d3ab8b03f567f9e761f36ff5a3e5b76adae85f`  
		Last Modified: Tue, 12 Nov 2024 03:06:57 GMT  
		Size: 26.9 KB (26858 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.6`

```console
$ docker pull haskell@sha256:832c7a4be4fd64fb7d7a56c70a05500df62face42f9f10b52e30fc7b014fac5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.6` - linux; amd64

```console
$ docker pull haskell@sha256:6bd6fd238d717c2e4871f09f7dd6098a82952c0a73aa79c3b237b2afd2fc2a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.4 MB (635381032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83e5723a02846dfdf765483a7df05c642ee3f149b1229f5afbde04b3c48e07f`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6a1660a85018c519774c704b99a2e4c8d1796e14a4eb53021e4d662c5d35d6`  
		Last Modified: Tue, 12 Nov 2024 02:05:22 GMT  
		Size: 133.5 MB (133465517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193950265113a9f7274c76f4354a1db8f4453bf653be99ab71dd852c0bd4a5cd`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42447e33ac8aae9aca4196ad5430470c287e19dc4c8f47f25ece476d4c556f25`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 8.0 MB (8003998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7159363bc8549aae0aa7c2ec967c7c5d048e0ecae3ba606a8b13d156e0c325`  
		Last Modified: Tue, 12 Nov 2024 02:05:26 GMT  
		Size: 417.2 MB (417167428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.6` - unknown; unknown

```console
$ docker pull haskell@sha256:8bf94be43de8a40b32f33fbfb6e6bb752c17740f747d4927f67bc0728c2e9972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9248706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e5dfeee4da6dcad35500d3dc25ae0bb485d9723bf92e88fec5befba448040`

```dockerfile
```

-	Layers:
	-	`sha256:ba04c49b941f9652b01075af23cfe0ca5493fbe5d0cec941e4a9cff01b3c31e1`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 9.2 MB (9222403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4337b11222e9533ccebce50551cabd13ae0e0cfcae197393e233d55260aec9ae`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 26.3 KB (26303 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e9db82392b6ec0fefb3abf6fb66ce1f842b8b2a59d548cb3a2794a9ef54ca232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.8 MB (647803312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbce8723f87c58163295464813807de64f12fb420f094f63b1907ba747b5097f`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d8d00371e2e7b40542b740d20a4c9e93e348e6fbe9e3aa7eb7a49b9665f21`  
		Last Modified: Tue, 12 Nov 2024 02:56:10 GMT  
		Size: 128.9 MB (128939082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d342905770afdf31d822922383c6ee818f7f7b39f0263bc5bd40c5c60722276`  
		Last Modified: Tue, 12 Nov 2024 02:56:08 GMT  
		Size: 23.9 MB (23858434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0551fcb5fbb4bc0cceb5f416167d16cec945e6b024c41639269a8e134e2e6d7`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 10.1 MB (10118237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8382f28071094481ce71aa1d752ec9b16ce5aebbacd37ff65927ac40ee53ecb`  
		Last Modified: Tue, 12 Nov 2024 03:03:52 GMT  
		Size: 431.1 MB (431130487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.6` - unknown; unknown

```console
$ docker pull haskell@sha256:12c48336d17e6fda4e3a5e8d8bac9ce9092cd1613e9b807a3682deb7355a7e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9250395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e861de1cb896fd02df759f76b6ceaf21f2d99df8c3e82297ffc19ead9bd3bf`

```dockerfile
```

-	Layers:
	-	`sha256:d9e1ababcd3361cd87439f712ccda7cd943bba6d59489fa21c0c3755e1b38624`  
		Last Modified: Tue, 12 Nov 2024 03:03:40 GMT  
		Size: 9.2 MB (9223942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b39e29e625d3ebd253f1d4b5fd1277da700856c82448ee3daaef01a9ba515fb`  
		Last Modified: Tue, 12 Nov 2024 03:03:39 GMT  
		Size: 26.5 KB (26453 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.6-bullseye`

```console
$ docker pull haskell@sha256:832c7a4be4fd64fb7d7a56c70a05500df62face42f9f10b52e30fc7b014fac5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.6-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:6bd6fd238d717c2e4871f09f7dd6098a82952c0a73aa79c3b237b2afd2fc2a69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **635.4 MB (635381032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83e5723a02846dfdf765483a7df05c642ee3f149b1229f5afbde04b3c48e07f`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6a1660a85018c519774c704b99a2e4c8d1796e14a4eb53021e4d662c5d35d6`  
		Last Modified: Tue, 12 Nov 2024 02:05:22 GMT  
		Size: 133.5 MB (133465517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193950265113a9f7274c76f4354a1db8f4453bf653be99ab71dd852c0bd4a5cd`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42447e33ac8aae9aca4196ad5430470c287e19dc4c8f47f25ece476d4c556f25`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 8.0 MB (8003998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7159363bc8549aae0aa7c2ec967c7c5d048e0ecae3ba606a8b13d156e0c325`  
		Last Modified: Tue, 12 Nov 2024 02:05:26 GMT  
		Size: 417.2 MB (417167428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:8bf94be43de8a40b32f33fbfb6e6bb752c17740f747d4927f67bc0728c2e9972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9248706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107e5dfeee4da6dcad35500d3dc25ae0bb485d9723bf92e88fec5befba448040`

```dockerfile
```

-	Layers:
	-	`sha256:ba04c49b941f9652b01075af23cfe0ca5493fbe5d0cec941e4a9cff01b3c31e1`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 9.2 MB (9222403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4337b11222e9533ccebce50551cabd13ae0e0cfcae197393e233d55260aec9ae`  
		Last Modified: Tue, 12 Nov 2024 02:05:20 GMT  
		Size: 26.3 KB (26303 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e9db82392b6ec0fefb3abf6fb66ce1f842b8b2a59d548cb3a2794a9ef54ca232
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **647.8 MB (647803312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbce8723f87c58163295464813807de64f12fb420f094f63b1907ba747b5097f`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d8d00371e2e7b40542b740d20a4c9e93e348e6fbe9e3aa7eb7a49b9665f21`  
		Last Modified: Tue, 12 Nov 2024 02:56:10 GMT  
		Size: 128.9 MB (128939082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d342905770afdf31d822922383c6ee818f7f7b39f0263bc5bd40c5c60722276`  
		Last Modified: Tue, 12 Nov 2024 02:56:08 GMT  
		Size: 23.9 MB (23858434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0551fcb5fbb4bc0cceb5f416167d16cec945e6b024c41639269a8e134e2e6d7`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 10.1 MB (10118237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8382f28071094481ce71aa1d752ec9b16ce5aebbacd37ff65927ac40ee53ecb`  
		Last Modified: Tue, 12 Nov 2024 03:03:52 GMT  
		Size: 431.1 MB (431130487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:12c48336d17e6fda4e3a5e8d8bac9ce9092cd1613e9b807a3682deb7355a7e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9250395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e861de1cb896fd02df759f76b6ceaf21f2d99df8c3e82297ffc19ead9bd3bf`

```dockerfile
```

-	Layers:
	-	`sha256:d9e1ababcd3361cd87439f712ccda7cd943bba6d59489fa21c0c3755e1b38624`  
		Last Modified: Tue, 12 Nov 2024 03:03:40 GMT  
		Size: 9.2 MB (9223942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b39e29e625d3ebd253f1d4b5fd1277da700856c82448ee3daaef01a9ba515fb`  
		Last Modified: Tue, 12 Nov 2024 03:03:39 GMT  
		Size: 26.5 KB (26453 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.6-slim`

```console
$ docker pull haskell@sha256:febe870a40e4c9be2f2c76464e00fb1cad6639a784b200cbce57a2b708809458
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:600297cad206b02dde1e82f667b38aaf7b1695410b41204920871c7c2a340f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446635424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695ea5037615d42f19d5016b343ed735ae910dff71544197434bd4a2f89a059a`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4523eb2cb215df95498f6bd77d18c8324a8d388dbff0613b1390d1fa63cc8a6f`  
		Last Modified: Tue, 12 Nov 2024 02:04:57 GMT  
		Size: 106.2 MB (106165469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d45044173027914610270695c4f2125bedea9de906196f1a2518c55885428bb`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42447e33ac8aae9aca4196ad5430470c287e19dc4c8f47f25ece476d4c556f25`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 8.0 MB (8003998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aab8e8a77f533e9d26be7aa3e768245e9e71bff4a638f06c8b751801ea7fbb8`  
		Last Modified: Tue, 12 Nov 2024 02:05:00 GMT  
		Size: 279.4 MB (279379087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:bcc31109e29dce9adc131aba75eb99a401561ab1bab2158c1002d1486e55107f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6602968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebc865fcaf63a9ef644f0cb8f21169ab5562c6faac6f548d6c772bd7ce861f9`

```dockerfile
```

-	Layers:
	-	`sha256:9f021da47d38b7c6db10b8b8589c2081f442c118e301220b054983863234d41f`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 6.6 MB (6576262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3398d3439a12a5dc501157bb971e3b1d79d3144803e5c19542757888512c5afd`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 26.7 KB (26706 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e89f17a5341d7fd358ea4a0c5f8fe047cc416b4ab5e2f1042deaeaf153078b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455461101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b98433a61c659bc6087fd13280d18a21c328571d0f0398d3c66fd5fbe5e188e`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e8b3f0cc178385a51ad68a206d52bc4b3fcd448831411e23411fd7e80aba0`  
		Last Modified: Tue, 12 Nov 2024 03:00:19 GMT  
		Size: 101.7 MB (101659657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8215a07b8bb8b861a6456ae3ad7292ce133b2099b3cc8696820ad419a7395`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 23.9 MB (23858407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c16122dfefec93c836ac69da5fa70576df559098feecc611cd500d34c3ece2`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 10.1 MB (10118220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ae0c2f761c8ed0a9ffb8727eb039896eba838dc87de6929b986104cb337dc9`  
		Last Modified: Tue, 12 Nov 2024 03:07:09 GMT  
		Size: 289.7 MB (289733217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:ba2c957d5520848be324574d5d85cc2c0001a13904365c2e8ef0225e9136788b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6605923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaed3ecb0decc61f950e7e1deacd59a13e74c9efc4d4b09a0c2db137489c19b`

```dockerfile
```

-	Layers:
	-	`sha256:c748dfceeb0b596b92d5e21af9397d87fff2116898553f74f72ccd225c04d89f`  
		Last Modified: Tue, 12 Nov 2024 03:06:58 GMT  
		Size: 6.6 MB (6579065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1e44e3fcdc44dd06bdcb6020d3ab8b03f567f9e761f36ff5a3e5b76adae85f`  
		Last Modified: Tue, 12 Nov 2024 03:06:57 GMT  
		Size: 26.9 KB (26858 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.6-slim-bullseye`

```console
$ docker pull haskell@sha256:febe870a40e4c9be2f2c76464e00fb1cad6639a784b200cbce57a2b708809458
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.6-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:600297cad206b02dde1e82f667b38aaf7b1695410b41204920871c7c2a340f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **446.6 MB (446635424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:695ea5037615d42f19d5016b343ed735ae910dff71544197434bd4a2f89a059a`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4523eb2cb215df95498f6bd77d18c8324a8d388dbff0613b1390d1fa63cc8a6f`  
		Last Modified: Tue, 12 Nov 2024 02:04:57 GMT  
		Size: 106.2 MB (106165469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d45044173027914610270695c4f2125bedea9de906196f1a2518c55885428bb`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42447e33ac8aae9aca4196ad5430470c287e19dc4c8f47f25ece476d4c556f25`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 8.0 MB (8003998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aab8e8a77f533e9d26be7aa3e768245e9e71bff4a638f06c8b751801ea7fbb8`  
		Last Modified: Tue, 12 Nov 2024 02:05:00 GMT  
		Size: 279.4 MB (279379087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:bcc31109e29dce9adc131aba75eb99a401561ab1bab2158c1002d1486e55107f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6602968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebc865fcaf63a9ef644f0cb8f21169ab5562c6faac6f548d6c772bd7ce861f9`

```dockerfile
```

-	Layers:
	-	`sha256:9f021da47d38b7c6db10b8b8589c2081f442c118e301220b054983863234d41f`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 6.6 MB (6576262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3398d3439a12a5dc501157bb971e3b1d79d3144803e5c19542757888512c5afd`  
		Last Modified: Tue, 12 Nov 2024 02:04:56 GMT  
		Size: 26.7 KB (26706 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.6-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e89f17a5341d7fd358ea4a0c5f8fe047cc416b4ab5e2f1042deaeaf153078b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **455.5 MB (455461101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b98433a61c659bc6087fd13280d18a21c328571d0f0398d3c66fd5fbe5e188e`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.6.6
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.6 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     case "$ARCH" in         'aarch64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";             GHC_SHA256='58d5ce65758ec5179b448e4e1a2f835924b4ada96cf56af80d011bed87d91fef';             ;;         'x86_64')             GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";             GHC_SHA256='a34bdfc1f65b000135d9c8eb12d69670026a64043a8b33ef5ba24b0f8e28d046';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.6/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e8b3f0cc178385a51ad68a206d52bc4b3fcd448831411e23411fd7e80aba0`  
		Last Modified: Tue, 12 Nov 2024 03:00:19 GMT  
		Size: 101.7 MB (101659657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8215a07b8bb8b861a6456ae3ad7292ce133b2099b3cc8696820ad419a7395`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 23.9 MB (23858407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c16122dfefec93c836ac69da5fa70576df559098feecc611cd500d34c3ece2`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 10.1 MB (10118220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ae0c2f761c8ed0a9ffb8727eb039896eba838dc87de6929b986104cb337dc9`  
		Last Modified: Tue, 12 Nov 2024 03:07:09 GMT  
		Size: 289.7 MB (289733217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:ba2c957d5520848be324574d5d85cc2c0001a13904365c2e8ef0225e9136788b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6605923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaed3ecb0decc61f950e7e1deacd59a13e74c9efc4d4b09a0c2db137489c19b`

```dockerfile
```

-	Layers:
	-	`sha256:c748dfceeb0b596b92d5e21af9397d87fff2116898553f74f72ccd225c04d89f`  
		Last Modified: Tue, 12 Nov 2024 03:06:58 GMT  
		Size: 6.6 MB (6579065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e1e44e3fcdc44dd06bdcb6020d3ab8b03f567f9e761f36ff5a3e5b76adae85f`  
		Last Modified: Tue, 12 Nov 2024 03:06:57 GMT  
		Size: 26.9 KB (26858 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:bullseye`

```console
$ docker pull haskell@sha256:5e08516a4fd13c48d22797c951c6e16ffda608da143dd9cbe5815b4ef1011337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:eb21b07abb915d5c68549a1e60b26ea484b40e29ad0f62e018c5a39fd0d78fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.3 MB (657278662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af874785f1fcee41e111c9e05adeded192f15a7a2a99ff51e7de2eed930eb27`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22677557f04c2c5f502453272eb2ddfff5e9987d79def541eba9e4148c3b1788`  
		Last Modified: Tue, 12 Nov 2024 02:05:37 GMT  
		Size: 133.5 MB (133465533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761f03c7787040f4a9084bbd05591f227ea792206e320c0f2132d3cebbb208ff`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd65be81f63555d7214c2ee2f895b5cdc4212c2df77d957f5d793cc3d2c238e`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 8.0 MB (8003993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dacef6f44feb22336740f78724f1360770ddd2cb39fa3c55f737e0a937ab0e`  
		Last Modified: Tue, 12 Nov 2024 02:05:42 GMT  
		Size: 439.1 MB (439065047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:aaa79158007aa6cfb429503b2115ec5ab2f82978d2778507c9370b5984d18568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9247851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25206c1c3999974f6fe38c644cb50280e768122352f482e0b23528dc5cf5999`

```dockerfile
```

-	Layers:
	-	`sha256:2e2d9b1a03fda50b14a8795a02a8d5341a5a9cf99dd0d7ccedc5a73724fb5e78`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 9.2 MB (9221612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c19d26835a02aab0b142dff9d0dc9d809b6f0ac3473f685988f484d88749df`  
		Last Modified: Tue, 12 Nov 2024 02:05:35 GMT  
		Size: 26.2 KB (26239 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e497d749e328bfe91867420976cb49e6c85a1878288a5859677af30ae0616193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.2 MB (663152118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96662e2d295c409dd249fb27d285f6573d1564e0f6d0e1594697bf31e072f18d`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d8d00371e2e7b40542b740d20a4c9e93e348e6fbe9e3aa7eb7a49b9665f21`  
		Last Modified: Tue, 12 Nov 2024 02:56:10 GMT  
		Size: 128.9 MB (128939082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d342905770afdf31d822922383c6ee818f7f7b39f0263bc5bd40c5c60722276`  
		Last Modified: Tue, 12 Nov 2024 02:56:08 GMT  
		Size: 23.9 MB (23858434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0551fcb5fbb4bc0cceb5f416167d16cec945e6b024c41639269a8e134e2e6d7`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 10.1 MB (10118237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb6ab606bf2c5c9bd189cbe7d090cea88527ee92f455a2f3116116e28f684d0`  
		Last Modified: Tue, 12 Nov 2024 02:56:18 GMT  
		Size: 446.5 MB (446479293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:19dc2d860390cd6df5d1fc3ed24f9d366933d7995e629a297580679939604b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9249589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ff21abf28e3e13ced40e808b9bdb9c969187d5166fe303a755772fea74965f`

```dockerfile
```

-	Layers:
	-	`sha256:bf597b52b0e99a2def071aa2d5787b898a4b52c8753c5ef40f7bd42457a83dc9`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 9.2 MB (9223175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba2bb8ee587de7c0e27d08bc14f75e2cc4f82c7e261ecac76478a50bb78dedb`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 26.4 KB (26414 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:latest`

```console
$ docker pull haskell@sha256:5e08516a4fd13c48d22797c951c6e16ffda608da143dd9cbe5815b4ef1011337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:eb21b07abb915d5c68549a1e60b26ea484b40e29ad0f62e018c5a39fd0d78fc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **657.3 MB (657278662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af874785f1fcee41e111c9e05adeded192f15a7a2a99ff51e7de2eed930eb27`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22677557f04c2c5f502453272eb2ddfff5e9987d79def541eba9e4148c3b1788`  
		Last Modified: Tue, 12 Nov 2024 02:05:37 GMT  
		Size: 133.5 MB (133465533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:761f03c7787040f4a9084bbd05591f227ea792206e320c0f2132d3cebbb208ff`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 21.6 MB (21635309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bd65be81f63555d7214c2ee2f895b5cdc4212c2df77d957f5d793cc3d2c238e`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 8.0 MB (8003993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dacef6f44feb22336740f78724f1360770ddd2cb39fa3c55f737e0a937ab0e`  
		Last Modified: Tue, 12 Nov 2024 02:05:42 GMT  
		Size: 439.1 MB (439065047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:aaa79158007aa6cfb429503b2115ec5ab2f82978d2778507c9370b5984d18568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9247851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25206c1c3999974f6fe38c644cb50280e768122352f482e0b23528dc5cf5999`

```dockerfile
```

-	Layers:
	-	`sha256:2e2d9b1a03fda50b14a8795a02a8d5341a5a9cf99dd0d7ccedc5a73724fb5e78`  
		Last Modified: Tue, 12 Nov 2024 02:05:36 GMT  
		Size: 9.2 MB (9221612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8c19d26835a02aab0b142dff9d0dc9d809b6f0ac3473f685988f484d88749df`  
		Last Modified: Tue, 12 Nov 2024 02:05:35 GMT  
		Size: 26.2 KB (26239 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e497d749e328bfe91867420976cb49e6c85a1878288a5859677af30ae0616193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.2 MB (663152118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96662e2d295c409dd249fb27d285f6573d1564e0f6d0e1594697bf31e072f18d`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:a839664fe62f615da74af799f94ccbc890a15d0f78470aac54302c2fd5475615`  
		Last Modified: Tue, 12 Nov 2024 00:57:41 GMT  
		Size: 53.8 MB (53757072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8d8d00371e2e7b40542b740d20a4c9e93e348e6fbe9e3aa7eb7a49b9665f21`  
		Last Modified: Tue, 12 Nov 2024 02:56:10 GMT  
		Size: 128.9 MB (128939082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d342905770afdf31d822922383c6ee818f7f7b39f0263bc5bd40c5c60722276`  
		Last Modified: Tue, 12 Nov 2024 02:56:08 GMT  
		Size: 23.9 MB (23858434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0551fcb5fbb4bc0cceb5f416167d16cec945e6b024c41639269a8e134e2e6d7`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 10.1 MB (10118237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb6ab606bf2c5c9bd189cbe7d090cea88527ee92f455a2f3116116e28f684d0`  
		Last Modified: Tue, 12 Nov 2024 02:56:18 GMT  
		Size: 446.5 MB (446479293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:19dc2d860390cd6df5d1fc3ed24f9d366933d7995e629a297580679939604b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9249589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ff21abf28e3e13ced40e808b9bdb9c969187d5166fe303a755772fea74965f`

```dockerfile
```

-	Layers:
	-	`sha256:bf597b52b0e99a2def071aa2d5787b898a4b52c8753c5ef40f7bd42457a83dc9`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 9.2 MB (9223175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba2bb8ee587de7c0e27d08bc14f75e2cc4f82c7e261ecac76478a50bb78dedb`  
		Last Modified: Tue, 12 Nov 2024 02:56:07 GMT  
		Size: 26.4 KB (26414 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim`

```console
$ docker pull haskell@sha256:6b5eef6a067bf18998088bb84710328e738096ae706099f5d4a15590bfd7bdd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:10786f2bc84220ad238b08fde58a2a71d7f14b1a01d9804e1418ac9736174219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.3 MB (606325189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352947a574330c0f506e1d0e268563be282eca5be96bb761dd45b0572a562a1b`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55589ce86d9ab62bee6eb57404aa4d74f66fa19602bfc9a8ff5319ebda246a1`  
		Last Modified: Tue, 12 Nov 2024 02:05:33 GMT  
		Size: 106.2 MB (106165547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca083f05228141441bded503ea2632c5046b643675dfa2281847754f53794bb`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 21.6 MB (21635310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac68d5f112a8a9f40485fe96f7abd6a3e2b173744bedcb065a54d01a4750cf`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 8.0 MB (8003992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb6058904372757735da5db92e2bb91645b5ff1c7a170991bc06cd8fb118db`  
		Last Modified: Tue, 12 Nov 2024 02:05:38 GMT  
		Size: 439.1 MB (439068779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim` - unknown; unknown

```console
$ docker pull haskell@sha256:dcbb1dc816ee3397648a97fc4b949ea13b5a39951d1ed10000a206ef735d1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6601781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7709c014028ddb2d3229e0fcaa6d64419990ba8cfe7784e7fbea64928258f41`

```dockerfile
```

-	Layers:
	-	`sha256:15ceee96e8dd9df6138930490c664fbf6e9fa80b76f5dba0c303d2407bd42772`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 6.6 MB (6575477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9db4cca4e25a569068990bb0bc20ca67504890227de6a7dff32127c68917df`  
		Last Modified: Tue, 12 Nov 2024 02:05:31 GMT  
		Size: 26.3 KB (26304 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:06183701126c89d6fdc8293fc113dd1402a0d954e3e48b36e7bb1b3dfe5ab977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.2 MB (612208868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab1c248ffd50882193ed988a1bdd29e3f6697434d6131180757efa778cdda9`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e8b3f0cc178385a51ad68a206d52bc4b3fcd448831411e23411fd7e80aba0`  
		Last Modified: Tue, 12 Nov 2024 03:00:19 GMT  
		Size: 101.7 MB (101659657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8215a07b8bb8b861a6456ae3ad7292ce133b2099b3cc8696820ad419a7395`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 23.9 MB (23858407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c16122dfefec93c836ac69da5fa70576df559098feecc611cd500d34c3ece2`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 10.1 MB (10118220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11c1871237a126594e5824d2cd67d890b64221a0e9c4801d82b87a38023bb3c`  
		Last Modified: Tue, 12 Nov 2024 03:00:26 GMT  
		Size: 446.5 MB (446480984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim` - unknown; unknown

```console
$ docker pull haskell@sha256:2d5770c5314ecc44ec1b2cae2863ae231c5644ec3ae823882aaf1a1b6e51ee5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6604783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299d49982a4719f297e8a2b6db5cdb6ad25d32c3358542313a27168550b5e627`

```dockerfile
```

-	Layers:
	-	`sha256:646726145ad3515e883dad6b77b4039dd643cffb32a124f169300547511ebf0b`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 6.6 MB (6578304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec3c5cf8f0f2a0e2eb5a15be33a852a4b1b0836194978c3a5f7422de9f16784`  
		Last Modified: Tue, 12 Nov 2024 03:00:16 GMT  
		Size: 26.5 KB (26479 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim-bullseye`

```console
$ docker pull haskell@sha256:6b5eef6a067bf18998088bb84710328e738096ae706099f5d4a15590bfd7bdd7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:10786f2bc84220ad238b08fde58a2a71d7f14b1a01d9804e1418ac9736174219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **606.3 MB (606325189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352947a574330c0f506e1d0e268563be282eca5be96bb761dd45b0572a562a1b`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:55ab1b300d4b4b00c98fb396b36f0f7ba5dab2f7d18927e3742d364632723cbe`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 31.5 MB (31451561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55589ce86d9ab62bee6eb57404aa4d74f66fa19602bfc9a8ff5319ebda246a1`  
		Last Modified: Tue, 12 Nov 2024 02:05:33 GMT  
		Size: 106.2 MB (106165547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca083f05228141441bded503ea2632c5046b643675dfa2281847754f53794bb`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 21.6 MB (21635310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ac68d5f112a8a9f40485fe96f7abd6a3e2b173744bedcb065a54d01a4750cf`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 8.0 MB (8003992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb6058904372757735da5db92e2bb91645b5ff1c7a170991bc06cd8fb118db`  
		Last Modified: Tue, 12 Nov 2024 02:05:38 GMT  
		Size: 439.1 MB (439068779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:dcbb1dc816ee3397648a97fc4b949ea13b5a39951d1ed10000a206ef735d1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6601781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7709c014028ddb2d3229e0fcaa6d64419990ba8cfe7784e7fbea64928258f41`

```dockerfile
```

-	Layers:
	-	`sha256:15ceee96e8dd9df6138930490c664fbf6e9fa80b76f5dba0c303d2407bd42772`  
		Last Modified: Tue, 12 Nov 2024 02:05:32 GMT  
		Size: 6.6 MB (6575477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e9db4cca4e25a569068990bb0bc20ca67504890227de6a7dff32127c68917df`  
		Last Modified: Tue, 12 Nov 2024 02:05:31 GMT  
		Size: 26.3 KB (26304 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:06183701126c89d6fdc8293fc113dd1402a0d954e3e48b36e7bb1b3dfe5ab977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.2 MB (612208868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eab1c248ffd50882193ed988a1bdd29e3f6697434d6131180757efa778cdda9`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 26 Sep 2024 13:58:54 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["bash"]
# Thu, 26 Sep 2024 13:58:54 GMT
ENV LANG=C.UTF-8
# Thu, 26 Sep 2024 13:58:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK=3.1.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL=3.10.3.0
# Thu, 26 Sep 2024 13:58:54 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='e0b6604d3596c5e5b7236e79ff4f5aa8af337792bf69ac4a90634c761f1b9ed5';             ;;         'x86_64')             CABAL_INSTALL_SHA256='12d018bdd07efed470f278f22d94b33655c4fcbc44d28d97b5ebb7944d5607c5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC=9.10.1
# Thu, 26 Sep 2024 13:58:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 26 Sep 2024 13:58:54 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 26 Sep 2024 13:58:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 26 Sep 2024 13:58:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ac25a60fd56d38d0bc3960243a812295a0e7b11d4ff324470ca32452e930a2d1`  
		Last Modified: Tue, 12 Nov 2024 00:58:02 GMT  
		Size: 30.1 MB (30091600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0e8b3f0cc178385a51ad68a206d52bc4b3fcd448831411e23411fd7e80aba0`  
		Last Modified: Tue, 12 Nov 2024 03:00:19 GMT  
		Size: 101.7 MB (101659657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d8215a07b8bb8b861a6456ae3ad7292ce133b2099b3cc8696820ad419a7395`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 23.9 MB (23858407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c16122dfefec93c836ac69da5fa70576df559098feecc611cd500d34c3ece2`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 10.1 MB (10118220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11c1871237a126594e5824d2cd67d890b64221a0e9c4801d82b87a38023bb3c`  
		Last Modified: Tue, 12 Nov 2024 03:00:26 GMT  
		Size: 446.5 MB (446480984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:2d5770c5314ecc44ec1b2cae2863ae231c5644ec3ae823882aaf1a1b6e51ee5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6604783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299d49982a4719f297e8a2b6db5cdb6ad25d32c3358542313a27168550b5e627`

```dockerfile
```

-	Layers:
	-	`sha256:646726145ad3515e883dad6b77b4039dd643cffb32a124f169300547511ebf0b`  
		Last Modified: Tue, 12 Nov 2024 03:00:17 GMT  
		Size: 6.6 MB (6578304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ec3c5cf8f0f2a0e2eb5a15be33a852a4b1b0836194978c3a5f7422de9f16784`  
		Last Modified: Tue, 12 Nov 2024 03:00:16 GMT  
		Size: 26.5 KB (26479 bytes)  
		MIME: application/vnd.in-toto+json
