## `haskell:slim-bullseye`

```console
$ docker pull haskell@sha256:06fd4915fab64cc907db21681c6c2ee840dcd8041008577262b8c42121102213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:098e8c2292fb05bd2b8bbd8f63e305741ed9ea6eb6762d6fa61648972ab47beb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608264563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:503f13c87bad7ade30d9dd2ed4abb08a00c37155e90a0401285221eeca736595`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:35 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:35 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:35 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:35 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:37 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:37 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:38 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:38 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:38 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:19:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174862d2fe32196d1c59d64256540f6d809449816d3c6d221fb047e7c1b041e6`  
		Last Modified: Mon, 29 Dec 2025 23:21:17 GMT  
		Size: 106.4 MB (106366639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c5a1b25709553c31011754680638ca7dbe52bdcc98b49d77bb73bc7e1998eb`  
		Last Modified: Mon, 29 Dec 2025 23:20:53 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9984c37ba1be3eee8b6dcdc868d1b82459660a037a54699e15914f3db1455577`  
		Last Modified: Mon, 29 Dec 2025 23:20:51 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3abd6280df70164e83119c8c0b48da5cf71435c37328041f33ce60ae392c69`  
		Last Modified: Mon, 29 Dec 2025 23:21:36 GMT  
		Size: 441.8 MB (441806492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:dc64a354be65fa59307a391d41c089590d8bad958ae52e2cc5b16d9e4f16ee48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99036e5a528ac2ba28bd5c645885a7ea0dd91892ac119397b239a85e007312fc`

```dockerfile
```

-	Layers:
	-	`sha256:d1858f4ac2a3ee34e4b98b57cbe48e038d97f837c601846ecb7a440827c9e922`  
		Last Modified: Tue, 30 Dec 2025 03:49:14 GMT  
		Size: 6.8 MB (6750929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1aa40dfe8d24ef60ee541f396a43ec876e9e7e0a5c378b2e8b8e93516128c4d3`  
		Last Modified: Tue, 30 Dec 2025 03:49:15 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:b3b1f80d08a9ddac51b2cbcfa37b1c8ce3aebd3f20c5e5074266f33ca97c29e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618563348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d85ef9158e447664542b319532ac7b904105ad31fa4cd4c6e0398130c45b5b5`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:16:55 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:55 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:55 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:55 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:57 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:57 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:58 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:58 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:16:58 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20dda41cf95c68215a888ecd78ad5715c27e8ac8bd93098019bee5ade47205e`  
		Last Modified: Mon, 29 Dec 2025 23:20:12 GMT  
		Size: 101.9 MB (101863729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd22da46ff1fa5a08c0dd35a307061942ce4aab54454900dd567af543a554be7`  
		Last Modified: Mon, 29 Dec 2025 23:20:06 GMT  
		Size: 24.5 MB (24528551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8283950ebce3ff15f63a4e4f45640cdbe625efb04b078a32a95d7cd78f9180`  
		Last Modified: Mon, 29 Dec 2025 23:20:04 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce48410471fc78656d88c2793b9d0ccbff8f9fd393c015ec255b2145b5287f3`  
		Last Modified: Mon, 29 Dec 2025 23:20:17 GMT  
		Size: 449.4 MB (449449645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:eb663cdc28306261afbc98176a077b52737a5d9af3fe056f1d71bd23817a28d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088b268dbea77fa58d22f0deaffb01d5bf10e0545d5cb1669304495a243e857f`

```dockerfile
```

-	Layers:
	-	`sha256:c974d70449cf9ef6440121cff76cab9e3d14edb6fbcfa932176f48533ff75550`  
		Last Modified: Tue, 30 Dec 2025 03:49:21 GMT  
		Size: 6.8 MB (6753439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae2c70fdc4831b60cb41b2857f1a006af08a0f6e586e5f800da081ee762f1789`  
		Last Modified: Tue, 30 Dec 2025 03:49:22 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json
