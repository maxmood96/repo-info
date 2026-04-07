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
