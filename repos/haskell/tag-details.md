<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:9`](#haskell9)
-	[`haskell:9-bookworm`](#haskell9-bookworm)
-	[`haskell:9-bullseye`](#haskell9-bullseye)
-	[`haskell:9-slim`](#haskell9-slim)
-	[`haskell:9-slim-bookworm`](#haskell9-slim-bookworm)
-	[`haskell:9-slim-bullseye`](#haskell9-slim-bullseye)
-	[`haskell:9.10`](#haskell910)
-	[`haskell:9.10-bookworm`](#haskell910-bookworm)
-	[`haskell:9.10-bullseye`](#haskell910-bullseye)
-	[`haskell:9.10-slim-bookworm`](#haskell910-slim-bookworm)
-	[`haskell:9.10-slim-bullseye`](#haskell910-slim-bullseye)
-	[`haskell:9.10.3`](#haskell9103)
-	[`haskell:9.10.3-bookworm`](#haskell9103-bookworm)
-	[`haskell:9.10.3-bullseye`](#haskell9103-bullseye)
-	[`haskell:9.10.3-slim-bookworm`](#haskell9103-slim-bookworm)
-	[`haskell:9.10.3-slim-bullseye`](#haskell9103-slim-bullseye)
-	[`haskell:9.12`](#haskell912)
-	[`haskell:9.12-bookworm`](#haskell912-bookworm)
-	[`haskell:9.12-slim-bookworm`](#haskell912-slim-bookworm)
-	[`haskell:9.12.2`](#haskell9122)
-	[`haskell:9.12.2-bookworm`](#haskell9122-bookworm)
-	[`haskell:9.12.2-slim-bookworm`](#haskell9122-slim-bookworm)
-	[`haskell:9.14`](#haskell914)
-	[`haskell:9.14-bookworm`](#haskell914-bookworm)
-	[`haskell:9.14-slim-bookworm`](#haskell914-slim-bookworm)
-	[`haskell:9.14.1`](#haskell9141)
-	[`haskell:9.14.1-bookworm`](#haskell9141-bookworm)
-	[`haskell:9.14.1-slim-bookworm`](#haskell9141-slim-bookworm)
-	[`haskell:9.6`](#haskell96)
-	[`haskell:9.6-bullseye`](#haskell96-bullseye)
-	[`haskell:9.6-slim`](#haskell96-slim)
-	[`haskell:9.6-slim-bullseye`](#haskell96-slim-bullseye)
-	[`haskell:9.6.7`](#haskell967)
-	[`haskell:9.6.7-bullseye`](#haskell967-bullseye)
-	[`haskell:9.6.7-slim`](#haskell967-slim)
-	[`haskell:9.6.7-slim-bullseye`](#haskell967-slim-bullseye)
-	[`haskell:9.8`](#haskell98)
-	[`haskell:9.8-bullseye`](#haskell98-bullseye)
-	[`haskell:9.8-slim`](#haskell98-slim)
-	[`haskell:9.8-slim-bullseye`](#haskell98-slim-bullseye)
-	[`haskell:9.8.4`](#haskell984)
-	[`haskell:9.8.4-bullseye`](#haskell984-bullseye)
-	[`haskell:9.8.4-slim`](#haskell984-slim)
-	[`haskell:9.8.4-slim-bullseye`](#haskell984-slim-bullseye)
-	[`haskell:bookworm`](#haskellbookworm)
-	[`haskell:bullseye`](#haskellbullseye)
-	[`haskell:latest`](#haskelllatest)
-	[`haskell:slim`](#haskellslim)
-	[`haskell:slim-bookworm`](#haskellslim-bookworm)
-	[`haskell:slim-bullseye`](#haskellslim-bullseye)

## `haskell:9`

```console
$ docker pull haskell@sha256:6cff7c33044cc6b6b5944e64860278df5f66e2fd6546526ee7a3f7b2a0bb302d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:1fbcda9feaaf6fdc37f04994416244502ffc60420ac87bf888b2e27fb4a7e3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f2e39e42a486cc41c8abaa23edc4b5bf18f3e6188c3005107b5376e6872757`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:05 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece92b353df31cd62bcf548d31f7e7551ad5001927d632dc72fdb96777c0a7de`  
		Last Modified: Tue, 07 Apr 2026 01:21:59 GMT  
		Size: 152.4 MB (152404537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9003a62dd97b742a849a6ffe605b33afae135ecf9a6963fa71ce25145093e9`  
		Last Modified: Tue, 07 Apr 2026 01:21:54 GMT  
		Size: 22.2 MB (22220764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03444700904b3892922358de25fdfe826f0169360d9f9cb036eeac113f25554c`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920399cab91d6ff0fc2201575339dc055750baca387d9ed10f94ed92d7adde`  
		Last Modified: Tue, 07 Apr 2026 01:22:11 GMT  
		Size: 593.7 MB (593665337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9` - unknown; unknown

```console
$ docker pull haskell@sha256:bb0b5eca366271d9faabc5051de30bf0ca84556d8d2311a229f9e9cfd86ac081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff0ec4d07cfb43474a87b2b0c0dab7ef9b2b9b1f3f76a5dc23866ef5c9b9169`

```dockerfile
```

-	Layers:
	-	`sha256:18227a676aaf76c21c1183a42a01b9a116a151db0b59a0ea80879bdb63f1e15a`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598a0a7da604db5b7571614d65ef77c3d89c33455779d8a7ae9656cacc7e243c`  
		Last Modified: Tue, 07 Apr 2026 01:21:52 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f32d990dc8da74f7f0341a333164cb1c8d6266a8ac9ad4a945b90117efaffa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.0 MB (827973880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0549a54963f5295de9aca4174ea8cd5c882c87f277d02b84d560108488fee`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:13 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8b2b86a1f61fbc06035adfc6d633c1ef0ac985ee5d01ad2035aa975e75bc5e`  
		Last Modified: Tue, 07 Apr 2026 01:22:18 GMT  
		Size: 146.6 MB (146574461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a921e64342db75f8743327ae9f72db69b755625911158c2ba61f7e5cc3c653`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 24.5 MB (24528556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04627812dc4bd20dfe4c8cdc15e97e22dc630d7688a5f6cf80d91b271266ee`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 15.9 MB (15944580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd72aeb1f170c652f08f92801ce519133208478741fd634ac455a534dd7f21`  
		Last Modified: Tue, 07 Apr 2026 01:22:26 GMT  
		Size: 592.6 MB (592553021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9` - unknown; unknown

```console
$ docker pull haskell@sha256:c5ee901f3e234f95818fd514b41636991e5c804c884191726bdfe9d398b131dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9a7278c6d71557554c28d4ca253da3efb5f1beb63668ba7412cd386f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:25ff4331c3bb33056dbba1acea83141c0be05c91a7822f564aa4ec8e37d10405`  
		Last Modified: Tue, 07 Apr 2026 01:22:13 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0c3e47baeb7423641c403b8e392683ef8fc8fa4cf31429b25de36abf9eb3`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-bookworm`

```console
$ docker pull haskell@sha256:6cff7c33044cc6b6b5944e64860278df5f66e2fd6546526ee7a3f7b2a0bb302d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:1fbcda9feaaf6fdc37f04994416244502ffc60420ac87bf888b2e27fb4a7e3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f2e39e42a486cc41c8abaa23edc4b5bf18f3e6188c3005107b5376e6872757`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:05 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece92b353df31cd62bcf548d31f7e7551ad5001927d632dc72fdb96777c0a7de`  
		Last Modified: Tue, 07 Apr 2026 01:21:59 GMT  
		Size: 152.4 MB (152404537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9003a62dd97b742a849a6ffe605b33afae135ecf9a6963fa71ce25145093e9`  
		Last Modified: Tue, 07 Apr 2026 01:21:54 GMT  
		Size: 22.2 MB (22220764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03444700904b3892922358de25fdfe826f0169360d9f9cb036eeac113f25554c`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920399cab91d6ff0fc2201575339dc055750baca387d9ed10f94ed92d7adde`  
		Last Modified: Tue, 07 Apr 2026 01:22:11 GMT  
		Size: 593.7 MB (593665337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:bb0b5eca366271d9faabc5051de30bf0ca84556d8d2311a229f9e9cfd86ac081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff0ec4d07cfb43474a87b2b0c0dab7ef9b2b9b1f3f76a5dc23866ef5c9b9169`

```dockerfile
```

-	Layers:
	-	`sha256:18227a676aaf76c21c1183a42a01b9a116a151db0b59a0ea80879bdb63f1e15a`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598a0a7da604db5b7571614d65ef77c3d89c33455779d8a7ae9656cacc7e243c`  
		Last Modified: Tue, 07 Apr 2026 01:21:52 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f32d990dc8da74f7f0341a333164cb1c8d6266a8ac9ad4a945b90117efaffa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.0 MB (827973880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0549a54963f5295de9aca4174ea8cd5c882c87f277d02b84d560108488fee`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:13 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8b2b86a1f61fbc06035adfc6d633c1ef0ac985ee5d01ad2035aa975e75bc5e`  
		Last Modified: Tue, 07 Apr 2026 01:22:18 GMT  
		Size: 146.6 MB (146574461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a921e64342db75f8743327ae9f72db69b755625911158c2ba61f7e5cc3c653`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 24.5 MB (24528556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04627812dc4bd20dfe4c8cdc15e97e22dc630d7688a5f6cf80d91b271266ee`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 15.9 MB (15944580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd72aeb1f170c652f08f92801ce519133208478741fd634ac455a534dd7f21`  
		Last Modified: Tue, 07 Apr 2026 01:22:26 GMT  
		Size: 592.6 MB (592553021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:c5ee901f3e234f95818fd514b41636991e5c804c884191726bdfe9d398b131dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9a7278c6d71557554c28d4ca253da3efb5f1beb63668ba7412cd386f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:25ff4331c3bb33056dbba1acea83141c0be05c91a7822f564aa4ec8e37d10405`  
		Last Modified: Tue, 07 Apr 2026 01:22:13 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0c3e47baeb7423641c403b8e392683ef8fc8fa4cf31429b25de36abf9eb3`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-bullseye`

```console
$ docker pull haskell@sha256:1434abf2aa95282e46916880a70ed9ee02566ef603698d969ce8371340212576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:40c7aeeca45ca813f36f3e80dea6918b5f9b316ba177eddcb323adcf30f07275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659223113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d840f2cefaa050966550674fb069f56f7ac499d54363561a4930035f5cfaad`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02dda58f98dd1b89ea56dad93ea597ab2d270a4c5488a5080ebfe4e22608c05`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 133.8 MB (133816646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6788ea23b7d8f664d2f75dfca6820d1905f375c4b0709aecf2e28c70adf4fff6`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6537af5e28a47f37be1aa665b630dbb58038dedb64aa2fe86bbc08b1567b095`  
		Last Modified: Tue, 07 Apr 2026 01:21:40 GMT  
		Size: 441.8 MB (441810672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:8b7321c089ffb9d02de572c043af25531fb81f3a1367778a6c10db105f1059d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93647ed1c3cbd8cdc4712413b2170c4c76076508be7f76e44ba8f2d9781b7aca`

```dockerfile
```

-	Layers:
	-	`sha256:7da85245cba7175d03e3f59cb8c744cb7ed18d6d58c00207d1643b72499ae200`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 9.4 MB (9408030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dc7e5b0791b03f692e44b1eeb39a1ffd1ad2ff71636daecd10aed90c468db1`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:efa0a620239a673d67ff573b2139b4db387c710a661a0f5d29c714dcab56061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.5 MB (669473057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b52e39a5e2aa5d80d316672bfb8122b184a94a08aaa270df7836b8ff6bca76`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:51 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c24e51cfa942997e098c6febaa4751e88ae4debf1f5dd07bc9bb72927972c8e`  
		Last Modified: Tue, 07 Apr 2026 01:20:53 GMT  
		Size: 129.3 MB (129273970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ab9ae73c524c4b51e32343734bbc89d93f0ebc83216d04951e9ef1ae57b01`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39dc89c8cb93b86dcf19088b6e096b806448b6954836844ef750d884b6f7ed`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c9395fb5fbcc181b749007653b2871b370c130abf6eba6eca01e3ab56865bd`  
		Last Modified: Tue, 07 Apr 2026 01:21:00 GMT  
		Size: 449.4 MB (449449962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a46ac3fa59dd96825e6b5930fcd7586bc903333e44d1e995b3c8a62d61538a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9435754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85495acd2d5e485183a23106106f0651c1873c05c7e291b51f2964306eb867e0`

```dockerfile
```

-	Layers:
	-	`sha256:88b942987203a63840e9e1594431326625e9b9168303b88fe5eff77a6d2a3af9`  
		Last Modified: Tue, 07 Apr 2026 01:20:47 GMT  
		Size: 9.4 MB (9409302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3837dcc5606b2cab1f0f41a5ade639d7471f70208472385abccb18ae80c7e53c`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:1f0099b81708e859d4d90f43d06187c8298c59d33ddf3bb01cff047131d0ab5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:ec468efccdfee2736254eced8aabda20caeb9a7413f8ba1a8d709c6e2657c264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776932258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2173d21f80bdb483477e015940670f09e33cb2d6136c82f12e7a62aeeae54191`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:01 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345dc3f621eb0094cd075ee66a2755b9c6d79d500a1a801483f92a7448eb3c94`  
		Last Modified: Tue, 07 Apr 2026 01:21:34 GMT  
		Size: 124.4 MB (124405560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47df7d2546cd081cd78569030f2b57711e56cd47e01f054fc6760b7a174ee51`  
		Last Modified: Tue, 07 Apr 2026 01:21:30 GMT  
		Size: 22.2 MB (22220780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bfa68860956218eb86763ac5169ed8198b6bbea47ea40ac15d1ebf0b9b0dff`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 8.4 MB (8403514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c93da93eff076094eefe1d30ebfb37597e0e6b28f746f73abfb52d017cd8a1`  
		Last Modified: Tue, 07 Apr 2026 01:21:45 GMT  
		Size: 593.7 MB (593666072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:f87ce515084b12c2b03afd14820dd24f68118fde8c3c6b8c1e403e1670e9c0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2783973dbc0d33a45942d152c97cdbdbbdd8bbf862118d42f67fea5aa0a1096`

```dockerfile
```

-	Layers:
	-	`sha256:c092357d6ac3da8e3a1826c5b11f41a26405d393fb292b5377971dc7b98e212e`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b95e9b4e1b098e6f3ec57d2b3c6af99d1a8df7b9f3209ff4af0e56079b2e641`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e1c5961de02a9617ad4548c1d388ed811218c2a6fb7d508aba60c74938d44586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779715156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b95888e8c56f17ea52f9af5f94f933872ac70f7e1de2186cd09a803989641dd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:28 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c64a7715b20f0ce9a276abdfad0e377d8a74adaf5d2859c0980c91ae630b4d`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 118.6 MB (118575900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bdb68ff57f6ba1cfef40b68fc13d52d983fea4a32dbb5ba9d9c8e1eead4472`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 24.5 MB (24528540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f297d7be8e2a3dc35e44249b90135de569e0e0a316932ef497d5c7355ee9cc79`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7eff1bbecd608dd9e4f7f8fc78d2ee29abe5147929e545743f63887773827b`  
		Last Modified: Tue, 07 Apr 2026 01:22:20 GMT  
		Size: 592.5 MB (592549959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:eedf5e08050e7b2b8156174a16878ba821e89ebcf36488a51d3bb981826922b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b836150ae1014e800aeb95401947eab6991470d3caa7e9540a9d17cc5761cd`

```dockerfile
```

-	Layers:
	-	`sha256:75326fdd5b5969006aae8e4354aac08e43a519226e95f4d2e114b656adf6c324`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7dc2a8ec36e9abaed5a00678037a830387b363f5f95362203a23446031a46d`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim-bookworm`

```console
$ docker pull haskell@sha256:1f0099b81708e859d4d90f43d06187c8298c59d33ddf3bb01cff047131d0ab5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:ec468efccdfee2736254eced8aabda20caeb9a7413f8ba1a8d709c6e2657c264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776932258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2173d21f80bdb483477e015940670f09e33cb2d6136c82f12e7a62aeeae54191`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:01 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345dc3f621eb0094cd075ee66a2755b9c6d79d500a1a801483f92a7448eb3c94`  
		Last Modified: Tue, 07 Apr 2026 01:21:34 GMT  
		Size: 124.4 MB (124405560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47df7d2546cd081cd78569030f2b57711e56cd47e01f054fc6760b7a174ee51`  
		Last Modified: Tue, 07 Apr 2026 01:21:30 GMT  
		Size: 22.2 MB (22220780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bfa68860956218eb86763ac5169ed8198b6bbea47ea40ac15d1ebf0b9b0dff`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 8.4 MB (8403514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c93da93eff076094eefe1d30ebfb37597e0e6b28f746f73abfb52d017cd8a1`  
		Last Modified: Tue, 07 Apr 2026 01:21:45 GMT  
		Size: 593.7 MB (593666072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:f87ce515084b12c2b03afd14820dd24f68118fde8c3c6b8c1e403e1670e9c0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2783973dbc0d33a45942d152c97cdbdbbdd8bbf862118d42f67fea5aa0a1096`

```dockerfile
```

-	Layers:
	-	`sha256:c092357d6ac3da8e3a1826c5b11f41a26405d393fb292b5377971dc7b98e212e`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b95e9b4e1b098e6f3ec57d2b3c6af99d1a8df7b9f3209ff4af0e56079b2e641`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e1c5961de02a9617ad4548c1d388ed811218c2a6fb7d508aba60c74938d44586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779715156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b95888e8c56f17ea52f9af5f94f933872ac70f7e1de2186cd09a803989641dd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:28 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c64a7715b20f0ce9a276abdfad0e377d8a74adaf5d2859c0980c91ae630b4d`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 118.6 MB (118575900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bdb68ff57f6ba1cfef40b68fc13d52d983fea4a32dbb5ba9d9c8e1eead4472`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 24.5 MB (24528540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f297d7be8e2a3dc35e44249b90135de569e0e0a316932ef497d5c7355ee9cc79`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7eff1bbecd608dd9e4f7f8fc78d2ee29abe5147929e545743f63887773827b`  
		Last Modified: Tue, 07 Apr 2026 01:22:20 GMT  
		Size: 592.5 MB (592549959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:eedf5e08050e7b2b8156174a16878ba821e89ebcf36488a51d3bb981826922b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b836150ae1014e800aeb95401947eab6991470d3caa7e9540a9d17cc5761cd`

```dockerfile
```

-	Layers:
	-	`sha256:75326fdd5b5969006aae8e4354aac08e43a519226e95f4d2e114b656adf6c324`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7dc2a8ec36e9abaed5a00678037a830387b363f5f95362203a23446031a46d`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim-bullseye`

```console
$ docker pull haskell@sha256:a308580ef820964e7ca93fd565372fefa7347349c9a5af98b467c1762663a850
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:861a6492cf7f9e816ef6e5d3571040aada4494200bbdc1ac68d2de6b2ccef2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608295417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab699b6bc5a2039c3aef4f4fc0e0e280be0d8fd661a762f96fed65441f94568c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a673ceb44a304ec95d9ec3a4552a15b6ec332792b6e9e7dacbe456dd47639f74`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 106.4 MB (106394062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406a8d52e21b244390398e286d5690db277efdc4135cad90bf063d8d750bdc45`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25536413a5ea7ad0ef10a0fccbafe0c896c0798cc3888db717ce1422e7b7d564`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 441.8 MB (441810322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:cc0137181d099ca6be11886c914f40a5fc12b5585e2a23bd5e992f7f630291c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6785093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e640fefb81716b0a37ad00b3d98e211e99c6b509d0dd66b2c0a880d7d451da3b`

```dockerfile
```

-	Layers:
	-	`sha256:96936ea297d348d566f764dad257e5bb36d2046c34109b1cb0affeb1fbfccaba`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 6.8 MB (6759349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234687df9ebda4f854bd9853b61cfbefbc9c066cf396d384141776c77d252f4d`  
		Last Modified: Tue, 07 Apr 2026 01:21:17 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d6e497909b113cb2cb3926ac6038eb43877f2dace0c6912deb394d9b3ead7472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618571434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca193d12285da7f428eea19dbb6befe80dffc9f4d445d659a0c2d9e041148d45`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3dc8eabee012b38c5d28f05e1e09419c198bbfa415a29299372a02971b20b9`  
		Last Modified: Tue, 07 Apr 2026 01:21:00 GMT  
		Size: 101.9 MB (101873470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e1600eaed1b321e505e24dbe932cf6d88b8c884784eef86fc53e03ec65e131`  
		Last Modified: Tue, 07 Apr 2026 01:20:57 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c1e1c1c0cb2d50b0ae3a91d5451717df8853eb61badd28cc1432f29707b0e`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b5b77b94f9b23f14c32c41fe6f786349c2b25fb8db77bd35e87f7e8ca07246`  
		Last Modified: Tue, 07 Apr 2026 01:21:06 GMT  
		Size: 449.5 MB (449451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:98029243c8be669546cc17cde279d431cc52a9bb23fff9d86bee26013598ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2878c3561ed3271d7ff0fb48abb223404d640cdeae180a2d3c12817642eab5e3`

```dockerfile
```

-	Layers:
	-	`sha256:d87037d3a1fb8b3e4550bb0a00dc329407aa2c01c3c4d091dae0119ec0975ab6`  
		Last Modified: Tue, 07 Apr 2026 01:20:56 GMT  
		Size: 6.8 MB (6761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df60e783acac74289b8eacab3af23d267ac28d89c798b1b4f61dae265d88f497`  
		Last Modified: Tue, 07 Apr 2026 01:20:56 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10`

```console
$ docker pull haskell@sha256:1434abf2aa95282e46916880a70ed9ee02566ef603698d969ce8371340212576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10` - linux; amd64

```console
$ docker pull haskell@sha256:40c7aeeca45ca813f36f3e80dea6918b5f9b316ba177eddcb323adcf30f07275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659223113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d840f2cefaa050966550674fb069f56f7ac499d54363561a4930035f5cfaad`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02dda58f98dd1b89ea56dad93ea597ab2d270a4c5488a5080ebfe4e22608c05`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 133.8 MB (133816646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6788ea23b7d8f664d2f75dfca6820d1905f375c4b0709aecf2e28c70adf4fff6`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6537af5e28a47f37be1aa665b630dbb58038dedb64aa2fe86bbc08b1567b095`  
		Last Modified: Tue, 07 Apr 2026 01:21:40 GMT  
		Size: 441.8 MB (441810672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10` - unknown; unknown

```console
$ docker pull haskell@sha256:8b7321c089ffb9d02de572c043af25531fb81f3a1367778a6c10db105f1059d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93647ed1c3cbd8cdc4712413b2170c4c76076508be7f76e44ba8f2d9781b7aca`

```dockerfile
```

-	Layers:
	-	`sha256:7da85245cba7175d03e3f59cb8c744cb7ed18d6d58c00207d1643b72499ae200`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 9.4 MB (9408030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dc7e5b0791b03f692e44b1eeb39a1ffd1ad2ff71636daecd10aed90c468db1`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:efa0a620239a673d67ff573b2139b4db387c710a661a0f5d29c714dcab56061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.5 MB (669473057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b52e39a5e2aa5d80d316672bfb8122b184a94a08aaa270df7836b8ff6bca76`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:51 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c24e51cfa942997e098c6febaa4751e88ae4debf1f5dd07bc9bb72927972c8e`  
		Last Modified: Tue, 07 Apr 2026 01:20:53 GMT  
		Size: 129.3 MB (129273970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ab9ae73c524c4b51e32343734bbc89d93f0ebc83216d04951e9ef1ae57b01`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39dc89c8cb93b86dcf19088b6e096b806448b6954836844ef750d884b6f7ed`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c9395fb5fbcc181b749007653b2871b370c130abf6eba6eca01e3ab56865bd`  
		Last Modified: Tue, 07 Apr 2026 01:21:00 GMT  
		Size: 449.4 MB (449449962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10` - unknown; unknown

```console
$ docker pull haskell@sha256:a46ac3fa59dd96825e6b5930fcd7586bc903333e44d1e995b3c8a62d61538a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9435754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85495acd2d5e485183a23106106f0651c1873c05c7e291b51f2964306eb867e0`

```dockerfile
```

-	Layers:
	-	`sha256:88b942987203a63840e9e1594431326625e9b9168303b88fe5eff77a6d2a3af9`  
		Last Modified: Tue, 07 Apr 2026 01:20:47 GMT  
		Size: 9.4 MB (9409302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3837dcc5606b2cab1f0f41a5ade639d7471f70208472385abccb18ae80c7e53c`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-bookworm`

```console
$ docker pull haskell@sha256:9c00ab3f6522ef32dc4816674186a90a94326343108bc585c60f83b7e5a05b55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:7a4dced33a78a02bf7bc9b69da18310dd23a2a80e04eebafcdf2573ccac00163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672837238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13b0c2047a030fa4e4b980ce309b0eaef034344c7f7b5248da3f05fcdc82fd1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:28 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:28 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:28 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:30 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:30 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:31 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4824b2452aaa97c41275ca903b43952213fee158674cfd0112af96a95c0f50`  
		Last Modified: Tue, 07 Apr 2026 01:21:21 GMT  
		Size: 152.4 MB (152404502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5e2de6d6bcf4f9c40426d78363699289de6979140f9c00907bacea6e898df9`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 22.2 MB (22220765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ab59e6839980084819e736ed1ecd3bf6d46598abd7102546933b581609c52`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48cb1aa3d0d7e1c2be6b4716eaf46a98951ff401a6b50e6c3ed24d315989fb8`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 442.1 MB (442116092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:9a2d8da308ec200865bd3f306a5ead89858525aae6d994871eb9db6be40e9ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9504459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf8e83681386c419e76dcc4d06dee7599c1524f38798e594720b3c3bba8a085`

```dockerfile
```

-	Layers:
	-	`sha256:3b73bdab7e0a3669a96aa8b3493927ecae9b667354bbec519c548a639992b14a`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 9.5 MB (9479105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:157ba3da256492a13cef23f71cf5d53acb2a6b96740e30abeac582ce423ac65f`  
		Last Modified: Tue, 07 Apr 2026 01:21:14 GMT  
		Size: 25.4 KB (25354 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:00f6c2f3ff1d4e2eb084a4e22b25257fb187d4056d65a758e1d2b2e062204e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.9 MB (682897412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072db9ec74ec23d0d050ea571b7b84f42d34dc95976bd6061d1b0944399b24d4`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:43 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:43 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:43 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:45 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:45 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:45 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:47 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:17:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3a34d08bcf4039db31f08aaf5845e966c603ce6970948910064a4d8840cf08`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 146.6 MB (146573550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2856eeca109f3ccdd4f8bdd7b1dfc63eab64d2d4eb3d9090b22851215ae026b7`  
		Last Modified: Tue, 07 Apr 2026 01:20:40 GMT  
		Size: 24.5 MB (24528541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62de76c9b3eafef4bb967c132f67f5a6917299d9b281c7b8b0f654381bd90228`  
		Last Modified: Tue, 07 Apr 2026 01:20:40 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dc610f5be7f75bdc50e90af5efb5b72dbaec9c168ebc0d32362357389da3a9`  
		Last Modified: Tue, 07 Apr 2026 01:20:54 GMT  
		Size: 449.5 MB (449453036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:41b8069f510d30ba42dfe923cd50716f1f3483131f0eb87b49d0238f442a68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9532369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d259a03a199677ce45a946eec32313ecf5a026d9870cc0721e163b66af870`

```dockerfile
```

-	Layers:
	-	`sha256:429daa1bd58b3d026985551bb38f77918eecaa3194a642ab571c05e07a7b2340`  
		Last Modified: Tue, 07 Apr 2026 01:20:39 GMT  
		Size: 9.5 MB (9506889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0748ca9b024c59d6a07371042ace8fb3e18b6c93194d82e7a35a3e642205bb`  
		Last Modified: Tue, 07 Apr 2026 01:20:38 GMT  
		Size: 25.5 KB (25480 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-bullseye`

```console
$ docker pull haskell@sha256:1434abf2aa95282e46916880a70ed9ee02566ef603698d969ce8371340212576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:40c7aeeca45ca813f36f3e80dea6918b5f9b316ba177eddcb323adcf30f07275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659223113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d840f2cefaa050966550674fb069f56f7ac499d54363561a4930035f5cfaad`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02dda58f98dd1b89ea56dad93ea597ab2d270a4c5488a5080ebfe4e22608c05`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 133.8 MB (133816646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6788ea23b7d8f664d2f75dfca6820d1905f375c4b0709aecf2e28c70adf4fff6`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6537af5e28a47f37be1aa665b630dbb58038dedb64aa2fe86bbc08b1567b095`  
		Last Modified: Tue, 07 Apr 2026 01:21:40 GMT  
		Size: 441.8 MB (441810672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:8b7321c089ffb9d02de572c043af25531fb81f3a1367778a6c10db105f1059d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93647ed1c3cbd8cdc4712413b2170c4c76076508be7f76e44ba8f2d9781b7aca`

```dockerfile
```

-	Layers:
	-	`sha256:7da85245cba7175d03e3f59cb8c744cb7ed18d6d58c00207d1643b72499ae200`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 9.4 MB (9408030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dc7e5b0791b03f692e44b1eeb39a1ffd1ad2ff71636daecd10aed90c468db1`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:efa0a620239a673d67ff573b2139b4db387c710a661a0f5d29c714dcab56061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.5 MB (669473057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b52e39a5e2aa5d80d316672bfb8122b184a94a08aaa270df7836b8ff6bca76`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:51 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c24e51cfa942997e098c6febaa4751e88ae4debf1f5dd07bc9bb72927972c8e`  
		Last Modified: Tue, 07 Apr 2026 01:20:53 GMT  
		Size: 129.3 MB (129273970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ab9ae73c524c4b51e32343734bbc89d93f0ebc83216d04951e9ef1ae57b01`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39dc89c8cb93b86dcf19088b6e096b806448b6954836844ef750d884b6f7ed`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c9395fb5fbcc181b749007653b2871b370c130abf6eba6eca01e3ab56865bd`  
		Last Modified: Tue, 07 Apr 2026 01:21:00 GMT  
		Size: 449.4 MB (449449962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a46ac3fa59dd96825e6b5930fcd7586bc903333e44d1e995b3c8a62d61538a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9435754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85495acd2d5e485183a23106106f0651c1873c05c7e291b51f2964306eb867e0`

```dockerfile
```

-	Layers:
	-	`sha256:88b942987203a63840e9e1594431326625e9b9168303b88fe5eff77a6d2a3af9`  
		Last Modified: Tue, 07 Apr 2026 01:20:47 GMT  
		Size: 9.4 MB (9409302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3837dcc5606b2cab1f0f41a5ade639d7471f70208472385abccb18ae80c7e53c`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-slim-bookworm`

```console
$ docker pull haskell@sha256:905809cfeca2f8854b62ffe0a52b834e7cc24d0ff6ef443e51b28c9d295762bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:49482b2dc3121e70066887c536464a6b1a987b4deca80317bd19f00e8e30ca93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.6 MB (624586389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9021ed1af91cd31b5ddd8aa6cf4fbbaee7c506013d666e7fa107cc0e48dd343`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:27 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:27 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:29 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:29 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:30 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c8040cfcc86a43e8d35e9cb51fdd3603bccebbc651d7f568ffa81c515d03da`  
		Last Modified: Tue, 07 Apr 2026 01:21:26 GMT  
		Size: 124.4 MB (124405019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23815f3d26fc568b3021db618fe7f0d365a1750e2e947fa11825622a4ea33e5`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e163e447d336b0ad85d5737fe36b06228de022381c7b1fba5ca4c85bf860de6`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 7.6 MB (7607052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb03629c654468cbbb739d9ea84110366b36583390f59cfab412fdb911999ff`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 442.1 MB (442117205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:7a44f7f6e7c02e7b3c1429e33fb254c62444e1e2a534fec84490762dac679c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5259017dca429fb26fbc9c10deca99f6f6a6d969c83c3eff123e003972821c`

```dockerfile
```

-	Layers:
	-	`sha256:4c15e4ef2276c2324b0a13ec0ca7ae841a749c5f0d84e4102f554a5cb77930ab`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 6.6 MB (6606033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de3563614436603dbba031d5add475bccc6efce506c604c8ad07fd453915fa8`  
		Last Modified: Tue, 07 Apr 2026 01:21:21 GMT  
		Size: 25.4 KB (25397 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e0618fda32935d7ab71de35527193d7675e5ad19e419a543ba166b24984d3b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.6 MB (634641870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6807e94885f52d2c7dc2f35bfa1d280dcfcc559872f1f56cb98c6edfebe0b16c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:44 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:44 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:48 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:17:48 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:22 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:22 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdad98a3be7dd13f7ecb023f7232cee62374d45077e06b8af773f436139c0550`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 118.6 MB (118575838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad33592cf2d5642a2fe32f8038d14bff0f8d4d1ee01f63ceaad5afee34c8be29`  
		Last Modified: Tue, 07 Apr 2026 01:20:40 GMT  
		Size: 24.5 MB (24528555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4051eb8248cc2bef949dd7a608bfa5ba96c34961f76ec95be45dde9dbb8238`  
		Last Modified: Tue, 07 Apr 2026 01:20:39 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7cda1f85331100a600a1fd9078beed4bfc4cd369f601b9e20fb873e1da2d21`  
		Last Modified: Tue, 07 Apr 2026 01:20:49 GMT  
		Size: 449.5 MB (449452288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:5654dbf749f822c99f8f95824806b1eee740627f01a6c771d3dd1d2aca9f1a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d443cfc274a27ea93a294d92131c1e973524a08064f6b87f8e8bb47b888707e`

```dockerfile
```

-	Layers:
	-	`sha256:d8a62499aefea71c4cb7c40f966a9d034c7047987a49a90f11f8f7028b2d5f04`  
		Last Modified: Tue, 07 Apr 2026 01:20:39 GMT  
		Size: 6.6 MB (6634444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1197d8bbab4ff72d972cfcc7adf1794a1ebf7a6d741c82aac752d5bff98d20a5`  
		Last Modified: Tue, 07 Apr 2026 01:20:39 GMT  
		Size: 25.5 KB (25524 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-slim-bullseye`

```console
$ docker pull haskell@sha256:a308580ef820964e7ca93fd565372fefa7347349c9a5af98b467c1762663a850
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:861a6492cf7f9e816ef6e5d3571040aada4494200bbdc1ac68d2de6b2ccef2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608295417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab699b6bc5a2039c3aef4f4fc0e0e280be0d8fd661a762f96fed65441f94568c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a673ceb44a304ec95d9ec3a4552a15b6ec332792b6e9e7dacbe456dd47639f74`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 106.4 MB (106394062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406a8d52e21b244390398e286d5690db277efdc4135cad90bf063d8d750bdc45`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25536413a5ea7ad0ef10a0fccbafe0c896c0798cc3888db717ce1422e7b7d564`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 441.8 MB (441810322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:cc0137181d099ca6be11886c914f40a5fc12b5585e2a23bd5e992f7f630291c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6785093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e640fefb81716b0a37ad00b3d98e211e99c6b509d0dd66b2c0a880d7d451da3b`

```dockerfile
```

-	Layers:
	-	`sha256:96936ea297d348d566f764dad257e5bb36d2046c34109b1cb0affeb1fbfccaba`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 6.8 MB (6759349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234687df9ebda4f854bd9853b61cfbefbc9c066cf396d384141776c77d252f4d`  
		Last Modified: Tue, 07 Apr 2026 01:21:17 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d6e497909b113cb2cb3926ac6038eb43877f2dace0c6912deb394d9b3ead7472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618571434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca193d12285da7f428eea19dbb6befe80dffc9f4d445d659a0c2d9e041148d45`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3dc8eabee012b38c5d28f05e1e09419c198bbfa415a29299372a02971b20b9`  
		Last Modified: Tue, 07 Apr 2026 01:21:00 GMT  
		Size: 101.9 MB (101873470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e1600eaed1b321e505e24dbe932cf6d88b8c884784eef86fc53e03ec65e131`  
		Last Modified: Tue, 07 Apr 2026 01:20:57 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c1e1c1c0cb2d50b0ae3a91d5451717df8853eb61badd28cc1432f29707b0e`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b5b77b94f9b23f14c32c41fe6f786349c2b25fb8db77bd35e87f7e8ca07246`  
		Last Modified: Tue, 07 Apr 2026 01:21:06 GMT  
		Size: 449.5 MB (449451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:98029243c8be669546cc17cde279d431cc52a9bb23fff9d86bee26013598ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2878c3561ed3271d7ff0fb48abb223404d640cdeae180a2d3c12817642eab5e3`

```dockerfile
```

-	Layers:
	-	`sha256:d87037d3a1fb8b3e4550bb0a00dc329407aa2c01c3c4d091dae0119ec0975ab6`  
		Last Modified: Tue, 07 Apr 2026 01:20:56 GMT  
		Size: 6.8 MB (6761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df60e783acac74289b8eacab3af23d267ac28d89c798b1b4f61dae265d88f497`  
		Last Modified: Tue, 07 Apr 2026 01:20:56 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3`

```console
$ docker pull haskell@sha256:1434abf2aa95282e46916880a70ed9ee02566ef603698d969ce8371340212576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3` - linux; amd64

```console
$ docker pull haskell@sha256:40c7aeeca45ca813f36f3e80dea6918b5f9b316ba177eddcb323adcf30f07275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659223113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d840f2cefaa050966550674fb069f56f7ac499d54363561a4930035f5cfaad`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02dda58f98dd1b89ea56dad93ea597ab2d270a4c5488a5080ebfe4e22608c05`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 133.8 MB (133816646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6788ea23b7d8f664d2f75dfca6820d1905f375c4b0709aecf2e28c70adf4fff6`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6537af5e28a47f37be1aa665b630dbb58038dedb64aa2fe86bbc08b1567b095`  
		Last Modified: Tue, 07 Apr 2026 01:21:40 GMT  
		Size: 441.8 MB (441810672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3` - unknown; unknown

```console
$ docker pull haskell@sha256:8b7321c089ffb9d02de572c043af25531fb81f3a1367778a6c10db105f1059d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93647ed1c3cbd8cdc4712413b2170c4c76076508be7f76e44ba8f2d9781b7aca`

```dockerfile
```

-	Layers:
	-	`sha256:7da85245cba7175d03e3f59cb8c744cb7ed18d6d58c00207d1643b72499ae200`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 9.4 MB (9408030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dc7e5b0791b03f692e44b1eeb39a1ffd1ad2ff71636daecd10aed90c468db1`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:efa0a620239a673d67ff573b2139b4db387c710a661a0f5d29c714dcab56061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.5 MB (669473057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b52e39a5e2aa5d80d316672bfb8122b184a94a08aaa270df7836b8ff6bca76`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:51 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c24e51cfa942997e098c6febaa4751e88ae4debf1f5dd07bc9bb72927972c8e`  
		Last Modified: Tue, 07 Apr 2026 01:20:53 GMT  
		Size: 129.3 MB (129273970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ab9ae73c524c4b51e32343734bbc89d93f0ebc83216d04951e9ef1ae57b01`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39dc89c8cb93b86dcf19088b6e096b806448b6954836844ef750d884b6f7ed`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c9395fb5fbcc181b749007653b2871b370c130abf6eba6eca01e3ab56865bd`  
		Last Modified: Tue, 07 Apr 2026 01:21:00 GMT  
		Size: 449.4 MB (449449962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3` - unknown; unknown

```console
$ docker pull haskell@sha256:a46ac3fa59dd96825e6b5930fcd7586bc903333e44d1e995b3c8a62d61538a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9435754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85495acd2d5e485183a23106106f0651c1873c05c7e291b51f2964306eb867e0`

```dockerfile
```

-	Layers:
	-	`sha256:88b942987203a63840e9e1594431326625e9b9168303b88fe5eff77a6d2a3af9`  
		Last Modified: Tue, 07 Apr 2026 01:20:47 GMT  
		Size: 9.4 MB (9409302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3837dcc5606b2cab1f0f41a5ade639d7471f70208472385abccb18ae80c7e53c`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-bookworm`

```console
$ docker pull haskell@sha256:9c00ab3f6522ef32dc4816674186a90a94326343108bc585c60f83b7e5a05b55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:7a4dced33a78a02bf7bc9b69da18310dd23a2a80e04eebafcdf2573ccac00163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672837238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13b0c2047a030fa4e4b980ce309b0eaef034344c7f7b5248da3f05fcdc82fd1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:28 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:28 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:28 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:30 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:30 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:31 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4824b2452aaa97c41275ca903b43952213fee158674cfd0112af96a95c0f50`  
		Last Modified: Tue, 07 Apr 2026 01:21:21 GMT  
		Size: 152.4 MB (152404502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5e2de6d6bcf4f9c40426d78363699289de6979140f9c00907bacea6e898df9`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 22.2 MB (22220765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ab59e6839980084819e736ed1ecd3bf6d46598abd7102546933b581609c52`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48cb1aa3d0d7e1c2be6b4716eaf46a98951ff401a6b50e6c3ed24d315989fb8`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 442.1 MB (442116092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:9a2d8da308ec200865bd3f306a5ead89858525aae6d994871eb9db6be40e9ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9504459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf8e83681386c419e76dcc4d06dee7599c1524f38798e594720b3c3bba8a085`

```dockerfile
```

-	Layers:
	-	`sha256:3b73bdab7e0a3669a96aa8b3493927ecae9b667354bbec519c548a639992b14a`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 9.5 MB (9479105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:157ba3da256492a13cef23f71cf5d53acb2a6b96740e30abeac582ce423ac65f`  
		Last Modified: Tue, 07 Apr 2026 01:21:14 GMT  
		Size: 25.4 KB (25354 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:00f6c2f3ff1d4e2eb084a4e22b25257fb187d4056d65a758e1d2b2e062204e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.9 MB (682897412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:072db9ec74ec23d0d050ea571b7b84f42d34dc95976bd6061d1b0944399b24d4`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:43 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:43 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:43 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:43 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:45 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:45 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:45 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:47 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:17:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3a34d08bcf4039db31f08aaf5845e966c603ce6970948910064a4d8840cf08`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 146.6 MB (146573550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2856eeca109f3ccdd4f8bdd7b1dfc63eab64d2d4eb3d9090b22851215ae026b7`  
		Last Modified: Tue, 07 Apr 2026 01:20:40 GMT  
		Size: 24.5 MB (24528541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62de76c9b3eafef4bb967c132f67f5a6917299d9b281c7b8b0f654381bd90228`  
		Last Modified: Tue, 07 Apr 2026 01:20:40 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dc610f5be7f75bdc50e90af5efb5b72dbaec9c168ebc0d32362357389da3a9`  
		Last Modified: Tue, 07 Apr 2026 01:20:54 GMT  
		Size: 449.5 MB (449453036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:41b8069f510d30ba42dfe923cd50716f1f3483131f0eb87b49d0238f442a68ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9532369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b94d259a03a199677ce45a946eec32313ecf5a026d9870cc0721e163b66af870`

```dockerfile
```

-	Layers:
	-	`sha256:429daa1bd58b3d026985551bb38f77918eecaa3194a642ab571c05e07a7b2340`  
		Last Modified: Tue, 07 Apr 2026 01:20:39 GMT  
		Size: 9.5 MB (9506889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c0748ca9b024c59d6a07371042ace8fb3e18b6c93194d82e7a35a3e642205bb`  
		Last Modified: Tue, 07 Apr 2026 01:20:38 GMT  
		Size: 25.5 KB (25480 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-bullseye`

```console
$ docker pull haskell@sha256:1434abf2aa95282e46916880a70ed9ee02566ef603698d969ce8371340212576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:40c7aeeca45ca813f36f3e80dea6918b5f9b316ba177eddcb323adcf30f07275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659223113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d840f2cefaa050966550674fb069f56f7ac499d54363561a4930035f5cfaad`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02dda58f98dd1b89ea56dad93ea597ab2d270a4c5488a5080ebfe4e22608c05`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 133.8 MB (133816646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6788ea23b7d8f664d2f75dfca6820d1905f375c4b0709aecf2e28c70adf4fff6`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6537af5e28a47f37be1aa665b630dbb58038dedb64aa2fe86bbc08b1567b095`  
		Last Modified: Tue, 07 Apr 2026 01:21:40 GMT  
		Size: 441.8 MB (441810672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:8b7321c089ffb9d02de572c043af25531fb81f3a1367778a6c10db105f1059d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93647ed1c3cbd8cdc4712413b2170c4c76076508be7f76e44ba8f2d9781b7aca`

```dockerfile
```

-	Layers:
	-	`sha256:7da85245cba7175d03e3f59cb8c744cb7ed18d6d58c00207d1643b72499ae200`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 9.4 MB (9408030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dc7e5b0791b03f692e44b1eeb39a1ffd1ad2ff71636daecd10aed90c468db1`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:efa0a620239a673d67ff573b2139b4db387c710a661a0f5d29c714dcab56061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.5 MB (669473057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b52e39a5e2aa5d80d316672bfb8122b184a94a08aaa270df7836b8ff6bca76`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:51 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c24e51cfa942997e098c6febaa4751e88ae4debf1f5dd07bc9bb72927972c8e`  
		Last Modified: Tue, 07 Apr 2026 01:20:53 GMT  
		Size: 129.3 MB (129273970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ab9ae73c524c4b51e32343734bbc89d93f0ebc83216d04951e9ef1ae57b01`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39dc89c8cb93b86dcf19088b6e096b806448b6954836844ef750d884b6f7ed`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c9395fb5fbcc181b749007653b2871b370c130abf6eba6eca01e3ab56865bd`  
		Last Modified: Tue, 07 Apr 2026 01:21:00 GMT  
		Size: 449.4 MB (449449962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a46ac3fa59dd96825e6b5930fcd7586bc903333e44d1e995b3c8a62d61538a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9435754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85495acd2d5e485183a23106106f0651c1873c05c7e291b51f2964306eb867e0`

```dockerfile
```

-	Layers:
	-	`sha256:88b942987203a63840e9e1594431326625e9b9168303b88fe5eff77a6d2a3af9`  
		Last Modified: Tue, 07 Apr 2026 01:20:47 GMT  
		Size: 9.4 MB (9409302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3837dcc5606b2cab1f0f41a5ade639d7471f70208472385abccb18ae80c7e53c`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-slim-bookworm`

```console
$ docker pull haskell@sha256:905809cfeca2f8854b62ffe0a52b834e7cc24d0ff6ef443e51b28c9d295762bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:49482b2dc3121e70066887c536464a6b1a987b4deca80317bd19f00e8e30ca93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.6 MB (624586389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9021ed1af91cd31b5ddd8aa6cf4fbbaee7c506013d666e7fa107cc0e48dd343`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:27 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:27 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:27 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:29 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:29 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:30 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:10 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:10 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c8040cfcc86a43e8d35e9cb51fdd3603bccebbc651d7f568ffa81c515d03da`  
		Last Modified: Tue, 07 Apr 2026 01:21:26 GMT  
		Size: 124.4 MB (124405019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23815f3d26fc568b3021db618fe7f0d365a1750e2e947fa11825622a4ea33e5`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e163e447d336b0ad85d5737fe36b06228de022381c7b1fba5ca4c85bf860de6`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 7.6 MB (7607052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb03629c654468cbbb739d9ea84110366b36583390f59cfab412fdb911999ff`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 442.1 MB (442117205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:7a44f7f6e7c02e7b3c1429e33fb254c62444e1e2a534fec84490762dac679c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f5259017dca429fb26fbc9c10deca99f6f6a6d969c83c3eff123e003972821c`

```dockerfile
```

-	Layers:
	-	`sha256:4c15e4ef2276c2324b0a13ec0ca7ae841a749c5f0d84e4102f554a5cb77930ab`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 6.6 MB (6606033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0de3563614436603dbba031d5add475bccc6efce506c604c8ad07fd453915fa8`  
		Last Modified: Tue, 07 Apr 2026 01:21:21 GMT  
		Size: 25.4 KB (25397 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e0618fda32935d7ab71de35527193d7675e5ad19e419a543ba166b24984d3b88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.6 MB (634641870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6807e94885f52d2c7dc2f35bfa1d280dcfcc559872f1f56cb98c6edfebe0b16c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:44 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:44 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:48 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:17:48 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:22 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:22 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdad98a3be7dd13f7ecb023f7232cee62374d45077e06b8af773f436139c0550`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 118.6 MB (118575838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad33592cf2d5642a2fe32f8038d14bff0f8d4d1ee01f63ceaad5afee34c8be29`  
		Last Modified: Tue, 07 Apr 2026 01:20:40 GMT  
		Size: 24.5 MB (24528555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4051eb8248cc2bef949dd7a608bfa5ba96c34961f76ec95be45dde9dbb8238`  
		Last Modified: Tue, 07 Apr 2026 01:20:39 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7cda1f85331100a600a1fd9078beed4bfc4cd369f601b9e20fb873e1da2d21`  
		Last Modified: Tue, 07 Apr 2026 01:20:49 GMT  
		Size: 449.5 MB (449452288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:5654dbf749f822c99f8f95824806b1eee740627f01a6c771d3dd1d2aca9f1a7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d443cfc274a27ea93a294d92131c1e973524a08064f6b87f8e8bb47b888707e`

```dockerfile
```

-	Layers:
	-	`sha256:d8a62499aefea71c4cb7c40f966a9d034c7047987a49a90f11f8f7028b2d5f04`  
		Last Modified: Tue, 07 Apr 2026 01:20:39 GMT  
		Size: 6.6 MB (6634444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1197d8bbab4ff72d972cfcc7adf1794a1ebf7a6d741c82aac752d5bff98d20a5`  
		Last Modified: Tue, 07 Apr 2026 01:20:39 GMT  
		Size: 25.5 KB (25524 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-slim-bullseye`

```console
$ docker pull haskell@sha256:a308580ef820964e7ca93fd565372fefa7347349c9a5af98b467c1762663a850
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:861a6492cf7f9e816ef6e5d3571040aada4494200bbdc1ac68d2de6b2ccef2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608295417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab699b6bc5a2039c3aef4f4fc0e0e280be0d8fd661a762f96fed65441f94568c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a673ceb44a304ec95d9ec3a4552a15b6ec332792b6e9e7dacbe456dd47639f74`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 106.4 MB (106394062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406a8d52e21b244390398e286d5690db277efdc4135cad90bf063d8d750bdc45`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25536413a5ea7ad0ef10a0fccbafe0c896c0798cc3888db717ce1422e7b7d564`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 441.8 MB (441810322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:cc0137181d099ca6be11886c914f40a5fc12b5585e2a23bd5e992f7f630291c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6785093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e640fefb81716b0a37ad00b3d98e211e99c6b509d0dd66b2c0a880d7d451da3b`

```dockerfile
```

-	Layers:
	-	`sha256:96936ea297d348d566f764dad257e5bb36d2046c34109b1cb0affeb1fbfccaba`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 6.8 MB (6759349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234687df9ebda4f854bd9853b61cfbefbc9c066cf396d384141776c77d252f4d`  
		Last Modified: Tue, 07 Apr 2026 01:21:17 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d6e497909b113cb2cb3926ac6038eb43877f2dace0c6912deb394d9b3ead7472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618571434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca193d12285da7f428eea19dbb6befe80dffc9f4d445d659a0c2d9e041148d45`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3dc8eabee012b38c5d28f05e1e09419c198bbfa415a29299372a02971b20b9`  
		Last Modified: Tue, 07 Apr 2026 01:21:00 GMT  
		Size: 101.9 MB (101873470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e1600eaed1b321e505e24dbe932cf6d88b8c884784eef86fc53e03ec65e131`  
		Last Modified: Tue, 07 Apr 2026 01:20:57 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c1e1c1c0cb2d50b0ae3a91d5451717df8853eb61badd28cc1432f29707b0e`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b5b77b94f9b23f14c32c41fe6f786349c2b25fb8db77bd35e87f7e8ca07246`  
		Last Modified: Tue, 07 Apr 2026 01:21:06 GMT  
		Size: 449.5 MB (449451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:98029243c8be669546cc17cde279d431cc52a9bb23fff9d86bee26013598ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2878c3561ed3271d7ff0fb48abb223404d640cdeae180a2d3c12817642eab5e3`

```dockerfile
```

-	Layers:
	-	`sha256:d87037d3a1fb8b3e4550bb0a00dc329407aa2c01c3c4d091dae0119ec0975ab6`  
		Last Modified: Tue, 07 Apr 2026 01:20:56 GMT  
		Size: 6.8 MB (6761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df60e783acac74289b8eacab3af23d267ac28d89c798b1b4f61dae265d88f497`  
		Last Modified: Tue, 07 Apr 2026 01:20:56 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12`

```console
$ docker pull haskell@sha256:0dabe39ff7116832afd8219ce4ef9e7b35f5ba7bb779c83da83fa0195ee9c73f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12` - linux; amd64

```console
$ docker pull haskell@sha256:7b23fbedef6254d1d822dc3d933c46c4af69eb1ef11052c007781d5c694e6329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.5 MB (822466482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca157c5e2099fbbfb0dacfb9c6adb7e5d5b4d799a22fb4f60a7928bdcf9c62d8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:24 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:24 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:26 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:20:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440fe1b122111638d3cade73f912508d249d51b8285659981d209900a2add658`  
		Last Modified: Tue, 07 Apr 2026 01:22:21 GMT  
		Size: 152.4 MB (152404561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f02c6211c2f0da9cfd02583c89439b2ad1211779f359ce3ee003358c7afe4bc`  
		Last Modified: Tue, 07 Apr 2026 01:22:17 GMT  
		Size: 22.2 MB (22220753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9771299f7baf8fa05c635cb80f5481447abb39a4d6ef11ed4bf462662028e1b`  
		Last Modified: Tue, 07 Apr 2026 01:22:06 GMT  
		Size: 7.6 MB (7607052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad7548f0b77aefb693c3e14363e0665a16e17f55704f06fb879d6f1fff797a1`  
		Last Modified: Tue, 07 Apr 2026 01:22:30 GMT  
		Size: 591.7 MB (591745293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12` - unknown; unknown

```console
$ docker pull haskell@sha256:6227c34b62948db4f84ba48ee5cf17d11319d4084d9c619b1b0f2fa99a7b0210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe7e5e3eb795ec07a23885295952be1190be68f8974bc589bb5f7b07cf6714f`

```dockerfile
```

-	Layers:
	-	`sha256:aac9e74e16878e9363de66000ca0d55b432065739733d1f308d8719e7005e4db`  
		Last Modified: Tue, 07 Apr 2026 01:22:16 GMT  
		Size: 9.5 MB (9478198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61165bd76ad2c26fe3cbed4b9d4e18788f75b57ff89239ce12278af44b4d8cad`  
		Last Modified: Tue, 07 Apr 2026 01:22:15 GMT  
		Size: 25.7 KB (25665 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:60d8837dbb228e6f08cff2e7ad50b4260b9eb6e7536dfbf9626a6edd98dd64da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.1 MB (825065423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8434c0469357d24c0291c7caafadf7d8a3faa43be390caeace801864563d34`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:39 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:39 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:43 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:17:43 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766c1c26262673e409289e61a687345c745accb7a186753969d334b44d79ae2d`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 146.6 MB (146573147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dd00dd759580dd21b8b172dbb340f6d127ad6d7ee14da528fb7b60ff571e83`  
		Last Modified: Tue, 07 Apr 2026 01:21:16 GMT  
		Size: 24.5 MB (24528549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a591f6a97df642d2982b8f0eaa0631f9ee4523fe8a53e2e271b18026bf5b00c4`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563228099aa1cedc5e49fd275aa02ee5d79400d48376f74c62afa05651e95dfc`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 591.6 MB (591621442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12` - unknown; unknown

```console
$ docker pull haskell@sha256:9921cbd7d5b0236103f0aedf361fd58c53b3d5f54cdd1a68358d1306c4f87928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9531822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64c18a66a1c147e11085586ad87082021f4f0041d126697d2d08be5327903ad`

```dockerfile
```

-	Layers:
	-	`sha256:93e6553674f98e70380e43562ee809e0c3e7c3745a778a32ea32d6d1d81ab11e`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 9.5 MB (9506006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb3ab633dd1a8fb7cf008db7e8ca3c79ef880b4f860019bc1950f596fb4cb4f7`  
		Last Modified: Tue, 07 Apr 2026 01:21:13 GMT  
		Size: 25.8 KB (25816 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12-bookworm`

```console
$ docker pull haskell@sha256:0dabe39ff7116832afd8219ce4ef9e7b35f5ba7bb779c83da83fa0195ee9c73f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:7b23fbedef6254d1d822dc3d933c46c4af69eb1ef11052c007781d5c694e6329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.5 MB (822466482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca157c5e2099fbbfb0dacfb9c6adb7e5d5b4d799a22fb4f60a7928bdcf9c62d8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:24 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:24 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:26 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:20:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440fe1b122111638d3cade73f912508d249d51b8285659981d209900a2add658`  
		Last Modified: Tue, 07 Apr 2026 01:22:21 GMT  
		Size: 152.4 MB (152404561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f02c6211c2f0da9cfd02583c89439b2ad1211779f359ce3ee003358c7afe4bc`  
		Last Modified: Tue, 07 Apr 2026 01:22:17 GMT  
		Size: 22.2 MB (22220753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9771299f7baf8fa05c635cb80f5481447abb39a4d6ef11ed4bf462662028e1b`  
		Last Modified: Tue, 07 Apr 2026 01:22:06 GMT  
		Size: 7.6 MB (7607052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad7548f0b77aefb693c3e14363e0665a16e17f55704f06fb879d6f1fff797a1`  
		Last Modified: Tue, 07 Apr 2026 01:22:30 GMT  
		Size: 591.7 MB (591745293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:6227c34b62948db4f84ba48ee5cf17d11319d4084d9c619b1b0f2fa99a7b0210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe7e5e3eb795ec07a23885295952be1190be68f8974bc589bb5f7b07cf6714f`

```dockerfile
```

-	Layers:
	-	`sha256:aac9e74e16878e9363de66000ca0d55b432065739733d1f308d8719e7005e4db`  
		Last Modified: Tue, 07 Apr 2026 01:22:16 GMT  
		Size: 9.5 MB (9478198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61165bd76ad2c26fe3cbed4b9d4e18788f75b57ff89239ce12278af44b4d8cad`  
		Last Modified: Tue, 07 Apr 2026 01:22:15 GMT  
		Size: 25.7 KB (25665 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:60d8837dbb228e6f08cff2e7ad50b4260b9eb6e7536dfbf9626a6edd98dd64da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.1 MB (825065423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8434c0469357d24c0291c7caafadf7d8a3faa43be390caeace801864563d34`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:39 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:39 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:43 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:17:43 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766c1c26262673e409289e61a687345c745accb7a186753969d334b44d79ae2d`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 146.6 MB (146573147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dd00dd759580dd21b8b172dbb340f6d127ad6d7ee14da528fb7b60ff571e83`  
		Last Modified: Tue, 07 Apr 2026 01:21:16 GMT  
		Size: 24.5 MB (24528549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a591f6a97df642d2982b8f0eaa0631f9ee4523fe8a53e2e271b18026bf5b00c4`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563228099aa1cedc5e49fd275aa02ee5d79400d48376f74c62afa05651e95dfc`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 591.6 MB (591621442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:9921cbd7d5b0236103f0aedf361fd58c53b3d5f54cdd1a68358d1306c4f87928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9531822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64c18a66a1c147e11085586ad87082021f4f0041d126697d2d08be5327903ad`

```dockerfile
```

-	Layers:
	-	`sha256:93e6553674f98e70380e43562ee809e0c3e7c3745a778a32ea32d6d1d81ab11e`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 9.5 MB (9506006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb3ab633dd1a8fb7cf008db7e8ca3c79ef880b4f860019bc1950f596fb4cb4f7`  
		Last Modified: Tue, 07 Apr 2026 01:21:13 GMT  
		Size: 25.8 KB (25816 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12-slim-bookworm`

```console
$ docker pull haskell@sha256:c83dcb092fff03ab85a6febf903f7ac378983ddadda53bb6da31ea74d70546f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:c6cf3635aaba6a5f98e51903be6cbc63e275b53f3ac74781b2893bb70c52d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774213868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18314a08051e864d860998f2a19e1fbc119bfcf22566624e40a291f1f7c059a3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:25 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:25 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:27 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:27 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:27 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:20:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcca444ccd6332cf72f55a8503109abd1d8669044021363eb7381918481df299`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 124.4 MB (124404766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dff130e2070e21945a402502f6f715b68bfe9d5f2f4868b63f6e325ca599d25`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 22.2 MB (22220782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9771299f7baf8fa05c635cb80f5481447abb39a4d6ef11ed4bf462662028e1b`  
		Last Modified: Tue, 07 Apr 2026 01:22:06 GMT  
		Size: 7.6 MB (7607052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bce2ac61c4bb17bc206205369b8ddd15b04e4486ea199326acf8326e26ac38f`  
		Last Modified: Tue, 07 Apr 2026 01:22:25 GMT  
		Size: 591.7 MB (591744936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:7866924182c26b2edca8071292e3bd2ea309627039c390f0b115f793c57815cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6629642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68051b93d4b4f49dfc1e49ee7d3da31c18f1adf0537472d0dab2c8b8d9a788a2`

```dockerfile
```

-	Layers:
	-	`sha256:e9f3bffd4bee627d7b5d59031f6bbe43242bb11c10fdb2542a2821261f98579b`  
		Last Modified: Tue, 07 Apr 2026 01:22:06 GMT  
		Size: 6.6 MB (6604530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c36e31cb200f3327c9fd3876ddf935532a0fa02e71862206a7e3231078d366eb`  
		Last Modified: Tue, 07 Apr 2026 01:22:05 GMT  
		Size: 25.1 KB (25112 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:9e82af5b976403329d4f4f45c8f7757ef99a56e7d0e55b8b3117330ecab16c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.8 MB (776815063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b849bf9fb2596f9315400f60226f87c02fc68a2fd46f40c49db54d4f06165bbb`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:16:14 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:16:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:16:14 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:16:14 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:16:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:16:17 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:16:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:16:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:16:19 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:18:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:18:11 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:18:11 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08d3887fe6c85d7b4db24fa3f015c74546c7d9f33ab5bf8bbad7b80ae7bae34`  
		Last Modified: Tue, 07 Apr 2026 01:19:52 GMT  
		Size: 118.6 MB (118575943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f0bc926fab019d6be1b938151addb4cca83581a24201ba915703c49d38fe99`  
		Last Modified: Tue, 07 Apr 2026 01:19:48 GMT  
		Size: 24.5 MB (24528593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a899b99035a51e2d6073781057c8c28919e23ebcad49a3ff8c1e1f2afdc42af`  
		Last Modified: Tue, 07 Apr 2026 01:19:48 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796cec720497e3a97682e131b9e0b8d26e9992b15d109b14a43eb849cc33b2de`  
		Last Modified: Tue, 07 Apr 2026 01:20:01 GMT  
		Size: 591.6 MB (591625338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:babd53b7025cbe735416944ba9ff6182a65084a6c72a31cbfb8a1434abf7e5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6658180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae2b3dfda194e4da797cb126e1acf09a9cb70a39840a74d5337206d9fcb41fc`

```dockerfile
```

-	Layers:
	-	`sha256:d0efcd3ef779ac43e57430fc57380400e58488add3fb9ab3644b504c5c658a41`  
		Last Modified: Tue, 07 Apr 2026 01:19:47 GMT  
		Size: 6.6 MB (6632941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927051b013834e0d66c18d912792ce7601f4839dc8a5e194b8c1da2cf31c4b57`  
		Last Modified: Tue, 07 Apr 2026 01:19:46 GMT  
		Size: 25.2 KB (25239 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2`

```console
$ docker pull haskell@sha256:0dabe39ff7116832afd8219ce4ef9e7b35f5ba7bb779c83da83fa0195ee9c73f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2` - linux; amd64

```console
$ docker pull haskell@sha256:7b23fbedef6254d1d822dc3d933c46c4af69eb1ef11052c007781d5c694e6329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.5 MB (822466482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca157c5e2099fbbfb0dacfb9c6adb7e5d5b4d799a22fb4f60a7928bdcf9c62d8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:24 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:24 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:26 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:20:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440fe1b122111638d3cade73f912508d249d51b8285659981d209900a2add658`  
		Last Modified: Tue, 07 Apr 2026 01:22:21 GMT  
		Size: 152.4 MB (152404561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f02c6211c2f0da9cfd02583c89439b2ad1211779f359ce3ee003358c7afe4bc`  
		Last Modified: Tue, 07 Apr 2026 01:22:17 GMT  
		Size: 22.2 MB (22220753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9771299f7baf8fa05c635cb80f5481447abb39a4d6ef11ed4bf462662028e1b`  
		Last Modified: Tue, 07 Apr 2026 01:22:06 GMT  
		Size: 7.6 MB (7607052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad7548f0b77aefb693c3e14363e0665a16e17f55704f06fb879d6f1fff797a1`  
		Last Modified: Tue, 07 Apr 2026 01:22:30 GMT  
		Size: 591.7 MB (591745293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2` - unknown; unknown

```console
$ docker pull haskell@sha256:6227c34b62948db4f84ba48ee5cf17d11319d4084d9c619b1b0f2fa99a7b0210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe7e5e3eb795ec07a23885295952be1190be68f8974bc589bb5f7b07cf6714f`

```dockerfile
```

-	Layers:
	-	`sha256:aac9e74e16878e9363de66000ca0d55b432065739733d1f308d8719e7005e4db`  
		Last Modified: Tue, 07 Apr 2026 01:22:16 GMT  
		Size: 9.5 MB (9478198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61165bd76ad2c26fe3cbed4b9d4e18788f75b57ff89239ce12278af44b4d8cad`  
		Last Modified: Tue, 07 Apr 2026 01:22:15 GMT  
		Size: 25.7 KB (25665 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:60d8837dbb228e6f08cff2e7ad50b4260b9eb6e7536dfbf9626a6edd98dd64da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.1 MB (825065423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8434c0469357d24c0291c7caafadf7d8a3faa43be390caeace801864563d34`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:39 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:39 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:43 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:17:43 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766c1c26262673e409289e61a687345c745accb7a186753969d334b44d79ae2d`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 146.6 MB (146573147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dd00dd759580dd21b8b172dbb340f6d127ad6d7ee14da528fb7b60ff571e83`  
		Last Modified: Tue, 07 Apr 2026 01:21:16 GMT  
		Size: 24.5 MB (24528549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a591f6a97df642d2982b8f0eaa0631f9ee4523fe8a53e2e271b18026bf5b00c4`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563228099aa1cedc5e49fd275aa02ee5d79400d48376f74c62afa05651e95dfc`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 591.6 MB (591621442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2` - unknown; unknown

```console
$ docker pull haskell@sha256:9921cbd7d5b0236103f0aedf361fd58c53b3d5f54cdd1a68358d1306c4f87928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9531822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64c18a66a1c147e11085586ad87082021f4f0041d126697d2d08be5327903ad`

```dockerfile
```

-	Layers:
	-	`sha256:93e6553674f98e70380e43562ee809e0c3e7c3745a778a32ea32d6d1d81ab11e`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 9.5 MB (9506006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb3ab633dd1a8fb7cf008db7e8ca3c79ef880b4f860019bc1950f596fb4cb4f7`  
		Last Modified: Tue, 07 Apr 2026 01:21:13 GMT  
		Size: 25.8 KB (25816 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2-bookworm`

```console
$ docker pull haskell@sha256:0dabe39ff7116832afd8219ce4ef9e7b35f5ba7bb779c83da83fa0195ee9c73f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:7b23fbedef6254d1d822dc3d933c46c4af69eb1ef11052c007781d5c694e6329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.5 MB (822466482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca157c5e2099fbbfb0dacfb9c6adb7e5d5b4d799a22fb4f60a7928bdcf9c62d8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:24 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:24 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:26 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:20:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440fe1b122111638d3cade73f912508d249d51b8285659981d209900a2add658`  
		Last Modified: Tue, 07 Apr 2026 01:22:21 GMT  
		Size: 152.4 MB (152404561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f02c6211c2f0da9cfd02583c89439b2ad1211779f359ce3ee003358c7afe4bc`  
		Last Modified: Tue, 07 Apr 2026 01:22:17 GMT  
		Size: 22.2 MB (22220753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9771299f7baf8fa05c635cb80f5481447abb39a4d6ef11ed4bf462662028e1b`  
		Last Modified: Tue, 07 Apr 2026 01:22:06 GMT  
		Size: 7.6 MB (7607052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad7548f0b77aefb693c3e14363e0665a16e17f55704f06fb879d6f1fff797a1`  
		Last Modified: Tue, 07 Apr 2026 01:22:30 GMT  
		Size: 591.7 MB (591745293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:6227c34b62948db4f84ba48ee5cf17d11319d4084d9c619b1b0f2fa99a7b0210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe7e5e3eb795ec07a23885295952be1190be68f8974bc589bb5f7b07cf6714f`

```dockerfile
```

-	Layers:
	-	`sha256:aac9e74e16878e9363de66000ca0d55b432065739733d1f308d8719e7005e4db`  
		Last Modified: Tue, 07 Apr 2026 01:22:16 GMT  
		Size: 9.5 MB (9478198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61165bd76ad2c26fe3cbed4b9d4e18788f75b57ff89239ce12278af44b4d8cad`  
		Last Modified: Tue, 07 Apr 2026 01:22:15 GMT  
		Size: 25.7 KB (25665 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:60d8837dbb228e6f08cff2e7ad50b4260b9eb6e7536dfbf9626a6edd98dd64da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.1 MB (825065423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8434c0469357d24c0291c7caafadf7d8a3faa43be390caeace801864563d34`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:39 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:39 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:43 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:17:43 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766c1c26262673e409289e61a687345c745accb7a186753969d334b44d79ae2d`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 146.6 MB (146573147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66dd00dd759580dd21b8b172dbb340f6d127ad6d7ee14da528fb7b60ff571e83`  
		Last Modified: Tue, 07 Apr 2026 01:21:16 GMT  
		Size: 24.5 MB (24528549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a591f6a97df642d2982b8f0eaa0631f9ee4523fe8a53e2e271b18026bf5b00c4`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563228099aa1cedc5e49fd275aa02ee5d79400d48376f74c62afa05651e95dfc`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 591.6 MB (591621442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:9921cbd7d5b0236103f0aedf361fd58c53b3d5f54cdd1a68358d1306c4f87928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9531822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64c18a66a1c147e11085586ad87082021f4f0041d126697d2d08be5327903ad`

```dockerfile
```

-	Layers:
	-	`sha256:93e6553674f98e70380e43562ee809e0c3e7c3745a778a32ea32d6d1d81ab11e`  
		Last Modified: Tue, 07 Apr 2026 01:21:15 GMT  
		Size: 9.5 MB (9506006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb3ab633dd1a8fb7cf008db7e8ca3c79ef880b4f860019bc1950f596fb4cb4f7`  
		Last Modified: Tue, 07 Apr 2026 01:21:13 GMT  
		Size: 25.8 KB (25816 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2-slim-bookworm`

```console
$ docker pull haskell@sha256:c83dcb092fff03ab85a6febf903f7ac378983ddadda53bb6da31ea74d70546f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:c6cf3635aaba6a5f98e51903be6cbc63e275b53f3ac74781b2893bb70c52d2d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774213868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18314a08051e864d860998f2a19e1fbc119bfcf22566624e40a291f1f7c059a3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:25 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:25 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:25 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:25 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:27 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:27 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:27 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:18:28 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:20:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcca444ccd6332cf72f55a8503109abd1d8669044021363eb7381918481df299`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 124.4 MB (124404766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dff130e2070e21945a402502f6f715b68bfe9d5f2f4868b63f6e325ca599d25`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 22.2 MB (22220782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9771299f7baf8fa05c635cb80f5481447abb39a4d6ef11ed4bf462662028e1b`  
		Last Modified: Tue, 07 Apr 2026 01:22:06 GMT  
		Size: 7.6 MB (7607052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bce2ac61c4bb17bc206205369b8ddd15b04e4486ea199326acf8326e26ac38f`  
		Last Modified: Tue, 07 Apr 2026 01:22:25 GMT  
		Size: 591.7 MB (591744936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:7866924182c26b2edca8071292e3bd2ea309627039c390f0b115f793c57815cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6629642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68051b93d4b4f49dfc1e49ee7d3da31c18f1adf0537472d0dab2c8b8d9a788a2`

```dockerfile
```

-	Layers:
	-	`sha256:e9f3bffd4bee627d7b5d59031f6bbe43242bb11c10fdb2542a2821261f98579b`  
		Last Modified: Tue, 07 Apr 2026 01:22:06 GMT  
		Size: 6.6 MB (6604530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c36e31cb200f3327c9fd3876ddf935532a0fa02e71862206a7e3231078d366eb`  
		Last Modified: Tue, 07 Apr 2026 01:22:05 GMT  
		Size: 25.1 KB (25112 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:9e82af5b976403329d4f4f45c8f7757ef99a56e7d0e55b8b3117330ecab16c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.8 MB (776815063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b849bf9fb2596f9315400f60226f87c02fc68a2fd46f40c49db54d4f06165bbb`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:16:14 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:16:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:16:14 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:16:14 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:16:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:16:17 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:16:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:16:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:16:19 GMT
ARG GHC=9.12.2
# Tue, 07 Apr 2026 01:16:19 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:18:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:18:11 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:18:11 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08d3887fe6c85d7b4db24fa3f015c74546c7d9f33ab5bf8bbad7b80ae7bae34`  
		Last Modified: Tue, 07 Apr 2026 01:19:52 GMT  
		Size: 118.6 MB (118575943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f0bc926fab019d6be1b938151addb4cca83581a24201ba915703c49d38fe99`  
		Last Modified: Tue, 07 Apr 2026 01:19:48 GMT  
		Size: 24.5 MB (24528593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a899b99035a51e2d6073781057c8c28919e23ebcad49a3ff8c1e1f2afdc42af`  
		Last Modified: Tue, 07 Apr 2026 01:19:48 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796cec720497e3a97682e131b9e0b8d26e9992b15d109b14a43eb849cc33b2de`  
		Last Modified: Tue, 07 Apr 2026 01:20:01 GMT  
		Size: 591.6 MB (591625338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:babd53b7025cbe735416944ba9ff6182a65084a6c72a31cbfb8a1434abf7e5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6658180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae2b3dfda194e4da797cb126e1acf09a9cb70a39840a74d5337206d9fcb41fc`

```dockerfile
```

-	Layers:
	-	`sha256:d0efcd3ef779ac43e57430fc57380400e58488add3fb9ab3644b504c5c658a41`  
		Last Modified: Tue, 07 Apr 2026 01:19:47 GMT  
		Size: 6.6 MB (6632941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:927051b013834e0d66c18d912792ce7601f4839dc8a5e194b8c1da2cf31c4b57`  
		Last Modified: Tue, 07 Apr 2026 01:19:46 GMT  
		Size: 25.2 KB (25239 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14`

```console
$ docker pull haskell@sha256:6cff7c33044cc6b6b5944e64860278df5f66e2fd6546526ee7a3f7b2a0bb302d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14` - linux; amd64

```console
$ docker pull haskell@sha256:1fbcda9feaaf6fdc37f04994416244502ffc60420ac87bf888b2e27fb4a7e3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f2e39e42a486cc41c8abaa23edc4b5bf18f3e6188c3005107b5376e6872757`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:05 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece92b353df31cd62bcf548d31f7e7551ad5001927d632dc72fdb96777c0a7de`  
		Last Modified: Tue, 07 Apr 2026 01:21:59 GMT  
		Size: 152.4 MB (152404537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9003a62dd97b742a849a6ffe605b33afae135ecf9a6963fa71ce25145093e9`  
		Last Modified: Tue, 07 Apr 2026 01:21:54 GMT  
		Size: 22.2 MB (22220764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03444700904b3892922358de25fdfe826f0169360d9f9cb036eeac113f25554c`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920399cab91d6ff0fc2201575339dc055750baca387d9ed10f94ed92d7adde`  
		Last Modified: Tue, 07 Apr 2026 01:22:11 GMT  
		Size: 593.7 MB (593665337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14` - unknown; unknown

```console
$ docker pull haskell@sha256:bb0b5eca366271d9faabc5051de30bf0ca84556d8d2311a229f9e9cfd86ac081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff0ec4d07cfb43474a87b2b0c0dab7ef9b2b9b1f3f76a5dc23866ef5c9b9169`

```dockerfile
```

-	Layers:
	-	`sha256:18227a676aaf76c21c1183a42a01b9a116a151db0b59a0ea80879bdb63f1e15a`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598a0a7da604db5b7571614d65ef77c3d89c33455779d8a7ae9656cacc7e243c`  
		Last Modified: Tue, 07 Apr 2026 01:21:52 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f32d990dc8da74f7f0341a333164cb1c8d6266a8ac9ad4a945b90117efaffa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.0 MB (827973880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0549a54963f5295de9aca4174ea8cd5c882c87f277d02b84d560108488fee`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:13 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8b2b86a1f61fbc06035adfc6d633c1ef0ac985ee5d01ad2035aa975e75bc5e`  
		Last Modified: Tue, 07 Apr 2026 01:22:18 GMT  
		Size: 146.6 MB (146574461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a921e64342db75f8743327ae9f72db69b755625911158c2ba61f7e5cc3c653`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 24.5 MB (24528556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04627812dc4bd20dfe4c8cdc15e97e22dc630d7688a5f6cf80d91b271266ee`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 15.9 MB (15944580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd72aeb1f170c652f08f92801ce519133208478741fd634ac455a534dd7f21`  
		Last Modified: Tue, 07 Apr 2026 01:22:26 GMT  
		Size: 592.6 MB (592553021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14` - unknown; unknown

```console
$ docker pull haskell@sha256:c5ee901f3e234f95818fd514b41636991e5c804c884191726bdfe9d398b131dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9a7278c6d71557554c28d4ca253da3efb5f1beb63668ba7412cd386f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:25ff4331c3bb33056dbba1acea83141c0be05c91a7822f564aa4ec8e37d10405`  
		Last Modified: Tue, 07 Apr 2026 01:22:13 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0c3e47baeb7423641c403b8e392683ef8fc8fa4cf31429b25de36abf9eb3`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14-bookworm`

```console
$ docker pull haskell@sha256:6cff7c33044cc6b6b5944e64860278df5f66e2fd6546526ee7a3f7b2a0bb302d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:1fbcda9feaaf6fdc37f04994416244502ffc60420ac87bf888b2e27fb4a7e3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f2e39e42a486cc41c8abaa23edc4b5bf18f3e6188c3005107b5376e6872757`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:05 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece92b353df31cd62bcf548d31f7e7551ad5001927d632dc72fdb96777c0a7de`  
		Last Modified: Tue, 07 Apr 2026 01:21:59 GMT  
		Size: 152.4 MB (152404537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9003a62dd97b742a849a6ffe605b33afae135ecf9a6963fa71ce25145093e9`  
		Last Modified: Tue, 07 Apr 2026 01:21:54 GMT  
		Size: 22.2 MB (22220764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03444700904b3892922358de25fdfe826f0169360d9f9cb036eeac113f25554c`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920399cab91d6ff0fc2201575339dc055750baca387d9ed10f94ed92d7adde`  
		Last Modified: Tue, 07 Apr 2026 01:22:11 GMT  
		Size: 593.7 MB (593665337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:bb0b5eca366271d9faabc5051de30bf0ca84556d8d2311a229f9e9cfd86ac081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff0ec4d07cfb43474a87b2b0c0dab7ef9b2b9b1f3f76a5dc23866ef5c9b9169`

```dockerfile
```

-	Layers:
	-	`sha256:18227a676aaf76c21c1183a42a01b9a116a151db0b59a0ea80879bdb63f1e15a`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598a0a7da604db5b7571614d65ef77c3d89c33455779d8a7ae9656cacc7e243c`  
		Last Modified: Tue, 07 Apr 2026 01:21:52 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f32d990dc8da74f7f0341a333164cb1c8d6266a8ac9ad4a945b90117efaffa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.0 MB (827973880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0549a54963f5295de9aca4174ea8cd5c882c87f277d02b84d560108488fee`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:13 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8b2b86a1f61fbc06035adfc6d633c1ef0ac985ee5d01ad2035aa975e75bc5e`  
		Last Modified: Tue, 07 Apr 2026 01:22:18 GMT  
		Size: 146.6 MB (146574461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a921e64342db75f8743327ae9f72db69b755625911158c2ba61f7e5cc3c653`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 24.5 MB (24528556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04627812dc4bd20dfe4c8cdc15e97e22dc630d7688a5f6cf80d91b271266ee`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 15.9 MB (15944580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd72aeb1f170c652f08f92801ce519133208478741fd634ac455a534dd7f21`  
		Last Modified: Tue, 07 Apr 2026 01:22:26 GMT  
		Size: 592.6 MB (592553021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:c5ee901f3e234f95818fd514b41636991e5c804c884191726bdfe9d398b131dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9a7278c6d71557554c28d4ca253da3efb5f1beb63668ba7412cd386f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:25ff4331c3bb33056dbba1acea83141c0be05c91a7822f564aa4ec8e37d10405`  
		Last Modified: Tue, 07 Apr 2026 01:22:13 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0c3e47baeb7423641c403b8e392683ef8fc8fa4cf31429b25de36abf9eb3`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14-slim-bookworm`

```console
$ docker pull haskell@sha256:1f0099b81708e859d4d90f43d06187c8298c59d33ddf3bb01cff047131d0ab5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:ec468efccdfee2736254eced8aabda20caeb9a7413f8ba1a8d709c6e2657c264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776932258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2173d21f80bdb483477e015940670f09e33cb2d6136c82f12e7a62aeeae54191`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:01 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345dc3f621eb0094cd075ee66a2755b9c6d79d500a1a801483f92a7448eb3c94`  
		Last Modified: Tue, 07 Apr 2026 01:21:34 GMT  
		Size: 124.4 MB (124405560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47df7d2546cd081cd78569030f2b57711e56cd47e01f054fc6760b7a174ee51`  
		Last Modified: Tue, 07 Apr 2026 01:21:30 GMT  
		Size: 22.2 MB (22220780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bfa68860956218eb86763ac5169ed8198b6bbea47ea40ac15d1ebf0b9b0dff`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 8.4 MB (8403514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c93da93eff076094eefe1d30ebfb37597e0e6b28f746f73abfb52d017cd8a1`  
		Last Modified: Tue, 07 Apr 2026 01:21:45 GMT  
		Size: 593.7 MB (593666072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:f87ce515084b12c2b03afd14820dd24f68118fde8c3c6b8c1e403e1670e9c0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2783973dbc0d33a45942d152c97cdbdbbdd8bbf862118d42f67fea5aa0a1096`

```dockerfile
```

-	Layers:
	-	`sha256:c092357d6ac3da8e3a1826c5b11f41a26405d393fb292b5377971dc7b98e212e`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b95e9b4e1b098e6f3ec57d2b3c6af99d1a8df7b9f3209ff4af0e56079b2e641`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e1c5961de02a9617ad4548c1d388ed811218c2a6fb7d508aba60c74938d44586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779715156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b95888e8c56f17ea52f9af5f94f933872ac70f7e1de2186cd09a803989641dd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:28 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c64a7715b20f0ce9a276abdfad0e377d8a74adaf5d2859c0980c91ae630b4d`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 118.6 MB (118575900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bdb68ff57f6ba1cfef40b68fc13d52d983fea4a32dbb5ba9d9c8e1eead4472`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 24.5 MB (24528540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f297d7be8e2a3dc35e44249b90135de569e0e0a316932ef497d5c7355ee9cc79`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7eff1bbecd608dd9e4f7f8fc78d2ee29abe5147929e545743f63887773827b`  
		Last Modified: Tue, 07 Apr 2026 01:22:20 GMT  
		Size: 592.5 MB (592549959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:eedf5e08050e7b2b8156174a16878ba821e89ebcf36488a51d3bb981826922b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b836150ae1014e800aeb95401947eab6991470d3caa7e9540a9d17cc5761cd`

```dockerfile
```

-	Layers:
	-	`sha256:75326fdd5b5969006aae8e4354aac08e43a519226e95f4d2e114b656adf6c324`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7dc2a8ec36e9abaed5a00678037a830387b363f5f95362203a23446031a46d`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14.1`

```console
$ docker pull haskell@sha256:6cff7c33044cc6b6b5944e64860278df5f66e2fd6546526ee7a3f7b2a0bb302d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14.1` - linux; amd64

```console
$ docker pull haskell@sha256:1fbcda9feaaf6fdc37f04994416244502ffc60420ac87bf888b2e27fb4a7e3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f2e39e42a486cc41c8abaa23edc4b5bf18f3e6188c3005107b5376e6872757`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:05 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece92b353df31cd62bcf548d31f7e7551ad5001927d632dc72fdb96777c0a7de`  
		Last Modified: Tue, 07 Apr 2026 01:21:59 GMT  
		Size: 152.4 MB (152404537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9003a62dd97b742a849a6ffe605b33afae135ecf9a6963fa71ce25145093e9`  
		Last Modified: Tue, 07 Apr 2026 01:21:54 GMT  
		Size: 22.2 MB (22220764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03444700904b3892922358de25fdfe826f0169360d9f9cb036eeac113f25554c`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920399cab91d6ff0fc2201575339dc055750baca387d9ed10f94ed92d7adde`  
		Last Modified: Tue, 07 Apr 2026 01:22:11 GMT  
		Size: 593.7 MB (593665337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1` - unknown; unknown

```console
$ docker pull haskell@sha256:bb0b5eca366271d9faabc5051de30bf0ca84556d8d2311a229f9e9cfd86ac081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff0ec4d07cfb43474a87b2b0c0dab7ef9b2b9b1f3f76a5dc23866ef5c9b9169`

```dockerfile
```

-	Layers:
	-	`sha256:18227a676aaf76c21c1183a42a01b9a116a151db0b59a0ea80879bdb63f1e15a`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598a0a7da604db5b7571614d65ef77c3d89c33455779d8a7ae9656cacc7e243c`  
		Last Modified: Tue, 07 Apr 2026 01:21:52 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14.1` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f32d990dc8da74f7f0341a333164cb1c8d6266a8ac9ad4a945b90117efaffa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.0 MB (827973880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0549a54963f5295de9aca4174ea8cd5c882c87f277d02b84d560108488fee`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:13 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8b2b86a1f61fbc06035adfc6d633c1ef0ac985ee5d01ad2035aa975e75bc5e`  
		Last Modified: Tue, 07 Apr 2026 01:22:18 GMT  
		Size: 146.6 MB (146574461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a921e64342db75f8743327ae9f72db69b755625911158c2ba61f7e5cc3c653`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 24.5 MB (24528556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04627812dc4bd20dfe4c8cdc15e97e22dc630d7688a5f6cf80d91b271266ee`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 15.9 MB (15944580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd72aeb1f170c652f08f92801ce519133208478741fd634ac455a534dd7f21`  
		Last Modified: Tue, 07 Apr 2026 01:22:26 GMT  
		Size: 592.6 MB (592553021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1` - unknown; unknown

```console
$ docker pull haskell@sha256:c5ee901f3e234f95818fd514b41636991e5c804c884191726bdfe9d398b131dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9a7278c6d71557554c28d4ca253da3efb5f1beb63668ba7412cd386f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:25ff4331c3bb33056dbba1acea83141c0be05c91a7822f564aa4ec8e37d10405`  
		Last Modified: Tue, 07 Apr 2026 01:22:13 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0c3e47baeb7423641c403b8e392683ef8fc8fa4cf31429b25de36abf9eb3`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14.1-bookworm`

```console
$ docker pull haskell@sha256:6cff7c33044cc6b6b5944e64860278df5f66e2fd6546526ee7a3f7b2a0bb302d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14.1-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:1fbcda9feaaf6fdc37f04994416244502ffc60420ac87bf888b2e27fb4a7e3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f2e39e42a486cc41c8abaa23edc4b5bf18f3e6188c3005107b5376e6872757`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:05 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece92b353df31cd62bcf548d31f7e7551ad5001927d632dc72fdb96777c0a7de`  
		Last Modified: Tue, 07 Apr 2026 01:21:59 GMT  
		Size: 152.4 MB (152404537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9003a62dd97b742a849a6ffe605b33afae135ecf9a6963fa71ce25145093e9`  
		Last Modified: Tue, 07 Apr 2026 01:21:54 GMT  
		Size: 22.2 MB (22220764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03444700904b3892922358de25fdfe826f0169360d9f9cb036eeac113f25554c`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920399cab91d6ff0fc2201575339dc055750baca387d9ed10f94ed92d7adde`  
		Last Modified: Tue, 07 Apr 2026 01:22:11 GMT  
		Size: 593.7 MB (593665337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:bb0b5eca366271d9faabc5051de30bf0ca84556d8d2311a229f9e9cfd86ac081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff0ec4d07cfb43474a87b2b0c0dab7ef9b2b9b1f3f76a5dc23866ef5c9b9169`

```dockerfile
```

-	Layers:
	-	`sha256:18227a676aaf76c21c1183a42a01b9a116a151db0b59a0ea80879bdb63f1e15a`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598a0a7da604db5b7571614d65ef77c3d89c33455779d8a7ae9656cacc7e243c`  
		Last Modified: Tue, 07 Apr 2026 01:21:52 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f32d990dc8da74f7f0341a333164cb1c8d6266a8ac9ad4a945b90117efaffa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.0 MB (827973880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0549a54963f5295de9aca4174ea8cd5c882c87f277d02b84d560108488fee`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:13 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8b2b86a1f61fbc06035adfc6d633c1ef0ac985ee5d01ad2035aa975e75bc5e`  
		Last Modified: Tue, 07 Apr 2026 01:22:18 GMT  
		Size: 146.6 MB (146574461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a921e64342db75f8743327ae9f72db69b755625911158c2ba61f7e5cc3c653`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 24.5 MB (24528556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04627812dc4bd20dfe4c8cdc15e97e22dc630d7688a5f6cf80d91b271266ee`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 15.9 MB (15944580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd72aeb1f170c652f08f92801ce519133208478741fd634ac455a534dd7f21`  
		Last Modified: Tue, 07 Apr 2026 01:22:26 GMT  
		Size: 592.6 MB (592553021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:c5ee901f3e234f95818fd514b41636991e5c804c884191726bdfe9d398b131dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9a7278c6d71557554c28d4ca253da3efb5f1beb63668ba7412cd386f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:25ff4331c3bb33056dbba1acea83141c0be05c91a7822f564aa4ec8e37d10405`  
		Last Modified: Tue, 07 Apr 2026 01:22:13 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0c3e47baeb7423641c403b8e392683ef8fc8fa4cf31429b25de36abf9eb3`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14.1-slim-bookworm`

```console
$ docker pull haskell@sha256:1f0099b81708e859d4d90f43d06187c8298c59d33ddf3bb01cff047131d0ab5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14.1-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:ec468efccdfee2736254eced8aabda20caeb9a7413f8ba1a8d709c6e2657c264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776932258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2173d21f80bdb483477e015940670f09e33cb2d6136c82f12e7a62aeeae54191`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:01 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345dc3f621eb0094cd075ee66a2755b9c6d79d500a1a801483f92a7448eb3c94`  
		Last Modified: Tue, 07 Apr 2026 01:21:34 GMT  
		Size: 124.4 MB (124405560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47df7d2546cd081cd78569030f2b57711e56cd47e01f054fc6760b7a174ee51`  
		Last Modified: Tue, 07 Apr 2026 01:21:30 GMT  
		Size: 22.2 MB (22220780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bfa68860956218eb86763ac5169ed8198b6bbea47ea40ac15d1ebf0b9b0dff`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 8.4 MB (8403514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c93da93eff076094eefe1d30ebfb37597e0e6b28f746f73abfb52d017cd8a1`  
		Last Modified: Tue, 07 Apr 2026 01:21:45 GMT  
		Size: 593.7 MB (593666072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:f87ce515084b12c2b03afd14820dd24f68118fde8c3c6b8c1e403e1670e9c0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2783973dbc0d33a45942d152c97cdbdbbdd8bbf862118d42f67fea5aa0a1096`

```dockerfile
```

-	Layers:
	-	`sha256:c092357d6ac3da8e3a1826c5b11f41a26405d393fb292b5377971dc7b98e212e`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b95e9b4e1b098e6f3ec57d2b3c6af99d1a8df7b9f3209ff4af0e56079b2e641`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14.1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e1c5961de02a9617ad4548c1d388ed811218c2a6fb7d508aba60c74938d44586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779715156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b95888e8c56f17ea52f9af5f94f933872ac70f7e1de2186cd09a803989641dd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:28 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c64a7715b20f0ce9a276abdfad0e377d8a74adaf5d2859c0980c91ae630b4d`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 118.6 MB (118575900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bdb68ff57f6ba1cfef40b68fc13d52d983fea4a32dbb5ba9d9c8e1eead4472`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 24.5 MB (24528540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f297d7be8e2a3dc35e44249b90135de569e0e0a316932ef497d5c7355ee9cc79`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7eff1bbecd608dd9e4f7f8fc78d2ee29abe5147929e545743f63887773827b`  
		Last Modified: Tue, 07 Apr 2026 01:22:20 GMT  
		Size: 592.5 MB (592549959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:eedf5e08050e7b2b8156174a16878ba821e89ebcf36488a51d3bb981826922b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b836150ae1014e800aeb95401947eab6991470d3caa7e9540a9d17cc5761cd`

```dockerfile
```

-	Layers:
	-	`sha256:75326fdd5b5969006aae8e4354aac08e43a519226e95f4d2e114b656adf6c324`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7dc2a8ec36e9abaed5a00678037a830387b363f5f95362203a23446031a46d`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6`

```console
$ docker pull haskell@sha256:d9609bb8f14b87636cb7432f3914407e14a832eb2d4980d21b2e4465b33dcc2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6` - linux; amd64

```console
$ docker pull haskell@sha256:006b552d40ef387f13149a6635cd5ced9fb26676f0b1ab739acb235600b23650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641634243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e36241573919b5f2e65f3c519282dce675b1ee558d4c6e55433f67d35b0589`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:56 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:21:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:23:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:23:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:23:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0f437936c2255161efab8ddeb40df77bcb3193d49636bf616849fb1606806`  
		Last Modified: Tue, 07 Apr 2026 01:24:34 GMT  
		Size: 133.8 MB (133816691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48748fe5d0f4632ec7d18ac491ce5cb0cffbe6d7234c32dfe6dc0bd4fb4b3850`  
		Last Modified: Tue, 07 Apr 2026 01:24:31 GMT  
		Size: 22.2 MB (22220768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b0509d5a5b35de64c85b97c4d9e0b91137e0b56f2bb4a7b83277acbcb2ecd5`  
		Last Modified: Tue, 07 Apr 2026 01:24:30 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f565d72108e48769ef7d7d980b8219a0f978727cd4391e8a680e89af65ffc61`  
		Last Modified: Tue, 07 Apr 2026 01:24:40 GMT  
		Size: 424.2 MB (424221758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6` - unknown; unknown

```console
$ docker pull haskell@sha256:694cf27f0136dfaa30e785046d28a52f827d9ceac1782f7af8fe676f7ddc8e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada9b6c5cb34a3f33ff8e3f9477f6927e1cb38ad6464a85443659e2f5e783004`

```dockerfile
```

-	Layers:
	-	`sha256:4294ca5b538bfc45e0bc48840e743de19d0c821197472b01f772465a8c734f00`  
		Last Modified: Tue, 07 Apr 2026 01:24:30 GMT  
		Size: 9.4 MB (9408813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376bb792fe3d16640dbd4862910286f7d47e7dc3ac76347cd92046eee51e6338`  
		Last Modified: Tue, 07 Apr 2026 01:24:29 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e5a91aca06e42ba3fda36fb56934958fd2ddc0b90435d5cb2b9f65a08aa637c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.4 MB (658374842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d905660dd1b06077148c46320b27a064ed3d093fb3f3a6cba860285c39206358`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:20:26 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:20:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:26 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:20:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:20:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:20:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:20:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:20:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:20:30 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:20:30 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:21:50 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:21:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:21:50 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bda1618f14cdd6eef348cdbbc94232b5ab08d6778e0cc9d1143a322b5a6da5`  
		Last Modified: Tue, 07 Apr 2026 01:23:12 GMT  
		Size: 129.3 MB (129273881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf3abd17a819ef74d1e95839c55290e5e7f0471606e598e285b7dc45eb8cdf`  
		Last Modified: Tue, 07 Apr 2026 01:23:07 GMT  
		Size: 24.5 MB (24528546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519926cdd4493d8a37aaf622139c565ef9e7c85a243373bb07f4153f3eea1f23`  
		Last Modified: Tue, 07 Apr 2026 01:23:07 GMT  
		Size: 14.0 MB (13972957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7816f6a5011a2a00352d6c8d852da65f69b7a67674f811cd031eb47816a91a65`  
		Last Modified: Tue, 07 Apr 2026 01:23:18 GMT  
		Size: 438.4 MB (438351843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6` - unknown; unknown

```console
$ docker pull haskell@sha256:e65434a147b543ced6308bbd018a6d914d051a1b563caa9745b729ab4abeca60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9436144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff8cfc0d3db92b8747d13af51d6d7a3c038be4954249b25e33d770e70658b61`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c61ee67d6dc6ff4cf78c9874150f7d5875934c9ba2bb486b7120d213b643`  
		Last Modified: Tue, 07 Apr 2026 01:23:06 GMT  
		Size: 9.4 MB (9410061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba302ab6ca37e4f84ad0b63b6aacff89b87bc97c09f1d3c2210530554555190c`  
		Last Modified: Tue, 07 Apr 2026 01:23:06 GMT  
		Size: 26.1 KB (26083 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-bullseye`

```console
$ docker pull haskell@sha256:d9609bb8f14b87636cb7432f3914407e14a832eb2d4980d21b2e4465b33dcc2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:006b552d40ef387f13149a6635cd5ced9fb26676f0b1ab739acb235600b23650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641634243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e36241573919b5f2e65f3c519282dce675b1ee558d4c6e55433f67d35b0589`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:56 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:21:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:23:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:23:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:23:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0f437936c2255161efab8ddeb40df77bcb3193d49636bf616849fb1606806`  
		Last Modified: Tue, 07 Apr 2026 01:24:34 GMT  
		Size: 133.8 MB (133816691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48748fe5d0f4632ec7d18ac491ce5cb0cffbe6d7234c32dfe6dc0bd4fb4b3850`  
		Last Modified: Tue, 07 Apr 2026 01:24:31 GMT  
		Size: 22.2 MB (22220768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b0509d5a5b35de64c85b97c4d9e0b91137e0b56f2bb4a7b83277acbcb2ecd5`  
		Last Modified: Tue, 07 Apr 2026 01:24:30 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f565d72108e48769ef7d7d980b8219a0f978727cd4391e8a680e89af65ffc61`  
		Last Modified: Tue, 07 Apr 2026 01:24:40 GMT  
		Size: 424.2 MB (424221758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:694cf27f0136dfaa30e785046d28a52f827d9ceac1782f7af8fe676f7ddc8e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada9b6c5cb34a3f33ff8e3f9477f6927e1cb38ad6464a85443659e2f5e783004`

```dockerfile
```

-	Layers:
	-	`sha256:4294ca5b538bfc45e0bc48840e743de19d0c821197472b01f772465a8c734f00`  
		Last Modified: Tue, 07 Apr 2026 01:24:30 GMT  
		Size: 9.4 MB (9408813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376bb792fe3d16640dbd4862910286f7d47e7dc3ac76347cd92046eee51e6338`  
		Last Modified: Tue, 07 Apr 2026 01:24:29 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e5a91aca06e42ba3fda36fb56934958fd2ddc0b90435d5cb2b9f65a08aa637c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.4 MB (658374842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d905660dd1b06077148c46320b27a064ed3d093fb3f3a6cba860285c39206358`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:20:26 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:20:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:26 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:20:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:20:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:20:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:20:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:20:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:20:30 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:20:30 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:21:50 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:21:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:21:50 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bda1618f14cdd6eef348cdbbc94232b5ab08d6778e0cc9d1143a322b5a6da5`  
		Last Modified: Tue, 07 Apr 2026 01:23:12 GMT  
		Size: 129.3 MB (129273881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf3abd17a819ef74d1e95839c55290e5e7f0471606e598e285b7dc45eb8cdf`  
		Last Modified: Tue, 07 Apr 2026 01:23:07 GMT  
		Size: 24.5 MB (24528546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519926cdd4493d8a37aaf622139c565ef9e7c85a243373bb07f4153f3eea1f23`  
		Last Modified: Tue, 07 Apr 2026 01:23:07 GMT  
		Size: 14.0 MB (13972957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7816f6a5011a2a00352d6c8d852da65f69b7a67674f811cd031eb47816a91a65`  
		Last Modified: Tue, 07 Apr 2026 01:23:18 GMT  
		Size: 438.4 MB (438351843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:e65434a147b543ced6308bbd018a6d914d051a1b563caa9745b729ab4abeca60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9436144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff8cfc0d3db92b8747d13af51d6d7a3c038be4954249b25e33d770e70658b61`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c61ee67d6dc6ff4cf78c9874150f7d5875934c9ba2bb486b7120d213b643`  
		Last Modified: Tue, 07 Apr 2026 01:23:06 GMT  
		Size: 9.4 MB (9410061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba302ab6ca37e4f84ad0b63b6aacff89b87bc97c09f1d3c2210530554555190c`  
		Last Modified: Tue, 07 Apr 2026 01:23:06 GMT  
		Size: 26.1 KB (26083 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-slim`

```console
$ docker pull haskell@sha256:6b9cddea37aaa9cf6c83024b437232c12295e9aa786b41fdc8c52238666bcb38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:55f11d8d81bc681115f8d66445727f18a9d8b61c535849118a9ffdc3ceeab8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590701827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52aa83116391add480cc426ffd3c6f655bae54d0802711669e308d55aed76ba`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:22:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a673ceb44a304ec95d9ec3a4552a15b6ec332792b6e9e7dacbe456dd47639f74`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 106.4 MB (106394062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406a8d52e21b244390398e286d5690db277efdc4135cad90bf063d8d750bdc45`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b15f285b15b73eba7b501530961dd1a15d25c8a436563bf4cdd6a7dce089a21`  
		Last Modified: Tue, 07 Apr 2026 01:24:06 GMT  
		Size: 424.2 MB (424216732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:05447ea2e29c5e644885341354bda070c198cc15f7c7dd1a6b3c9a1f96c37436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55628b8168d611af165cdd6c57bb1bd9dd3ab59c029edf4bd9523ada9e8310`

```dockerfile
```

-	Layers:
	-	`sha256:4617d0e6c2d2ac4602f53f885b0d49a25e922ac02585a47058ee99b09e17b40e`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 6.8 MB (6760728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b51503fd29bb7700c2d0a26181b0078502d3dcebd9978c9a31ecdae55ca7ea5`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:1413bb058f5fb67119e3e7d0653f056993448d5da356c974268196f186ecff93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607467677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce19e587f61a9c5bf96f24d0e78470189867dddc0969cc96a5651d2a880cbfc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:12 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:16 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:21:16 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:22:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bf839e1a3eee900a080e41a0a1a0883eb8988fdfb6b52ee8c0adc79184e79e`  
		Last Modified: Tue, 07 Apr 2026 01:24:00 GMT  
		Size: 101.9 MB (101873264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb6c1a061a19435eb47ed16fbd819e504e5490a3c4a3b3467a18f7a1ecd857f`  
		Last Modified: Tue, 07 Apr 2026 01:23:57 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0e03b7ff27c0c481d0805f12107b30d46f14f1b217a3c7da235ad675d1c220`  
		Last Modified: Tue, 07 Apr 2026 01:23:57 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35281edca7d14407e582f0963503c4498184d02ff39602c51936535a580b4b4`  
		Last Modified: Tue, 07 Apr 2026 01:24:06 GMT  
		Size: 438.3 MB (438348215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:83c7944f788e2e928c00a6722403e6747f8432569def1d22f2022c313c353674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99637615982611990b6da94aca9afde2d67964195fafb041775cb92e2f666c0f`

```dockerfile
```

-	Layers:
	-	`sha256:e40c96760f83ee67164f9179476b99ffe349e2e2d6935a3c0aeb791bf16ca217`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 6.8 MB (6763238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e738e4d037ba88b326c93761545816135c87e400b7371c3479b57b7a946208ed`  
		Last Modified: Tue, 07 Apr 2026 01:23:55 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-slim-bullseye`

```console
$ docker pull haskell@sha256:6b9cddea37aaa9cf6c83024b437232c12295e9aa786b41fdc8c52238666bcb38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:55f11d8d81bc681115f8d66445727f18a9d8b61c535849118a9ffdc3ceeab8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590701827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52aa83116391add480cc426ffd3c6f655bae54d0802711669e308d55aed76ba`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:22:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a673ceb44a304ec95d9ec3a4552a15b6ec332792b6e9e7dacbe456dd47639f74`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 106.4 MB (106394062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406a8d52e21b244390398e286d5690db277efdc4135cad90bf063d8d750bdc45`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b15f285b15b73eba7b501530961dd1a15d25c8a436563bf4cdd6a7dce089a21`  
		Last Modified: Tue, 07 Apr 2026 01:24:06 GMT  
		Size: 424.2 MB (424216732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:05447ea2e29c5e644885341354bda070c198cc15f7c7dd1a6b3c9a1f96c37436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55628b8168d611af165cdd6c57bb1bd9dd3ab59c029edf4bd9523ada9e8310`

```dockerfile
```

-	Layers:
	-	`sha256:4617d0e6c2d2ac4602f53f885b0d49a25e922ac02585a47058ee99b09e17b40e`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 6.8 MB (6760728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b51503fd29bb7700c2d0a26181b0078502d3dcebd9978c9a31ecdae55ca7ea5`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:1413bb058f5fb67119e3e7d0653f056993448d5da356c974268196f186ecff93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607467677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce19e587f61a9c5bf96f24d0e78470189867dddc0969cc96a5651d2a880cbfc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:12 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:16 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:21:16 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:22:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bf839e1a3eee900a080e41a0a1a0883eb8988fdfb6b52ee8c0adc79184e79e`  
		Last Modified: Tue, 07 Apr 2026 01:24:00 GMT  
		Size: 101.9 MB (101873264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb6c1a061a19435eb47ed16fbd819e504e5490a3c4a3b3467a18f7a1ecd857f`  
		Last Modified: Tue, 07 Apr 2026 01:23:57 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0e03b7ff27c0c481d0805f12107b30d46f14f1b217a3c7da235ad675d1c220`  
		Last Modified: Tue, 07 Apr 2026 01:23:57 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35281edca7d14407e582f0963503c4498184d02ff39602c51936535a580b4b4`  
		Last Modified: Tue, 07 Apr 2026 01:24:06 GMT  
		Size: 438.3 MB (438348215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:83c7944f788e2e928c00a6722403e6747f8432569def1d22f2022c313c353674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99637615982611990b6da94aca9afde2d67964195fafb041775cb92e2f666c0f`

```dockerfile
```

-	Layers:
	-	`sha256:e40c96760f83ee67164f9179476b99ffe349e2e2d6935a3c0aeb791bf16ca217`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 6.8 MB (6763238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e738e4d037ba88b326c93761545816135c87e400b7371c3479b57b7a946208ed`  
		Last Modified: Tue, 07 Apr 2026 01:23:55 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7`

```console
$ docker pull haskell@sha256:d9609bb8f14b87636cb7432f3914407e14a832eb2d4980d21b2e4465b33dcc2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7` - linux; amd64

```console
$ docker pull haskell@sha256:006b552d40ef387f13149a6635cd5ced9fb26676f0b1ab739acb235600b23650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641634243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e36241573919b5f2e65f3c519282dce675b1ee558d4c6e55433f67d35b0589`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:56 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:21:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:23:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:23:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:23:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0f437936c2255161efab8ddeb40df77bcb3193d49636bf616849fb1606806`  
		Last Modified: Tue, 07 Apr 2026 01:24:34 GMT  
		Size: 133.8 MB (133816691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48748fe5d0f4632ec7d18ac491ce5cb0cffbe6d7234c32dfe6dc0bd4fb4b3850`  
		Last Modified: Tue, 07 Apr 2026 01:24:31 GMT  
		Size: 22.2 MB (22220768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b0509d5a5b35de64c85b97c4d9e0b91137e0b56f2bb4a7b83277acbcb2ecd5`  
		Last Modified: Tue, 07 Apr 2026 01:24:30 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f565d72108e48769ef7d7d980b8219a0f978727cd4391e8a680e89af65ffc61`  
		Last Modified: Tue, 07 Apr 2026 01:24:40 GMT  
		Size: 424.2 MB (424221758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7` - unknown; unknown

```console
$ docker pull haskell@sha256:694cf27f0136dfaa30e785046d28a52f827d9ceac1782f7af8fe676f7ddc8e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada9b6c5cb34a3f33ff8e3f9477f6927e1cb38ad6464a85443659e2f5e783004`

```dockerfile
```

-	Layers:
	-	`sha256:4294ca5b538bfc45e0bc48840e743de19d0c821197472b01f772465a8c734f00`  
		Last Modified: Tue, 07 Apr 2026 01:24:30 GMT  
		Size: 9.4 MB (9408813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376bb792fe3d16640dbd4862910286f7d47e7dc3ac76347cd92046eee51e6338`  
		Last Modified: Tue, 07 Apr 2026 01:24:29 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e5a91aca06e42ba3fda36fb56934958fd2ddc0b90435d5cb2b9f65a08aa637c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.4 MB (658374842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d905660dd1b06077148c46320b27a064ed3d093fb3f3a6cba860285c39206358`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:20:26 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:20:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:26 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:20:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:20:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:20:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:20:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:20:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:20:30 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:20:30 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:21:50 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:21:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:21:50 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bda1618f14cdd6eef348cdbbc94232b5ab08d6778e0cc9d1143a322b5a6da5`  
		Last Modified: Tue, 07 Apr 2026 01:23:12 GMT  
		Size: 129.3 MB (129273881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf3abd17a819ef74d1e95839c55290e5e7f0471606e598e285b7dc45eb8cdf`  
		Last Modified: Tue, 07 Apr 2026 01:23:07 GMT  
		Size: 24.5 MB (24528546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519926cdd4493d8a37aaf622139c565ef9e7c85a243373bb07f4153f3eea1f23`  
		Last Modified: Tue, 07 Apr 2026 01:23:07 GMT  
		Size: 14.0 MB (13972957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7816f6a5011a2a00352d6c8d852da65f69b7a67674f811cd031eb47816a91a65`  
		Last Modified: Tue, 07 Apr 2026 01:23:18 GMT  
		Size: 438.4 MB (438351843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7` - unknown; unknown

```console
$ docker pull haskell@sha256:e65434a147b543ced6308bbd018a6d914d051a1b563caa9745b729ab4abeca60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9436144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff8cfc0d3db92b8747d13af51d6d7a3c038be4954249b25e33d770e70658b61`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c61ee67d6dc6ff4cf78c9874150f7d5875934c9ba2bb486b7120d213b643`  
		Last Modified: Tue, 07 Apr 2026 01:23:06 GMT  
		Size: 9.4 MB (9410061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba302ab6ca37e4f84ad0b63b6aacff89b87bc97c09f1d3c2210530554555190c`  
		Last Modified: Tue, 07 Apr 2026 01:23:06 GMT  
		Size: 26.1 KB (26083 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-bullseye`

```console
$ docker pull haskell@sha256:d9609bb8f14b87636cb7432f3914407e14a832eb2d4980d21b2e4465b33dcc2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:006b552d40ef387f13149a6635cd5ced9fb26676f0b1ab739acb235600b23650
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641634243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e36241573919b5f2e65f3c519282dce675b1ee558d4c6e55433f67d35b0589`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:53 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:53 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:56 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:21:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:23:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:23:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:23:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b0f437936c2255161efab8ddeb40df77bcb3193d49636bf616849fb1606806`  
		Last Modified: Tue, 07 Apr 2026 01:24:34 GMT  
		Size: 133.8 MB (133816691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48748fe5d0f4632ec7d18ac491ce5cb0cffbe6d7234c32dfe6dc0bd4fb4b3850`  
		Last Modified: Tue, 07 Apr 2026 01:24:31 GMT  
		Size: 22.2 MB (22220768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b0509d5a5b35de64c85b97c4d9e0b91137e0b56f2bb4a7b83277acbcb2ecd5`  
		Last Modified: Tue, 07 Apr 2026 01:24:30 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f565d72108e48769ef7d7d980b8219a0f978727cd4391e8a680e89af65ffc61`  
		Last Modified: Tue, 07 Apr 2026 01:24:40 GMT  
		Size: 424.2 MB (424221758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:694cf27f0136dfaa30e785046d28a52f827d9ceac1782f7af8fe676f7ddc8e3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada9b6c5cb34a3f33ff8e3f9477f6927e1cb38ad6464a85443659e2f5e783004`

```dockerfile
```

-	Layers:
	-	`sha256:4294ca5b538bfc45e0bc48840e743de19d0c821197472b01f772465a8c734f00`  
		Last Modified: Tue, 07 Apr 2026 01:24:30 GMT  
		Size: 9.4 MB (9408813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376bb792fe3d16640dbd4862910286f7d47e7dc3ac76347cd92046eee51e6338`  
		Last Modified: Tue, 07 Apr 2026 01:24:29 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e5a91aca06e42ba3fda36fb56934958fd2ddc0b90435d5cb2b9f65a08aa637c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.4 MB (658374842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d905660dd1b06077148c46320b27a064ed3d093fb3f3a6cba860285c39206358`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:20:26 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:20:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:20:26 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:20:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:20:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:20:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:20:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:20:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:20:30 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:20:30 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:21:50 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:21:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:21:50 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bda1618f14cdd6eef348cdbbc94232b5ab08d6778e0cc9d1143a322b5a6da5`  
		Last Modified: Tue, 07 Apr 2026 01:23:12 GMT  
		Size: 129.3 MB (129273881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf3abd17a819ef74d1e95839c55290e5e7f0471606e598e285b7dc45eb8cdf`  
		Last Modified: Tue, 07 Apr 2026 01:23:07 GMT  
		Size: 24.5 MB (24528546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519926cdd4493d8a37aaf622139c565ef9e7c85a243373bb07f4153f3eea1f23`  
		Last Modified: Tue, 07 Apr 2026 01:23:07 GMT  
		Size: 14.0 MB (13972957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7816f6a5011a2a00352d6c8d852da65f69b7a67674f811cd031eb47816a91a65`  
		Last Modified: Tue, 07 Apr 2026 01:23:18 GMT  
		Size: 438.4 MB (438351843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:e65434a147b543ced6308bbd018a6d914d051a1b563caa9745b729ab4abeca60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9436144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aff8cfc0d3db92b8747d13af51d6d7a3c038be4954249b25e33d770e70658b61`

```dockerfile
```

-	Layers:
	-	`sha256:2de1c61ee67d6dc6ff4cf78c9874150f7d5875934c9ba2bb486b7120d213b643`  
		Last Modified: Tue, 07 Apr 2026 01:23:06 GMT  
		Size: 9.4 MB (9410061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba302ab6ca37e4f84ad0b63b6aacff89b87bc97c09f1d3c2210530554555190c`  
		Last Modified: Tue, 07 Apr 2026 01:23:06 GMT  
		Size: 26.1 KB (26083 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-slim`

```console
$ docker pull haskell@sha256:6b9cddea37aaa9cf6c83024b437232c12295e9aa786b41fdc8c52238666bcb38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-slim` - linux; amd64

```console
$ docker pull haskell@sha256:55f11d8d81bc681115f8d66445727f18a9d8b61c535849118a9ffdc3ceeab8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590701827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52aa83116391add480cc426ffd3c6f655bae54d0802711669e308d55aed76ba`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:22:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a673ceb44a304ec95d9ec3a4552a15b6ec332792b6e9e7dacbe456dd47639f74`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 106.4 MB (106394062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406a8d52e21b244390398e286d5690db277efdc4135cad90bf063d8d750bdc45`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b15f285b15b73eba7b501530961dd1a15d25c8a436563bf4cdd6a7dce089a21`  
		Last Modified: Tue, 07 Apr 2026 01:24:06 GMT  
		Size: 424.2 MB (424216732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:05447ea2e29c5e644885341354bda070c198cc15f7c7dd1a6b3c9a1f96c37436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55628b8168d611af165cdd6c57bb1bd9dd3ab59c029edf4bd9523ada9e8310`

```dockerfile
```

-	Layers:
	-	`sha256:4617d0e6c2d2ac4602f53f885b0d49a25e922ac02585a47058ee99b09e17b40e`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 6.8 MB (6760728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b51503fd29bb7700c2d0a26181b0078502d3dcebd9978c9a31ecdae55ca7ea5`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:1413bb058f5fb67119e3e7d0653f056993448d5da356c974268196f186ecff93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607467677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce19e587f61a9c5bf96f24d0e78470189867dddc0969cc96a5651d2a880cbfc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:12 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:16 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:21:16 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:22:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bf839e1a3eee900a080e41a0a1a0883eb8988fdfb6b52ee8c0adc79184e79e`  
		Last Modified: Tue, 07 Apr 2026 01:24:00 GMT  
		Size: 101.9 MB (101873264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb6c1a061a19435eb47ed16fbd819e504e5490a3c4a3b3467a18f7a1ecd857f`  
		Last Modified: Tue, 07 Apr 2026 01:23:57 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0e03b7ff27c0c481d0805f12107b30d46f14f1b217a3c7da235ad675d1c220`  
		Last Modified: Tue, 07 Apr 2026 01:23:57 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35281edca7d14407e582f0963503c4498184d02ff39602c51936535a580b4b4`  
		Last Modified: Tue, 07 Apr 2026 01:24:06 GMT  
		Size: 438.3 MB (438348215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:83c7944f788e2e928c00a6722403e6747f8432569def1d22f2022c313c353674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99637615982611990b6da94aca9afde2d67964195fafb041775cb92e2f666c0f`

```dockerfile
```

-	Layers:
	-	`sha256:e40c96760f83ee67164f9179476b99ffe349e2e2d6935a3c0aeb791bf16ca217`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 6.8 MB (6763238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e738e4d037ba88b326c93761545816135c87e400b7371c3479b57b7a946208ed`  
		Last Modified: Tue, 07 Apr 2026 01:23:55 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-slim-bullseye`

```console
$ docker pull haskell@sha256:6b9cddea37aaa9cf6c83024b437232c12295e9aa786b41fdc8c52238666bcb38
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:55f11d8d81bc681115f8d66445727f18a9d8b61c535849118a9ffdc3ceeab8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590701827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52aa83116391add480cc426ffd3c6f655bae54d0802711669e308d55aed76ba`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:22:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a673ceb44a304ec95d9ec3a4552a15b6ec332792b6e9e7dacbe456dd47639f74`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 106.4 MB (106394062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406a8d52e21b244390398e286d5690db277efdc4135cad90bf063d8d750bdc45`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b15f285b15b73eba7b501530961dd1a15d25c8a436563bf4cdd6a7dce089a21`  
		Last Modified: Tue, 07 Apr 2026 01:24:06 GMT  
		Size: 424.2 MB (424216732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:05447ea2e29c5e644885341354bda070c198cc15f7c7dd1a6b3c9a1f96c37436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b55628b8168d611af165cdd6c57bb1bd9dd3ab59c029edf4bd9523ada9e8310`

```dockerfile
```

-	Layers:
	-	`sha256:4617d0e6c2d2ac4602f53f885b0d49a25e922ac02585a47058ee99b09e17b40e`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 6.8 MB (6760728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b51503fd29bb7700c2d0a26181b0078502d3dcebd9978c9a31ecdae55ca7ea5`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:1413bb058f5fb67119e3e7d0653f056993448d5da356c974268196f186ecff93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607467677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce19e587f61a9c5bf96f24d0e78470189867dddc0969cc96a5651d2a880cbfc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:12 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:12 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:16 GMT
ARG GHC=9.6.7
# Tue, 07 Apr 2026 01:21:16 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 07 Apr 2026 01:22:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bf839e1a3eee900a080e41a0a1a0883eb8988fdfb6b52ee8c0adc79184e79e`  
		Last Modified: Tue, 07 Apr 2026 01:24:00 GMT  
		Size: 101.9 MB (101873264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb6c1a061a19435eb47ed16fbd819e504e5490a3c4a3b3467a18f7a1ecd857f`  
		Last Modified: Tue, 07 Apr 2026 01:23:57 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0e03b7ff27c0c481d0805f12107b30d46f14f1b217a3c7da235ad675d1c220`  
		Last Modified: Tue, 07 Apr 2026 01:23:57 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35281edca7d14407e582f0963503c4498184d02ff39602c51936535a580b4b4`  
		Last Modified: Tue, 07 Apr 2026 01:24:06 GMT  
		Size: 438.3 MB (438348215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:83c7944f788e2e928c00a6722403e6747f8432569def1d22f2022c313c353674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99637615982611990b6da94aca9afde2d67964195fafb041775cb92e2f666c0f`

```dockerfile
```

-	Layers:
	-	`sha256:e40c96760f83ee67164f9179476b99ffe349e2e2d6935a3c0aeb791bf16ca217`  
		Last Modified: Tue, 07 Apr 2026 01:23:56 GMT  
		Size: 6.8 MB (6763238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e738e4d037ba88b326c93761545816135c87e400b7371c3479b57b7a946208ed`  
		Last Modified: Tue, 07 Apr 2026 01:23:55 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8`

```console
$ docker pull haskell@sha256:915b315884d994bfc71b735acd9eb68191abadc4aa7c9d5ae94f52c5c0ed452b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8` - linux; amd64

```console
$ docker pull haskell@sha256:77b862bb369d317241cf60f468e134ca82b2335888903466ed0cf95e393b4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653629561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bfbaf6321dfc4a7359185a9f2c30ae8b2ecffe23e2d9dc66bcf233e924290b`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:42 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:42 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:44 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:44 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:45 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:45 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:45 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:20:13 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0d1819ba7d2cec2e647e6418ea1b3c8fca720db74353ed57043d4129c0dc81`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 133.8 MB (133816306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c71821fdfcba4c8bc9bf00f093afd6540e16c14a20fe96bafc1b9ab66e15916`  
		Last Modified: Tue, 07 Apr 2026 01:21:20 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a21e15024b4b4d4b2c2c2f933fd4cbd182a465feb5ad58ca0536032d6873c46`  
		Last Modified: Tue, 07 Apr 2026 01:21:19 GMT  
		Size: 7.6 MB (7612231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8441208f16579666b0922527ac389b3888dd8575506a5e1c6b3aa7e37ef4151f`  
		Last Modified: Tue, 07 Apr 2026 01:21:39 GMT  
		Size: 436.2 MB (436217450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8` - unknown; unknown

```console
$ docker pull haskell@sha256:865512da89994d79832f57ca34c3e2ca9a0ae7392b64d73e2cd3d68d403bcf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf91400a324315d439c73e3542d832ea9fa51b09b09e72462d03e3c71fab7f6`

```dockerfile
```

-	Layers:
	-	`sha256:ecb7472999c6d314641672dd50b329ac7cab58950ff7c7be7b34e59a222a72dd`  
		Last Modified: Tue, 07 Apr 2026 01:21:19 GMT  
		Size: 9.4 MB (9408813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da3bbffdc72ae8dad1404da27f2b21c62b8768de840fb7957138c57a4838c37`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:165bc1e969df9e7ab0b5a3a6c092e6ed8738d07e2437be7f160dec0bf9068b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663820222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b04d1c24b6ad6eac731b2755d6878daa01cb74c0f3cd9f5926d882af807f82`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:58 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:27 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f8e62004484d00a1050d5768e36bb09b11de7d5bf17c3a5841e51b62ab277a`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 129.3 MB (129274059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7e4f46f6f1f19609845e0460c1b0e9eb963d8b78f3333d293169584ac5f0f6`  
		Last Modified: Tue, 07 Apr 2026 01:20:45 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099222138cfa774aa0ea888dd0e81b3f9316e4e9153f82a5f5a69346e831bfdb`  
		Last Modified: Tue, 07 Apr 2026 01:20:44 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c4c03d22838a0110c27bd0f58795d2d7cf9888a099dd3774534a2588f1d5a7`  
		Last Modified: Tue, 07 Apr 2026 01:20:54 GMT  
		Size: 443.8 MB (443797036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8` - unknown; unknown

```console
$ docker pull haskell@sha256:b6e80797456bf7de46122104d2ac0c66ee5519b5a55b3886dff7175b87220004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9435866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca429f50899c3f361b5708fd250988cb16339cfd8cfeedf2a348fc479c7cd01b`

```dockerfile
```

-	Layers:
	-	`sha256:fd3d82c72f3b043686ee4482500ddd6442c85661d2a621e831002837921133f7`  
		Last Modified: Tue, 07 Apr 2026 01:20:44 GMT  
		Size: 9.4 MB (9410061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77906b2d531e743d2d67316718b13c7b0571031ff7acd90aadc67f3d1e9cbc61`  
		Last Modified: Tue, 07 Apr 2026 01:20:43 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-bullseye`

```console
$ docker pull haskell@sha256:915b315884d994bfc71b735acd9eb68191abadc4aa7c9d5ae94f52c5c0ed452b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:77b862bb369d317241cf60f468e134ca82b2335888903466ed0cf95e393b4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653629561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bfbaf6321dfc4a7359185a9f2c30ae8b2ecffe23e2d9dc66bcf233e924290b`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:42 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:42 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:44 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:44 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:45 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:45 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:45 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:20:13 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0d1819ba7d2cec2e647e6418ea1b3c8fca720db74353ed57043d4129c0dc81`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 133.8 MB (133816306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c71821fdfcba4c8bc9bf00f093afd6540e16c14a20fe96bafc1b9ab66e15916`  
		Last Modified: Tue, 07 Apr 2026 01:21:20 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a21e15024b4b4d4b2c2c2f933fd4cbd182a465feb5ad58ca0536032d6873c46`  
		Last Modified: Tue, 07 Apr 2026 01:21:19 GMT  
		Size: 7.6 MB (7612231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8441208f16579666b0922527ac389b3888dd8575506a5e1c6b3aa7e37ef4151f`  
		Last Modified: Tue, 07 Apr 2026 01:21:39 GMT  
		Size: 436.2 MB (436217450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:865512da89994d79832f57ca34c3e2ca9a0ae7392b64d73e2cd3d68d403bcf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf91400a324315d439c73e3542d832ea9fa51b09b09e72462d03e3c71fab7f6`

```dockerfile
```

-	Layers:
	-	`sha256:ecb7472999c6d314641672dd50b329ac7cab58950ff7c7be7b34e59a222a72dd`  
		Last Modified: Tue, 07 Apr 2026 01:21:19 GMT  
		Size: 9.4 MB (9408813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da3bbffdc72ae8dad1404da27f2b21c62b8768de840fb7957138c57a4838c37`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:165bc1e969df9e7ab0b5a3a6c092e6ed8738d07e2437be7f160dec0bf9068b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663820222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b04d1c24b6ad6eac731b2755d6878daa01cb74c0f3cd9f5926d882af807f82`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:58 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:27 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f8e62004484d00a1050d5768e36bb09b11de7d5bf17c3a5841e51b62ab277a`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 129.3 MB (129274059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7e4f46f6f1f19609845e0460c1b0e9eb963d8b78f3333d293169584ac5f0f6`  
		Last Modified: Tue, 07 Apr 2026 01:20:45 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099222138cfa774aa0ea888dd0e81b3f9316e4e9153f82a5f5a69346e831bfdb`  
		Last Modified: Tue, 07 Apr 2026 01:20:44 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c4c03d22838a0110c27bd0f58795d2d7cf9888a099dd3774534a2588f1d5a7`  
		Last Modified: Tue, 07 Apr 2026 01:20:54 GMT  
		Size: 443.8 MB (443797036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b6e80797456bf7de46122104d2ac0c66ee5519b5a55b3886dff7175b87220004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9435866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca429f50899c3f361b5708fd250988cb16339cfd8cfeedf2a348fc479c7cd01b`

```dockerfile
```

-	Layers:
	-	`sha256:fd3d82c72f3b043686ee4482500ddd6442c85661d2a621e831002837921133f7`  
		Last Modified: Tue, 07 Apr 2026 01:20:44 GMT  
		Size: 9.4 MB (9410061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77906b2d531e743d2d67316718b13c7b0571031ff7acd90aadc67f3d1e9cbc61`  
		Last Modified: Tue, 07 Apr 2026 01:20:43 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-slim`

```console
$ docker pull haskell@sha256:a3d4f9268b7d21f57798084a62194a453ad0e13c9d36231b7e9fd1a8876c70dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:f00c7949c7d269ae534997f02b148c283a2b1e688b3bf3b06620103dfe2bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602696918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea78f72fe36f1de0a103a1a760ceb09e2d9ac58310377e64abf956d039a581c7`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:00 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:02 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:02 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:04 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:21:04 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:22:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:35 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070840201c2b8960186ad4615acab73ea3c17163e112773fd4dbd23daa269b46`  
		Last Modified: Tue, 07 Apr 2026 01:23:51 GMT  
		Size: 106.4 MB (106393897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d694fad034f2a56f47d5287e0d14e4548f0bdea145d1b881e4fd34ea5673660`  
		Last Modified: Tue, 07 Apr 2026 01:23:48 GMT  
		Size: 22.2 MB (22220782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f343e580ad1778a4fe62bba222d6e8b9e7cf3ceded56b53d06c795e39d3700`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 7.6 MB (7612226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8755cab515ea33af75a9e0358e5540694c45e125c5c45b7e38e7c094a9dc166f`  
		Last Modified: Tue, 07 Apr 2026 01:23:58 GMT  
		Size: 436.2 MB (436211994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:ded31a1b7789ab600df43e420455c965c6b34e0302d5c9e0ddd092588dcd7bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ee690cd5928cd5f1850d1ac436ad43fadde02b6e94f79a4a46be701192c39f`

```dockerfile
```

-	Layers:
	-	`sha256:ea6917317bf88a7c0201bc2e418de62a9eb351cdadc84a3c9dc09158971eee5a`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 6.8 MB (6760728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40c5b6e0ec5fc28afd44172a0acff23cbe117a11aa4f77b24700b0891fdc344`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:154976a0cd7e72f9cd6b3ac772255385944f8f0d7cdd71f71c501a35bf091bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612920823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20dbbf5182ed9b92411bad2a371a74110f4af92294abc656dc35a0cbc49ffdc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:32 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:32 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911fe2bb7940b9768a70e949de8d81e6507f7ff34215684e84af18732528bf81`  
		Last Modified: Tue, 07 Apr 2026 01:20:51 GMT  
		Size: 101.9 MB (101873464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9121d016d5f953151fed041985521b5196b8268beede07dd2cd3d3f7ebb328b1`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 24.5 MB (24528621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c1e1c1c0cb2d50b0ae3a91d5451717df8853eb61badd28cc1432f29707b0e`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034d157d87748895c438f14901dc95f49a8b2e7add7f2145351b59e0301f4869`  
		Last Modified: Tue, 07 Apr 2026 01:20:57 GMT  
		Size: 443.8 MB (443801087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:39b72cb8232a4e2f50158ed805060047979c672363f8ae8fcf86060eccc7fa5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7812466682348ad17f5960b26e9f10396c01fbe1cdbf1a404c4cfe9e4e26913`

```dockerfile
```

-	Layers:
	-	`sha256:77a24a79d3c388fe22757705003f7655c1ffa21fd2b59ebd1c0e3e2627572f33`  
		Last Modified: Tue, 07 Apr 2026 01:20:47 GMT  
		Size: 6.8 MB (6763238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb965493f73796ddf28479abb5ebeef7848f4204da756a377692bca88370d0aa`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-slim-bullseye`

```console
$ docker pull haskell@sha256:a3d4f9268b7d21f57798084a62194a453ad0e13c9d36231b7e9fd1a8876c70dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f00c7949c7d269ae534997f02b148c283a2b1e688b3bf3b06620103dfe2bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602696918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea78f72fe36f1de0a103a1a760ceb09e2d9ac58310377e64abf956d039a581c7`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:00 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:02 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:02 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:04 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:21:04 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:22:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:35 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070840201c2b8960186ad4615acab73ea3c17163e112773fd4dbd23daa269b46`  
		Last Modified: Tue, 07 Apr 2026 01:23:51 GMT  
		Size: 106.4 MB (106393897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d694fad034f2a56f47d5287e0d14e4548f0bdea145d1b881e4fd34ea5673660`  
		Last Modified: Tue, 07 Apr 2026 01:23:48 GMT  
		Size: 22.2 MB (22220782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f343e580ad1778a4fe62bba222d6e8b9e7cf3ceded56b53d06c795e39d3700`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 7.6 MB (7612226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8755cab515ea33af75a9e0358e5540694c45e125c5c45b7e38e7c094a9dc166f`  
		Last Modified: Tue, 07 Apr 2026 01:23:58 GMT  
		Size: 436.2 MB (436211994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:ded31a1b7789ab600df43e420455c965c6b34e0302d5c9e0ddd092588dcd7bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ee690cd5928cd5f1850d1ac436ad43fadde02b6e94f79a4a46be701192c39f`

```dockerfile
```

-	Layers:
	-	`sha256:ea6917317bf88a7c0201bc2e418de62a9eb351cdadc84a3c9dc09158971eee5a`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 6.8 MB (6760728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40c5b6e0ec5fc28afd44172a0acff23cbe117a11aa4f77b24700b0891fdc344`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:154976a0cd7e72f9cd6b3ac772255385944f8f0d7cdd71f71c501a35bf091bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612920823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20dbbf5182ed9b92411bad2a371a74110f4af92294abc656dc35a0cbc49ffdc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:32 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:32 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911fe2bb7940b9768a70e949de8d81e6507f7ff34215684e84af18732528bf81`  
		Last Modified: Tue, 07 Apr 2026 01:20:51 GMT  
		Size: 101.9 MB (101873464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9121d016d5f953151fed041985521b5196b8268beede07dd2cd3d3f7ebb328b1`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 24.5 MB (24528621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c1e1c1c0cb2d50b0ae3a91d5451717df8853eb61badd28cc1432f29707b0e`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034d157d87748895c438f14901dc95f49a8b2e7add7f2145351b59e0301f4869`  
		Last Modified: Tue, 07 Apr 2026 01:20:57 GMT  
		Size: 443.8 MB (443801087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:39b72cb8232a4e2f50158ed805060047979c672363f8ae8fcf86060eccc7fa5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7812466682348ad17f5960b26e9f10396c01fbe1cdbf1a404c4cfe9e4e26913`

```dockerfile
```

-	Layers:
	-	`sha256:77a24a79d3c388fe22757705003f7655c1ffa21fd2b59ebd1c0e3e2627572f33`  
		Last Modified: Tue, 07 Apr 2026 01:20:47 GMT  
		Size: 6.8 MB (6763238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb965493f73796ddf28479abb5ebeef7848f4204da756a377692bca88370d0aa`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4`

```console
$ docker pull haskell@sha256:915b315884d994bfc71b735acd9eb68191abadc4aa7c9d5ae94f52c5c0ed452b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4` - linux; amd64

```console
$ docker pull haskell@sha256:77b862bb369d317241cf60f468e134ca82b2335888903466ed0cf95e393b4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653629561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bfbaf6321dfc4a7359185a9f2c30ae8b2ecffe23e2d9dc66bcf233e924290b`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:42 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:42 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:44 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:44 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:45 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:45 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:45 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:20:13 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0d1819ba7d2cec2e647e6418ea1b3c8fca720db74353ed57043d4129c0dc81`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 133.8 MB (133816306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c71821fdfcba4c8bc9bf00f093afd6540e16c14a20fe96bafc1b9ab66e15916`  
		Last Modified: Tue, 07 Apr 2026 01:21:20 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a21e15024b4b4d4b2c2c2f933fd4cbd182a465feb5ad58ca0536032d6873c46`  
		Last Modified: Tue, 07 Apr 2026 01:21:19 GMT  
		Size: 7.6 MB (7612231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8441208f16579666b0922527ac389b3888dd8575506a5e1c6b3aa7e37ef4151f`  
		Last Modified: Tue, 07 Apr 2026 01:21:39 GMT  
		Size: 436.2 MB (436217450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4` - unknown; unknown

```console
$ docker pull haskell@sha256:865512da89994d79832f57ca34c3e2ca9a0ae7392b64d73e2cd3d68d403bcf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf91400a324315d439c73e3542d832ea9fa51b09b09e72462d03e3c71fab7f6`

```dockerfile
```

-	Layers:
	-	`sha256:ecb7472999c6d314641672dd50b329ac7cab58950ff7c7be7b34e59a222a72dd`  
		Last Modified: Tue, 07 Apr 2026 01:21:19 GMT  
		Size: 9.4 MB (9408813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da3bbffdc72ae8dad1404da27f2b21c62b8768de840fb7957138c57a4838c37`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:165bc1e969df9e7ab0b5a3a6c092e6ed8738d07e2437be7f160dec0bf9068b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663820222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b04d1c24b6ad6eac731b2755d6878daa01cb74c0f3cd9f5926d882af807f82`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:58 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:27 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f8e62004484d00a1050d5768e36bb09b11de7d5bf17c3a5841e51b62ab277a`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 129.3 MB (129274059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7e4f46f6f1f19609845e0460c1b0e9eb963d8b78f3333d293169584ac5f0f6`  
		Last Modified: Tue, 07 Apr 2026 01:20:45 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099222138cfa774aa0ea888dd0e81b3f9316e4e9153f82a5f5a69346e831bfdb`  
		Last Modified: Tue, 07 Apr 2026 01:20:44 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c4c03d22838a0110c27bd0f58795d2d7cf9888a099dd3774534a2588f1d5a7`  
		Last Modified: Tue, 07 Apr 2026 01:20:54 GMT  
		Size: 443.8 MB (443797036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4` - unknown; unknown

```console
$ docker pull haskell@sha256:b6e80797456bf7de46122104d2ac0c66ee5519b5a55b3886dff7175b87220004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9435866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca429f50899c3f361b5708fd250988cb16339cfd8cfeedf2a348fc479c7cd01b`

```dockerfile
```

-	Layers:
	-	`sha256:fd3d82c72f3b043686ee4482500ddd6442c85661d2a621e831002837921133f7`  
		Last Modified: Tue, 07 Apr 2026 01:20:44 GMT  
		Size: 9.4 MB (9410061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77906b2d531e743d2d67316718b13c7b0571031ff7acd90aadc67f3d1e9cbc61`  
		Last Modified: Tue, 07 Apr 2026 01:20:43 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-bullseye`

```console
$ docker pull haskell@sha256:915b315884d994bfc71b735acd9eb68191abadc4aa7c9d5ae94f52c5c0ed452b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:77b862bb369d317241cf60f468e134ca82b2335888903466ed0cf95e393b4259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653629561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bfbaf6321dfc4a7359185a9f2c30ae8b2ecffe23e2d9dc66bcf233e924290b`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:42 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:42 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:42 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:42 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:44 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:44 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:44 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:45 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:45 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:45 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:20:13 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0d1819ba7d2cec2e647e6418ea1b3c8fca720db74353ed57043d4129c0dc81`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 133.8 MB (133816306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c71821fdfcba4c8bc9bf00f093afd6540e16c14a20fe96bafc1b9ab66e15916`  
		Last Modified: Tue, 07 Apr 2026 01:21:20 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a21e15024b4b4d4b2c2c2f933fd4cbd182a465feb5ad58ca0536032d6873c46`  
		Last Modified: Tue, 07 Apr 2026 01:21:19 GMT  
		Size: 7.6 MB (7612231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8441208f16579666b0922527ac389b3888dd8575506a5e1c6b3aa7e37ef4151f`  
		Last Modified: Tue, 07 Apr 2026 01:21:39 GMT  
		Size: 436.2 MB (436217450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:865512da89994d79832f57ca34c3e2ca9a0ae7392b64d73e2cd3d68d403bcf3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf91400a324315d439c73e3542d832ea9fa51b09b09e72462d03e3c71fab7f6`

```dockerfile
```

-	Layers:
	-	`sha256:ecb7472999c6d314641672dd50b329ac7cab58950ff7c7be7b34e59a222a72dd`  
		Last Modified: Tue, 07 Apr 2026 01:21:19 GMT  
		Size: 9.4 MB (9408813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1da3bbffdc72ae8dad1404da27f2b21c62b8768de840fb7957138c57a4838c37`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:165bc1e969df9e7ab0b5a3a6c092e6ed8738d07e2437be7f160dec0bf9068b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663820222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b04d1c24b6ad6eac731b2755d6878daa01cb74c0f3cd9f5926d882af807f82`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:58 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:58 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:27 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:27 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f8e62004484d00a1050d5768e36bb09b11de7d5bf17c3a5841e51b62ab277a`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 129.3 MB (129274059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7e4f46f6f1f19609845e0460c1b0e9eb963d8b78f3333d293169584ac5f0f6`  
		Last Modified: Tue, 07 Apr 2026 01:20:45 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099222138cfa774aa0ea888dd0e81b3f9316e4e9153f82a5f5a69346e831bfdb`  
		Last Modified: Tue, 07 Apr 2026 01:20:44 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c4c03d22838a0110c27bd0f58795d2d7cf9888a099dd3774534a2588f1d5a7`  
		Last Modified: Tue, 07 Apr 2026 01:20:54 GMT  
		Size: 443.8 MB (443797036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b6e80797456bf7de46122104d2ac0c66ee5519b5a55b3886dff7175b87220004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9435866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca429f50899c3f361b5708fd250988cb16339cfd8cfeedf2a348fc479c7cd01b`

```dockerfile
```

-	Layers:
	-	`sha256:fd3d82c72f3b043686ee4482500ddd6442c85661d2a621e831002837921133f7`  
		Last Modified: Tue, 07 Apr 2026 01:20:44 GMT  
		Size: 9.4 MB (9410061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77906b2d531e743d2d67316718b13c7b0571031ff7acd90aadc67f3d1e9cbc61`  
		Last Modified: Tue, 07 Apr 2026 01:20:43 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-slim`

```console
$ docker pull haskell@sha256:a3d4f9268b7d21f57798084a62194a453ad0e13c9d36231b7e9fd1a8876c70dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-slim` - linux; amd64

```console
$ docker pull haskell@sha256:f00c7949c7d269ae534997f02b148c283a2b1e688b3bf3b06620103dfe2bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602696918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea78f72fe36f1de0a103a1a760ceb09e2d9ac58310377e64abf956d039a581c7`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:00 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:02 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:02 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:04 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:21:04 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:22:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:35 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070840201c2b8960186ad4615acab73ea3c17163e112773fd4dbd23daa269b46`  
		Last Modified: Tue, 07 Apr 2026 01:23:51 GMT  
		Size: 106.4 MB (106393897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d694fad034f2a56f47d5287e0d14e4548f0bdea145d1b881e4fd34ea5673660`  
		Last Modified: Tue, 07 Apr 2026 01:23:48 GMT  
		Size: 22.2 MB (22220782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f343e580ad1778a4fe62bba222d6e8b9e7cf3ceded56b53d06c795e39d3700`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 7.6 MB (7612226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8755cab515ea33af75a9e0358e5540694c45e125c5c45b7e38e7c094a9dc166f`  
		Last Modified: Tue, 07 Apr 2026 01:23:58 GMT  
		Size: 436.2 MB (436211994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:ded31a1b7789ab600df43e420455c965c6b34e0302d5c9e0ddd092588dcd7bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ee690cd5928cd5f1850d1ac436ad43fadde02b6e94f79a4a46be701192c39f`

```dockerfile
```

-	Layers:
	-	`sha256:ea6917317bf88a7c0201bc2e418de62a9eb351cdadc84a3c9dc09158971eee5a`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 6.8 MB (6760728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40c5b6e0ec5fc28afd44172a0acff23cbe117a11aa4f77b24700b0891fdc344`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:154976a0cd7e72f9cd6b3ac772255385944f8f0d7cdd71f71c501a35bf091bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612920823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20dbbf5182ed9b92411bad2a371a74110f4af92294abc656dc35a0cbc49ffdc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:32 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:32 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911fe2bb7940b9768a70e949de8d81e6507f7ff34215684e84af18732528bf81`  
		Last Modified: Tue, 07 Apr 2026 01:20:51 GMT  
		Size: 101.9 MB (101873464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9121d016d5f953151fed041985521b5196b8268beede07dd2cd3d3f7ebb328b1`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 24.5 MB (24528621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c1e1c1c0cb2d50b0ae3a91d5451717df8853eb61badd28cc1432f29707b0e`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034d157d87748895c438f14901dc95f49a8b2e7add7f2145351b59e0301f4869`  
		Last Modified: Tue, 07 Apr 2026 01:20:57 GMT  
		Size: 443.8 MB (443801087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:39b72cb8232a4e2f50158ed805060047979c672363f8ae8fcf86060eccc7fa5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7812466682348ad17f5960b26e9f10396c01fbe1cdbf1a404c4cfe9e4e26913`

```dockerfile
```

-	Layers:
	-	`sha256:77a24a79d3c388fe22757705003f7655c1ffa21fd2b59ebd1c0e3e2627572f33`  
		Last Modified: Tue, 07 Apr 2026 01:20:47 GMT  
		Size: 6.8 MB (6763238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb965493f73796ddf28479abb5ebeef7848f4204da756a377692bca88370d0aa`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-slim-bullseye`

```console
$ docker pull haskell@sha256:a3d4f9268b7d21f57798084a62194a453ad0e13c9d36231b7e9fd1a8876c70dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f00c7949c7d269ae534997f02b148c283a2b1e688b3bf3b06620103dfe2bc940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602696918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea78f72fe36f1de0a103a1a760ceb09e2d9ac58310377e64abf956d039a581c7`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:21:00 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:21:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:21:00 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:21:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:21:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:21:02 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:21:02 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:21:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:21:04 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:21:04 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:22:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:22:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:22:35 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:070840201c2b8960186ad4615acab73ea3c17163e112773fd4dbd23daa269b46`  
		Last Modified: Tue, 07 Apr 2026 01:23:51 GMT  
		Size: 106.4 MB (106393897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d694fad034f2a56f47d5287e0d14e4548f0bdea145d1b881e4fd34ea5673660`  
		Last Modified: Tue, 07 Apr 2026 01:23:48 GMT  
		Size: 22.2 MB (22220782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f343e580ad1778a4fe62bba222d6e8b9e7cf3ceded56b53d06c795e39d3700`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 7.6 MB (7612226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8755cab515ea33af75a9e0358e5540694c45e125c5c45b7e38e7c094a9dc166f`  
		Last Modified: Tue, 07 Apr 2026 01:23:58 GMT  
		Size: 436.2 MB (436211994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:ded31a1b7789ab600df43e420455c965c6b34e0302d5c9e0ddd092588dcd7bc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ee690cd5928cd5f1850d1ac436ad43fadde02b6e94f79a4a46be701192c39f`

```dockerfile
```

-	Layers:
	-	`sha256:ea6917317bf88a7c0201bc2e418de62a9eb351cdadc84a3c9dc09158971eee5a`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 6.8 MB (6760728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f40c5b6e0ec5fc28afd44172a0acff23cbe117a11aa4f77b24700b0891fdc344`  
		Last Modified: Tue, 07 Apr 2026 01:23:46 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:154976a0cd7e72f9cd6b3ac772255385944f8f0d7cdd71f71c501a35bf091bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612920823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f20dbbf5182ed9b92411bad2a371a74110f4af92294abc656dc35a0cbc49ffdc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.8.4
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 07 Apr 2026 01:19:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:32 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:32 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911fe2bb7940b9768a70e949de8d81e6507f7ff34215684e84af18732528bf81`  
		Last Modified: Tue, 07 Apr 2026 01:20:51 GMT  
		Size: 101.9 MB (101873464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9121d016d5f953151fed041985521b5196b8268beede07dd2cd3d3f7ebb328b1`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 24.5 MB (24528621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c1e1c1c0cb2d50b0ae3a91d5451717df8853eb61badd28cc1432f29707b0e`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034d157d87748895c438f14901dc95f49a8b2e7add7f2145351b59e0301f4869`  
		Last Modified: Tue, 07 Apr 2026 01:20:57 GMT  
		Size: 443.8 MB (443801087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:39b72cb8232a4e2f50158ed805060047979c672363f8ae8fcf86060eccc7fa5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7812466682348ad17f5960b26e9f10396c01fbe1cdbf1a404c4cfe9e4e26913`

```dockerfile
```

-	Layers:
	-	`sha256:77a24a79d3c388fe22757705003f7655c1ffa21fd2b59ebd1c0e3e2627572f33`  
		Last Modified: Tue, 07 Apr 2026 01:20:47 GMT  
		Size: 6.8 MB (6763238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb965493f73796ddf28479abb5ebeef7848f4204da756a377692bca88370d0aa`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:bookworm`

```console
$ docker pull haskell@sha256:6cff7c33044cc6b6b5944e64860278df5f66e2fd6546526ee7a3f7b2a0bb302d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:1fbcda9feaaf6fdc37f04994416244502ffc60420ac87bf888b2e27fb4a7e3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f2e39e42a486cc41c8abaa23edc4b5bf18f3e6188c3005107b5376e6872757`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:05 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece92b353df31cd62bcf548d31f7e7551ad5001927d632dc72fdb96777c0a7de`  
		Last Modified: Tue, 07 Apr 2026 01:21:59 GMT  
		Size: 152.4 MB (152404537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9003a62dd97b742a849a6ffe605b33afae135ecf9a6963fa71ce25145093e9`  
		Last Modified: Tue, 07 Apr 2026 01:21:54 GMT  
		Size: 22.2 MB (22220764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03444700904b3892922358de25fdfe826f0169360d9f9cb036eeac113f25554c`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920399cab91d6ff0fc2201575339dc055750baca387d9ed10f94ed92d7adde`  
		Last Modified: Tue, 07 Apr 2026 01:22:11 GMT  
		Size: 593.7 MB (593665337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:bb0b5eca366271d9faabc5051de30bf0ca84556d8d2311a229f9e9cfd86ac081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff0ec4d07cfb43474a87b2b0c0dab7ef9b2b9b1f3f76a5dc23866ef5c9b9169`

```dockerfile
```

-	Layers:
	-	`sha256:18227a676aaf76c21c1183a42a01b9a116a151db0b59a0ea80879bdb63f1e15a`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598a0a7da604db5b7571614d65ef77c3d89c33455779d8a7ae9656cacc7e243c`  
		Last Modified: Tue, 07 Apr 2026 01:21:52 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f32d990dc8da74f7f0341a333164cb1c8d6266a8ac9ad4a945b90117efaffa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.0 MB (827973880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0549a54963f5295de9aca4174ea8cd5c882c87f277d02b84d560108488fee`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:13 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8b2b86a1f61fbc06035adfc6d633c1ef0ac985ee5d01ad2035aa975e75bc5e`  
		Last Modified: Tue, 07 Apr 2026 01:22:18 GMT  
		Size: 146.6 MB (146574461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a921e64342db75f8743327ae9f72db69b755625911158c2ba61f7e5cc3c653`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 24.5 MB (24528556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04627812dc4bd20dfe4c8cdc15e97e22dc630d7688a5f6cf80d91b271266ee`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 15.9 MB (15944580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd72aeb1f170c652f08f92801ce519133208478741fd634ac455a534dd7f21`  
		Last Modified: Tue, 07 Apr 2026 01:22:26 GMT  
		Size: 592.6 MB (592553021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:c5ee901f3e234f95818fd514b41636991e5c804c884191726bdfe9d398b131dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9a7278c6d71557554c28d4ca253da3efb5f1beb63668ba7412cd386f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:25ff4331c3bb33056dbba1acea83141c0be05c91a7822f564aa4ec8e37d10405`  
		Last Modified: Tue, 07 Apr 2026 01:22:13 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0c3e47baeb7423641c403b8e392683ef8fc8fa4cf31429b25de36abf9eb3`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:bullseye`

```console
$ docker pull haskell@sha256:1434abf2aa95282e46916880a70ed9ee02566ef603698d969ce8371340212576
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:40c7aeeca45ca813f36f3e80dea6918b5f9b316ba177eddcb323adcf30f07275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659223113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d840f2cefaa050966550674fb069f56f7ac499d54363561a4930035f5cfaad`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:32 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:32 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:32 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d02dda58f98dd1b89ea56dad93ea597ab2d270a4c5488a5080ebfe4e22608c05`  
		Last Modified: Tue, 07 Apr 2026 01:21:33 GMT  
		Size: 133.8 MB (133816646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6788ea23b7d8f664d2f75dfca6820d1905f375c4b0709aecf2e28c70adf4fff6`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6537af5e28a47f37be1aa665b630dbb58038dedb64aa2fe86bbc08b1567b095`  
		Last Modified: Tue, 07 Apr 2026 01:21:40 GMT  
		Size: 441.8 MB (441810672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:8b7321c089ffb9d02de572c043af25531fb81f3a1367778a6c10db105f1059d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9434307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93647ed1c3cbd8cdc4712413b2170c4c76076508be7f76e44ba8f2d9781b7aca`

```dockerfile
```

-	Layers:
	-	`sha256:7da85245cba7175d03e3f59cb8c744cb7ed18d6d58c00207d1643b72499ae200`  
		Last Modified: Tue, 07 Apr 2026 01:21:28 GMT  
		Size: 9.4 MB (9408030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dc7e5b0791b03f692e44b1eeb39a1ffd1ad2ff71636daecd10aed90c468db1`  
		Last Modified: Tue, 07 Apr 2026 01:21:27 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:efa0a620239a673d67ff573b2139b4db387c710a661a0f5d29c714dcab56061b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.5 MB (669473057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24b52e39a5e2aa5d80d316672bfb8122b184a94a08aaa270df7836b8ff6bca76`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:51 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:17:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:17:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:17:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c24e51cfa942997e098c6febaa4751e88ae4debf1f5dd07bc9bb72927972c8e`  
		Last Modified: Tue, 07 Apr 2026 01:20:53 GMT  
		Size: 129.3 MB (129273970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374ab9ae73c524c4b51e32343734bbc89d93f0ebc83216d04951e9ef1ae57b01`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d39dc89c8cb93b86dcf19088b6e096b806448b6954836844ef750d884b6f7ed`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c9395fb5fbcc181b749007653b2871b370c130abf6eba6eca01e3ab56865bd`  
		Last Modified: Tue, 07 Apr 2026 01:21:00 GMT  
		Size: 449.4 MB (449449962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a46ac3fa59dd96825e6b5930fcd7586bc903333e44d1e995b3c8a62d61538a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9435754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85495acd2d5e485183a23106106f0651c1873c05c7e291b51f2964306eb867e0`

```dockerfile
```

-	Layers:
	-	`sha256:88b942987203a63840e9e1594431326625e9b9168303b88fe5eff77a6d2a3af9`  
		Last Modified: Tue, 07 Apr 2026 01:20:47 GMT  
		Size: 9.4 MB (9409302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3837dcc5606b2cab1f0f41a5ade639d7471f70208472385abccb18ae80c7e53c`  
		Last Modified: Tue, 07 Apr 2026 01:20:46 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:latest`

```console
$ docker pull haskell@sha256:6cff7c33044cc6b6b5944e64860278df5f66e2fd6546526ee7a3f7b2a0bb302d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:1fbcda9feaaf6fdc37f04994416244502ffc60420ac87bf888b2e27fb4a7e3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825182966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f2e39e42a486cc41c8abaa23edc4b5bf18f3e6188c3005107b5376e6872757`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:05 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:05 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:07 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:08 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece92b353df31cd62bcf548d31f7e7551ad5001927d632dc72fdb96777c0a7de`  
		Last Modified: Tue, 07 Apr 2026 01:21:59 GMT  
		Size: 152.4 MB (152404537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9003a62dd97b742a849a6ffe605b33afae135ecf9a6963fa71ce25145093e9`  
		Last Modified: Tue, 07 Apr 2026 01:21:54 GMT  
		Size: 22.2 MB (22220764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03444700904b3892922358de25fdfe826f0169360d9f9cb036eeac113f25554c`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73920399cab91d6ff0fc2201575339dc055750baca387d9ed10f94ed92d7adde`  
		Last Modified: Tue, 07 Apr 2026 01:22:11 GMT  
		Size: 593.7 MB (593665337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:bb0b5eca366271d9faabc5051de30bf0ca84556d8d2311a229f9e9cfd86ac081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff0ec4d07cfb43474a87b2b0c0dab7ef9b2b9b1f3f76a5dc23866ef5c9b9169`

```dockerfile
```

-	Layers:
	-	`sha256:18227a676aaf76c21c1183a42a01b9a116a151db0b59a0ea80879bdb63f1e15a`  
		Last Modified: Tue, 07 Apr 2026 01:21:53 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:598a0a7da604db5b7571614d65ef77c3d89c33455779d8a7ae9656cacc7e243c`  
		Last Modified: Tue, 07 Apr 2026 01:21:52 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f32d990dc8da74f7f0341a333164cb1c8d6266a8ac9ad4a945b90117efaffa0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **828.0 MB (827973880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb0549a54963f5295de9aca4174ea8cd5c882c87f277d02b84d560108488fee`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:13 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:13 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:13 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:15 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:17 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8b2b86a1f61fbc06035adfc6d633c1ef0ac985ee5d01ad2035aa975e75bc5e`  
		Last Modified: Tue, 07 Apr 2026 01:22:18 GMT  
		Size: 146.6 MB (146574461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a921e64342db75f8743327ae9f72db69b755625911158c2ba61f7e5cc3c653`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 24.5 MB (24528556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e04627812dc4bd20dfe4c8cdc15e97e22dc630d7688a5f6cf80d91b271266ee`  
		Last Modified: Tue, 07 Apr 2026 01:22:14 GMT  
		Size: 15.9 MB (15944580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccdd72aeb1f170c652f08f92801ce519133208478741fd634ac455a534dd7f21`  
		Last Modified: Tue, 07 Apr 2026 01:22:26 GMT  
		Size: 592.6 MB (592553021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:c5ee901f3e234f95818fd514b41636991e5c804c884191726bdfe9d398b131dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95bd9a7278c6d71557554c28d4ca253da3efb5f1beb63668ba7412cd386f0eac`

```dockerfile
```

-	Layers:
	-	`sha256:25ff4331c3bb33056dbba1acea83141c0be05c91a7822f564aa4ec8e37d10405`  
		Last Modified: Tue, 07 Apr 2026 01:22:13 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d0c3e47baeb7423641c403b8e392683ef8fc8fa4cf31429b25de36abf9eb3`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim`

```console
$ docker pull haskell@sha256:1f0099b81708e859d4d90f43d06187c8298c59d33ddf3bb01cff047131d0ab5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:ec468efccdfee2736254eced8aabda20caeb9a7413f8ba1a8d709c6e2657c264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776932258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2173d21f80bdb483477e015940670f09e33cb2d6136c82f12e7a62aeeae54191`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:01 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345dc3f621eb0094cd075ee66a2755b9c6d79d500a1a801483f92a7448eb3c94`  
		Last Modified: Tue, 07 Apr 2026 01:21:34 GMT  
		Size: 124.4 MB (124405560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47df7d2546cd081cd78569030f2b57711e56cd47e01f054fc6760b7a174ee51`  
		Last Modified: Tue, 07 Apr 2026 01:21:30 GMT  
		Size: 22.2 MB (22220780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bfa68860956218eb86763ac5169ed8198b6bbea47ea40ac15d1ebf0b9b0dff`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 8.4 MB (8403514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c93da93eff076094eefe1d30ebfb37597e0e6b28f746f73abfb52d017cd8a1`  
		Last Modified: Tue, 07 Apr 2026 01:21:45 GMT  
		Size: 593.7 MB (593666072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim` - unknown; unknown

```console
$ docker pull haskell@sha256:f87ce515084b12c2b03afd14820dd24f68118fde8c3c6b8c1e403e1670e9c0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2783973dbc0d33a45942d152c97cdbdbbdd8bbf862118d42f67fea5aa0a1096`

```dockerfile
```

-	Layers:
	-	`sha256:c092357d6ac3da8e3a1826c5b11f41a26405d393fb292b5377971dc7b98e212e`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b95e9b4e1b098e6f3ec57d2b3c6af99d1a8df7b9f3209ff4af0e56079b2e641`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e1c5961de02a9617ad4548c1d388ed811218c2a6fb7d508aba60c74938d44586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779715156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b95888e8c56f17ea52f9af5f94f933872ac70f7e1de2186cd09a803989641dd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:28 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c64a7715b20f0ce9a276abdfad0e377d8a74adaf5d2859c0980c91ae630b4d`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 118.6 MB (118575900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bdb68ff57f6ba1cfef40b68fc13d52d983fea4a32dbb5ba9d9c8e1eead4472`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 24.5 MB (24528540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f297d7be8e2a3dc35e44249b90135de569e0e0a316932ef497d5c7355ee9cc79`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7eff1bbecd608dd9e4f7f8fc78d2ee29abe5147929e545743f63887773827b`  
		Last Modified: Tue, 07 Apr 2026 01:22:20 GMT  
		Size: 592.5 MB (592549959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim` - unknown; unknown

```console
$ docker pull haskell@sha256:eedf5e08050e7b2b8156174a16878ba821e89ebcf36488a51d3bb981826922b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b836150ae1014e800aeb95401947eab6991470d3caa7e9540a9d17cc5761cd`

```dockerfile
```

-	Layers:
	-	`sha256:75326fdd5b5969006aae8e4354aac08e43a519226e95f4d2e114b656adf6c324`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7dc2a8ec36e9abaed5a00678037a830387b363f5f95362203a23446031a46d`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim-bookworm`

```console
$ docker pull haskell@sha256:1f0099b81708e859d4d90f43d06187c8298c59d33ddf3bb01cff047131d0ab5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:ec468efccdfee2736254eced8aabda20caeb9a7413f8ba1a8d709c6e2657c264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776932258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2173d21f80bdb483477e015940670f09e33cb2d6136c82f12e7a62aeeae54191`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:18:01 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:18:04 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:18:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:18:05 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345dc3f621eb0094cd075ee66a2755b9c6d79d500a1a801483f92a7448eb3c94`  
		Last Modified: Tue, 07 Apr 2026 01:21:34 GMT  
		Size: 124.4 MB (124405560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47df7d2546cd081cd78569030f2b57711e56cd47e01f054fc6760b7a174ee51`  
		Last Modified: Tue, 07 Apr 2026 01:21:30 GMT  
		Size: 22.2 MB (22220780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bfa68860956218eb86763ac5169ed8198b6bbea47ea40ac15d1ebf0b9b0dff`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 8.4 MB (8403514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c93da93eff076094eefe1d30ebfb37597e0e6b28f746f73abfb52d017cd8a1`  
		Last Modified: Tue, 07 Apr 2026 01:21:45 GMT  
		Size: 593.7 MB (593666072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:f87ce515084b12c2b03afd14820dd24f68118fde8c3c6b8c1e403e1670e9c0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2783973dbc0d33a45942d152c97cdbdbbdd8bbf862118d42f67fea5aa0a1096`

```dockerfile
```

-	Layers:
	-	`sha256:c092357d6ac3da8e3a1826c5b11f41a26405d393fb292b5377971dc7b98e212e`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b95e9b4e1b098e6f3ec57d2b3c6af99d1a8df7b9f3209ff4af0e56079b2e641`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e1c5961de02a9617ad4548c1d388ed811218c2a6fb7d508aba60c74938d44586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779715156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b95888e8c56f17ea52f9af5f94f933872ac70f7e1de2186cd09a803989641dd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:17:28 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:28 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:28 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:17:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 07 Apr 2026 01:17:31 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 07 Apr 2026 01:17:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC=9.14.1
# Tue, 07 Apr 2026 01:17:32 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c64a7715b20f0ce9a276abdfad0e377d8a74adaf5d2859c0980c91ae630b4d`  
		Last Modified: Tue, 07 Apr 2026 01:22:12 GMT  
		Size: 118.6 MB (118575900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bdb68ff57f6ba1cfef40b68fc13d52d983fea4a32dbb5ba9d9c8e1eead4472`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 24.5 MB (24528540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f297d7be8e2a3dc35e44249b90135de569e0e0a316932ef497d5c7355ee9cc79`  
		Last Modified: Tue, 07 Apr 2026 01:22:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7eff1bbecd608dd9e4f7f8fc78d2ee29abe5147929e545743f63887773827b`  
		Last Modified: Tue, 07 Apr 2026 01:22:20 GMT  
		Size: 592.5 MB (592549959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:eedf5e08050e7b2b8156174a16878ba821e89ebcf36488a51d3bb981826922b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51b836150ae1014e800aeb95401947eab6991470d3caa7e9540a9d17cc5761cd`

```dockerfile
```

-	Layers:
	-	`sha256:75326fdd5b5969006aae8e4354aac08e43a519226e95f4d2e114b656adf6c324`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d7dc2a8ec36e9abaed5a00678037a830387b363f5f95362203a23446031a46d`  
		Last Modified: Tue, 07 Apr 2026 01:22:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim-bullseye`

```console
$ docker pull haskell@sha256:a308580ef820964e7ca93fd565372fefa7347349c9a5af98b467c1762663a850
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:861a6492cf7f9e816ef6e5d3571040aada4494200bbdc1ac68d2de6b2ccef2b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608295417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab699b6bc5a2039c3aef4f4fc0e0e280be0d8fd661a762f96fed65441f94568c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:18:33 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:18:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:18:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:36 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:20:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:20:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:20:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:60fb1d5aba60afdf7cbf00cf9bd0c125e0c9c2ef7f454a7a88b456dd51794fab`  
		Last Modified: Tue, 07 Apr 2026 00:11:21 GMT  
		Size: 30.3 MB (30258019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a673ceb44a304ec95d9ec3a4552a15b6ec332792b6e9e7dacbe456dd47639f74`  
		Last Modified: Tue, 07 Apr 2026 01:21:22 GMT  
		Size: 106.4 MB (106394062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406a8d52e21b244390398e286d5690db277efdc4135cad90bf063d8d750bdc45`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 22.2 MB (22220781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e7e5bcfd82c195252a5e0a8d2dede7323108d6d95606693e64cffea03ea6d`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25536413a5ea7ad0ef10a0fccbafe0c896c0798cc3888db717ce1422e7b7d564`  
		Last Modified: Tue, 07 Apr 2026 01:21:29 GMT  
		Size: 441.8 MB (441810322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:cc0137181d099ca6be11886c914f40a5fc12b5585e2a23bd5e992f7f630291c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6785093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e640fefb81716b0a37ad00b3d98e211e99c6b509d0dd66b2c0a880d7d451da3b`

```dockerfile
```

-	Layers:
	-	`sha256:96936ea297d348d566f764dad257e5bb36d2046c34109b1cb0affeb1fbfccaba`  
		Last Modified: Tue, 07 Apr 2026 01:21:18 GMT  
		Size: 6.8 MB (6759349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234687df9ebda4f854bd9853b61cfbefbc9c066cf396d384141776c77d252f4d`  
		Last Modified: Tue, 07 Apr 2026 01:21:17 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d6e497909b113cb2cb3926ac6038eb43877f2dace0c6912deb394d9b3ead7472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618571434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca193d12285da7f428eea19dbb6befe80dffc9f4d445d659a0c2d9e041148d45`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Tue, 07 Apr 2026 01:17:57 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:17:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK=3.3.1
# Tue, 07 Apr 2026 01:17:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 07 Apr 2026 01:18:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 07 Apr 2026 01:18:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 07 Apr 2026 01:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC=9.10.3
# Tue, 07 Apr 2026 01:18:02 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 07 Apr 2026 01:19:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 07 Apr 2026 01:19:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:19:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:44aeebb720693ad47eb3913009383fd4ae7e8c24a3e1abb1683ccdac7f879495`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.7 MB (28744688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3dc8eabee012b38c5d28f05e1e09419c198bbfa415a29299372a02971b20b9`  
		Last Modified: Tue, 07 Apr 2026 01:21:00 GMT  
		Size: 101.9 MB (101873470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e1600eaed1b321e505e24dbe932cf6d88b8c884784eef86fc53e03ec65e131`  
		Last Modified: Tue, 07 Apr 2026 01:20:57 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3c1e1c1c0cb2d50b0ae3a91d5451717df8853eb61badd28cc1432f29707b0e`  
		Last Modified: Tue, 07 Apr 2026 01:20:48 GMT  
		Size: 14.0 MB (13972963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b5b77b94f9b23f14c32c41fe6f786349c2b25fb8db77bd35e87f7e8ca07246`  
		Last Modified: Tue, 07 Apr 2026 01:21:06 GMT  
		Size: 449.5 MB (449451761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:98029243c8be669546cc17cde279d431cc52a9bb23fff9d86bee26013598ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2878c3561ed3271d7ff0fb48abb223404d640cdeae180a2d3c12817642eab5e3`

```dockerfile
```

-	Layers:
	-	`sha256:d87037d3a1fb8b3e4550bb0a00dc329407aa2c01c3c4d091dae0119ec0975ab6`  
		Last Modified: Tue, 07 Apr 2026 01:20:56 GMT  
		Size: 6.8 MB (6761859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df60e783acac74289b8eacab3af23d267ac28d89c798b1b4f61dae265d88f497`  
		Last Modified: Tue, 07 Apr 2026 01:20:56 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json
