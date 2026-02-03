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
$ docker pull haskell@sha256:8e045c47c827e23a327facff2522cbdced501bfffc6a094790ea3acee5f80271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:f299e044461def92978fc02e1e09552447341fc5c94ea3fde855356920ce098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825154630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63dd23015457b14a600b2dbe468a91166b8b706e868ab525cd551f1e6752392`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08794db77b402d64775f4e981b74315507b6698f4e772bacb62fdc7b5735b9`  
		Last Modified: Tue, 03 Feb 2026 02:20:56 GMT  
		Size: 152.4 MB (152378556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b299d79199c316ba1c329518d60279d166e472b155f0c55f2a42d63bb555ff6`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 22.2 MB (22220734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf9f8fc6d29b3d4e84084da560dd2ce71e871ccddc8c93c22ff66bf7e77dee`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbba24a3271904d1646e97c601cdd0e42bb50d0b10c10c9b00ab7e261d98aa9`  
		Last Modified: Tue, 03 Feb 2026 02:21:04 GMT  
		Size: 593.7 MB (593670352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9` - unknown; unknown

```console
$ docker pull haskell@sha256:b65ceb02ebede4bb61233c4b3228185b02f49b4c1cc6b2567df8edb48897c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e72c5a7ed2a057767454c8042905556f8493bdeedad4ec5bfa2dc52a5be25`

```dockerfile
```

-	Layers:
	-	`sha256:3a41aa03b940ddcb25fbd9428922b0f9b80e650d1d1cead15187736cba9433c6`  
		Last Modified: Tue, 03 Feb 2026 02:20:51 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60457317faadd06cb6ad537a6c0fb420942fbce0fcc24a3abaf5ad72e07f835`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3647e354c660ae20c53edfcbfb91f43c4d9d3f2b34e786cf1c51e9d6c04192ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.9 MB (827938406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab6dc3d055aef05cb68b4a5a96286c18de7d4623962bf4f310e617e9cf6279`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:21:35 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:21:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:21:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:21:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:23:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:23:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:23:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ae27c4297057722c43286a8294938ff609b4d211656df39e2178c8277df13`  
		Last Modified: Thu, 29 Jan 2026 20:25:24 GMT  
		Size: 146.5 MB (146547971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0bc56010070d4e8fd82ec69ac9be3c9a3ba21af3a73437fa720285f651edf9`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc9ecd04267369e82fde7fe99460dc9d508021a337f569b1d96fb58aea97940`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a7bfdf951d98afe3fbbbfd846edc57c7dbfb14ff061e20cedcbd12808fd44`  
		Last Modified: Thu, 29 Jan 2026 20:25:35 GMT  
		Size: 592.6 MB (592551222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9` - unknown; unknown

```console
$ docker pull haskell@sha256:28996c9136802910cbfa3de6faaa5f9df4c033a64d313bd21b8e2cc1c6f5ac09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30fbc1a52bca5749a1beddc1d1fd5e8218cf4834d4bfdf119591d410ae7d516`

```dockerfile
```

-	Layers:
	-	`sha256:8f8f009cad10ee83982e723ea3e97386d783620402ef46fa4847511228f91da9`  
		Last Modified: Thu, 29 Jan 2026 20:25:17 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0d371f55e52b36c5159955ffb3ceb5b15c9f552ed0fc7ed5ea5fb0930fd50f`  
		Last Modified: Thu, 29 Jan 2026 20:25:16 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-bookworm`

```console
$ docker pull haskell@sha256:8e045c47c827e23a327facff2522cbdced501bfffc6a094790ea3acee5f80271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:f299e044461def92978fc02e1e09552447341fc5c94ea3fde855356920ce098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825154630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63dd23015457b14a600b2dbe468a91166b8b706e868ab525cd551f1e6752392`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08794db77b402d64775f4e981b74315507b6698f4e772bacb62fdc7b5735b9`  
		Last Modified: Tue, 03 Feb 2026 02:20:56 GMT  
		Size: 152.4 MB (152378556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b299d79199c316ba1c329518d60279d166e472b155f0c55f2a42d63bb555ff6`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 22.2 MB (22220734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf9f8fc6d29b3d4e84084da560dd2ce71e871ccddc8c93c22ff66bf7e77dee`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbba24a3271904d1646e97c601cdd0e42bb50d0b10c10c9b00ab7e261d98aa9`  
		Last Modified: Tue, 03 Feb 2026 02:21:04 GMT  
		Size: 593.7 MB (593670352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:b65ceb02ebede4bb61233c4b3228185b02f49b4c1cc6b2567df8edb48897c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e72c5a7ed2a057767454c8042905556f8493bdeedad4ec5bfa2dc52a5be25`

```dockerfile
```

-	Layers:
	-	`sha256:3a41aa03b940ddcb25fbd9428922b0f9b80e650d1d1cead15187736cba9433c6`  
		Last Modified: Tue, 03 Feb 2026 02:20:51 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60457317faadd06cb6ad537a6c0fb420942fbce0fcc24a3abaf5ad72e07f835`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3647e354c660ae20c53edfcbfb91f43c4d9d3f2b34e786cf1c51e9d6c04192ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.9 MB (827938406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab6dc3d055aef05cb68b4a5a96286c18de7d4623962bf4f310e617e9cf6279`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:21:35 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:21:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:21:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:21:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:23:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:23:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:23:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ae27c4297057722c43286a8294938ff609b4d211656df39e2178c8277df13`  
		Last Modified: Thu, 29 Jan 2026 20:25:24 GMT  
		Size: 146.5 MB (146547971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0bc56010070d4e8fd82ec69ac9be3c9a3ba21af3a73437fa720285f651edf9`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc9ecd04267369e82fde7fe99460dc9d508021a337f569b1d96fb58aea97940`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a7bfdf951d98afe3fbbbfd846edc57c7dbfb14ff061e20cedcbd12808fd44`  
		Last Modified: Thu, 29 Jan 2026 20:25:35 GMT  
		Size: 592.6 MB (592551222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:28996c9136802910cbfa3de6faaa5f9df4c033a64d313bd21b8e2cc1c6f5ac09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30fbc1a52bca5749a1beddc1d1fd5e8218cf4834d4bfdf119591d410ae7d516`

```dockerfile
```

-	Layers:
	-	`sha256:8f8f009cad10ee83982e723ea3e97386d783620402ef46fa4847511228f91da9`  
		Last Modified: Thu, 29 Jan 2026 20:25:17 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0d371f55e52b36c5159955ffb3ceb5b15c9f552ed0fc7ed5ea5fb0930fd50f`  
		Last Modified: Thu, 29 Jan 2026 20:25:16 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-bullseye`

```console
$ docker pull haskell@sha256:121d7cc72202a98998536934817f66ec8dc2ddd73ed4c432cba16b5256efae08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:6d62c2c22558a9f4be9082d56ccc48718e81169760aa4499b9bea2bac24c2d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659144428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d89ab7703666e67c3606548f21bfb723bdad64966357caadae7ee1d74eddd3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75238d6ce97658590d0e7ca1aaf30fcba7bcb5c26bbd70cd884882a7979de149`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 133.8 MB (133753898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e15615986ee567d17dab5c314e85877d951095edac5c31e416f1681e2ab9e3`  
		Last Modified: Tue, 03 Feb 2026 02:20:38 GMT  
		Size: 22.2 MB (22220752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c76124521720024b593e6b7c5f34bb17689543c866b3a3c5ef960357ac11da`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 441.8 MB (441801274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:53d5b173bff7b231b60abbb2b322a9eb1325f442ef0a5b9467745353f1e151e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ef0c54bf6ad45c85aca74ad4802897d276198be4a7175cf1170062d7b556f0`

```dockerfile
```

-	Layers:
	-	`sha256:4b2fbe4f1a16763366e46ddbe8e41491b1d25e11b2f630c0ea068449342c0b4d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff45e85ac1e2cbaa45d82b33c17bdd2a40f1c919de0910d6f11911b02deb40`  
		Last Modified: Tue, 03 Feb 2026 02:20:36 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e7d2bb12473e8ca564817405f80a72f9a6a6f998c64e1e9b30a7c4bd213773af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669449125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9493023ab675c91b402548eab4fe024cc03aced2e301621b79d999597cda7e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904396a1ed19b72c34ac049fddb833b77d8ff29212b034f306b89170224c3e79`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 129.2 MB (129241147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6443d9a1a7bef1d3bb5e84daf420ce96bfa38211f22d03407b6f9b40283f5360`  
		Last Modified: Tue, 13 Jan 2026 01:21:23 GMT  
		Size: 24.5 MB (24528541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb39a72843976163048a101d67acc696b91e09c912f82db26b3cb2793d23db6`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6530d9b1cee1556dc890910c703727045b89398292afa180324e9634fae5f8f`  
		Last Modified: Tue, 13 Jan 2026 01:21:32 GMT  
		Size: 449.4 MB (449448708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:ff116e5d6ea811b71d7978c9385d3e9284b88978d48c6e0d98be9d714b8bd3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8ee2f44400a71e0a3a8bc51250a3388920d22ef10e42f8b0f3947eff178c0b`

```dockerfile
```

-	Layers:
	-	`sha256:38ba952907a41a1a43d318514c3c500b5a565d28343b20908c7958204b833496`  
		Last Modified: Tue, 13 Jan 2026 01:21:22 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba83d152e0054fc4751a8f2ae28ec41dfa93bdfa35769379f2d00f0c6725866`  
		Last Modified: Tue, 13 Jan 2026 01:21:21 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:421d5abd82604d78c08e4438bfb81df19816c79c08abd7ba6e74e7018df11c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:110d4a2d1efeeddb62ae38b915474444040487c6a4b644a37597bacb652f6460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776930005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e17615141dab7f099ff2b4faa0260fda01bdebca0a3a049d99937148a1eb06`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fe43daec195aa75262a2e86f9dc0ba4805f1705d8cd95c334dfd178dc9f11`  
		Last Modified: Tue, 03 Feb 2026 02:21:11 GMT  
		Size: 124.4 MB (124406060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e90ee734b1d3e56d7e2c6c778dda05a971c7333a05589fd21b9acd055603e`  
		Last Modified: Tue, 03 Feb 2026 02:21:08 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c41bcf39676cc775bbe10c12641791e3c3663f6a9bf7d661910276e362c26a2`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba2b992b4373bf7d394ffc39402a056b50fcc2fe9128c8856debcd41019dc5`  
		Last Modified: Tue, 03 Feb 2026 02:21:20 GMT  
		Size: 593.7 MB (593671184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:65b9a880c769cf5ce7cf9d1784ebd941644fff1242af9e2ece0a74c1fd5227c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef83333c9d00ac92e175ccb2585258325e7d4da865be37a85b8ca928cde3ac47`

```dockerfile
```

-	Layers:
	-	`sha256:88cb24a779b9ff5b1a8c0db293620ff74fec7cc2142f09dd8360962ecdc27e6b`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd146a8e20014ebf818d4bfb1265a4d978f26ba9a61f8c9ec2e8bd4c1511f61c`  
		Last Modified: Tue, 03 Feb 2026 02:21:06 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3a36953ac7ac34d4f2c7498322c3266d227776b5a1374aaef40ef1dbb95a17e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779705710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d69fc402d5193d22afabc71d151a6dbee4eca69e5d5e0466c257538101922cf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:22:31 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:22:31 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:22:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:22:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:24:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:24:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:24:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4f4ed0fd2c28ce4be76881e223763ccd903d7068141aa943944e73ca61468a`  
		Last Modified: Thu, 29 Jan 2026 20:26:12 GMT  
		Size: 118.6 MB (118575484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc78c2319953580a1d9cb773453a236d84f48dec9454c1b1534ef532fe1effd`  
		Last Modified: Thu, 29 Jan 2026 20:26:09 GMT  
		Size: 24.5 MB (24528567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc147b79cfae7eb4a1b9bdde1478144c933c31fd6f6402300042448a3640ac55`  
		Last Modified: Thu, 29 Jan 2026 20:26:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d318096c027eaa2441061e88514b6b1d35edece3563f243ee9d20f2938d35c5b`  
		Last Modified: Thu, 29 Jan 2026 20:26:20 GMT  
		Size: 592.5 MB (592549179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:7aba8a6d02bbaad684351341c59715c03e30704c97b1699ecdaf17ef77701320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e874e120e22a3c1bd835535e506ad86b8efcd95a6e43b5e756976a218455f01f`

```dockerfile
```

-	Layers:
	-	`sha256:6b1e3e7fb716a9221df7a76d1eac6ca105121dd69f7decb039b19b8318ae9d43`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e3e173986e5627199e41d6685f1ff63e51f059ddb7b6dcd86c0412d9598faf`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim-bookworm`

```console
$ docker pull haskell@sha256:421d5abd82604d78c08e4438bfb81df19816c79c08abd7ba6e74e7018df11c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:110d4a2d1efeeddb62ae38b915474444040487c6a4b644a37597bacb652f6460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776930005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e17615141dab7f099ff2b4faa0260fda01bdebca0a3a049d99937148a1eb06`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fe43daec195aa75262a2e86f9dc0ba4805f1705d8cd95c334dfd178dc9f11`  
		Last Modified: Tue, 03 Feb 2026 02:21:11 GMT  
		Size: 124.4 MB (124406060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e90ee734b1d3e56d7e2c6c778dda05a971c7333a05589fd21b9acd055603e`  
		Last Modified: Tue, 03 Feb 2026 02:21:08 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c41bcf39676cc775bbe10c12641791e3c3663f6a9bf7d661910276e362c26a2`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba2b992b4373bf7d394ffc39402a056b50fcc2fe9128c8856debcd41019dc5`  
		Last Modified: Tue, 03 Feb 2026 02:21:20 GMT  
		Size: 593.7 MB (593671184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:65b9a880c769cf5ce7cf9d1784ebd941644fff1242af9e2ece0a74c1fd5227c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef83333c9d00ac92e175ccb2585258325e7d4da865be37a85b8ca928cde3ac47`

```dockerfile
```

-	Layers:
	-	`sha256:88cb24a779b9ff5b1a8c0db293620ff74fec7cc2142f09dd8360962ecdc27e6b`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd146a8e20014ebf818d4bfb1265a4d978f26ba9a61f8c9ec2e8bd4c1511f61c`  
		Last Modified: Tue, 03 Feb 2026 02:21:06 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3a36953ac7ac34d4f2c7498322c3266d227776b5a1374aaef40ef1dbb95a17e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779705710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d69fc402d5193d22afabc71d151a6dbee4eca69e5d5e0466c257538101922cf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:22:31 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:22:31 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:22:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:22:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:24:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:24:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:24:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4f4ed0fd2c28ce4be76881e223763ccd903d7068141aa943944e73ca61468a`  
		Last Modified: Thu, 29 Jan 2026 20:26:12 GMT  
		Size: 118.6 MB (118575484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc78c2319953580a1d9cb773453a236d84f48dec9454c1b1534ef532fe1effd`  
		Last Modified: Thu, 29 Jan 2026 20:26:09 GMT  
		Size: 24.5 MB (24528567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc147b79cfae7eb4a1b9bdde1478144c933c31fd6f6402300042448a3640ac55`  
		Last Modified: Thu, 29 Jan 2026 20:26:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d318096c027eaa2441061e88514b6b1d35edece3563f243ee9d20f2938d35c5b`  
		Last Modified: Thu, 29 Jan 2026 20:26:20 GMT  
		Size: 592.5 MB (592549179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:7aba8a6d02bbaad684351341c59715c03e30704c97b1699ecdaf17ef77701320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e874e120e22a3c1bd835535e506ad86b8efcd95a6e43b5e756976a218455f01f`

```dockerfile
```

-	Layers:
	-	`sha256:6b1e3e7fb716a9221df7a76d1eac6ca105121dd69f7decb039b19b8318ae9d43`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e3e173986e5627199e41d6685f1ff63e51f059ddb7b6dcd86c0412d9598faf`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim-bullseye`

```console
$ docker pull haskell@sha256:5fa6651a439e5aac88472c8a0599e184f05678e4330d98bde9ebd1f50987cc0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:592e51cede7db0b4910f951a43961024661c7a8b55f47acd4bf2efe91bd88852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608259149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f9101bb8a800a45e5d6f78526a9623f8c5157af03c8e8f7d41aea34288d3f1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3c918a9dbef90c820e3b8f89e3eb745c6b8206768d5dc801bad637f07de68e`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 106.4 MB (106366909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d52fe0f0d6d3c84e13aa5a5843a10b3a0bb4cfc47cacc90ce709f6df933977f`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02604587704ad580a78c07fd1af9da93ffe6e276cd976c310847887f0742710c`  
		Last Modified: Tue, 03 Feb 2026 02:21:00 GMT  
		Size: 441.8 MB (441800960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b71502010e6068c6d40b4b8a361b29059ba4a86dc02be5e86ecd71dfb557e152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999c96a2c5eb622c8c95795883265b90267932ff8488e9032d04781b644c86e7`

```dockerfile
```

-	Layers:
	-	`sha256:0d8b88f8077a1d894aab234933ffdcb791f8e0730003ef65ae1f41d2ddfe73ce`  
		Last Modified: Tue, 03 Feb 2026 02:20:49 GMT  
		Size: 6.8 MB (6750929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0054b7fb8b6ae305be385f6ab8726d5c07a6db46e848a0ce3e842b853006ba8e`  
		Last Modified: Tue, 03 Feb 2026 02:20:49 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f56b48eefc38564ec24bd6c46efcf5e42428b594bb064d3c56a143f02b480b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618563538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fef4d36395c024b1be79dc5189fc28cf16c2f14cb1aebd8daedf43437783f7`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:23 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:23 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:23 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:25 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:25 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:25 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:27 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:27 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:27 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:19:59 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:19:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:59 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a96c3c611e1717d66afae67d6fb8eba49eb7f9ac36228fcd7b6136699549fe`  
		Last Modified: Tue, 13 Jan 2026 01:21:20 GMT  
		Size: 101.9 MB (101863954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c652f3f14d418494191692b21fa54656e5b70879faead69be341a17cd6f2841`  
		Last Modified: Tue, 13 Jan 2026 01:21:16 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3879388bec87dd8f22e12521634d07e8ae09151739d3e7636cb0c34e2d0b4a70`  
		Last Modified: Tue, 13 Jan 2026 01:21:16 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4896f989cd82087a24fcc86dea60eec6c0dd1307426e36fabe717b12939a8d9`  
		Last Modified: Tue, 13 Jan 2026 01:21:26 GMT  
		Size: 449.4 MB (449449555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:040eadb249af5b8b1cf61e5cc13d4e0cbb95dac5da5b1af59e931e53f57cfc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28288cabdcabf2ef88791f546297fa382f032786da32f5ae7c834b484595bd40`

```dockerfile
```

-	Layers:
	-	`sha256:e20461454727c7d76eb386d0ada378ce79198d146fe58555bba010ac323a4c51`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 6.8 MB (6753439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b260842ec1bfdc58222371116a8ccbbd05a84123643c55bbded00788700a5222`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10`

```console
$ docker pull haskell@sha256:121d7cc72202a98998536934817f66ec8dc2ddd73ed4c432cba16b5256efae08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10` - linux; amd64

```console
$ docker pull haskell@sha256:6d62c2c22558a9f4be9082d56ccc48718e81169760aa4499b9bea2bac24c2d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659144428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d89ab7703666e67c3606548f21bfb723bdad64966357caadae7ee1d74eddd3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75238d6ce97658590d0e7ca1aaf30fcba7bcb5c26bbd70cd884882a7979de149`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 133.8 MB (133753898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e15615986ee567d17dab5c314e85877d951095edac5c31e416f1681e2ab9e3`  
		Last Modified: Tue, 03 Feb 2026 02:20:38 GMT  
		Size: 22.2 MB (22220752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c76124521720024b593e6b7c5f34bb17689543c866b3a3c5ef960357ac11da`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 441.8 MB (441801274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10` - unknown; unknown

```console
$ docker pull haskell@sha256:53d5b173bff7b231b60abbb2b322a9eb1325f442ef0a5b9467745353f1e151e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ef0c54bf6ad45c85aca74ad4802897d276198be4a7175cf1170062d7b556f0`

```dockerfile
```

-	Layers:
	-	`sha256:4b2fbe4f1a16763366e46ddbe8e41491b1d25e11b2f630c0ea068449342c0b4d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff45e85ac1e2cbaa45d82b33c17bdd2a40f1c919de0910d6f11911b02deb40`  
		Last Modified: Tue, 03 Feb 2026 02:20:36 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e7d2bb12473e8ca564817405f80a72f9a6a6f998c64e1e9b30a7c4bd213773af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669449125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9493023ab675c91b402548eab4fe024cc03aced2e301621b79d999597cda7e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904396a1ed19b72c34ac049fddb833b77d8ff29212b034f306b89170224c3e79`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 129.2 MB (129241147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6443d9a1a7bef1d3bb5e84daf420ce96bfa38211f22d03407b6f9b40283f5360`  
		Last Modified: Tue, 13 Jan 2026 01:21:23 GMT  
		Size: 24.5 MB (24528541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb39a72843976163048a101d67acc696b91e09c912f82db26b3cb2793d23db6`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6530d9b1cee1556dc890910c703727045b89398292afa180324e9634fae5f8f`  
		Last Modified: Tue, 13 Jan 2026 01:21:32 GMT  
		Size: 449.4 MB (449448708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10` - unknown; unknown

```console
$ docker pull haskell@sha256:ff116e5d6ea811b71d7978c9385d3e9284b88978d48c6e0d98be9d714b8bd3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8ee2f44400a71e0a3a8bc51250a3388920d22ef10e42f8b0f3947eff178c0b`

```dockerfile
```

-	Layers:
	-	`sha256:38ba952907a41a1a43d318514c3c500b5a565d28343b20908c7958204b833496`  
		Last Modified: Tue, 13 Jan 2026 01:21:22 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba83d152e0054fc4751a8f2ae28ec41dfa93bdfa35769379f2d00f0c6725866`  
		Last Modified: Tue, 13 Jan 2026 01:21:21 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-bookworm`

```console
$ docker pull haskell@sha256:c9334d1485216511e34a92888287c417a6038a9644b16af9e9fbd09b61a5d0e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:b3338c5c390f6dba72e2ddc72d95157da32d63348ccc85d2b648d1cb5349de19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672809110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8187d6524f8e02e47bb178bf8e61b0d64b1746d18be55dcc7e0c3d83375ff5`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:39 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:39 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:42 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:43 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:24 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:24 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:24 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033886e9b41283b91ad60daad2760bf2c15b8c7e230246c0895a3014e5cf50f4`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 152.4 MB (152378198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6056091128945e6de4e5781fec667f1bb690376225c4d9a155c3575d9293559b`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 22.2 MB (22220758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae1b4e89983d825bd60f229ad69e61a352ec70410347952f188b3e3ff51ff8b`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 7.6 MB (7607048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6553e22f10a6858a49b294a420f07be7f5a7600e1d25c5a6f91d0bdad8449b9`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 442.1 MB (442121623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:468099c2aeb9b5d9c2a558348b75d2470fd9294818dc3b5a5996fb08cc9a8015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9504459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc544225446d659728f955de970b8013b436835ab1fc76d6a4da51bcef59c23`

```dockerfile
```

-	Layers:
	-	`sha256:38047cd03d97c3847f9bdf72e30be07e0216f4aacd970595f090af7477401cb9`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 9.5 MB (9479105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dec10ff78e00b018edd7557a494b4ad0e051991a6ed265447ae657dc7557300`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 25.4 KB (25354 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8c2e787617c798cb205c1e9721902b8b25db6e4de0b0d03f34764fbe9bf73ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.9 MB (682860205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30542466556ea720f4335e70af338860f156c2658a21e2b87bc8c98ae4d12154`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:47 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:16:47 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:16:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:16:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:16:49 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:16:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:16:51 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:16:51 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:16:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:18:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:18:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:18:26 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfabc667501f67409fc390477d2bd28f31024026819883c36f0edd70be1fc11f`  
		Last Modified: Tue, 13 Jan 2026 01:19:53 GMT  
		Size: 146.5 MB (146548867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ad960213d31a39bb28b0d6199412ba0e26ca5b7c9d9134dae34601fbb66b21`  
		Last Modified: Tue, 13 Jan 2026 01:19:49 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58eb92b1a20d057eef39e4ebab79e2954a5cf1bd1a2e7149cc44a1f2874bc02f`  
		Last Modified: Tue, 13 Jan 2026 01:19:48 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4476482b7fee14df773e5308fbbda70ad059d08cad960e5b1212d94ff2fcf486`  
		Last Modified: Tue, 13 Jan 2026 01:20:00 GMT  
		Size: 449.4 MB (449447693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:8a7123bb4e8cf73e02e81b229e128b2e9c656b0694a20097c46f6e55d044b8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9532370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7b1305f73614e9a79bbdf30a33b2b97de22c9c3378a24d0669e61fd6ec94e`

```dockerfile
```

-	Layers:
	-	`sha256:0ceafa94fb6f7ccd5b767bde3dcd90943e2c80a1a1ecf629a86dba70863cc7fa`  
		Last Modified: Tue, 13 Jan 2026 01:19:48 GMT  
		Size: 9.5 MB (9506889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5adbd78d1e78af4cc4b78cb8670053486ae59545a177da7d779c369ce8c558`  
		Last Modified: Tue, 13 Jan 2026 01:19:47 GMT  
		Size: 25.5 KB (25481 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-bullseye`

```console
$ docker pull haskell@sha256:121d7cc72202a98998536934817f66ec8dc2ddd73ed4c432cba16b5256efae08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:6d62c2c22558a9f4be9082d56ccc48718e81169760aa4499b9bea2bac24c2d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659144428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d89ab7703666e67c3606548f21bfb723bdad64966357caadae7ee1d74eddd3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75238d6ce97658590d0e7ca1aaf30fcba7bcb5c26bbd70cd884882a7979de149`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 133.8 MB (133753898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e15615986ee567d17dab5c314e85877d951095edac5c31e416f1681e2ab9e3`  
		Last Modified: Tue, 03 Feb 2026 02:20:38 GMT  
		Size: 22.2 MB (22220752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c76124521720024b593e6b7c5f34bb17689543c866b3a3c5ef960357ac11da`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 441.8 MB (441801274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:53d5b173bff7b231b60abbb2b322a9eb1325f442ef0a5b9467745353f1e151e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ef0c54bf6ad45c85aca74ad4802897d276198be4a7175cf1170062d7b556f0`

```dockerfile
```

-	Layers:
	-	`sha256:4b2fbe4f1a16763366e46ddbe8e41491b1d25e11b2f630c0ea068449342c0b4d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff45e85ac1e2cbaa45d82b33c17bdd2a40f1c919de0910d6f11911b02deb40`  
		Last Modified: Tue, 03 Feb 2026 02:20:36 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e7d2bb12473e8ca564817405f80a72f9a6a6f998c64e1e9b30a7c4bd213773af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669449125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9493023ab675c91b402548eab4fe024cc03aced2e301621b79d999597cda7e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904396a1ed19b72c34ac049fddb833b77d8ff29212b034f306b89170224c3e79`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 129.2 MB (129241147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6443d9a1a7bef1d3bb5e84daf420ce96bfa38211f22d03407b6f9b40283f5360`  
		Last Modified: Tue, 13 Jan 2026 01:21:23 GMT  
		Size: 24.5 MB (24528541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb39a72843976163048a101d67acc696b91e09c912f82db26b3cb2793d23db6`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6530d9b1cee1556dc890910c703727045b89398292afa180324e9634fae5f8f`  
		Last Modified: Tue, 13 Jan 2026 01:21:32 GMT  
		Size: 449.4 MB (449448708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:ff116e5d6ea811b71d7978c9385d3e9284b88978d48c6e0d98be9d714b8bd3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8ee2f44400a71e0a3a8bc51250a3388920d22ef10e42f8b0f3947eff178c0b`

```dockerfile
```

-	Layers:
	-	`sha256:38ba952907a41a1a43d318514c3c500b5a565d28343b20908c7958204b833496`  
		Last Modified: Tue, 13 Jan 2026 01:21:22 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba83d152e0054fc4751a8f2ae28ec41dfa93bdfa35769379f2d00f0c6725866`  
		Last Modified: Tue, 13 Jan 2026 01:21:21 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-slim-bookworm`

```console
$ docker pull haskell@sha256:5cc917747a8fdd54026b43853ca5cc9dc7f86e2334a76a520eeec809cc655075
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:853445b5b6937a5f1da28871fce3d98d78c9fd57d00c6ee559f19d6514cd3a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.6 MB (624585251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b744210e3b457b10544f543f9cedc1f30cfdfec0ab73826d0566040ab02ecc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:44 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:44 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:47 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:26 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48467f4c780344366912304cbe7dfc704286fa599688ed182b7828514d0c842b`  
		Last Modified: Tue, 03 Feb 2026 02:20:45 GMT  
		Size: 124.4 MB (124406084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbb737c2fa60d764318ac70a7045768bb2ef3c87d61ee97c0b15aa9924957eb`  
		Last Modified: Tue, 03 Feb 2026 02:20:42 GMT  
		Size: 22.2 MB (22220767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d1e215f43d3048806c8c7e9a43b2f2f06f89aff36b3cb6a195af29df9ed8df`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 7.6 MB (7607051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7e997144fcd70902763aa48966ba3583c159b973f4be345d33a669f4b91be6`  
		Last Modified: Tue, 03 Feb 2026 02:20:51 GMT  
		Size: 442.1 MB (442122862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:912966bf0c16fede60e4b00325860fc6975a6dd35860952848fe633d516882e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6316d07d1c826b3370e2733326a1bc7f8b25b04b101940f2c78feee18f7539bc`

```dockerfile
```

-	Layers:
	-	`sha256:a443b336153f6415bf7a2b15660ee1ab89e09e464b8e85df8c7191ded14a9922`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 6.6 MB (6606033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7b431c0b751027f482b27788ac0e51143e079bc3395186c23dc70444c58d9a`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 25.4 KB (25397 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:688b184defc0e9215e9edde716f138309d067e349617792fab0c9be732173c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.6 MB (634627259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314d1d7391cc500139b7d675f410aa96f592765f6cc4f65e326c49614b4902da`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:18:15 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:15 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:15 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:17 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:18 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:19:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:19:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf965bd7e969d15740345bd03d410d0535bcc55e667282a068a7c51e14012fa5`  
		Last Modified: Tue, 13 Jan 2026 01:21:10 GMT  
		Size: 118.6 MB (118576286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82a90fa32b3bd92426bb71d0f3b6f21b7cdcfd21b1f506e577ba16693ba48b3`  
		Last Modified: Tue, 13 Jan 2026 01:21:07 GMT  
		Size: 24.5 MB (24528608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad496bfa46b59baa0e37af69a215d2dffd01fb61f27af40aa7cab953f9b8e22d`  
		Last Modified: Tue, 13 Jan 2026 01:21:06 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee2ecf16af813f0e8d8be830d30bd1f08ae71e80205eb195349fca33e1ddbd`  
		Last Modified: Tue, 13 Jan 2026 01:21:16 GMT  
		Size: 449.4 MB (449445453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:83c59fa01c961609f8314e684df31c3daadf1df4710a44d089a9c856f1d85854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f36b875c7051aea8ee13ed88a78606094c34e72f376724ddb6ebaa0020e13b`

```dockerfile
```

-	Layers:
	-	`sha256:c0d67e0736a9838e991b5e68ed7ab175558af34490ebdef7e5f0756e5067b7b8`  
		Last Modified: Tue, 13 Jan 2026 01:21:06 GMT  
		Size: 6.6 MB (6634444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bb376b555c4663840edf9973c351b8ebf62cf9ff15ff7cbf454babc86f00355`  
		Last Modified: Tue, 13 Jan 2026 01:21:05 GMT  
		Size: 25.5 KB (25524 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-slim-bullseye`

```console
$ docker pull haskell@sha256:5fa6651a439e5aac88472c8a0599e184f05678e4330d98bde9ebd1f50987cc0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:592e51cede7db0b4910f951a43961024661c7a8b55f47acd4bf2efe91bd88852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608259149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f9101bb8a800a45e5d6f78526a9623f8c5157af03c8e8f7d41aea34288d3f1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3c918a9dbef90c820e3b8f89e3eb745c6b8206768d5dc801bad637f07de68e`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 106.4 MB (106366909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d52fe0f0d6d3c84e13aa5a5843a10b3a0bb4cfc47cacc90ce709f6df933977f`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02604587704ad580a78c07fd1af9da93ffe6e276cd976c310847887f0742710c`  
		Last Modified: Tue, 03 Feb 2026 02:21:00 GMT  
		Size: 441.8 MB (441800960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b71502010e6068c6d40b4b8a361b29059ba4a86dc02be5e86ecd71dfb557e152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999c96a2c5eb622c8c95795883265b90267932ff8488e9032d04781b644c86e7`

```dockerfile
```

-	Layers:
	-	`sha256:0d8b88f8077a1d894aab234933ffdcb791f8e0730003ef65ae1f41d2ddfe73ce`  
		Last Modified: Tue, 03 Feb 2026 02:20:49 GMT  
		Size: 6.8 MB (6750929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0054b7fb8b6ae305be385f6ab8726d5c07a6db46e848a0ce3e842b853006ba8e`  
		Last Modified: Tue, 03 Feb 2026 02:20:49 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f56b48eefc38564ec24bd6c46efcf5e42428b594bb064d3c56a143f02b480b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618563538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fef4d36395c024b1be79dc5189fc28cf16c2f14cb1aebd8daedf43437783f7`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:23 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:23 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:23 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:25 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:25 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:25 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:27 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:27 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:27 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:19:59 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:19:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:59 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a96c3c611e1717d66afae67d6fb8eba49eb7f9ac36228fcd7b6136699549fe`  
		Last Modified: Tue, 13 Jan 2026 01:21:20 GMT  
		Size: 101.9 MB (101863954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c652f3f14d418494191692b21fa54656e5b70879faead69be341a17cd6f2841`  
		Last Modified: Tue, 13 Jan 2026 01:21:16 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3879388bec87dd8f22e12521634d07e8ae09151739d3e7636cb0c34e2d0b4a70`  
		Last Modified: Tue, 13 Jan 2026 01:21:16 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4896f989cd82087a24fcc86dea60eec6c0dd1307426e36fabe717b12939a8d9`  
		Last Modified: Tue, 13 Jan 2026 01:21:26 GMT  
		Size: 449.4 MB (449449555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:040eadb249af5b8b1cf61e5cc13d4e0cbb95dac5da5b1af59e931e53f57cfc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28288cabdcabf2ef88791f546297fa382f032786da32f5ae7c834b484595bd40`

```dockerfile
```

-	Layers:
	-	`sha256:e20461454727c7d76eb386d0ada378ce79198d146fe58555bba010ac323a4c51`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 6.8 MB (6753439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b260842ec1bfdc58222371116a8ccbbd05a84123643c55bbded00788700a5222`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3`

```console
$ docker pull haskell@sha256:121d7cc72202a98998536934817f66ec8dc2ddd73ed4c432cba16b5256efae08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3` - linux; amd64

```console
$ docker pull haskell@sha256:6d62c2c22558a9f4be9082d56ccc48718e81169760aa4499b9bea2bac24c2d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659144428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d89ab7703666e67c3606548f21bfb723bdad64966357caadae7ee1d74eddd3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75238d6ce97658590d0e7ca1aaf30fcba7bcb5c26bbd70cd884882a7979de149`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 133.8 MB (133753898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e15615986ee567d17dab5c314e85877d951095edac5c31e416f1681e2ab9e3`  
		Last Modified: Tue, 03 Feb 2026 02:20:38 GMT  
		Size: 22.2 MB (22220752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c76124521720024b593e6b7c5f34bb17689543c866b3a3c5ef960357ac11da`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 441.8 MB (441801274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3` - unknown; unknown

```console
$ docker pull haskell@sha256:53d5b173bff7b231b60abbb2b322a9eb1325f442ef0a5b9467745353f1e151e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ef0c54bf6ad45c85aca74ad4802897d276198be4a7175cf1170062d7b556f0`

```dockerfile
```

-	Layers:
	-	`sha256:4b2fbe4f1a16763366e46ddbe8e41491b1d25e11b2f630c0ea068449342c0b4d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff45e85ac1e2cbaa45d82b33c17bdd2a40f1c919de0910d6f11911b02deb40`  
		Last Modified: Tue, 03 Feb 2026 02:20:36 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e7d2bb12473e8ca564817405f80a72f9a6a6f998c64e1e9b30a7c4bd213773af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669449125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9493023ab675c91b402548eab4fe024cc03aced2e301621b79d999597cda7e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904396a1ed19b72c34ac049fddb833b77d8ff29212b034f306b89170224c3e79`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 129.2 MB (129241147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6443d9a1a7bef1d3bb5e84daf420ce96bfa38211f22d03407b6f9b40283f5360`  
		Last Modified: Tue, 13 Jan 2026 01:21:23 GMT  
		Size: 24.5 MB (24528541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb39a72843976163048a101d67acc696b91e09c912f82db26b3cb2793d23db6`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6530d9b1cee1556dc890910c703727045b89398292afa180324e9634fae5f8f`  
		Last Modified: Tue, 13 Jan 2026 01:21:32 GMT  
		Size: 449.4 MB (449448708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3` - unknown; unknown

```console
$ docker pull haskell@sha256:ff116e5d6ea811b71d7978c9385d3e9284b88978d48c6e0d98be9d714b8bd3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8ee2f44400a71e0a3a8bc51250a3388920d22ef10e42f8b0f3947eff178c0b`

```dockerfile
```

-	Layers:
	-	`sha256:38ba952907a41a1a43d318514c3c500b5a565d28343b20908c7958204b833496`  
		Last Modified: Tue, 13 Jan 2026 01:21:22 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba83d152e0054fc4751a8f2ae28ec41dfa93bdfa35769379f2d00f0c6725866`  
		Last Modified: Tue, 13 Jan 2026 01:21:21 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-bookworm`

```console
$ docker pull haskell@sha256:c9334d1485216511e34a92888287c417a6038a9644b16af9e9fbd09b61a5d0e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:b3338c5c390f6dba72e2ddc72d95157da32d63348ccc85d2b648d1cb5349de19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672809110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b8187d6524f8e02e47bb178bf8e61b0d64b1746d18be55dcc7e0c3d83375ff5`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:39 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:39 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:42 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:42 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:43 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:24 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:24 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:24 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033886e9b41283b91ad60daad2760bf2c15b8c7e230246c0895a3014e5cf50f4`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 152.4 MB (152378198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6056091128945e6de4e5781fec667f1bb690376225c4d9a155c3575d9293559b`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 22.2 MB (22220758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae1b4e89983d825bd60f229ad69e61a352ec70410347952f188b3e3ff51ff8b`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 7.6 MB (7607048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6553e22f10a6858a49b294a420f07be7f5a7600e1d25c5a6f91d0bdad8449b9`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 442.1 MB (442121623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:468099c2aeb9b5d9c2a558348b75d2470fd9294818dc3b5a5996fb08cc9a8015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9504459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc544225446d659728f955de970b8013b436835ab1fc76d6a4da51bcef59c23`

```dockerfile
```

-	Layers:
	-	`sha256:38047cd03d97c3847f9bdf72e30be07e0216f4aacd970595f090af7477401cb9`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 9.5 MB (9479105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1dec10ff78e00b018edd7557a494b4ad0e051991a6ed265447ae657dc7557300`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 25.4 KB (25354 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8c2e787617c798cb205c1e9721902b8b25db6e4de0b0d03f34764fbe9bf73ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.9 MB (682860205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30542466556ea720f4335e70af338860f156c2658a21e2b87bc8c98ae4d12154`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:47 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:47 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:16:47 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:16:47 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:16:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:16:49 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:16:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:16:51 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:16:51 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:16:51 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:18:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:18:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:18:26 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfabc667501f67409fc390477d2bd28f31024026819883c36f0edd70be1fc11f`  
		Last Modified: Tue, 13 Jan 2026 01:19:53 GMT  
		Size: 146.5 MB (146548867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ad960213d31a39bb28b0d6199412ba0e26ca5b7c9d9134dae34601fbb66b21`  
		Last Modified: Tue, 13 Jan 2026 01:19:49 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58eb92b1a20d057eef39e4ebab79e2954a5cf1bd1a2e7149cc44a1f2874bc02f`  
		Last Modified: Tue, 13 Jan 2026 01:19:48 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4476482b7fee14df773e5308fbbda70ad059d08cad960e5b1212d94ff2fcf486`  
		Last Modified: Tue, 13 Jan 2026 01:20:00 GMT  
		Size: 449.4 MB (449447693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:8a7123bb4e8cf73e02e81b229e128b2e9c656b0694a20097c46f6e55d044b8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9532370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7b1305f73614e9a79bbdf30a33b2b97de22c9c3378a24d0669e61fd6ec94e`

```dockerfile
```

-	Layers:
	-	`sha256:0ceafa94fb6f7ccd5b767bde3dcd90943e2c80a1a1ecf629a86dba70863cc7fa`  
		Last Modified: Tue, 13 Jan 2026 01:19:48 GMT  
		Size: 9.5 MB (9506889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5adbd78d1e78af4cc4b78cb8670053486ae59545a177da7d779c369ce8c558`  
		Last Modified: Tue, 13 Jan 2026 01:19:47 GMT  
		Size: 25.5 KB (25481 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-bullseye`

```console
$ docker pull haskell@sha256:121d7cc72202a98998536934817f66ec8dc2ddd73ed4c432cba16b5256efae08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:6d62c2c22558a9f4be9082d56ccc48718e81169760aa4499b9bea2bac24c2d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659144428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d89ab7703666e67c3606548f21bfb723bdad64966357caadae7ee1d74eddd3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75238d6ce97658590d0e7ca1aaf30fcba7bcb5c26bbd70cd884882a7979de149`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 133.8 MB (133753898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e15615986ee567d17dab5c314e85877d951095edac5c31e416f1681e2ab9e3`  
		Last Modified: Tue, 03 Feb 2026 02:20:38 GMT  
		Size: 22.2 MB (22220752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c76124521720024b593e6b7c5f34bb17689543c866b3a3c5ef960357ac11da`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 441.8 MB (441801274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:53d5b173bff7b231b60abbb2b322a9eb1325f442ef0a5b9467745353f1e151e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ef0c54bf6ad45c85aca74ad4802897d276198be4a7175cf1170062d7b556f0`

```dockerfile
```

-	Layers:
	-	`sha256:4b2fbe4f1a16763366e46ddbe8e41491b1d25e11b2f630c0ea068449342c0b4d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff45e85ac1e2cbaa45d82b33c17bdd2a40f1c919de0910d6f11911b02deb40`  
		Last Modified: Tue, 03 Feb 2026 02:20:36 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e7d2bb12473e8ca564817405f80a72f9a6a6f998c64e1e9b30a7c4bd213773af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669449125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9493023ab675c91b402548eab4fe024cc03aced2e301621b79d999597cda7e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904396a1ed19b72c34ac049fddb833b77d8ff29212b034f306b89170224c3e79`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 129.2 MB (129241147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6443d9a1a7bef1d3bb5e84daf420ce96bfa38211f22d03407b6f9b40283f5360`  
		Last Modified: Tue, 13 Jan 2026 01:21:23 GMT  
		Size: 24.5 MB (24528541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb39a72843976163048a101d67acc696b91e09c912f82db26b3cb2793d23db6`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6530d9b1cee1556dc890910c703727045b89398292afa180324e9634fae5f8f`  
		Last Modified: Tue, 13 Jan 2026 01:21:32 GMT  
		Size: 449.4 MB (449448708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:ff116e5d6ea811b71d7978c9385d3e9284b88978d48c6e0d98be9d714b8bd3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8ee2f44400a71e0a3a8bc51250a3388920d22ef10e42f8b0f3947eff178c0b`

```dockerfile
```

-	Layers:
	-	`sha256:38ba952907a41a1a43d318514c3c500b5a565d28343b20908c7958204b833496`  
		Last Modified: Tue, 13 Jan 2026 01:21:22 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba83d152e0054fc4751a8f2ae28ec41dfa93bdfa35769379f2d00f0c6725866`  
		Last Modified: Tue, 13 Jan 2026 01:21:21 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-slim-bookworm`

```console
$ docker pull haskell@sha256:5cc917747a8fdd54026b43853ca5cc9dc7f86e2334a76a520eeec809cc655075
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:853445b5b6937a5f1da28871fce3d98d78c9fd57d00c6ee559f19d6514cd3a07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.6 MB (624585251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91b744210e3b457b10544f543f9cedc1f30cfdfec0ab73826d0566040ab02ecc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:44 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:44 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:47 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:47 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:26 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48467f4c780344366912304cbe7dfc704286fa599688ed182b7828514d0c842b`  
		Last Modified: Tue, 03 Feb 2026 02:20:45 GMT  
		Size: 124.4 MB (124406084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbb737c2fa60d764318ac70a7045768bb2ef3c87d61ee97c0b15aa9924957eb`  
		Last Modified: Tue, 03 Feb 2026 02:20:42 GMT  
		Size: 22.2 MB (22220767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d1e215f43d3048806c8c7e9a43b2f2f06f89aff36b3cb6a195af29df9ed8df`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 7.6 MB (7607051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7e997144fcd70902763aa48966ba3583c159b973f4be345d33a669f4b91be6`  
		Last Modified: Tue, 03 Feb 2026 02:20:51 GMT  
		Size: 442.1 MB (442122862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:912966bf0c16fede60e4b00325860fc6975a6dd35860952848fe633d516882e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6316d07d1c826b3370e2733326a1bc7f8b25b04b101940f2c78feee18f7539bc`

```dockerfile
```

-	Layers:
	-	`sha256:a443b336153f6415bf7a2b15660ee1ab89e09e464b8e85df8c7191ded14a9922`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 6.6 MB (6606033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a7b431c0b751027f482b27788ac0e51143e079bc3395186c23dc70444c58d9a`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 25.4 KB (25397 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:688b184defc0e9215e9edde716f138309d067e349617792fab0c9be732173c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.6 MB (634627259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314d1d7391cc500139b7d675f410aa96f592765f6cc4f65e326c49614b4902da`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:18:15 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:15 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:15 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:15 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:17 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:17 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:18 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:19:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:19:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf965bd7e969d15740345bd03d410d0535bcc55e667282a068a7c51e14012fa5`  
		Last Modified: Tue, 13 Jan 2026 01:21:10 GMT  
		Size: 118.6 MB (118576286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82a90fa32b3bd92426bb71d0f3b6f21b7cdcfd21b1f506e577ba16693ba48b3`  
		Last Modified: Tue, 13 Jan 2026 01:21:07 GMT  
		Size: 24.5 MB (24528608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad496bfa46b59baa0e37af69a215d2dffd01fb61f27af40aa7cab953f9b8e22d`  
		Last Modified: Tue, 13 Jan 2026 01:21:06 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aee2ecf16af813f0e8d8be830d30bd1f08ae71e80205eb195349fca33e1ddbd`  
		Last Modified: Tue, 13 Jan 2026 01:21:16 GMT  
		Size: 449.4 MB (449445453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:83c59fa01c961609f8314e684df31c3daadf1df4710a44d089a9c856f1d85854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0f36b875c7051aea8ee13ed88a78606094c34e72f376724ddb6ebaa0020e13b`

```dockerfile
```

-	Layers:
	-	`sha256:c0d67e0736a9838e991b5e68ed7ab175558af34490ebdef7e5f0756e5067b7b8`  
		Last Modified: Tue, 13 Jan 2026 01:21:06 GMT  
		Size: 6.6 MB (6634444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bb376b555c4663840edf9973c351b8ebf62cf9ff15ff7cbf454babc86f00355`  
		Last Modified: Tue, 13 Jan 2026 01:21:05 GMT  
		Size: 25.5 KB (25524 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-slim-bullseye`

```console
$ docker pull haskell@sha256:5fa6651a439e5aac88472c8a0599e184f05678e4330d98bde9ebd1f50987cc0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:592e51cede7db0b4910f951a43961024661c7a8b55f47acd4bf2efe91bd88852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608259149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f9101bb8a800a45e5d6f78526a9623f8c5157af03c8e8f7d41aea34288d3f1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3c918a9dbef90c820e3b8f89e3eb745c6b8206768d5dc801bad637f07de68e`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 106.4 MB (106366909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d52fe0f0d6d3c84e13aa5a5843a10b3a0bb4cfc47cacc90ce709f6df933977f`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02604587704ad580a78c07fd1af9da93ffe6e276cd976c310847887f0742710c`  
		Last Modified: Tue, 03 Feb 2026 02:21:00 GMT  
		Size: 441.8 MB (441800960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b71502010e6068c6d40b4b8a361b29059ba4a86dc02be5e86ecd71dfb557e152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999c96a2c5eb622c8c95795883265b90267932ff8488e9032d04781b644c86e7`

```dockerfile
```

-	Layers:
	-	`sha256:0d8b88f8077a1d894aab234933ffdcb791f8e0730003ef65ae1f41d2ddfe73ce`  
		Last Modified: Tue, 03 Feb 2026 02:20:49 GMT  
		Size: 6.8 MB (6750929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0054b7fb8b6ae305be385f6ab8726d5c07a6db46e848a0ce3e842b853006ba8e`  
		Last Modified: Tue, 03 Feb 2026 02:20:49 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f56b48eefc38564ec24bd6c46efcf5e42428b594bb064d3c56a143f02b480b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618563538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fef4d36395c024b1be79dc5189fc28cf16c2f14cb1aebd8daedf43437783f7`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:23 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:23 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:23 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:25 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:25 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:25 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:27 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:27 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:27 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:19:59 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:19:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:59 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a96c3c611e1717d66afae67d6fb8eba49eb7f9ac36228fcd7b6136699549fe`  
		Last Modified: Tue, 13 Jan 2026 01:21:20 GMT  
		Size: 101.9 MB (101863954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c652f3f14d418494191692b21fa54656e5b70879faead69be341a17cd6f2841`  
		Last Modified: Tue, 13 Jan 2026 01:21:16 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3879388bec87dd8f22e12521634d07e8ae09151739d3e7636cb0c34e2d0b4a70`  
		Last Modified: Tue, 13 Jan 2026 01:21:16 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4896f989cd82087a24fcc86dea60eec6c0dd1307426e36fabe717b12939a8d9`  
		Last Modified: Tue, 13 Jan 2026 01:21:26 GMT  
		Size: 449.4 MB (449449555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:040eadb249af5b8b1cf61e5cc13d4e0cbb95dac5da5b1af59e931e53f57cfc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28288cabdcabf2ef88791f546297fa382f032786da32f5ae7c834b484595bd40`

```dockerfile
```

-	Layers:
	-	`sha256:e20461454727c7d76eb386d0ada378ce79198d146fe58555bba010ac323a4c51`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 6.8 MB (6753439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b260842ec1bfdc58222371116a8ccbbd05a84123643c55bbded00788700a5222`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12`

```console
$ docker pull haskell@sha256:056ba4087ec1c7b06df6b3b42abd1941372909cfd2cd84955a71a58dc68b3787
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12` - linux; amd64

```console
$ docker pull haskell@sha256:4134c7ba3656b0e7f071f5dcbb610afa01dc72f2caeb6ecb5a24159e533cb303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822440781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad067cf1dfbe8997c8bd62182e752dfb45bd3e4e1582b0cc01886b44501e072`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:30 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:30 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:30 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:32 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:33 GMT
ARG GHC=9.12.2
# Tue, 03 Feb 2026 02:17:33 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:19:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847cff8536ee4a541a9257d05446303870ec05a03b69312ab86f64273989ba07`  
		Last Modified: Tue, 03 Feb 2026 02:21:02 GMT  
		Size: 152.4 MB (152378177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08c43e296379639da9ea6f97d946a951a99dd197cc54e3d9076cf38a3e4018`  
		Last Modified: Tue, 03 Feb 2026 02:20:58 GMT  
		Size: 22.2 MB (22220735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65fdeab8786fcb88c566980bcab41d4a7399d7032af8ee0a3350361af84dfc1`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 7.6 MB (7607049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326a74e6d19282e106a43c7323d3e5d56295dd3da006a4537b2183ec37f8df2a`  
		Last Modified: Tue, 03 Feb 2026 02:21:13 GMT  
		Size: 591.8 MB (591753337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12` - unknown; unknown

```console
$ docker pull haskell@sha256:44649afdc7a69e1ca17c21e15b6149b9c8872d6551aa49d1b12004ff17267f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee5a0cfa1aa4219c285cdd0d42e7fccdea59e6c33d4ea9f4c5096d0c5137255`

```dockerfile
```

-	Layers:
	-	`sha256:63f3971ae78f809b05246c6aa8d4c65f8463dc6c85d3c97600b9a85c306b1369`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 9.5 MB (9478198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c5ff92e17b7c2ad4385cc0eb99403ff898793970471f779ccf04dee203d50cd`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 25.7 KB (25665 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:334d3085e673ab21675af6c46f9b191a9ed3ec09cb3cad401cb0899ddbacd1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.0 MB (825036324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8eec7b5f1894f9d62a6f5721a73acff007b1ad67e329df06dc169585a48b05d`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:21 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:16:21 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:16:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:16:24 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:16:24 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:16:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:16:25 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:16:25 GMT
ARG GHC=9.12.2
# Tue, 13 Jan 2026 01:16:25 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:18:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:18:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:18:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074b886571fd834213116382ddd00112215cdce8d4c0ba894541b77fc30c74e1`  
		Last Modified: Tue, 13 Jan 2026 01:20:03 GMT  
		Size: 146.5 MB (146548925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e131f44f58629f156679074d741d71bb115d35021a34a3499a32f8e06f8ead8c`  
		Last Modified: Tue, 13 Jan 2026 01:19:59 GMT  
		Size: 24.5 MB (24528579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e8c4961adfe1b9b6a35827ff86dc3fe640cb21c7fed95717838d278e274bc7`  
		Last Modified: Tue, 13 Jan 2026 01:19:58 GMT  
		Size: 14.0 MB (13969026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3d5746ca63ede15566ee3edaec9d90713ebd7c41154e8d8e7ee432c1c83c83`  
		Last Modified: Tue, 13 Jan 2026 01:20:14 GMT  
		Size: 591.6 MB (591623722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12` - unknown; unknown

```console
$ docker pull haskell@sha256:5beecea2cbe2959e990e940ff5dc6fabbc63f2b1d5ec27410187f8cb983d7a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3e0b1252c38f2d6b19062be1a7492648ba17592a50d48b3455947f6e355647`

```dockerfile
```

-	Layers:
	-	`sha256:217d289c67464fbc2facc9fbfccb2ca86cc98654b6507014680c65585d87b809`  
		Last Modified: Tue, 13 Jan 2026 01:19:58 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea6a3f0698116df50b2f29db08426164c74951104d225236d963e6d4f1f8df0`  
		Last Modified: Tue, 13 Jan 2026 01:19:57 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12-bookworm`

```console
$ docker pull haskell@sha256:056ba4087ec1c7b06df6b3b42abd1941372909cfd2cd84955a71a58dc68b3787
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:4134c7ba3656b0e7f071f5dcbb610afa01dc72f2caeb6ecb5a24159e533cb303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822440781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad067cf1dfbe8997c8bd62182e752dfb45bd3e4e1582b0cc01886b44501e072`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:30 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:30 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:30 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:32 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:33 GMT
ARG GHC=9.12.2
# Tue, 03 Feb 2026 02:17:33 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:19:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847cff8536ee4a541a9257d05446303870ec05a03b69312ab86f64273989ba07`  
		Last Modified: Tue, 03 Feb 2026 02:21:02 GMT  
		Size: 152.4 MB (152378177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08c43e296379639da9ea6f97d946a951a99dd197cc54e3d9076cf38a3e4018`  
		Last Modified: Tue, 03 Feb 2026 02:20:58 GMT  
		Size: 22.2 MB (22220735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65fdeab8786fcb88c566980bcab41d4a7399d7032af8ee0a3350361af84dfc1`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 7.6 MB (7607049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326a74e6d19282e106a43c7323d3e5d56295dd3da006a4537b2183ec37f8df2a`  
		Last Modified: Tue, 03 Feb 2026 02:21:13 GMT  
		Size: 591.8 MB (591753337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:44649afdc7a69e1ca17c21e15b6149b9c8872d6551aa49d1b12004ff17267f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee5a0cfa1aa4219c285cdd0d42e7fccdea59e6c33d4ea9f4c5096d0c5137255`

```dockerfile
```

-	Layers:
	-	`sha256:63f3971ae78f809b05246c6aa8d4c65f8463dc6c85d3c97600b9a85c306b1369`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 9.5 MB (9478198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c5ff92e17b7c2ad4385cc0eb99403ff898793970471f779ccf04dee203d50cd`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 25.7 KB (25665 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:334d3085e673ab21675af6c46f9b191a9ed3ec09cb3cad401cb0899ddbacd1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.0 MB (825036324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8eec7b5f1894f9d62a6f5721a73acff007b1ad67e329df06dc169585a48b05d`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:21 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:16:21 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:16:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:16:24 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:16:24 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:16:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:16:25 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:16:25 GMT
ARG GHC=9.12.2
# Tue, 13 Jan 2026 01:16:25 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:18:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:18:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:18:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074b886571fd834213116382ddd00112215cdce8d4c0ba894541b77fc30c74e1`  
		Last Modified: Tue, 13 Jan 2026 01:20:03 GMT  
		Size: 146.5 MB (146548925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e131f44f58629f156679074d741d71bb115d35021a34a3499a32f8e06f8ead8c`  
		Last Modified: Tue, 13 Jan 2026 01:19:59 GMT  
		Size: 24.5 MB (24528579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e8c4961adfe1b9b6a35827ff86dc3fe640cb21c7fed95717838d278e274bc7`  
		Last Modified: Tue, 13 Jan 2026 01:19:58 GMT  
		Size: 14.0 MB (13969026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3d5746ca63ede15566ee3edaec9d90713ebd7c41154e8d8e7ee432c1c83c83`  
		Last Modified: Tue, 13 Jan 2026 01:20:14 GMT  
		Size: 591.6 MB (591623722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:5beecea2cbe2959e990e940ff5dc6fabbc63f2b1d5ec27410187f8cb983d7a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3e0b1252c38f2d6b19062be1a7492648ba17592a50d48b3455947f6e355647`

```dockerfile
```

-	Layers:
	-	`sha256:217d289c67464fbc2facc9fbfccb2ca86cc98654b6507014680c65585d87b809`  
		Last Modified: Tue, 13 Jan 2026 01:19:58 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea6a3f0698116df50b2f29db08426164c74951104d225236d963e6d4f1f8df0`  
		Last Modified: Tue, 13 Jan 2026 01:19:57 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12-slim-bookworm`

```console
$ docker pull haskell@sha256:4ba7f2d37ed6da10d34d0ce7c465aab484c6100a28f79f7ec7c8c4a8e65e5377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:c3c04929abe385f6ce80ed80a9f978d3bbeae3400453d22fbe49cd56091fef44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774219335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f319e1581eba559dc103979f1c9f3e931371f1b1568defe6768e51b5592267`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:35 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:35 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:37 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:38 GMT
ARG GHC=9.12.2
# Tue, 03 Feb 2026 02:17:38 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277fcd715c389cd82df104554b49bd5e960d09dfe736cfad39ff1bc5510d0979`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 124.4 MB (124406044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98214d79697563f5f263bec26d64c92c2b4c7217ae8f08cad7bc33f99b11a19e`  
		Last Modified: Tue, 03 Feb 2026 02:21:04 GMT  
		Size: 22.2 MB (22220763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a6e50abf17162f01ec004f68b166a305272741b5425e755450e944e0f6ead`  
		Last Modified: Tue, 03 Feb 2026 02:21:03 GMT  
		Size: 7.6 MB (7607051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1afdfb858e4984ff9cc4ed655246b325b4127883303009abb9e670669cf1f7`  
		Last Modified: Tue, 03 Feb 2026 02:21:15 GMT  
		Size: 591.8 MB (591756990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:51e6adf46b2e29290c5d6d8d29d7879f2e5483bdcd66847c89094f49398a77cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6629642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902f26eeddeb2d977eafe31a839baed71026a3800fd25c545db8835ec85af3d4`

```dockerfile
```

-	Layers:
	-	`sha256:84ec9b6fe17184890440220c1252b6388fca96663c19ea84f2bea7c6f2d1a88b`  
		Last Modified: Tue, 03 Feb 2026 02:21:02 GMT  
		Size: 6.6 MB (6604530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:146f9f9ed1e674a0a80294ef9a0ee84ebdf3380aed428c2bc337d7a65830edca`  
		Last Modified: Tue, 03 Feb 2026 02:21:02 GMT  
		Size: 25.1 KB (25112 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8919e82613029971d8129b51ffbe61140f61e51b4cbfb79f90da7be9e59b67ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.8 MB (776808011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557190dd3ace019ef6e7ee14a66f838773242b200fa1af4d09f5101e153e0311`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:44 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:16:44 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:16:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:16:47 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:16:47 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:16:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:16:49 GMT
ARG GHC=9.12.2
# Tue, 13 Jan 2026 01:16:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:18:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:18:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:18:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d92d09680a14c3ff498adad82780adc733d5f18a8399bffaebdf9980e3e48`  
		Last Modified: Tue, 13 Jan 2026 01:20:23 GMT  
		Size: 118.6 MB (118576114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adecfc55c40d24671b57ef3bc05828f010e4952eba3561dd8bf365cf86845a42`  
		Last Modified: Tue, 13 Jan 2026 01:20:19 GMT  
		Size: 24.5 MB (24528621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acff82551c1696fa85bdfdd6ed618e064331d146fd04057b684891e91066a70`  
		Last Modified: Tue, 13 Jan 2026 01:20:18 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2931561e81452f1c4c00bd25680e79c041b8b9fc8525d57557df67773d4d4ec3`  
		Last Modified: Tue, 13 Jan 2026 01:20:33 GMT  
		Size: 591.6 MB (591626365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:e3124e8a5d71958c986d6c1bcfbf85c3db103b6637281442759d8eb49855441a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4fafa982a29a4a73e461ce1f98fac927c57f24c507ad7fbf1a50cd6c805c6d`

```dockerfile
```

-	Layers:
	-	`sha256:7cc1d6298fe8a220335aafdf752de84c858b37fde7e2b0d79129cf035030e6ab`  
		Last Modified: Tue, 13 Jan 2026 01:20:17 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cffff7202452d065a64dbb8a4c02e25a137ccc8835af714735b6268c1f69b3`  
		Last Modified: Tue, 13 Jan 2026 01:20:16 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2`

```console
$ docker pull haskell@sha256:056ba4087ec1c7b06df6b3b42abd1941372909cfd2cd84955a71a58dc68b3787
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2` - linux; amd64

```console
$ docker pull haskell@sha256:4134c7ba3656b0e7f071f5dcbb610afa01dc72f2caeb6ecb5a24159e533cb303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822440781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad067cf1dfbe8997c8bd62182e752dfb45bd3e4e1582b0cc01886b44501e072`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:30 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:30 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:30 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:32 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:33 GMT
ARG GHC=9.12.2
# Tue, 03 Feb 2026 02:17:33 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:19:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847cff8536ee4a541a9257d05446303870ec05a03b69312ab86f64273989ba07`  
		Last Modified: Tue, 03 Feb 2026 02:21:02 GMT  
		Size: 152.4 MB (152378177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08c43e296379639da9ea6f97d946a951a99dd197cc54e3d9076cf38a3e4018`  
		Last Modified: Tue, 03 Feb 2026 02:20:58 GMT  
		Size: 22.2 MB (22220735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65fdeab8786fcb88c566980bcab41d4a7399d7032af8ee0a3350361af84dfc1`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 7.6 MB (7607049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326a74e6d19282e106a43c7323d3e5d56295dd3da006a4537b2183ec37f8df2a`  
		Last Modified: Tue, 03 Feb 2026 02:21:13 GMT  
		Size: 591.8 MB (591753337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2` - unknown; unknown

```console
$ docker pull haskell@sha256:44649afdc7a69e1ca17c21e15b6149b9c8872d6551aa49d1b12004ff17267f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee5a0cfa1aa4219c285cdd0d42e7fccdea59e6c33d4ea9f4c5096d0c5137255`

```dockerfile
```

-	Layers:
	-	`sha256:63f3971ae78f809b05246c6aa8d4c65f8463dc6c85d3c97600b9a85c306b1369`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 9.5 MB (9478198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c5ff92e17b7c2ad4385cc0eb99403ff898793970471f779ccf04dee203d50cd`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 25.7 KB (25665 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:334d3085e673ab21675af6c46f9b191a9ed3ec09cb3cad401cb0899ddbacd1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.0 MB (825036324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8eec7b5f1894f9d62a6f5721a73acff007b1ad67e329df06dc169585a48b05d`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:21 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:16:21 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:16:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:16:24 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:16:24 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:16:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:16:25 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:16:25 GMT
ARG GHC=9.12.2
# Tue, 13 Jan 2026 01:16:25 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:18:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:18:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:18:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074b886571fd834213116382ddd00112215cdce8d4c0ba894541b77fc30c74e1`  
		Last Modified: Tue, 13 Jan 2026 01:20:03 GMT  
		Size: 146.5 MB (146548925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e131f44f58629f156679074d741d71bb115d35021a34a3499a32f8e06f8ead8c`  
		Last Modified: Tue, 13 Jan 2026 01:19:59 GMT  
		Size: 24.5 MB (24528579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e8c4961adfe1b9b6a35827ff86dc3fe640cb21c7fed95717838d278e274bc7`  
		Last Modified: Tue, 13 Jan 2026 01:19:58 GMT  
		Size: 14.0 MB (13969026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3d5746ca63ede15566ee3edaec9d90713ebd7c41154e8d8e7ee432c1c83c83`  
		Last Modified: Tue, 13 Jan 2026 01:20:14 GMT  
		Size: 591.6 MB (591623722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2` - unknown; unknown

```console
$ docker pull haskell@sha256:5beecea2cbe2959e990e940ff5dc6fabbc63f2b1d5ec27410187f8cb983d7a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3e0b1252c38f2d6b19062be1a7492648ba17592a50d48b3455947f6e355647`

```dockerfile
```

-	Layers:
	-	`sha256:217d289c67464fbc2facc9fbfccb2ca86cc98654b6507014680c65585d87b809`  
		Last Modified: Tue, 13 Jan 2026 01:19:58 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea6a3f0698116df50b2f29db08426164c74951104d225236d963e6d4f1f8df0`  
		Last Modified: Tue, 13 Jan 2026 01:19:57 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2-bookworm`

```console
$ docker pull haskell@sha256:056ba4087ec1c7b06df6b3b42abd1941372909cfd2cd84955a71a58dc68b3787
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:4134c7ba3656b0e7f071f5dcbb610afa01dc72f2caeb6ecb5a24159e533cb303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822440781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad067cf1dfbe8997c8bd62182e752dfb45bd3e4e1582b0cc01886b44501e072`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:30 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:30 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:30 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:30 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:32 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:32 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:32 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:33 GMT
ARG GHC=9.12.2
# Tue, 03 Feb 2026 02:17:33 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:19:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847cff8536ee4a541a9257d05446303870ec05a03b69312ab86f64273989ba07`  
		Last Modified: Tue, 03 Feb 2026 02:21:02 GMT  
		Size: 152.4 MB (152378177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed08c43e296379639da9ea6f97d946a951a99dd197cc54e3d9076cf38a3e4018`  
		Last Modified: Tue, 03 Feb 2026 02:20:58 GMT  
		Size: 22.2 MB (22220735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65fdeab8786fcb88c566980bcab41d4a7399d7032af8ee0a3350361af84dfc1`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 7.6 MB (7607049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326a74e6d19282e106a43c7323d3e5d56295dd3da006a4537b2183ec37f8df2a`  
		Last Modified: Tue, 03 Feb 2026 02:21:13 GMT  
		Size: 591.8 MB (591753337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:44649afdc7a69e1ca17c21e15b6149b9c8872d6551aa49d1b12004ff17267f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fee5a0cfa1aa4219c285cdd0d42e7fccdea59e6c33d4ea9f4c5096d0c5137255`

```dockerfile
```

-	Layers:
	-	`sha256:63f3971ae78f809b05246c6aa8d4c65f8463dc6c85d3c97600b9a85c306b1369`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 9.5 MB (9478198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c5ff92e17b7c2ad4385cc0eb99403ff898793970471f779ccf04dee203d50cd`  
		Last Modified: Tue, 03 Feb 2026 02:20:57 GMT  
		Size: 25.7 KB (25665 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:334d3085e673ab21675af6c46f9b191a9ed3ec09cb3cad401cb0899ddbacd1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.0 MB (825036324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8eec7b5f1894f9d62a6f5721a73acff007b1ad67e329df06dc169585a48b05d`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:21 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:21 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:16:21 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:16:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:16:24 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:16:24 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:16:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:16:25 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:16:25 GMT
ARG GHC=9.12.2
# Tue, 13 Jan 2026 01:16:25 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:18:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:18:19 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:18:19 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:074b886571fd834213116382ddd00112215cdce8d4c0ba894541b77fc30c74e1`  
		Last Modified: Tue, 13 Jan 2026 01:20:03 GMT  
		Size: 146.5 MB (146548925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e131f44f58629f156679074d741d71bb115d35021a34a3499a32f8e06f8ead8c`  
		Last Modified: Tue, 13 Jan 2026 01:19:59 GMT  
		Size: 24.5 MB (24528579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e8c4961adfe1b9b6a35827ff86dc3fe640cb21c7fed95717838d278e274bc7`  
		Last Modified: Tue, 13 Jan 2026 01:19:58 GMT  
		Size: 14.0 MB (13969026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3d5746ca63ede15566ee3edaec9d90713ebd7c41154e8d8e7ee432c1c83c83`  
		Last Modified: Tue, 13 Jan 2026 01:20:14 GMT  
		Size: 591.6 MB (591623722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:5beecea2cbe2959e990e940ff5dc6fabbc63f2b1d5ec27410187f8cb983d7a13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c3e0b1252c38f2d6b19062be1a7492648ba17592a50d48b3455947f6e355647`

```dockerfile
```

-	Layers:
	-	`sha256:217d289c67464fbc2facc9fbfccb2ca86cc98654b6507014680c65585d87b809`  
		Last Modified: Tue, 13 Jan 2026 01:19:58 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea6a3f0698116df50b2f29db08426164c74951104d225236d963e6d4f1f8df0`  
		Last Modified: Tue, 13 Jan 2026 01:19:57 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2-slim-bookworm`

```console
$ docker pull haskell@sha256:4ba7f2d37ed6da10d34d0ce7c465aab484c6100a28f79f7ec7c8c4a8e65e5377
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:c3c04929abe385f6ce80ed80a9f978d3bbeae3400453d22fbe49cd56091fef44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774219335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f319e1581eba559dc103979f1c9f3e931371f1b1568defe6768e51b5592267`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:35 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:35 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:37 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:38 GMT
ARG GHC=9.12.2
# Tue, 03 Feb 2026 02:17:38 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277fcd715c389cd82df104554b49bd5e960d09dfe736cfad39ff1bc5510d0979`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 124.4 MB (124406044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98214d79697563f5f263bec26d64c92c2b4c7217ae8f08cad7bc33f99b11a19e`  
		Last Modified: Tue, 03 Feb 2026 02:21:04 GMT  
		Size: 22.2 MB (22220763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3a6e50abf17162f01ec004f68b166a305272741b5425e755450e944e0f6ead`  
		Last Modified: Tue, 03 Feb 2026 02:21:03 GMT  
		Size: 7.6 MB (7607051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e1afdfb858e4984ff9cc4ed655246b325b4127883303009abb9e670669cf1f7`  
		Last Modified: Tue, 03 Feb 2026 02:21:15 GMT  
		Size: 591.8 MB (591756990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:51e6adf46b2e29290c5d6d8d29d7879f2e5483bdcd66847c89094f49398a77cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6629642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:902f26eeddeb2d977eafe31a839baed71026a3800fd25c545db8835ec85af3d4`

```dockerfile
```

-	Layers:
	-	`sha256:84ec9b6fe17184890440220c1252b6388fca96663c19ea84f2bea7c6f2d1a88b`  
		Last Modified: Tue, 03 Feb 2026 02:21:02 GMT  
		Size: 6.6 MB (6604530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:146f9f9ed1e674a0a80294ef9a0ee84ebdf3380aed428c2bc337d7a65830edca`  
		Last Modified: Tue, 03 Feb 2026 02:21:02 GMT  
		Size: 25.1 KB (25112 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8919e82613029971d8129b51ffbe61140f61e51b4cbfb79f90da7be9e59b67ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.8 MB (776808011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:557190dd3ace019ef6e7ee14a66f838773242b200fa1af4d09f5101e153e0311`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Tue, 13 Jan 2026 01:16:44 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:16:44 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:16:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:16:47 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:16:47 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:16:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:16:49 GMT
ARG GHC=9.12.2
# Tue, 13 Jan 2026 01:16:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:18:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:18:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:18:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7d92d09680a14c3ff498adad82780adc733d5f18a8399bffaebdf9980e3e48`  
		Last Modified: Tue, 13 Jan 2026 01:20:23 GMT  
		Size: 118.6 MB (118576114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adecfc55c40d24671b57ef3bc05828f010e4952eba3561dd8bf365cf86845a42`  
		Last Modified: Tue, 13 Jan 2026 01:20:19 GMT  
		Size: 24.5 MB (24528621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acff82551c1696fa85bdfdd6ed618e064331d146fd04057b684891e91066a70`  
		Last Modified: Tue, 13 Jan 2026 01:20:18 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2931561e81452f1c4c00bd25680e79c041b8b9fc8525d57557df67773d4d4ec3`  
		Last Modified: Tue, 13 Jan 2026 01:20:33 GMT  
		Size: 591.6 MB (591626365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:e3124e8a5d71958c986d6c1bcfbf85c3db103b6637281442759d8eb49855441a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4fafa982a29a4a73e461ce1f98fac927c57f24c507ad7fbf1a50cd6c805c6d`

```dockerfile
```

-	Layers:
	-	`sha256:7cc1d6298fe8a220335aafdf752de84c858b37fde7e2b0d79129cf035030e6ab`  
		Last Modified: Tue, 13 Jan 2026 01:20:17 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0cffff7202452d065a64dbb8a4c02e25a137ccc8835af714735b6268c1f69b3`  
		Last Modified: Tue, 13 Jan 2026 01:20:16 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14`

```console
$ docker pull haskell@sha256:8e045c47c827e23a327facff2522cbdced501bfffc6a094790ea3acee5f80271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14` - linux; amd64

```console
$ docker pull haskell@sha256:f299e044461def92978fc02e1e09552447341fc5c94ea3fde855356920ce098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825154630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63dd23015457b14a600b2dbe468a91166b8b706e868ab525cd551f1e6752392`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08794db77b402d64775f4e981b74315507b6698f4e772bacb62fdc7b5735b9`  
		Last Modified: Tue, 03 Feb 2026 02:20:56 GMT  
		Size: 152.4 MB (152378556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b299d79199c316ba1c329518d60279d166e472b155f0c55f2a42d63bb555ff6`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 22.2 MB (22220734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf9f8fc6d29b3d4e84084da560dd2ce71e871ccddc8c93c22ff66bf7e77dee`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbba24a3271904d1646e97c601cdd0e42bb50d0b10c10c9b00ab7e261d98aa9`  
		Last Modified: Tue, 03 Feb 2026 02:21:04 GMT  
		Size: 593.7 MB (593670352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14` - unknown; unknown

```console
$ docker pull haskell@sha256:b65ceb02ebede4bb61233c4b3228185b02f49b4c1cc6b2567df8edb48897c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e72c5a7ed2a057767454c8042905556f8493bdeedad4ec5bfa2dc52a5be25`

```dockerfile
```

-	Layers:
	-	`sha256:3a41aa03b940ddcb25fbd9428922b0f9b80e650d1d1cead15187736cba9433c6`  
		Last Modified: Tue, 03 Feb 2026 02:20:51 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60457317faadd06cb6ad537a6c0fb420942fbce0fcc24a3abaf5ad72e07f835`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3647e354c660ae20c53edfcbfb91f43c4d9d3f2b34e786cf1c51e9d6c04192ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.9 MB (827938406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab6dc3d055aef05cb68b4a5a96286c18de7d4623962bf4f310e617e9cf6279`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:21:35 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:21:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:21:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:21:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:23:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:23:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:23:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ae27c4297057722c43286a8294938ff609b4d211656df39e2178c8277df13`  
		Last Modified: Thu, 29 Jan 2026 20:25:24 GMT  
		Size: 146.5 MB (146547971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0bc56010070d4e8fd82ec69ac9be3c9a3ba21af3a73437fa720285f651edf9`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc9ecd04267369e82fde7fe99460dc9d508021a337f569b1d96fb58aea97940`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a7bfdf951d98afe3fbbbfd846edc57c7dbfb14ff061e20cedcbd12808fd44`  
		Last Modified: Thu, 29 Jan 2026 20:25:35 GMT  
		Size: 592.6 MB (592551222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14` - unknown; unknown

```console
$ docker pull haskell@sha256:28996c9136802910cbfa3de6faaa5f9df4c033a64d313bd21b8e2cc1c6f5ac09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30fbc1a52bca5749a1beddc1d1fd5e8218cf4834d4bfdf119591d410ae7d516`

```dockerfile
```

-	Layers:
	-	`sha256:8f8f009cad10ee83982e723ea3e97386d783620402ef46fa4847511228f91da9`  
		Last Modified: Thu, 29 Jan 2026 20:25:17 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0d371f55e52b36c5159955ffb3ceb5b15c9f552ed0fc7ed5ea5fb0930fd50f`  
		Last Modified: Thu, 29 Jan 2026 20:25:16 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14-bookworm`

```console
$ docker pull haskell@sha256:8e045c47c827e23a327facff2522cbdced501bfffc6a094790ea3acee5f80271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:f299e044461def92978fc02e1e09552447341fc5c94ea3fde855356920ce098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825154630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63dd23015457b14a600b2dbe468a91166b8b706e868ab525cd551f1e6752392`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08794db77b402d64775f4e981b74315507b6698f4e772bacb62fdc7b5735b9`  
		Last Modified: Tue, 03 Feb 2026 02:20:56 GMT  
		Size: 152.4 MB (152378556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b299d79199c316ba1c329518d60279d166e472b155f0c55f2a42d63bb555ff6`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 22.2 MB (22220734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf9f8fc6d29b3d4e84084da560dd2ce71e871ccddc8c93c22ff66bf7e77dee`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbba24a3271904d1646e97c601cdd0e42bb50d0b10c10c9b00ab7e261d98aa9`  
		Last Modified: Tue, 03 Feb 2026 02:21:04 GMT  
		Size: 593.7 MB (593670352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:b65ceb02ebede4bb61233c4b3228185b02f49b4c1cc6b2567df8edb48897c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e72c5a7ed2a057767454c8042905556f8493bdeedad4ec5bfa2dc52a5be25`

```dockerfile
```

-	Layers:
	-	`sha256:3a41aa03b940ddcb25fbd9428922b0f9b80e650d1d1cead15187736cba9433c6`  
		Last Modified: Tue, 03 Feb 2026 02:20:51 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60457317faadd06cb6ad537a6c0fb420942fbce0fcc24a3abaf5ad72e07f835`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3647e354c660ae20c53edfcbfb91f43c4d9d3f2b34e786cf1c51e9d6c04192ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.9 MB (827938406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab6dc3d055aef05cb68b4a5a96286c18de7d4623962bf4f310e617e9cf6279`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:21:35 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:21:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:21:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:21:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:23:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:23:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:23:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ae27c4297057722c43286a8294938ff609b4d211656df39e2178c8277df13`  
		Last Modified: Thu, 29 Jan 2026 20:25:24 GMT  
		Size: 146.5 MB (146547971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0bc56010070d4e8fd82ec69ac9be3c9a3ba21af3a73437fa720285f651edf9`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc9ecd04267369e82fde7fe99460dc9d508021a337f569b1d96fb58aea97940`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a7bfdf951d98afe3fbbbfd846edc57c7dbfb14ff061e20cedcbd12808fd44`  
		Last Modified: Thu, 29 Jan 2026 20:25:35 GMT  
		Size: 592.6 MB (592551222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:28996c9136802910cbfa3de6faaa5f9df4c033a64d313bd21b8e2cc1c6f5ac09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30fbc1a52bca5749a1beddc1d1fd5e8218cf4834d4bfdf119591d410ae7d516`

```dockerfile
```

-	Layers:
	-	`sha256:8f8f009cad10ee83982e723ea3e97386d783620402ef46fa4847511228f91da9`  
		Last Modified: Thu, 29 Jan 2026 20:25:17 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0d371f55e52b36c5159955ffb3ceb5b15c9f552ed0fc7ed5ea5fb0930fd50f`  
		Last Modified: Thu, 29 Jan 2026 20:25:16 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14-slim-bookworm`

```console
$ docker pull haskell@sha256:421d5abd82604d78c08e4438bfb81df19816c79c08abd7ba6e74e7018df11c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:110d4a2d1efeeddb62ae38b915474444040487c6a4b644a37597bacb652f6460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776930005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e17615141dab7f099ff2b4faa0260fda01bdebca0a3a049d99937148a1eb06`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fe43daec195aa75262a2e86f9dc0ba4805f1705d8cd95c334dfd178dc9f11`  
		Last Modified: Tue, 03 Feb 2026 02:21:11 GMT  
		Size: 124.4 MB (124406060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e90ee734b1d3e56d7e2c6c778dda05a971c7333a05589fd21b9acd055603e`  
		Last Modified: Tue, 03 Feb 2026 02:21:08 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c41bcf39676cc775bbe10c12641791e3c3663f6a9bf7d661910276e362c26a2`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba2b992b4373bf7d394ffc39402a056b50fcc2fe9128c8856debcd41019dc5`  
		Last Modified: Tue, 03 Feb 2026 02:21:20 GMT  
		Size: 593.7 MB (593671184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:65b9a880c769cf5ce7cf9d1784ebd941644fff1242af9e2ece0a74c1fd5227c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef83333c9d00ac92e175ccb2585258325e7d4da865be37a85b8ca928cde3ac47`

```dockerfile
```

-	Layers:
	-	`sha256:88cb24a779b9ff5b1a8c0db293620ff74fec7cc2142f09dd8360962ecdc27e6b`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd146a8e20014ebf818d4bfb1265a4d978f26ba9a61f8c9ec2e8bd4c1511f61c`  
		Last Modified: Tue, 03 Feb 2026 02:21:06 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3a36953ac7ac34d4f2c7498322c3266d227776b5a1374aaef40ef1dbb95a17e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779705710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d69fc402d5193d22afabc71d151a6dbee4eca69e5d5e0466c257538101922cf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:22:31 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:22:31 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:22:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:22:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:24:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:24:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:24:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4f4ed0fd2c28ce4be76881e223763ccd903d7068141aa943944e73ca61468a`  
		Last Modified: Thu, 29 Jan 2026 20:26:12 GMT  
		Size: 118.6 MB (118575484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc78c2319953580a1d9cb773453a236d84f48dec9454c1b1534ef532fe1effd`  
		Last Modified: Thu, 29 Jan 2026 20:26:09 GMT  
		Size: 24.5 MB (24528567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc147b79cfae7eb4a1b9bdde1478144c933c31fd6f6402300042448a3640ac55`  
		Last Modified: Thu, 29 Jan 2026 20:26:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d318096c027eaa2441061e88514b6b1d35edece3563f243ee9d20f2938d35c5b`  
		Last Modified: Thu, 29 Jan 2026 20:26:20 GMT  
		Size: 592.5 MB (592549179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:7aba8a6d02bbaad684351341c59715c03e30704c97b1699ecdaf17ef77701320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e874e120e22a3c1bd835535e506ad86b8efcd95a6e43b5e756976a218455f01f`

```dockerfile
```

-	Layers:
	-	`sha256:6b1e3e7fb716a9221df7a76d1eac6ca105121dd69f7decb039b19b8318ae9d43`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e3e173986e5627199e41d6685f1ff63e51f059ddb7b6dcd86c0412d9598faf`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14.1`

```console
$ docker pull haskell@sha256:8e045c47c827e23a327facff2522cbdced501bfffc6a094790ea3acee5f80271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14.1` - linux; amd64

```console
$ docker pull haskell@sha256:f299e044461def92978fc02e1e09552447341fc5c94ea3fde855356920ce098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825154630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63dd23015457b14a600b2dbe468a91166b8b706e868ab525cd551f1e6752392`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08794db77b402d64775f4e981b74315507b6698f4e772bacb62fdc7b5735b9`  
		Last Modified: Tue, 03 Feb 2026 02:20:56 GMT  
		Size: 152.4 MB (152378556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b299d79199c316ba1c329518d60279d166e472b155f0c55f2a42d63bb555ff6`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 22.2 MB (22220734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf9f8fc6d29b3d4e84084da560dd2ce71e871ccddc8c93c22ff66bf7e77dee`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbba24a3271904d1646e97c601cdd0e42bb50d0b10c10c9b00ab7e261d98aa9`  
		Last Modified: Tue, 03 Feb 2026 02:21:04 GMT  
		Size: 593.7 MB (593670352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1` - unknown; unknown

```console
$ docker pull haskell@sha256:b65ceb02ebede4bb61233c4b3228185b02f49b4c1cc6b2567df8edb48897c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e72c5a7ed2a057767454c8042905556f8493bdeedad4ec5bfa2dc52a5be25`

```dockerfile
```

-	Layers:
	-	`sha256:3a41aa03b940ddcb25fbd9428922b0f9b80e650d1d1cead15187736cba9433c6`  
		Last Modified: Tue, 03 Feb 2026 02:20:51 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60457317faadd06cb6ad537a6c0fb420942fbce0fcc24a3abaf5ad72e07f835`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14.1` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3647e354c660ae20c53edfcbfb91f43c4d9d3f2b34e786cf1c51e9d6c04192ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.9 MB (827938406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab6dc3d055aef05cb68b4a5a96286c18de7d4623962bf4f310e617e9cf6279`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:21:35 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:21:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:21:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:21:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:23:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:23:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:23:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ae27c4297057722c43286a8294938ff609b4d211656df39e2178c8277df13`  
		Last Modified: Thu, 29 Jan 2026 20:25:24 GMT  
		Size: 146.5 MB (146547971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0bc56010070d4e8fd82ec69ac9be3c9a3ba21af3a73437fa720285f651edf9`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc9ecd04267369e82fde7fe99460dc9d508021a337f569b1d96fb58aea97940`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a7bfdf951d98afe3fbbbfd846edc57c7dbfb14ff061e20cedcbd12808fd44`  
		Last Modified: Thu, 29 Jan 2026 20:25:35 GMT  
		Size: 592.6 MB (592551222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1` - unknown; unknown

```console
$ docker pull haskell@sha256:28996c9136802910cbfa3de6faaa5f9df4c033a64d313bd21b8e2cc1c6f5ac09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30fbc1a52bca5749a1beddc1d1fd5e8218cf4834d4bfdf119591d410ae7d516`

```dockerfile
```

-	Layers:
	-	`sha256:8f8f009cad10ee83982e723ea3e97386d783620402ef46fa4847511228f91da9`  
		Last Modified: Thu, 29 Jan 2026 20:25:17 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0d371f55e52b36c5159955ffb3ceb5b15c9f552ed0fc7ed5ea5fb0930fd50f`  
		Last Modified: Thu, 29 Jan 2026 20:25:16 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14.1-bookworm`

```console
$ docker pull haskell@sha256:8e045c47c827e23a327facff2522cbdced501bfffc6a094790ea3acee5f80271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14.1-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:f299e044461def92978fc02e1e09552447341fc5c94ea3fde855356920ce098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825154630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63dd23015457b14a600b2dbe468a91166b8b706e868ab525cd551f1e6752392`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08794db77b402d64775f4e981b74315507b6698f4e772bacb62fdc7b5735b9`  
		Last Modified: Tue, 03 Feb 2026 02:20:56 GMT  
		Size: 152.4 MB (152378556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b299d79199c316ba1c329518d60279d166e472b155f0c55f2a42d63bb555ff6`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 22.2 MB (22220734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf9f8fc6d29b3d4e84084da560dd2ce71e871ccddc8c93c22ff66bf7e77dee`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbba24a3271904d1646e97c601cdd0e42bb50d0b10c10c9b00ab7e261d98aa9`  
		Last Modified: Tue, 03 Feb 2026 02:21:04 GMT  
		Size: 593.7 MB (593670352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:b65ceb02ebede4bb61233c4b3228185b02f49b4c1cc6b2567df8edb48897c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e72c5a7ed2a057767454c8042905556f8493bdeedad4ec5bfa2dc52a5be25`

```dockerfile
```

-	Layers:
	-	`sha256:3a41aa03b940ddcb25fbd9428922b0f9b80e650d1d1cead15187736cba9433c6`  
		Last Modified: Tue, 03 Feb 2026 02:20:51 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60457317faadd06cb6ad537a6c0fb420942fbce0fcc24a3abaf5ad72e07f835`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3647e354c660ae20c53edfcbfb91f43c4d9d3f2b34e786cf1c51e9d6c04192ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.9 MB (827938406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab6dc3d055aef05cb68b4a5a96286c18de7d4623962bf4f310e617e9cf6279`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:21:35 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:21:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:21:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:21:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:23:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:23:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:23:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ae27c4297057722c43286a8294938ff609b4d211656df39e2178c8277df13`  
		Last Modified: Thu, 29 Jan 2026 20:25:24 GMT  
		Size: 146.5 MB (146547971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0bc56010070d4e8fd82ec69ac9be3c9a3ba21af3a73437fa720285f651edf9`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc9ecd04267369e82fde7fe99460dc9d508021a337f569b1d96fb58aea97940`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a7bfdf951d98afe3fbbbfd846edc57c7dbfb14ff061e20cedcbd12808fd44`  
		Last Modified: Thu, 29 Jan 2026 20:25:35 GMT  
		Size: 592.6 MB (592551222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:28996c9136802910cbfa3de6faaa5f9df4c033a64d313bd21b8e2cc1c6f5ac09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30fbc1a52bca5749a1beddc1d1fd5e8218cf4834d4bfdf119591d410ae7d516`

```dockerfile
```

-	Layers:
	-	`sha256:8f8f009cad10ee83982e723ea3e97386d783620402ef46fa4847511228f91da9`  
		Last Modified: Thu, 29 Jan 2026 20:25:17 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0d371f55e52b36c5159955ffb3ceb5b15c9f552ed0fc7ed5ea5fb0930fd50f`  
		Last Modified: Thu, 29 Jan 2026 20:25:16 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.14.1-slim-bookworm`

```console
$ docker pull haskell@sha256:421d5abd82604d78c08e4438bfb81df19816c79c08abd7ba6e74e7018df11c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.14.1-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:110d4a2d1efeeddb62ae38b915474444040487c6a4b644a37597bacb652f6460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776930005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e17615141dab7f099ff2b4faa0260fda01bdebca0a3a049d99937148a1eb06`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fe43daec195aa75262a2e86f9dc0ba4805f1705d8cd95c334dfd178dc9f11`  
		Last Modified: Tue, 03 Feb 2026 02:21:11 GMT  
		Size: 124.4 MB (124406060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e90ee734b1d3e56d7e2c6c778dda05a971c7333a05589fd21b9acd055603e`  
		Last Modified: Tue, 03 Feb 2026 02:21:08 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c41bcf39676cc775bbe10c12641791e3c3663f6a9bf7d661910276e362c26a2`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba2b992b4373bf7d394ffc39402a056b50fcc2fe9128c8856debcd41019dc5`  
		Last Modified: Tue, 03 Feb 2026 02:21:20 GMT  
		Size: 593.7 MB (593671184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:65b9a880c769cf5ce7cf9d1784ebd941644fff1242af9e2ece0a74c1fd5227c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef83333c9d00ac92e175ccb2585258325e7d4da865be37a85b8ca928cde3ac47`

```dockerfile
```

-	Layers:
	-	`sha256:88cb24a779b9ff5b1a8c0db293620ff74fec7cc2142f09dd8360962ecdc27e6b`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd146a8e20014ebf818d4bfb1265a4d978f26ba9a61f8c9ec2e8bd4c1511f61c`  
		Last Modified: Tue, 03 Feb 2026 02:21:06 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.14.1-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3a36953ac7ac34d4f2c7498322c3266d227776b5a1374aaef40ef1dbb95a17e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779705710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d69fc402d5193d22afabc71d151a6dbee4eca69e5d5e0466c257538101922cf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:22:31 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:22:31 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:22:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:22:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:24:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:24:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:24:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4f4ed0fd2c28ce4be76881e223763ccd903d7068141aa943944e73ca61468a`  
		Last Modified: Thu, 29 Jan 2026 20:26:12 GMT  
		Size: 118.6 MB (118575484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc78c2319953580a1d9cb773453a236d84f48dec9454c1b1534ef532fe1effd`  
		Last Modified: Thu, 29 Jan 2026 20:26:09 GMT  
		Size: 24.5 MB (24528567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc147b79cfae7eb4a1b9bdde1478144c933c31fd6f6402300042448a3640ac55`  
		Last Modified: Thu, 29 Jan 2026 20:26:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d318096c027eaa2441061e88514b6b1d35edece3563f243ee9d20f2938d35c5b`  
		Last Modified: Thu, 29 Jan 2026 20:26:20 GMT  
		Size: 592.5 MB (592549179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.14.1-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:7aba8a6d02bbaad684351341c59715c03e30704c97b1699ecdaf17ef77701320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e874e120e22a3c1bd835535e506ad86b8efcd95a6e43b5e756976a218455f01f`

```dockerfile
```

-	Layers:
	-	`sha256:6b1e3e7fb716a9221df7a76d1eac6ca105121dd69f7decb039b19b8318ae9d43`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e3e173986e5627199e41d6685f1ff63e51f059ddb7b6dcd86c0412d9598faf`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6`

```console
$ docker pull haskell@sha256:1995ee1a0659f2a209a2d3dc85398977fb7578c8e5804b8635b57e35896b244e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6` - linux; amd64

```console
$ docker pull haskell@sha256:ef9b9a8948d4d26d3ddfc5799559da43b8b7ccde2eee63423721ea8e07f6ab10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641568569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dabf6b1346eca125437d0258efc9b82f037017d8df80b261cc498dd2dfd5fde`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.6.7
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 03 Feb 2026 02:22:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:22:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:22:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75238d6ce97658590d0e7ca1aaf30fcba7bcb5c26bbd70cd884882a7979de149`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 133.8 MB (133753898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e15615986ee567d17dab5c314e85877d951095edac5c31e416f1681e2ab9e3`  
		Last Modified: Tue, 03 Feb 2026 02:20:38 GMT  
		Size: 22.2 MB (22220752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942fd0d25d80acdb7c2774885eaa17e3d93e5dbfc722b533fd3bd38888e36cac`  
		Last Modified: Tue, 03 Feb 2026 02:23:25 GMT  
		Size: 424.2 MB (424225415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6` - unknown; unknown

```console
$ docker pull haskell@sha256:8c4fd91f6b57e3234c74f3bc6a29564222a19b831cc19bd7154dd96bcd8e5906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c2a01cad7310d78fc1119dee1c6a1fee7f9472cec94157453be6c8dab2c1ee`

```dockerfile
```

-	Layers:
	-	`sha256:0c3c982f6b1431449a371db68c3489b68e7db13b196a13e64e08415c86028a17`  
		Last Modified: Tue, 03 Feb 2026 02:23:18 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed146138c71068e69fa1c823d5d4f410bd20e5b29b6fe92a2faf2862a5746b8e`  
		Last Modified: Tue, 03 Feb 2026 02:23:17 GMT  
		Size: 25.9 KB (25932 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dbee87ee5334b36283a188f3cf02074a05dc0f5a8e87522e0bad1dc294faa119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.3 MB (658348341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a9b89ad24dd7f0b8220c53bf45afff269f4106131e8d3d87215082920779e2`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:19:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:19:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:01 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:19:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:19:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:19:03 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:19:03 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:19:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:19:05 GMT
ARG GHC=9.6.7
# Tue, 13 Jan 2026 01:19:05 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 13 Jan 2026 01:20:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56c8e381c4c548efa2e0c514882920bda51a8b40be3ae501c5cc51d496b07b9`  
		Last Modified: Tue, 13 Jan 2026 01:21:49 GMT  
		Size: 129.2 MB (129241172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97b0f71e0456e365148f4e9bf1cf16be60a084676b0d6bcaeb913f6f0a1295`  
		Last Modified: Tue, 13 Jan 2026 01:21:46 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c740a1766ee13eb7baa30438c154bc1ae83a904c9ec3a5aadbcfb465805aca`  
		Last Modified: Tue, 13 Jan 2026 01:21:45 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7038b252ae807d953a08095f4d5c04fc5036007d833f461743ad79d86bfd7beb`  
		Last Modified: Tue, 13 Jan 2026 01:21:56 GMT  
		Size: 438.3 MB (438347889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6` - unknown; unknown

```console
$ docker pull haskell@sha256:a06fcb3bba11ce5186c27d8b337d361f096075a9d0cf915bc40423b21748a9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75085a9bf66c5f32c3fdb07d1c8bc886c0d772b55dd31837eabe5057adce0c7d`

```dockerfile
```

-	Layers:
	-	`sha256:9494340f729cfe127b476597730adc09f750193cccf2475d85d86e7e51d0e2b2`  
		Last Modified: Tue, 13 Jan 2026 01:21:45 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3012246b847824d7c5f7fbe527a0687a9eb59b615e695359a7e768604be530`  
		Last Modified: Tue, 13 Jan 2026 01:21:44 GMT  
		Size: 26.1 KB (26083 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-bullseye`

```console
$ docker pull haskell@sha256:1995ee1a0659f2a209a2d3dc85398977fb7578c8e5804b8635b57e35896b244e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:ef9b9a8948d4d26d3ddfc5799559da43b8b7ccde2eee63423721ea8e07f6ab10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641568569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dabf6b1346eca125437d0258efc9b82f037017d8df80b261cc498dd2dfd5fde`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.6.7
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 03 Feb 2026 02:22:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:22:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:22:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75238d6ce97658590d0e7ca1aaf30fcba7bcb5c26bbd70cd884882a7979de149`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 133.8 MB (133753898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e15615986ee567d17dab5c314e85877d951095edac5c31e416f1681e2ab9e3`  
		Last Modified: Tue, 03 Feb 2026 02:20:38 GMT  
		Size: 22.2 MB (22220752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942fd0d25d80acdb7c2774885eaa17e3d93e5dbfc722b533fd3bd38888e36cac`  
		Last Modified: Tue, 03 Feb 2026 02:23:25 GMT  
		Size: 424.2 MB (424225415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:8c4fd91f6b57e3234c74f3bc6a29564222a19b831cc19bd7154dd96bcd8e5906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c2a01cad7310d78fc1119dee1c6a1fee7f9472cec94157453be6c8dab2c1ee`

```dockerfile
```

-	Layers:
	-	`sha256:0c3c982f6b1431449a371db68c3489b68e7db13b196a13e64e08415c86028a17`  
		Last Modified: Tue, 03 Feb 2026 02:23:18 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed146138c71068e69fa1c823d5d4f410bd20e5b29b6fe92a2faf2862a5746b8e`  
		Last Modified: Tue, 03 Feb 2026 02:23:17 GMT  
		Size: 25.9 KB (25932 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dbee87ee5334b36283a188f3cf02074a05dc0f5a8e87522e0bad1dc294faa119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.3 MB (658348341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a9b89ad24dd7f0b8220c53bf45afff269f4106131e8d3d87215082920779e2`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:19:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:19:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:01 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:19:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:19:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:19:03 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:19:03 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:19:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:19:05 GMT
ARG GHC=9.6.7
# Tue, 13 Jan 2026 01:19:05 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 13 Jan 2026 01:20:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56c8e381c4c548efa2e0c514882920bda51a8b40be3ae501c5cc51d496b07b9`  
		Last Modified: Tue, 13 Jan 2026 01:21:49 GMT  
		Size: 129.2 MB (129241172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97b0f71e0456e365148f4e9bf1cf16be60a084676b0d6bcaeb913f6f0a1295`  
		Last Modified: Tue, 13 Jan 2026 01:21:46 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c740a1766ee13eb7baa30438c154bc1ae83a904c9ec3a5aadbcfb465805aca`  
		Last Modified: Tue, 13 Jan 2026 01:21:45 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7038b252ae807d953a08095f4d5c04fc5036007d833f461743ad79d86bfd7beb`  
		Last Modified: Tue, 13 Jan 2026 01:21:56 GMT  
		Size: 438.3 MB (438347889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a06fcb3bba11ce5186c27d8b337d361f096075a9d0cf915bc40423b21748a9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75085a9bf66c5f32c3fdb07d1c8bc886c0d772b55dd31837eabe5057adce0c7d`

```dockerfile
```

-	Layers:
	-	`sha256:9494340f729cfe127b476597730adc09f750193cccf2475d85d86e7e51d0e2b2`  
		Last Modified: Tue, 13 Jan 2026 01:21:45 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3012246b847824d7c5f7fbe527a0687a9eb59b615e695359a7e768604be530`  
		Last Modified: Tue, 13 Jan 2026 01:21:44 GMT  
		Size: 26.1 KB (26083 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-slim`

```console
$ docker pull haskell@sha256:ba3475794a144c75ab7e47ef9302457fb35930541cb5eab21b335b24f2567836
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:430ba02e7e9ef6cdfb2331fa0885ea315e0801bd11c04329f566e0c5209a46d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590685455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da6f4f589f2df00ec6aae437ad47b181e9f0a00e63ff8de7e71bbcf7c48986c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:21:16 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:16 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:21:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:21:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:21:19 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:21:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:21:20 GMT
ARG GHC=9.6.7
# Tue, 03 Feb 2026 02:21:20 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 03 Feb 2026 02:22:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:22:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:22:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0396c7992a947bf789cdb1173e683b5dce6c8581d4e93bc14e091a93f33fce34`  
		Last Modified: Tue, 03 Feb 2026 02:24:04 GMT  
		Size: 106.4 MB (106366884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e749ca54d8dcd5bbb3dd70b0626f41b7b76b2c15e6d598edfc34bcca1ce864`  
		Last Modified: Tue, 03 Feb 2026 02:24:01 GMT  
		Size: 22.2 MB (22220747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6731b4bcdb707c127e6cea67aab24dad9a0f60572a200435579c2011e209b8e4`  
		Last Modified: Tue, 03 Feb 2026 02:24:00 GMT  
		Size: 7.6 MB (7612232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855184aa1c4b0fe6fac40c1a7880e4179566b760b68355c020c0180fd4347b80`  
		Last Modified: Tue, 03 Feb 2026 02:24:10 GMT  
		Size: 424.2 MB (424227308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:4608a720352257cd646b872e7c99d887cdd0a8e8416fdaa1bdec7af255b7e148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4b21e9743299be007a49255ccfb92d6e51ef6e6069dd95947e96f15b5119c9`

```dockerfile
```

-	Layers:
	-	`sha256:1d589f69c7e4ea13e19add1e579da955edad9f37712e8418dc5f83017ed5b9fa`  
		Last Modified: Tue, 03 Feb 2026 02:24:00 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8efcd5858463c94cc5445bf334bc876ba322e7b5bb45605b62ee72f7bdacb8c6`  
		Last Modified: Tue, 03 Feb 2026 02:23:59 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:524968482cf8bea96565dcd680b6aa54e1457b083e09a52f033815ffc2b29cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607457480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5103a12d9e967680ffe94150f39d6cddfac090d0c244f87ec02424ab506185e3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:19:06 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:19:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:06 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:19:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:19:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:19:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:19:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:19:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:19:10 GMT
ARG GHC=9.6.7
# Tue, 13 Jan 2026 01:19:10 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 13 Jan 2026 01:20:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e602d12a094731919be5a765aed515e8a3bc526d84482bad3f751ce3464ba8aa`  
		Last Modified: Tue, 13 Jan 2026 01:21:56 GMT  
		Size: 101.9 MB (101864314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771a124d8113c2f2af009067ec18dfbb39a0e53650226c1ac8555fc7552c1a83`  
		Last Modified: Tue, 13 Jan 2026 01:21:53 GMT  
		Size: 24.5 MB (24528542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb609dcf194d75684aa2a8dfa3668528c2dffd00c8346e927c7a694c9deaa51`  
		Last Modified: Tue, 13 Jan 2026 01:21:53 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2e6859d9c4163bb8d2ae7c09f6445c1f26764dd828549770661d636695ef8a`  
		Last Modified: Tue, 13 Jan 2026 01:22:02 GMT  
		Size: 438.3 MB (438343145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:0b98c6ebc4e0c6698f1da2a23ad54ae4eacee91f98f8257ddaa6c59ecc056711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264fc0d05417c95212733290610f75659c5cf4c6d3f401fb10805fd1f0a837f9`

```dockerfile
```

-	Layers:
	-	`sha256:28093510d6b14712b43b900287b7c3763e34fb77899c0c70f6d8a26fe80fdff6`  
		Last Modified: Tue, 13 Jan 2026 01:21:52 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23564d405bd95d512e585e59933f85d89465f9c3b43bdc7f51d788bdc7bf8b99`  
		Last Modified: Tue, 13 Jan 2026 01:21:51 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-slim-bullseye`

```console
$ docker pull haskell@sha256:ba3475794a144c75ab7e47ef9302457fb35930541cb5eab21b335b24f2567836
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:430ba02e7e9ef6cdfb2331fa0885ea315e0801bd11c04329f566e0c5209a46d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590685455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da6f4f589f2df00ec6aae437ad47b181e9f0a00e63ff8de7e71bbcf7c48986c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:21:16 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:16 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:21:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:21:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:21:19 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:21:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:21:20 GMT
ARG GHC=9.6.7
# Tue, 03 Feb 2026 02:21:20 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 03 Feb 2026 02:22:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:22:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:22:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0396c7992a947bf789cdb1173e683b5dce6c8581d4e93bc14e091a93f33fce34`  
		Last Modified: Tue, 03 Feb 2026 02:24:04 GMT  
		Size: 106.4 MB (106366884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e749ca54d8dcd5bbb3dd70b0626f41b7b76b2c15e6d598edfc34bcca1ce864`  
		Last Modified: Tue, 03 Feb 2026 02:24:01 GMT  
		Size: 22.2 MB (22220747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6731b4bcdb707c127e6cea67aab24dad9a0f60572a200435579c2011e209b8e4`  
		Last Modified: Tue, 03 Feb 2026 02:24:00 GMT  
		Size: 7.6 MB (7612232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855184aa1c4b0fe6fac40c1a7880e4179566b760b68355c020c0180fd4347b80`  
		Last Modified: Tue, 03 Feb 2026 02:24:10 GMT  
		Size: 424.2 MB (424227308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:4608a720352257cd646b872e7c99d887cdd0a8e8416fdaa1bdec7af255b7e148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4b21e9743299be007a49255ccfb92d6e51ef6e6069dd95947e96f15b5119c9`

```dockerfile
```

-	Layers:
	-	`sha256:1d589f69c7e4ea13e19add1e579da955edad9f37712e8418dc5f83017ed5b9fa`  
		Last Modified: Tue, 03 Feb 2026 02:24:00 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8efcd5858463c94cc5445bf334bc876ba322e7b5bb45605b62ee72f7bdacb8c6`  
		Last Modified: Tue, 03 Feb 2026 02:23:59 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:524968482cf8bea96565dcd680b6aa54e1457b083e09a52f033815ffc2b29cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607457480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5103a12d9e967680ffe94150f39d6cddfac090d0c244f87ec02424ab506185e3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:19:06 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:19:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:06 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:19:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:19:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:19:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:19:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:19:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:19:10 GMT
ARG GHC=9.6.7
# Tue, 13 Jan 2026 01:19:10 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 13 Jan 2026 01:20:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e602d12a094731919be5a765aed515e8a3bc526d84482bad3f751ce3464ba8aa`  
		Last Modified: Tue, 13 Jan 2026 01:21:56 GMT  
		Size: 101.9 MB (101864314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771a124d8113c2f2af009067ec18dfbb39a0e53650226c1ac8555fc7552c1a83`  
		Last Modified: Tue, 13 Jan 2026 01:21:53 GMT  
		Size: 24.5 MB (24528542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb609dcf194d75684aa2a8dfa3668528c2dffd00c8346e927c7a694c9deaa51`  
		Last Modified: Tue, 13 Jan 2026 01:21:53 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2e6859d9c4163bb8d2ae7c09f6445c1f26764dd828549770661d636695ef8a`  
		Last Modified: Tue, 13 Jan 2026 01:22:02 GMT  
		Size: 438.3 MB (438343145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:0b98c6ebc4e0c6698f1da2a23ad54ae4eacee91f98f8257ddaa6c59ecc056711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264fc0d05417c95212733290610f75659c5cf4c6d3f401fb10805fd1f0a837f9`

```dockerfile
```

-	Layers:
	-	`sha256:28093510d6b14712b43b900287b7c3763e34fb77899c0c70f6d8a26fe80fdff6`  
		Last Modified: Tue, 13 Jan 2026 01:21:52 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23564d405bd95d512e585e59933f85d89465f9c3b43bdc7f51d788bdc7bf8b99`  
		Last Modified: Tue, 13 Jan 2026 01:21:51 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7`

```console
$ docker pull haskell@sha256:1995ee1a0659f2a209a2d3dc85398977fb7578c8e5804b8635b57e35896b244e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7` - linux; amd64

```console
$ docker pull haskell@sha256:ef9b9a8948d4d26d3ddfc5799559da43b8b7ccde2eee63423721ea8e07f6ab10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641568569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dabf6b1346eca125437d0258efc9b82f037017d8df80b261cc498dd2dfd5fde`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.6.7
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 03 Feb 2026 02:22:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:22:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:22:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75238d6ce97658590d0e7ca1aaf30fcba7bcb5c26bbd70cd884882a7979de149`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 133.8 MB (133753898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e15615986ee567d17dab5c314e85877d951095edac5c31e416f1681e2ab9e3`  
		Last Modified: Tue, 03 Feb 2026 02:20:38 GMT  
		Size: 22.2 MB (22220752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942fd0d25d80acdb7c2774885eaa17e3d93e5dbfc722b533fd3bd38888e36cac`  
		Last Modified: Tue, 03 Feb 2026 02:23:25 GMT  
		Size: 424.2 MB (424225415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7` - unknown; unknown

```console
$ docker pull haskell@sha256:8c4fd91f6b57e3234c74f3bc6a29564222a19b831cc19bd7154dd96bcd8e5906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c2a01cad7310d78fc1119dee1c6a1fee7f9472cec94157453be6c8dab2c1ee`

```dockerfile
```

-	Layers:
	-	`sha256:0c3c982f6b1431449a371db68c3489b68e7db13b196a13e64e08415c86028a17`  
		Last Modified: Tue, 03 Feb 2026 02:23:18 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed146138c71068e69fa1c823d5d4f410bd20e5b29b6fe92a2faf2862a5746b8e`  
		Last Modified: Tue, 03 Feb 2026 02:23:17 GMT  
		Size: 25.9 KB (25932 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dbee87ee5334b36283a188f3cf02074a05dc0f5a8e87522e0bad1dc294faa119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.3 MB (658348341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a9b89ad24dd7f0b8220c53bf45afff269f4106131e8d3d87215082920779e2`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:19:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:19:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:01 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:19:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:19:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:19:03 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:19:03 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:19:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:19:05 GMT
ARG GHC=9.6.7
# Tue, 13 Jan 2026 01:19:05 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 13 Jan 2026 01:20:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56c8e381c4c548efa2e0c514882920bda51a8b40be3ae501c5cc51d496b07b9`  
		Last Modified: Tue, 13 Jan 2026 01:21:49 GMT  
		Size: 129.2 MB (129241172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97b0f71e0456e365148f4e9bf1cf16be60a084676b0d6bcaeb913f6f0a1295`  
		Last Modified: Tue, 13 Jan 2026 01:21:46 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c740a1766ee13eb7baa30438c154bc1ae83a904c9ec3a5aadbcfb465805aca`  
		Last Modified: Tue, 13 Jan 2026 01:21:45 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7038b252ae807d953a08095f4d5c04fc5036007d833f461743ad79d86bfd7beb`  
		Last Modified: Tue, 13 Jan 2026 01:21:56 GMT  
		Size: 438.3 MB (438347889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7` - unknown; unknown

```console
$ docker pull haskell@sha256:a06fcb3bba11ce5186c27d8b337d361f096075a9d0cf915bc40423b21748a9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75085a9bf66c5f32c3fdb07d1c8bc886c0d772b55dd31837eabe5057adce0c7d`

```dockerfile
```

-	Layers:
	-	`sha256:9494340f729cfe127b476597730adc09f750193cccf2475d85d86e7e51d0e2b2`  
		Last Modified: Tue, 13 Jan 2026 01:21:45 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3012246b847824d7c5f7fbe527a0687a9eb59b615e695359a7e768604be530`  
		Last Modified: Tue, 13 Jan 2026 01:21:44 GMT  
		Size: 26.1 KB (26083 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-bullseye`

```console
$ docker pull haskell@sha256:1995ee1a0659f2a209a2d3dc85398977fb7578c8e5804b8635b57e35896b244e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:ef9b9a8948d4d26d3ddfc5799559da43b8b7ccde2eee63423721ea8e07f6ab10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641568569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dabf6b1346eca125437d0258efc9b82f037017d8df80b261cc498dd2dfd5fde`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.6.7
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 03 Feb 2026 02:22:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:22:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:22:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75238d6ce97658590d0e7ca1aaf30fcba7bcb5c26bbd70cd884882a7979de149`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 133.8 MB (133753898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e15615986ee567d17dab5c314e85877d951095edac5c31e416f1681e2ab9e3`  
		Last Modified: Tue, 03 Feb 2026 02:20:38 GMT  
		Size: 22.2 MB (22220752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942fd0d25d80acdb7c2774885eaa17e3d93e5dbfc722b533fd3bd38888e36cac`  
		Last Modified: Tue, 03 Feb 2026 02:23:25 GMT  
		Size: 424.2 MB (424225415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:8c4fd91f6b57e3234c74f3bc6a29564222a19b831cc19bd7154dd96bcd8e5906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97c2a01cad7310d78fc1119dee1c6a1fee7f9472cec94157453be6c8dab2c1ee`

```dockerfile
```

-	Layers:
	-	`sha256:0c3c982f6b1431449a371db68c3489b68e7db13b196a13e64e08415c86028a17`  
		Last Modified: Tue, 03 Feb 2026 02:23:18 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed146138c71068e69fa1c823d5d4f410bd20e5b29b6fe92a2faf2862a5746b8e`  
		Last Modified: Tue, 03 Feb 2026 02:23:17 GMT  
		Size: 25.9 KB (25932 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dbee87ee5334b36283a188f3cf02074a05dc0f5a8e87522e0bad1dc294faa119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.3 MB (658348341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a9b89ad24dd7f0b8220c53bf45afff269f4106131e8d3d87215082920779e2`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:19:01 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:19:01 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:01 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:19:01 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:19:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:19:03 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:19:03 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:19:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:19:05 GMT
ARG GHC=9.6.7
# Tue, 13 Jan 2026 01:19:05 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 13 Jan 2026 01:20:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56c8e381c4c548efa2e0c514882920bda51a8b40be3ae501c5cc51d496b07b9`  
		Last Modified: Tue, 13 Jan 2026 01:21:49 GMT  
		Size: 129.2 MB (129241172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b97b0f71e0456e365148f4e9bf1cf16be60a084676b0d6bcaeb913f6f0a1295`  
		Last Modified: Tue, 13 Jan 2026 01:21:46 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c740a1766ee13eb7baa30438c154bc1ae83a904c9ec3a5aadbcfb465805aca`  
		Last Modified: Tue, 13 Jan 2026 01:21:45 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7038b252ae807d953a08095f4d5c04fc5036007d833f461743ad79d86bfd7beb`  
		Last Modified: Tue, 13 Jan 2026 01:21:56 GMT  
		Size: 438.3 MB (438347889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a06fcb3bba11ce5186c27d8b337d361f096075a9d0cf915bc40423b21748a9f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75085a9bf66c5f32c3fdb07d1c8bc886c0d772b55dd31837eabe5057adce0c7d`

```dockerfile
```

-	Layers:
	-	`sha256:9494340f729cfe127b476597730adc09f750193cccf2475d85d86e7e51d0e2b2`  
		Last Modified: Tue, 13 Jan 2026 01:21:45 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d3012246b847824d7c5f7fbe527a0687a9eb59b615e695359a7e768604be530`  
		Last Modified: Tue, 13 Jan 2026 01:21:44 GMT  
		Size: 26.1 KB (26083 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-slim`

```console
$ docker pull haskell@sha256:ba3475794a144c75ab7e47ef9302457fb35930541cb5eab21b335b24f2567836
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-slim` - linux; amd64

```console
$ docker pull haskell@sha256:430ba02e7e9ef6cdfb2331fa0885ea315e0801bd11c04329f566e0c5209a46d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590685455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da6f4f589f2df00ec6aae437ad47b181e9f0a00e63ff8de7e71bbcf7c48986c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:21:16 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:16 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:21:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:21:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:21:19 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:21:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:21:20 GMT
ARG GHC=9.6.7
# Tue, 03 Feb 2026 02:21:20 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 03 Feb 2026 02:22:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:22:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:22:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0396c7992a947bf789cdb1173e683b5dce6c8581d4e93bc14e091a93f33fce34`  
		Last Modified: Tue, 03 Feb 2026 02:24:04 GMT  
		Size: 106.4 MB (106366884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e749ca54d8dcd5bbb3dd70b0626f41b7b76b2c15e6d598edfc34bcca1ce864`  
		Last Modified: Tue, 03 Feb 2026 02:24:01 GMT  
		Size: 22.2 MB (22220747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6731b4bcdb707c127e6cea67aab24dad9a0f60572a200435579c2011e209b8e4`  
		Last Modified: Tue, 03 Feb 2026 02:24:00 GMT  
		Size: 7.6 MB (7612232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855184aa1c4b0fe6fac40c1a7880e4179566b760b68355c020c0180fd4347b80`  
		Last Modified: Tue, 03 Feb 2026 02:24:10 GMT  
		Size: 424.2 MB (424227308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:4608a720352257cd646b872e7c99d887cdd0a8e8416fdaa1bdec7af255b7e148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4b21e9743299be007a49255ccfb92d6e51ef6e6069dd95947e96f15b5119c9`

```dockerfile
```

-	Layers:
	-	`sha256:1d589f69c7e4ea13e19add1e579da955edad9f37712e8418dc5f83017ed5b9fa`  
		Last Modified: Tue, 03 Feb 2026 02:24:00 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8efcd5858463c94cc5445bf334bc876ba322e7b5bb45605b62ee72f7bdacb8c6`  
		Last Modified: Tue, 03 Feb 2026 02:23:59 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:524968482cf8bea96565dcd680b6aa54e1457b083e09a52f033815ffc2b29cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607457480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5103a12d9e967680ffe94150f39d6cddfac090d0c244f87ec02424ab506185e3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:19:06 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:19:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:06 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:19:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:19:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:19:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:19:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:19:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:19:10 GMT
ARG GHC=9.6.7
# Tue, 13 Jan 2026 01:19:10 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 13 Jan 2026 01:20:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e602d12a094731919be5a765aed515e8a3bc526d84482bad3f751ce3464ba8aa`  
		Last Modified: Tue, 13 Jan 2026 01:21:56 GMT  
		Size: 101.9 MB (101864314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771a124d8113c2f2af009067ec18dfbb39a0e53650226c1ac8555fc7552c1a83`  
		Last Modified: Tue, 13 Jan 2026 01:21:53 GMT  
		Size: 24.5 MB (24528542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb609dcf194d75684aa2a8dfa3668528c2dffd00c8346e927c7a694c9deaa51`  
		Last Modified: Tue, 13 Jan 2026 01:21:53 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2e6859d9c4163bb8d2ae7c09f6445c1f26764dd828549770661d636695ef8a`  
		Last Modified: Tue, 13 Jan 2026 01:22:02 GMT  
		Size: 438.3 MB (438343145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:0b98c6ebc4e0c6698f1da2a23ad54ae4eacee91f98f8257ddaa6c59ecc056711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264fc0d05417c95212733290610f75659c5cf4c6d3f401fb10805fd1f0a837f9`

```dockerfile
```

-	Layers:
	-	`sha256:28093510d6b14712b43b900287b7c3763e34fb77899c0c70f6d8a26fe80fdff6`  
		Last Modified: Tue, 13 Jan 2026 01:21:52 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23564d405bd95d512e585e59933f85d89465f9c3b43bdc7f51d788bdc7bf8b99`  
		Last Modified: Tue, 13 Jan 2026 01:21:51 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-slim-bullseye`

```console
$ docker pull haskell@sha256:ba3475794a144c75ab7e47ef9302457fb35930541cb5eab21b335b24f2567836
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:430ba02e7e9ef6cdfb2331fa0885ea315e0801bd11c04329f566e0c5209a46d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590685455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5da6f4f589f2df00ec6aae437ad47b181e9f0a00e63ff8de7e71bbcf7c48986c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:21:16 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:21:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:21:16 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:21:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:21:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:21:19 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:21:19 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:21:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:21:20 GMT
ARG GHC=9.6.7
# Tue, 03 Feb 2026 02:21:20 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 03 Feb 2026 02:22:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:22:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:22:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0396c7992a947bf789cdb1173e683b5dce6c8581d4e93bc14e091a93f33fce34`  
		Last Modified: Tue, 03 Feb 2026 02:24:04 GMT  
		Size: 106.4 MB (106366884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e749ca54d8dcd5bbb3dd70b0626f41b7b76b2c15e6d598edfc34bcca1ce864`  
		Last Modified: Tue, 03 Feb 2026 02:24:01 GMT  
		Size: 22.2 MB (22220747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6731b4bcdb707c127e6cea67aab24dad9a0f60572a200435579c2011e209b8e4`  
		Last Modified: Tue, 03 Feb 2026 02:24:00 GMT  
		Size: 7.6 MB (7612232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855184aa1c4b0fe6fac40c1a7880e4179566b760b68355c020c0180fd4347b80`  
		Last Modified: Tue, 03 Feb 2026 02:24:10 GMT  
		Size: 424.2 MB (424227308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:4608a720352257cd646b872e7c99d887cdd0a8e8416fdaa1bdec7af255b7e148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e4b21e9743299be007a49255ccfb92d6e51ef6e6069dd95947e96f15b5119c9`

```dockerfile
```

-	Layers:
	-	`sha256:1d589f69c7e4ea13e19add1e579da955edad9f37712e8418dc5f83017ed5b9fa`  
		Last Modified: Tue, 03 Feb 2026 02:24:00 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8efcd5858463c94cc5445bf334bc876ba322e7b5bb45605b62ee72f7bdacb8c6`  
		Last Modified: Tue, 03 Feb 2026 02:23:59 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:524968482cf8bea96565dcd680b6aa54e1457b083e09a52f033815ffc2b29cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607457480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5103a12d9e967680ffe94150f39d6cddfac090d0c244f87ec02424ab506185e3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:19:06 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:19:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:19:06 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:19:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:19:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:19:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:19:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:19:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:19:10 GMT
ARG GHC=9.6.7
# Tue, 13 Jan 2026 01:19:10 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 13 Jan 2026 01:20:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e602d12a094731919be5a765aed515e8a3bc526d84482bad3f751ce3464ba8aa`  
		Last Modified: Tue, 13 Jan 2026 01:21:56 GMT  
		Size: 101.9 MB (101864314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:771a124d8113c2f2af009067ec18dfbb39a0e53650226c1ac8555fc7552c1a83`  
		Last Modified: Tue, 13 Jan 2026 01:21:53 GMT  
		Size: 24.5 MB (24528542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb609dcf194d75684aa2a8dfa3668528c2dffd00c8346e927c7a694c9deaa51`  
		Last Modified: Tue, 13 Jan 2026 01:21:53 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2e6859d9c4163bb8d2ae7c09f6445c1f26764dd828549770661d636695ef8a`  
		Last Modified: Tue, 13 Jan 2026 01:22:02 GMT  
		Size: 438.3 MB (438343145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:0b98c6ebc4e0c6698f1da2a23ad54ae4eacee91f98f8257ddaa6c59ecc056711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264fc0d05417c95212733290610f75659c5cf4c6d3f401fb10805fd1f0a837f9`

```dockerfile
```

-	Layers:
	-	`sha256:28093510d6b14712b43b900287b7c3763e34fb77899c0c70f6d8a26fe80fdff6`  
		Last Modified: Tue, 13 Jan 2026 01:21:52 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23564d405bd95d512e585e59933f85d89465f9c3b43bdc7f51d788bdc7bf8b99`  
		Last Modified: Tue, 13 Jan 2026 01:21:51 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8`

```console
$ docker pull haskell@sha256:6948a24d07e4d8287d8f2d2e065e4fd573a7234677286b51f9d82d132d9d5890
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8` - linux; amd64

```console
$ docker pull haskell@sha256:55c49aeda7e5fe2d5709bafa500e60c4070dd941460421a59c2e5c77ddc80669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653558875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca960cf3f599a243493658912e774ed256e13d5081f2cad5e504a087ab43534`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:18:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:18:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:00 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:18:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:18:02 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:18:02 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:18:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:18:03 GMT
ARG GHC=9.8.4
# Tue, 03 Feb 2026 02:18:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ef41ec6c3b696a25a3fe020c2ab8b2a20cbbf118e92f522d64d0cc483b37b6`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 133.8 MB (133754173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66d7d3f6793fa144613370ea477f98271153e4f0041ca2c93105c993daa9e9`  
		Last Modified: Tue, 03 Feb 2026 02:20:42 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c99fc38e6aa71efbdb6c31fb2bf21975eba456885923353df1b28d20371647a`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 7.6 MB (7612226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb4c3bbe411c434e073e722f545be22b08ca0152ce3a90aafa8947cb0fad6d`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 436.2 MB (436215466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8` - unknown; unknown

```console
$ docker pull haskell@sha256:482e7f550ed71088390095f4d4ebeafedd950d450cd83cc00d3aa90d204c1c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1521905bb67faeca7e39939249a17e64e53af9ca1944ee0ac110f30a50be71dc`

```dockerfile
```

-	Layers:
	-	`sha256:a139e95214e07775a10bb21aac311570e88c686ee27532a95ce61ab4ba38de52`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf6d6745b91934447e6e9e85f187bb18e65fa879a5c9d225a500328f64975fb`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 25.7 KB (25653 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:40f54e790d1e900941ea0394f78cfc7ba667ff7d3a9433c20b25ae4a82b90651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663797900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4c64f1a8af6487778ee3b31198f52130a50b204729e67a3d74d6ef1b385264`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:27 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:27 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:27 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:29 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:29 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC=9.8.4
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:19:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:19:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1964549c3237b9988e0cf9a24568d4eb660de7215966cddbb6b5a13dd484d13`  
		Last Modified: Tue, 13 Jan 2026 01:21:19 GMT  
		Size: 129.2 MB (129240846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cb002fe691ce07613312777e22a8c64292d69f4813c2e5a893f925e9be318b`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 24.5 MB (24528548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb39a72843976163048a101d67acc696b91e09c912f82db26b3cb2793d23db6`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f779d6887af22e2729c834d73d78bbc1a385329a326e700b9784a53ff8e2c`  
		Last Modified: Tue, 13 Jan 2026 01:21:26 GMT  
		Size: 443.8 MB (443797777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8` - unknown; unknown

```console
$ docker pull haskell@sha256:da12da9c9825c5cb9a45f8ae9b8e76b1d297f8ce21d84ec6abf9b00acaabba6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0529dcc3fcb71cb36556ca363c82c41217da9bad0c38076b14a78af19119c0d`

```dockerfile
```

-	Layers:
	-	`sha256:aa4cc35bb0000f6e2e0c340e1ef07c3ae8834a7d47017e8522d7d768469bdea1`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5b564712b92012adf69c114f661e943c75ed384fc522918923f5170770d6cf`  
		Last Modified: Tue, 13 Jan 2026 01:21:13 GMT  
		Size: 25.8 KB (25804 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-bullseye`

```console
$ docker pull haskell@sha256:6948a24d07e4d8287d8f2d2e065e4fd573a7234677286b51f9d82d132d9d5890
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:55c49aeda7e5fe2d5709bafa500e60c4070dd941460421a59c2e5c77ddc80669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653558875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca960cf3f599a243493658912e774ed256e13d5081f2cad5e504a087ab43534`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:18:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:18:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:00 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:18:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:18:02 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:18:02 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:18:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:18:03 GMT
ARG GHC=9.8.4
# Tue, 03 Feb 2026 02:18:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ef41ec6c3b696a25a3fe020c2ab8b2a20cbbf118e92f522d64d0cc483b37b6`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 133.8 MB (133754173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66d7d3f6793fa144613370ea477f98271153e4f0041ca2c93105c993daa9e9`  
		Last Modified: Tue, 03 Feb 2026 02:20:42 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c99fc38e6aa71efbdb6c31fb2bf21975eba456885923353df1b28d20371647a`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 7.6 MB (7612226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb4c3bbe411c434e073e722f545be22b08ca0152ce3a90aafa8947cb0fad6d`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 436.2 MB (436215466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:482e7f550ed71088390095f4d4ebeafedd950d450cd83cc00d3aa90d204c1c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1521905bb67faeca7e39939249a17e64e53af9ca1944ee0ac110f30a50be71dc`

```dockerfile
```

-	Layers:
	-	`sha256:a139e95214e07775a10bb21aac311570e88c686ee27532a95ce61ab4ba38de52`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf6d6745b91934447e6e9e85f187bb18e65fa879a5c9d225a500328f64975fb`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 25.7 KB (25653 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:40f54e790d1e900941ea0394f78cfc7ba667ff7d3a9433c20b25ae4a82b90651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663797900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4c64f1a8af6487778ee3b31198f52130a50b204729e67a3d74d6ef1b385264`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:27 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:27 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:27 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:29 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:29 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC=9.8.4
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:19:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:19:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1964549c3237b9988e0cf9a24568d4eb660de7215966cddbb6b5a13dd484d13`  
		Last Modified: Tue, 13 Jan 2026 01:21:19 GMT  
		Size: 129.2 MB (129240846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cb002fe691ce07613312777e22a8c64292d69f4813c2e5a893f925e9be318b`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 24.5 MB (24528548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb39a72843976163048a101d67acc696b91e09c912f82db26b3cb2793d23db6`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f779d6887af22e2729c834d73d78bbc1a385329a326e700b9784a53ff8e2c`  
		Last Modified: Tue, 13 Jan 2026 01:21:26 GMT  
		Size: 443.8 MB (443797777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:da12da9c9825c5cb9a45f8ae9b8e76b1d297f8ce21d84ec6abf9b00acaabba6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0529dcc3fcb71cb36556ca363c82c41217da9bad0c38076b14a78af19119c0d`

```dockerfile
```

-	Layers:
	-	`sha256:aa4cc35bb0000f6e2e0c340e1ef07c3ae8834a7d47017e8522d7d768469bdea1`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5b564712b92012adf69c114f661e943c75ed384fc522918923f5170770d6cf`  
		Last Modified: Tue, 13 Jan 2026 01:21:13 GMT  
		Size: 25.8 KB (25804 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-slim`

```console
$ docker pull haskell@sha256:f5753309d67b2b68d2a7970d1e5d44b70044f89f1efd0e9caa9426968e8144da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:a338b8731512af9f2e6214b036826590a37db2980309f404263856d8d6665c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602675048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7b8266eb82f541ab5e1a2b5f1e1f770f36bfad78b4a1cb467d2b8894ff8210`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:18 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:20:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:20:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:20:21 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:20:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:20:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:20:22 GMT
ARG GHC=9.8.4
# Tue, 03 Feb 2026 02:20:22 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:21:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:21:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:21:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2039578beff5636bcf8d1b7f9769caaf40d289945e5e9e9717708d10e328d44`  
		Last Modified: Tue, 03 Feb 2026 02:23:13 GMT  
		Size: 106.4 MB (106366818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2756e75d1d2d4df35d71912adb330d100b933509d142e5f6a6f5c9987de1a8f`  
		Last Modified: Tue, 03 Feb 2026 02:23:09 GMT  
		Size: 22.2 MB (22220737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1820376bd763e408f27c30dd87f579a6f38438fcd920dd11ad8721f41e285573`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f9fbb55f749546b39eceb821411bf56ecc9303472e30aa66386d636441eedd`  
		Last Modified: Tue, 03 Feb 2026 02:23:22 GMT  
		Size: 436.2 MB (436216976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:9845cb92af4296a6101abe82ff915a63c715f39e4849048b388f8037b36c8502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f1f861899acc68cd6deea7b6bd383be16c70754c766b1e46191572b01460fd`

```dockerfile
```

-	Layers:
	-	`sha256:178b2668aaa0baacde2a2516b7b805d791a2928ab550439740b1cdded82d78c4`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d847d8ae0cda6aae76eef92b096dde65f137b136c81ec4b71f8fff92232f78b4`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:0eeed44918a6ca5aeece943e2403f441b758454bc1bd88a7896746d641b7f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612913448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fcfb710e956080a54770d2c2f52f36490b14a8c5d4ce5a12bbc8d7f8296ddd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:45 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:45 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:47 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:47 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:48 GMT
ARG GHC=9.8.4
# Tue, 13 Jan 2026 01:18:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:20:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2139cfff3814561bd4e3b79c5bf4007efe6dd0c1dc087cd909a1fffad2ba8d3`  
		Last Modified: Tue, 13 Jan 2026 01:21:32 GMT  
		Size: 101.9 MB (101864067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac05cf83330bc2926b2df571891e74c490737237279915967146c50c60101b8`  
		Last Modified: Tue, 13 Jan 2026 01:21:29 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3d0bf2d77ae7f41a7d1729d3120a9efa034610ab144cd96a1d1159a2395f48`  
		Last Modified: Tue, 13 Jan 2026 01:21:28 GMT  
		Size: 14.0 MB (13972962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56176152ccf0719db62bcb47bc6c69c92ff8281466e958ec3156325605c6ea22`  
		Last Modified: Tue, 13 Jan 2026 01:21:39 GMT  
		Size: 443.8 MB (443799354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:24c37ec8e855210dc58c362fe80a4418cc527175d7d7bcc0e7dc6410d76778d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e5ef18b24ba15f487d96da7ae375414276bd6e1e3484c93040a4f005f0f8f7`

```dockerfile
```

-	Layers:
	-	`sha256:229a4aa92f9300eedecb5d771f52078c4171e43ab34901786df3a37689fe5021`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c16259cbf1dcafafca5ca7291c6c4bb61e17b7fe0ec90713095a791f1ac908`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-slim-bullseye`

```console
$ docker pull haskell@sha256:f5753309d67b2b68d2a7970d1e5d44b70044f89f1efd0e9caa9426968e8144da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:a338b8731512af9f2e6214b036826590a37db2980309f404263856d8d6665c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602675048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7b8266eb82f541ab5e1a2b5f1e1f770f36bfad78b4a1cb467d2b8894ff8210`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:18 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:20:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:20:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:20:21 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:20:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:20:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:20:22 GMT
ARG GHC=9.8.4
# Tue, 03 Feb 2026 02:20:22 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:21:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:21:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:21:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2039578beff5636bcf8d1b7f9769caaf40d289945e5e9e9717708d10e328d44`  
		Last Modified: Tue, 03 Feb 2026 02:23:13 GMT  
		Size: 106.4 MB (106366818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2756e75d1d2d4df35d71912adb330d100b933509d142e5f6a6f5c9987de1a8f`  
		Last Modified: Tue, 03 Feb 2026 02:23:09 GMT  
		Size: 22.2 MB (22220737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1820376bd763e408f27c30dd87f579a6f38438fcd920dd11ad8721f41e285573`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f9fbb55f749546b39eceb821411bf56ecc9303472e30aa66386d636441eedd`  
		Last Modified: Tue, 03 Feb 2026 02:23:22 GMT  
		Size: 436.2 MB (436216976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:9845cb92af4296a6101abe82ff915a63c715f39e4849048b388f8037b36c8502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f1f861899acc68cd6deea7b6bd383be16c70754c766b1e46191572b01460fd`

```dockerfile
```

-	Layers:
	-	`sha256:178b2668aaa0baacde2a2516b7b805d791a2928ab550439740b1cdded82d78c4`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d847d8ae0cda6aae76eef92b096dde65f137b136c81ec4b71f8fff92232f78b4`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:0eeed44918a6ca5aeece943e2403f441b758454bc1bd88a7896746d641b7f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612913448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fcfb710e956080a54770d2c2f52f36490b14a8c5d4ce5a12bbc8d7f8296ddd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:45 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:45 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:47 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:47 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:48 GMT
ARG GHC=9.8.4
# Tue, 13 Jan 2026 01:18:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:20:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2139cfff3814561bd4e3b79c5bf4007efe6dd0c1dc087cd909a1fffad2ba8d3`  
		Last Modified: Tue, 13 Jan 2026 01:21:32 GMT  
		Size: 101.9 MB (101864067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac05cf83330bc2926b2df571891e74c490737237279915967146c50c60101b8`  
		Last Modified: Tue, 13 Jan 2026 01:21:29 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3d0bf2d77ae7f41a7d1729d3120a9efa034610ab144cd96a1d1159a2395f48`  
		Last Modified: Tue, 13 Jan 2026 01:21:28 GMT  
		Size: 14.0 MB (13972962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56176152ccf0719db62bcb47bc6c69c92ff8281466e958ec3156325605c6ea22`  
		Last Modified: Tue, 13 Jan 2026 01:21:39 GMT  
		Size: 443.8 MB (443799354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:24c37ec8e855210dc58c362fe80a4418cc527175d7d7bcc0e7dc6410d76778d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e5ef18b24ba15f487d96da7ae375414276bd6e1e3484c93040a4f005f0f8f7`

```dockerfile
```

-	Layers:
	-	`sha256:229a4aa92f9300eedecb5d771f52078c4171e43ab34901786df3a37689fe5021`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c16259cbf1dcafafca5ca7291c6c4bb61e17b7fe0ec90713095a791f1ac908`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4`

```console
$ docker pull haskell@sha256:6948a24d07e4d8287d8f2d2e065e4fd573a7234677286b51f9d82d132d9d5890
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4` - linux; amd64

```console
$ docker pull haskell@sha256:55c49aeda7e5fe2d5709bafa500e60c4070dd941460421a59c2e5c77ddc80669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653558875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca960cf3f599a243493658912e774ed256e13d5081f2cad5e504a087ab43534`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:18:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:18:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:00 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:18:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:18:02 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:18:02 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:18:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:18:03 GMT
ARG GHC=9.8.4
# Tue, 03 Feb 2026 02:18:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ef41ec6c3b696a25a3fe020c2ab8b2a20cbbf118e92f522d64d0cc483b37b6`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 133.8 MB (133754173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66d7d3f6793fa144613370ea477f98271153e4f0041ca2c93105c993daa9e9`  
		Last Modified: Tue, 03 Feb 2026 02:20:42 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c99fc38e6aa71efbdb6c31fb2bf21975eba456885923353df1b28d20371647a`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 7.6 MB (7612226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb4c3bbe411c434e073e722f545be22b08ca0152ce3a90aafa8947cb0fad6d`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 436.2 MB (436215466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4` - unknown; unknown

```console
$ docker pull haskell@sha256:482e7f550ed71088390095f4d4ebeafedd950d450cd83cc00d3aa90d204c1c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1521905bb67faeca7e39939249a17e64e53af9ca1944ee0ac110f30a50be71dc`

```dockerfile
```

-	Layers:
	-	`sha256:a139e95214e07775a10bb21aac311570e88c686ee27532a95ce61ab4ba38de52`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf6d6745b91934447e6e9e85f187bb18e65fa879a5c9d225a500328f64975fb`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 25.7 KB (25653 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:40f54e790d1e900941ea0394f78cfc7ba667ff7d3a9433c20b25ae4a82b90651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663797900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4c64f1a8af6487778ee3b31198f52130a50b204729e67a3d74d6ef1b385264`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:27 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:27 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:27 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:29 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:29 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC=9.8.4
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:19:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:19:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1964549c3237b9988e0cf9a24568d4eb660de7215966cddbb6b5a13dd484d13`  
		Last Modified: Tue, 13 Jan 2026 01:21:19 GMT  
		Size: 129.2 MB (129240846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cb002fe691ce07613312777e22a8c64292d69f4813c2e5a893f925e9be318b`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 24.5 MB (24528548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb39a72843976163048a101d67acc696b91e09c912f82db26b3cb2793d23db6`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f779d6887af22e2729c834d73d78bbc1a385329a326e700b9784a53ff8e2c`  
		Last Modified: Tue, 13 Jan 2026 01:21:26 GMT  
		Size: 443.8 MB (443797777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4` - unknown; unknown

```console
$ docker pull haskell@sha256:da12da9c9825c5cb9a45f8ae9b8e76b1d297f8ce21d84ec6abf9b00acaabba6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0529dcc3fcb71cb36556ca363c82c41217da9bad0c38076b14a78af19119c0d`

```dockerfile
```

-	Layers:
	-	`sha256:aa4cc35bb0000f6e2e0c340e1ef07c3ae8834a7d47017e8522d7d768469bdea1`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5b564712b92012adf69c114f661e943c75ed384fc522918923f5170770d6cf`  
		Last Modified: Tue, 13 Jan 2026 01:21:13 GMT  
		Size: 25.8 KB (25804 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-bullseye`

```console
$ docker pull haskell@sha256:6948a24d07e4d8287d8f2d2e065e4fd573a7234677286b51f9d82d132d9d5890
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:55c49aeda7e5fe2d5709bafa500e60c4070dd941460421a59c2e5c77ddc80669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653558875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ca960cf3f599a243493658912e774ed256e13d5081f2cad5e504a087ab43534`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:18:00 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:18:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:18:00 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:18:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:18:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:18:02 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:18:02 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:18:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:18:03 GMT
ARG GHC=9.8.4
# Tue, 03 Feb 2026 02:18:03 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ef41ec6c3b696a25a3fe020c2ab8b2a20cbbf118e92f522d64d0cc483b37b6`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 133.8 MB (133754173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b66d7d3f6793fa144613370ea477f98271153e4f0041ca2c93105c993daa9e9`  
		Last Modified: Tue, 03 Feb 2026 02:20:42 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c99fc38e6aa71efbdb6c31fb2bf21975eba456885923353df1b28d20371647a`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 7.6 MB (7612226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb4c3bbe411c434e073e722f545be22b08ca0152ce3a90aafa8947cb0fad6d`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 436.2 MB (436215466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:482e7f550ed71088390095f4d4ebeafedd950d450cd83cc00d3aa90d204c1c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1521905bb67faeca7e39939249a17e64e53af9ca1944ee0ac110f30a50be71dc`

```dockerfile
```

-	Layers:
	-	`sha256:a139e95214e07775a10bb21aac311570e88c686ee27532a95ce61ab4ba38de52`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bf6d6745b91934447e6e9e85f187bb18e65fa879a5c9d225a500328f64975fb`  
		Last Modified: Tue, 03 Feb 2026 02:20:40 GMT  
		Size: 25.7 KB (25653 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:40f54e790d1e900941ea0394f78cfc7ba667ff7d3a9433c20b25ae4a82b90651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663797900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4c64f1a8af6487778ee3b31198f52130a50b204729e67a3d74d6ef1b385264`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:27 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:27 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:27 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:29 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:29 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC=9.8.4
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:19:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:19:56 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:56 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1964549c3237b9988e0cf9a24568d4eb660de7215966cddbb6b5a13dd484d13`  
		Last Modified: Tue, 13 Jan 2026 01:21:19 GMT  
		Size: 129.2 MB (129240846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0cb002fe691ce07613312777e22a8c64292d69f4813c2e5a893f925e9be318b`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 24.5 MB (24528548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb39a72843976163048a101d67acc696b91e09c912f82db26b3cb2793d23db6`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8f779d6887af22e2729c834d73d78bbc1a385329a326e700b9784a53ff8e2c`  
		Last Modified: Tue, 13 Jan 2026 01:21:26 GMT  
		Size: 443.8 MB (443797777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:da12da9c9825c5cb9a45f8ae9b8e76b1d297f8ce21d84ec6abf9b00acaabba6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0529dcc3fcb71cb36556ca363c82c41217da9bad0c38076b14a78af19119c0d`

```dockerfile
```

-	Layers:
	-	`sha256:aa4cc35bb0000f6e2e0c340e1ef07c3ae8834a7d47017e8522d7d768469bdea1`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d5b564712b92012adf69c114f661e943c75ed384fc522918923f5170770d6cf`  
		Last Modified: Tue, 13 Jan 2026 01:21:13 GMT  
		Size: 25.8 KB (25804 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-slim`

```console
$ docker pull haskell@sha256:f5753309d67b2b68d2a7970d1e5d44b70044f89f1efd0e9caa9426968e8144da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-slim` - linux; amd64

```console
$ docker pull haskell@sha256:a338b8731512af9f2e6214b036826590a37db2980309f404263856d8d6665c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602675048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7b8266eb82f541ab5e1a2b5f1e1f770f36bfad78b4a1cb467d2b8894ff8210`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:18 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:20:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:20:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:20:21 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:20:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:20:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:20:22 GMT
ARG GHC=9.8.4
# Tue, 03 Feb 2026 02:20:22 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:21:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:21:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:21:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2039578beff5636bcf8d1b7f9769caaf40d289945e5e9e9717708d10e328d44`  
		Last Modified: Tue, 03 Feb 2026 02:23:13 GMT  
		Size: 106.4 MB (106366818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2756e75d1d2d4df35d71912adb330d100b933509d142e5f6a6f5c9987de1a8f`  
		Last Modified: Tue, 03 Feb 2026 02:23:09 GMT  
		Size: 22.2 MB (22220737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1820376bd763e408f27c30dd87f579a6f38438fcd920dd11ad8721f41e285573`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f9fbb55f749546b39eceb821411bf56ecc9303472e30aa66386d636441eedd`  
		Last Modified: Tue, 03 Feb 2026 02:23:22 GMT  
		Size: 436.2 MB (436216976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:9845cb92af4296a6101abe82ff915a63c715f39e4849048b388f8037b36c8502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f1f861899acc68cd6deea7b6bd383be16c70754c766b1e46191572b01460fd`

```dockerfile
```

-	Layers:
	-	`sha256:178b2668aaa0baacde2a2516b7b805d791a2928ab550439740b1cdded82d78c4`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d847d8ae0cda6aae76eef92b096dde65f137b136c81ec4b71f8fff92232f78b4`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:0eeed44918a6ca5aeece943e2403f441b758454bc1bd88a7896746d641b7f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612913448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fcfb710e956080a54770d2c2f52f36490b14a8c5d4ce5a12bbc8d7f8296ddd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:45 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:45 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:47 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:47 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:48 GMT
ARG GHC=9.8.4
# Tue, 13 Jan 2026 01:18:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:20:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2139cfff3814561bd4e3b79c5bf4007efe6dd0c1dc087cd909a1fffad2ba8d3`  
		Last Modified: Tue, 13 Jan 2026 01:21:32 GMT  
		Size: 101.9 MB (101864067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac05cf83330bc2926b2df571891e74c490737237279915967146c50c60101b8`  
		Last Modified: Tue, 13 Jan 2026 01:21:29 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3d0bf2d77ae7f41a7d1729d3120a9efa034610ab144cd96a1d1159a2395f48`  
		Last Modified: Tue, 13 Jan 2026 01:21:28 GMT  
		Size: 14.0 MB (13972962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56176152ccf0719db62bcb47bc6c69c92ff8281466e958ec3156325605c6ea22`  
		Last Modified: Tue, 13 Jan 2026 01:21:39 GMT  
		Size: 443.8 MB (443799354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:24c37ec8e855210dc58c362fe80a4418cc527175d7d7bcc0e7dc6410d76778d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e5ef18b24ba15f487d96da7ae375414276bd6e1e3484c93040a4f005f0f8f7`

```dockerfile
```

-	Layers:
	-	`sha256:229a4aa92f9300eedecb5d771f52078c4171e43ab34901786df3a37689fe5021`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c16259cbf1dcafafca5ca7291c6c4bb61e17b7fe0ec90713095a791f1ac908`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-slim-bullseye`

```console
$ docker pull haskell@sha256:f5753309d67b2b68d2a7970d1e5d44b70044f89f1efd0e9caa9426968e8144da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:a338b8731512af9f2e6214b036826590a37db2980309f404263856d8d6665c8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602675048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c7b8266eb82f541ab5e1a2b5f1e1f770f36bfad78b4a1cb467d2b8894ff8210`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:20:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:20:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:20:18 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:20:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:20:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:20:21 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:20:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:20:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:20:22 GMT
ARG GHC=9.8.4
# Tue, 03 Feb 2026 02:20:22 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 03 Feb 2026 02:21:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:21:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:21:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2039578beff5636bcf8d1b7f9769caaf40d289945e5e9e9717708d10e328d44`  
		Last Modified: Tue, 03 Feb 2026 02:23:13 GMT  
		Size: 106.4 MB (106366818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2756e75d1d2d4df35d71912adb330d100b933509d142e5f6a6f5c9987de1a8f`  
		Last Modified: Tue, 03 Feb 2026 02:23:09 GMT  
		Size: 22.2 MB (22220737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1820376bd763e408f27c30dd87f579a6f38438fcd920dd11ad8721f41e285573`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 7.6 MB (7612233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f9fbb55f749546b39eceb821411bf56ecc9303472e30aa66386d636441eedd`  
		Last Modified: Tue, 03 Feb 2026 02:23:22 GMT  
		Size: 436.2 MB (436216976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:9845cb92af4296a6101abe82ff915a63c715f39e4849048b388f8037b36c8502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f1f861899acc68cd6deea7b6bd383be16c70754c766b1e46191572b01460fd`

```dockerfile
```

-	Layers:
	-	`sha256:178b2668aaa0baacde2a2516b7b805d791a2928ab550439740b1cdded82d78c4`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d847d8ae0cda6aae76eef92b096dde65f137b136c81ec4b71f8fff92232f78b4`  
		Last Modified: Tue, 03 Feb 2026 02:23:08 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:0eeed44918a6ca5aeece943e2403f441b758454bc1bd88a7896746d641b7f951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612913448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fcfb710e956080a54770d2c2f52f36490b14a8c5d4ce5a12bbc8d7f8296ddd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:45 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:45 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:47 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:47 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:48 GMT
ARG GHC=9.8.4
# Tue, 13 Jan 2026 01:18:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 13 Jan 2026 01:20:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:12 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:12 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2139cfff3814561bd4e3b79c5bf4007efe6dd0c1dc087cd909a1fffad2ba8d3`  
		Last Modified: Tue, 13 Jan 2026 01:21:32 GMT  
		Size: 101.9 MB (101864067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac05cf83330bc2926b2df571891e74c490737237279915967146c50c60101b8`  
		Last Modified: Tue, 13 Jan 2026 01:21:29 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3d0bf2d77ae7f41a7d1729d3120a9efa034610ab144cd96a1d1159a2395f48`  
		Last Modified: Tue, 13 Jan 2026 01:21:28 GMT  
		Size: 14.0 MB (13972962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56176152ccf0719db62bcb47bc6c69c92ff8281466e958ec3156325605c6ea22`  
		Last Modified: Tue, 13 Jan 2026 01:21:39 GMT  
		Size: 443.8 MB (443799354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:24c37ec8e855210dc58c362fe80a4418cc527175d7d7bcc0e7dc6410d76778d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e5ef18b24ba15f487d96da7ae375414276bd6e1e3484c93040a4f005f0f8f7`

```dockerfile
```

-	Layers:
	-	`sha256:229a4aa92f9300eedecb5d771f52078c4171e43ab34901786df3a37689fe5021`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51c16259cbf1dcafafca5ca7291c6c4bb61e17b7fe0ec90713095a791f1ac908`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:bookworm`

```console
$ docker pull haskell@sha256:8e045c47c827e23a327facff2522cbdced501bfffc6a094790ea3acee5f80271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:f299e044461def92978fc02e1e09552447341fc5c94ea3fde855356920ce098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825154630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63dd23015457b14a600b2dbe468a91166b8b706e868ab525cd551f1e6752392`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08794db77b402d64775f4e981b74315507b6698f4e772bacb62fdc7b5735b9`  
		Last Modified: Tue, 03 Feb 2026 02:20:56 GMT  
		Size: 152.4 MB (152378556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b299d79199c316ba1c329518d60279d166e472b155f0c55f2a42d63bb555ff6`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 22.2 MB (22220734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf9f8fc6d29b3d4e84084da560dd2ce71e871ccddc8c93c22ff66bf7e77dee`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbba24a3271904d1646e97c601cdd0e42bb50d0b10c10c9b00ab7e261d98aa9`  
		Last Modified: Tue, 03 Feb 2026 02:21:04 GMT  
		Size: 593.7 MB (593670352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:b65ceb02ebede4bb61233c4b3228185b02f49b4c1cc6b2567df8edb48897c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e72c5a7ed2a057767454c8042905556f8493bdeedad4ec5bfa2dc52a5be25`

```dockerfile
```

-	Layers:
	-	`sha256:3a41aa03b940ddcb25fbd9428922b0f9b80e650d1d1cead15187736cba9433c6`  
		Last Modified: Tue, 03 Feb 2026 02:20:51 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60457317faadd06cb6ad537a6c0fb420942fbce0fcc24a3abaf5ad72e07f835`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3647e354c660ae20c53edfcbfb91f43c4d9d3f2b34e786cf1c51e9d6c04192ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.9 MB (827938406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab6dc3d055aef05cb68b4a5a96286c18de7d4623962bf4f310e617e9cf6279`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:21:35 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:21:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:21:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:21:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:23:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:23:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:23:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ae27c4297057722c43286a8294938ff609b4d211656df39e2178c8277df13`  
		Last Modified: Thu, 29 Jan 2026 20:25:24 GMT  
		Size: 146.5 MB (146547971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0bc56010070d4e8fd82ec69ac9be3c9a3ba21af3a73437fa720285f651edf9`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc9ecd04267369e82fde7fe99460dc9d508021a337f569b1d96fb58aea97940`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a7bfdf951d98afe3fbbbfd846edc57c7dbfb14ff061e20cedcbd12808fd44`  
		Last Modified: Thu, 29 Jan 2026 20:25:35 GMT  
		Size: 592.6 MB (592551222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:28996c9136802910cbfa3de6faaa5f9df4c033a64d313bd21b8e2cc1c6f5ac09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30fbc1a52bca5749a1beddc1d1fd5e8218cf4834d4bfdf119591d410ae7d516`

```dockerfile
```

-	Layers:
	-	`sha256:8f8f009cad10ee83982e723ea3e97386d783620402ef46fa4847511228f91da9`  
		Last Modified: Thu, 29 Jan 2026 20:25:17 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0d371f55e52b36c5159955ffb3ceb5b15c9f552ed0fc7ed5ea5fb0930fd50f`  
		Last Modified: Thu, 29 Jan 2026 20:25:16 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:bullseye`

```console
$ docker pull haskell@sha256:121d7cc72202a98998536934817f66ec8dc2ddd73ed4c432cba16b5256efae08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:6d62c2c22558a9f4be9082d56ccc48718e81169760aa4499b9bea2bac24c2d40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659144428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d89ab7703666e67c3606548f21bfb723bdad64966357caadae7ee1d74eddd3`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75238d6ce97658590d0e7ca1aaf30fcba7bcb5c26bbd70cd884882a7979de149`  
		Last Modified: Tue, 03 Feb 2026 02:20:41 GMT  
		Size: 133.8 MB (133753898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e15615986ee567d17dab5c314e85877d951095edac5c31e416f1681e2ab9e3`  
		Last Modified: Tue, 03 Feb 2026 02:20:38 GMT  
		Size: 22.2 MB (22220752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c76124521720024b593e6b7c5f34bb17689543c866b3a3c5ef960357ac11da`  
		Last Modified: Tue, 03 Feb 2026 02:20:46 GMT  
		Size: 441.8 MB (441801274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:53d5b173bff7b231b60abbb2b322a9eb1325f442ef0a5b9467745353f1e151e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ef0c54bf6ad45c85aca74ad4802897d276198be4a7175cf1170062d7b556f0`

```dockerfile
```

-	Layers:
	-	`sha256:4b2fbe4f1a16763366e46ddbe8e41491b1d25e11b2f630c0ea068449342c0b4d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86ff45e85ac1e2cbaa45d82b33c17bdd2a40f1c919de0910d6f11911b02deb40`  
		Last Modified: Tue, 03 Feb 2026 02:20:36 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:e7d2bb12473e8ca564817405f80a72f9a6a6f998c64e1e9b30a7c4bd213773af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669449125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c9493023ab675c91b402548eab4fe024cc03aced2e301621b79d999597cda7e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:26 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:20:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:20:03 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:20:03 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904396a1ed19b72c34ac049fddb833b77d8ff29212b034f306b89170224c3e79`  
		Last Modified: Tue, 13 Jan 2026 01:21:27 GMT  
		Size: 129.2 MB (129241147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6443d9a1a7bef1d3bb5e84daf420ce96bfa38211f22d03407b6f9b40283f5360`  
		Last Modified: Tue, 13 Jan 2026 01:21:23 GMT  
		Size: 24.5 MB (24528541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb39a72843976163048a101d67acc696b91e09c912f82db26b3cb2793d23db6`  
		Last Modified: Tue, 13 Jan 2026 01:21:14 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6530d9b1cee1556dc890910c703727045b89398292afa180324e9634fae5f8f`  
		Last Modified: Tue, 13 Jan 2026 01:21:32 GMT  
		Size: 449.4 MB (449448708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:ff116e5d6ea811b71d7978c9385d3e9284b88978d48c6e0d98be9d714b8bd3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8ee2f44400a71e0a3a8bc51250a3388920d22ef10e42f8b0f3947eff178c0b`

```dockerfile
```

-	Layers:
	-	`sha256:38ba952907a41a1a43d318514c3c500b5a565d28343b20908c7958204b833496`  
		Last Modified: Tue, 13 Jan 2026 01:21:22 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba83d152e0054fc4751a8f2ae28ec41dfa93bdfa35769379f2d00f0c6725866`  
		Last Modified: Tue, 13 Jan 2026 01:21:21 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:latest`

```console
$ docker pull haskell@sha256:8e045c47c827e23a327facff2522cbdced501bfffc6a094790ea3acee5f80271
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:f299e044461def92978fc02e1e09552447341fc5c94ea3fde855356920ce098e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **825.2 MB (825154630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c63dd23015457b14a600b2dbe468a91166b8b706e868ab525cd551f1e6752392`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:08 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:08 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:08 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:15 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6bc9f599b3efabc64230fd3b969d7654fcd6c6c98ad7cf7470093fe85274a7fc`  
		Last Modified: Tue, 03 Feb 2026 01:13:20 GMT  
		Size: 48.5 MB (48481483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a08794db77b402d64775f4e981b74315507b6698f4e772bacb62fdc7b5735b9`  
		Last Modified: Tue, 03 Feb 2026 02:20:56 GMT  
		Size: 152.4 MB (152378556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b299d79199c316ba1c329518d60279d166e472b155f0c55f2a42d63bb555ff6`  
		Last Modified: Tue, 03 Feb 2026 02:20:52 GMT  
		Size: 22.2 MB (22220734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cf9f8fc6d29b3d4e84084da560dd2ce71e871ccddc8c93c22ff66bf7e77dee`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbba24a3271904d1646e97c601cdd0e42bb50d0b10c10c9b00ab7e261d98aa9`  
		Last Modified: Tue, 03 Feb 2026 02:21:04 GMT  
		Size: 593.7 MB (593670352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:b65ceb02ebede4bb61233c4b3228185b02f49b4c1cc6b2567df8edb48897c507
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9506267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366e72c5a7ed2a057767454c8042905556f8493bdeedad4ec5bfa2dc52a5be25`

```dockerfile
```

-	Layers:
	-	`sha256:3a41aa03b940ddcb25fbd9428922b0f9b80e650d1d1cead15187736cba9433c6`  
		Last Modified: Tue, 03 Feb 2026 02:20:51 GMT  
		Size: 9.5 MB (9479400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a60457317faadd06cb6ad537a6c0fb420942fbce0fcc24a3abaf5ad72e07f835`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3647e354c660ae20c53edfcbfb91f43c4d9d3f2b34e786cf1c51e9d6c04192ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **827.9 MB (827938406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ab6dc3d055aef05cb68b4a5a96286c18de7d4623962bf4f310e617e9cf6279`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:21:35 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:21:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:21:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:21:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:21:38 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:21:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:21:43 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:23:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:23:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:23:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1029f5ddc0d24726f1cefbb8def7a88f8ec819a1fdc4c05ce523011b4b73c72d`  
		Last Modified: Tue, 13 Jan 2026 00:41:14 GMT  
		Size: 48.4 MB (48366072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ae27c4297057722c43286a8294938ff609b4d211656df39e2178c8277df13`  
		Last Modified: Thu, 29 Jan 2026 20:25:24 GMT  
		Size: 146.5 MB (146547971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0bc56010070d4e8fd82ec69ac9be3c9a3ba21af3a73437fa720285f651edf9`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc9ecd04267369e82fde7fe99460dc9d508021a337f569b1d96fb58aea97940`  
		Last Modified: Thu, 29 Jan 2026 20:25:18 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10a7bfdf951d98afe3fbbbfd846edc57c7dbfb14ff061e20cedcbd12808fd44`  
		Last Modified: Thu, 29 Jan 2026 20:25:35 GMT  
		Size: 592.6 MB (592551222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:28996c9136802910cbfa3de6faaa5f9df4c033a64d313bd21b8e2cc1c6f5ac09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9534322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b30fbc1a52bca5749a1beddc1d1fd5e8218cf4834d4bfdf119591d410ae7d516`

```dockerfile
```

-	Layers:
	-	`sha256:8f8f009cad10ee83982e723ea3e97386d783620402ef46fa4847511228f91da9`  
		Last Modified: Thu, 29 Jan 2026 20:25:17 GMT  
		Size: 9.5 MB (9507256 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0d371f55e52b36c5159955ffb3ceb5b15c9f552ed0fc7ed5ea5fb0930fd50f`  
		Last Modified: Thu, 29 Jan 2026 20:25:16 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim`

```console
$ docker pull haskell@sha256:421d5abd82604d78c08e4438bfb81df19816c79c08abd7ba6e74e7018df11c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:110d4a2d1efeeddb62ae38b915474444040487c6a4b644a37597bacb652f6460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776930005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e17615141dab7f099ff2b4faa0260fda01bdebca0a3a049d99937148a1eb06`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fe43daec195aa75262a2e86f9dc0ba4805f1705d8cd95c334dfd178dc9f11`  
		Last Modified: Tue, 03 Feb 2026 02:21:11 GMT  
		Size: 124.4 MB (124406060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e90ee734b1d3e56d7e2c6c778dda05a971c7333a05589fd21b9acd055603e`  
		Last Modified: Tue, 03 Feb 2026 02:21:08 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c41bcf39676cc775bbe10c12641791e3c3663f6a9bf7d661910276e362c26a2`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba2b992b4373bf7d394ffc39402a056b50fcc2fe9128c8856debcd41019dc5`  
		Last Modified: Tue, 03 Feb 2026 02:21:20 GMT  
		Size: 593.7 MB (593671184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim` - unknown; unknown

```console
$ docker pull haskell@sha256:65b9a880c769cf5ce7cf9d1784ebd941644fff1242af9e2ece0a74c1fd5227c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef83333c9d00ac92e175ccb2585258325e7d4da865be37a85b8ca928cde3ac47`

```dockerfile
```

-	Layers:
	-	`sha256:88cb24a779b9ff5b1a8c0db293620ff74fec7cc2142f09dd8360962ecdc27e6b`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd146a8e20014ebf818d4bfb1265a4d978f26ba9a61f8c9ec2e8bd4c1511f61c`  
		Last Modified: Tue, 03 Feb 2026 02:21:06 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3a36953ac7ac34d4f2c7498322c3266d227776b5a1374aaef40ef1dbb95a17e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779705710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d69fc402d5193d22afabc71d151a6dbee4eca69e5d5e0466c257538101922cf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:22:31 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:22:31 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:22:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:22:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:24:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:24:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:24:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4f4ed0fd2c28ce4be76881e223763ccd903d7068141aa943944e73ca61468a`  
		Last Modified: Thu, 29 Jan 2026 20:26:12 GMT  
		Size: 118.6 MB (118575484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc78c2319953580a1d9cb773453a236d84f48dec9454c1b1534ef532fe1effd`  
		Last Modified: Thu, 29 Jan 2026 20:26:09 GMT  
		Size: 24.5 MB (24528567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc147b79cfae7eb4a1b9bdde1478144c933c31fd6f6402300042448a3640ac55`  
		Last Modified: Thu, 29 Jan 2026 20:26:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d318096c027eaa2441061e88514b6b1d35edece3563f243ee9d20f2938d35c5b`  
		Last Modified: Thu, 29 Jan 2026 20:26:20 GMT  
		Size: 592.5 MB (592549179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim` - unknown; unknown

```console
$ docker pull haskell@sha256:7aba8a6d02bbaad684351341c59715c03e30704c97b1699ecdaf17ef77701320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e874e120e22a3c1bd835535e506ad86b8efcd95a6e43b5e756976a218455f01f`

```dockerfile
```

-	Layers:
	-	`sha256:6b1e3e7fb716a9221df7a76d1eac6ca105121dd69f7decb039b19b8318ae9d43`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e3e173986e5627199e41d6685f1ff63e51f059ddb7b6dcd86c0412d9598faf`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim-bookworm`

```console
$ docker pull haskell@sha256:421d5abd82604d78c08e4438bfb81df19816c79c08abd7ba6e74e7018df11c00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:110d4a2d1efeeddb62ae38b915474444040487c6a4b644a37597bacb652f6460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.9 MB (776930005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e17615141dab7f099ff2b4faa0260fda01bdebca0a3a049d99937148a1eb06`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 02:17:18 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:18 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:18 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL=3.16.1.0
# Tue, 03 Feb 2026 02:17:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 03 Feb 2026 02:17:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC=9.14.1
# Tue, 03 Feb 2026 02:17:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1fe43daec195aa75262a2e86f9dc0ba4805f1705d8cd95c334dfd178dc9f11`  
		Last Modified: Tue, 03 Feb 2026 02:21:11 GMT  
		Size: 124.4 MB (124406060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3e90ee734b1d3e56d7e2c6c778dda05a971c7333a05589fd21b9acd055603e`  
		Last Modified: Tue, 03 Feb 2026 02:21:08 GMT  
		Size: 22.2 MB (22220769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c41bcf39676cc775bbe10c12641791e3c3663f6a9bf7d661910276e362c26a2`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 8.4 MB (8403505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ba2b992b4373bf7d394ffc39402a056b50fcc2fe9128c8856debcd41019dc5`  
		Last Modified: Tue, 03 Feb 2026 02:21:20 GMT  
		Size: 593.7 MB (593671184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:65b9a880c769cf5ce7cf9d1784ebd941644fff1242af9e2ece0a74c1fd5227c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef83333c9d00ac92e175ccb2585258325e7d4da865be37a85b8ca928cde3ac47`

```dockerfile
```

-	Layers:
	-	`sha256:88cb24a779b9ff5b1a8c0db293620ff74fec7cc2142f09dd8360962ecdc27e6b`  
		Last Modified: Tue, 03 Feb 2026 02:21:07 GMT  
		Size: 6.6 MB (6605758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd146a8e20014ebf818d4bfb1265a4d978f26ba9a61f8c9ec2e8bd4c1511f61c`  
		Last Modified: Tue, 03 Feb 2026 02:21:06 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:3a36953ac7ac34d4f2c7498322c3266d227776b5a1374aaef40ef1dbb95a17e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **779.7 MB (779705710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d69fc402d5193d22afabc71d151a6dbee4eca69e5d5e0466c257538101922cf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1768176000'
# Thu, 29 Jan 2026 20:22:31 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 20:22:31 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK=3.3.1
# Thu, 29 Jan 2026 20:22:31 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 29 Jan 2026 20:22:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL=3.16.1.0
# Thu, 29 Jan 2026 20:22:33 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Thu, 29 Jan 2026 20:22:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='41d8fc43de1c652c00d85799d0273f8b6600bc71603126bc651ca4e3917a1b84';             ;;         'x86_64')             CABAL_INSTALL_SHA256='209987f6abdd1119f6b2674a0d1012857a783464774708cb4f3fd9e156ea7bea';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC=9.14.1
# Thu, 29 Jan 2026 20:22:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 29 Jan 2026 20:24:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.16.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.14.1 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='6aa27a377451851c851eefdd869e8f5a9217b02ce66c6ca9b418b72efee28427';             ;;         'x86_64')             GHC_SHA256='60f7ab75f28df892729fbaff3a54f58ee3ad7e731929f1b2f3eb0208f73de841';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Thu, 29 Jan 2026 20:24:30 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.14.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Jan 2026 20:24:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:33bdc9671af8942d96d2f78f67aeec06580065dde1272decac3732689ec7c0e8`  
		Last Modified: Tue, 13 Jan 2026 00:42:00 GMT  
		Size: 28.1 MB (28107889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4f4ed0fd2c28ce4be76881e223763ccd903d7068141aa943944e73ca61468a`  
		Last Modified: Thu, 29 Jan 2026 20:26:12 GMT  
		Size: 118.6 MB (118575484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc78c2319953580a1d9cb773453a236d84f48dec9454c1b1534ef532fe1effd`  
		Last Modified: Thu, 29 Jan 2026 20:26:09 GMT  
		Size: 24.5 MB (24528567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc147b79cfae7eb4a1b9bdde1478144c933c31fd6f6402300042448a3640ac55`  
		Last Modified: Thu, 29 Jan 2026 20:26:08 GMT  
		Size: 15.9 MB (15944591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d318096c027eaa2441061e88514b6b1d35edece3563f243ee9d20f2938d35c5b`  
		Last Modified: Thu, 29 Jan 2026 20:26:20 GMT  
		Size: 592.5 MB (592549179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:7aba8a6d02bbaad684351341c59715c03e30704c97b1699ecdaf17ef77701320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e874e120e22a3c1bd835535e506ad86b8efcd95a6e43b5e756976a218455f01f`

```dockerfile
```

-	Layers:
	-	`sha256:6b1e3e7fb716a9221df7a76d1eac6ca105121dd69f7decb039b19b8318ae9d43`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 6.6 MB (6634217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e3e173986e5627199e41d6685f1ff63e51f059ddb7b6dcd86c0412d9598faf`  
		Last Modified: Thu, 29 Jan 2026 20:26:07 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim-bullseye`

```console
$ docker pull haskell@sha256:5fa6651a439e5aac88472c8a0599e184f05678e4330d98bde9ebd1f50987cc0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:592e51cede7db0b4910f951a43961024661c7a8b55f47acd4bf2efe91bd88852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608259149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f9101bb8a800a45e5d6f78526a9623f8c5157af03c8e8f7d41aea34288d3f1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 02:17:53 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 02:17:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK=3.3.1
# Tue, 03 Feb 2026 02:17:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 03 Feb 2026 02:17:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 03 Feb 2026 02:17:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 03 Feb 2026 02:17:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC=9.10.3
# Tue, 03 Feb 2026 02:17:56 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 03 Feb 2026 02:19:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 03 Feb 2026 02:19:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 02:19:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1c3e0f92551cc087b68faa686aead2fc80d99c54c34e9e72a0db197b668ac6be`  
		Last Modified: Tue, 03 Feb 2026 01:14:04 GMT  
		Size: 30.3 MB (30258284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3c918a9dbef90c820e3b8f89e3eb745c6b8206768d5dc801bad637f07de68e`  
		Last Modified: Tue, 03 Feb 2026 02:20:53 GMT  
		Size: 106.4 MB (106366909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d52fe0f0d6d3c84e13aa5a5843a10b3a0bb4cfc47cacc90ce709f6df933977f`  
		Last Modified: Tue, 03 Feb 2026 02:20:50 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6284ef99bd50ff24e2fd134c630747f0c59dd5cb753275230a8a26aa3c97527d`  
		Last Modified: Tue, 03 Feb 2026 02:20:37 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02604587704ad580a78c07fd1af9da93ffe6e276cd976c310847887f0742710c`  
		Last Modified: Tue, 03 Feb 2026 02:21:00 GMT  
		Size: 441.8 MB (441800960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b71502010e6068c6d40b4b8a361b29059ba4a86dc02be5e86ecd71dfb557e152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999c96a2c5eb622c8c95795883265b90267932ff8488e9032d04781b644c86e7`

```dockerfile
```

-	Layers:
	-	`sha256:0d8b88f8077a1d894aab234933ffdcb791f8e0730003ef65ae1f41d2ddfe73ce`  
		Last Modified: Tue, 03 Feb 2026 02:20:49 GMT  
		Size: 6.8 MB (6750929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0054b7fb8b6ae305be385f6ab8726d5c07a6db46e848a0ce3e842b853006ba8e`  
		Last Modified: Tue, 03 Feb 2026 02:20:49 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f56b48eefc38564ec24bd6c46efcf5e42428b594bb064d3c56a143f02b480b5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618563538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fef4d36395c024b1be79dc5189fc28cf16c2f14cb1aebd8daedf43437783f7`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Tue, 13 Jan 2026 01:18:23 GMT
ENV LANG=C.UTF-8
# Tue, 13 Jan 2026 01:18:23 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 01:18:23 GMT
ARG STACK=3.3.1
# Tue, 13 Jan 2026 01:18:23 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 13 Jan 2026 01:18:25 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 13 Jan 2026 01:18:25 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 13 Jan 2026 01:18:25 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 13 Jan 2026 01:18:27 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 13 Jan 2026 01:18:27 GMT
ARG GHC=9.10.3
# Tue, 13 Jan 2026 01:18:27 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 13 Jan 2026 01:19:59 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 13 Jan 2026 01:19:59 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 01:19:59 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:51 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a96c3c611e1717d66afae67d6fb8eba49eb7f9ac36228fcd7b6136699549fe`  
		Last Modified: Tue, 13 Jan 2026 01:21:20 GMT  
		Size: 101.9 MB (101863954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c652f3f14d418494191692b21fa54656e5b70879faead69be341a17cd6f2841`  
		Last Modified: Tue, 13 Jan 2026 01:21:16 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3879388bec87dd8f22e12521634d07e8ae09151739d3e7636cb0c34e2d0b4a70`  
		Last Modified: Tue, 13 Jan 2026 01:21:16 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4896f989cd82087a24fcc86dea60eec6c0dd1307426e36fabe717b12939a8d9`  
		Last Modified: Tue, 13 Jan 2026 01:21:26 GMT  
		Size: 449.4 MB (449449555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:040eadb249af5b8b1cf61e5cc13d4e0cbb95dac5da5b1af59e931e53f57cfc6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28288cabdcabf2ef88791f546297fa382f032786da32f5ae7c834b484595bd40`

```dockerfile
```

-	Layers:
	-	`sha256:e20461454727c7d76eb386d0ada378ce79198d146fe58555bba010ac323a4c51`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 6.8 MB (6753439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b260842ec1bfdc58222371116a8ccbbd05a84123643c55bbded00788700a5222`  
		Last Modified: Tue, 13 Jan 2026 01:21:15 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json
