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
