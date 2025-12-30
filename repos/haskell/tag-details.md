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
$ docker pull haskell@sha256:590e9e9c918d1c7b0a87badb0a6449105732fa0b7152be87ecfc149576d09614
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:5906cacce760379bcdc745eb02f756846ca4a0fa213ad3b21604c4095c61403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822424053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5191a918085facf1d579e06d8b7976ae263fcec63b12d04d5114171e9b9bce1f`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851bd5b066c6bc5263113a72ba6b03f8cd26c0e11ec21b4faee09fd49138f9ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 152.4 MB (152360257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7702220116f89c51e73d9030008d264fb0d258f70cdeb0d47124192649a8a8b`  
		Last Modified: Mon, 29 Dec 2025 23:20:33 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d7dacad299c850062d8a60ca3d62f23a1fb27e132af8d6a96b6c5c092153f`  
		Last Modified: Mon, 29 Dec 2025 23:21:18 GMT  
		Size: 591.8 MB (591755193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9` - unknown; unknown

```console
$ docker pull haskell@sha256:c69dd9d58a2b4448bae5da7b44258efdf56f2b65fdfe2f1a425957c533faa84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620bcbc4e5d5426966bf9ea47bf486a0deef8d2b58e5aa9138e8c9a2d2277789`

```dockerfile
```

-	Layers:
	-	`sha256:a7c0c8cc14b721859c072fa36cd314b05d699933152bfe89930e04763ca67b65`  
		Last Modified: Tue, 30 Dec 2025 03:48:44 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da0a224b9700730cef9f784ff1c3bb008a0263ca3fdb5450e166255f06b420f`  
		Last Modified: Tue, 30 Dec 2025 03:48:45 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:bd4d7f122bfeb2b8ca0c8b666401862e03a7d2e91efd424f16f6e9687e765644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824926337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8255e5e92ffc6a0d411a4c3fdfa15b5a1aea3bec710d3ac9048714708a2483a1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c29931c3e00184d8309814c6bb94b8eae48b8d44cd8bb0b34c0a96704a32e1`  
		Last Modified: Mon, 29 Dec 2025 23:22:32 GMT  
		Size: 146.4 MB (146442606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd77a5299206d5e51acf0a90a31f30864e48172b41eeb9ee9efb392da0d93d6b`  
		Last Modified: Mon, 29 Dec 2025 23:21:52 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea94209ec2fd884df59dfdc57f9ffbe524964ff8aa73611e3e3e09146f5b027`  
		Last Modified: Mon, 29 Dec 2025 23:21:54 GMT  
		Size: 14.0 MB (13969019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e41e6094016ad14b3382f6e3587baeda522cea539bbf6ed42f7b692c200574`  
		Last Modified: Mon, 29 Dec 2025 23:22:26 GMT  
		Size: 591.6 MB (591627013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9` - unknown; unknown

```console
$ docker pull haskell@sha256:31602177a7c7a147780a5579401ae9cd255111cc88275dc22e9aa05020184ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802e3273d59f837cff1550dd346cfe9d8495d6eafd81ef3bb361eb4af81a7555`

```dockerfile
```

-	Layers:
	-	`sha256:31c781c3abc8afecf26acbe00ddba616277b794b7932b9a23939a5a387d1da54`  
		Last Modified: Tue, 30 Dec 2025 03:48:53 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a259963f6a750d76c85f50b4a729093daf2b1543b7d7f0f56961c8853a9aa5`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-bookworm`

```console
$ docker pull haskell@sha256:590e9e9c918d1c7b0a87badb0a6449105732fa0b7152be87ecfc149576d09614
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:5906cacce760379bcdc745eb02f756846ca4a0fa213ad3b21604c4095c61403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822424053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5191a918085facf1d579e06d8b7976ae263fcec63b12d04d5114171e9b9bce1f`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851bd5b066c6bc5263113a72ba6b03f8cd26c0e11ec21b4faee09fd49138f9ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 152.4 MB (152360257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7702220116f89c51e73d9030008d264fb0d258f70cdeb0d47124192649a8a8b`  
		Last Modified: Mon, 29 Dec 2025 23:20:33 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d7dacad299c850062d8a60ca3d62f23a1fb27e132af8d6a96b6c5c092153f`  
		Last Modified: Mon, 29 Dec 2025 23:21:18 GMT  
		Size: 591.8 MB (591755193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:c69dd9d58a2b4448bae5da7b44258efdf56f2b65fdfe2f1a425957c533faa84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620bcbc4e5d5426966bf9ea47bf486a0deef8d2b58e5aa9138e8c9a2d2277789`

```dockerfile
```

-	Layers:
	-	`sha256:a7c0c8cc14b721859c072fa36cd314b05d699933152bfe89930e04763ca67b65`  
		Last Modified: Tue, 30 Dec 2025 03:48:44 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da0a224b9700730cef9f784ff1c3bb008a0263ca3fdb5450e166255f06b420f`  
		Last Modified: Tue, 30 Dec 2025 03:48:45 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:bd4d7f122bfeb2b8ca0c8b666401862e03a7d2e91efd424f16f6e9687e765644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824926337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8255e5e92ffc6a0d411a4c3fdfa15b5a1aea3bec710d3ac9048714708a2483a1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c29931c3e00184d8309814c6bb94b8eae48b8d44cd8bb0b34c0a96704a32e1`  
		Last Modified: Mon, 29 Dec 2025 23:22:32 GMT  
		Size: 146.4 MB (146442606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd77a5299206d5e51acf0a90a31f30864e48172b41eeb9ee9efb392da0d93d6b`  
		Last Modified: Mon, 29 Dec 2025 23:21:52 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea94209ec2fd884df59dfdc57f9ffbe524964ff8aa73611e3e3e09146f5b027`  
		Last Modified: Mon, 29 Dec 2025 23:21:54 GMT  
		Size: 14.0 MB (13969019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e41e6094016ad14b3382f6e3587baeda522cea539bbf6ed42f7b692c200574`  
		Last Modified: Mon, 29 Dec 2025 23:22:26 GMT  
		Size: 591.6 MB (591627013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:31602177a7c7a147780a5579401ae9cd255111cc88275dc22e9aa05020184ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802e3273d59f837cff1550dd346cfe9d8495d6eafd81ef3bb361eb4af81a7555`

```dockerfile
```

-	Layers:
	-	`sha256:31c781c3abc8afecf26acbe00ddba616277b794b7932b9a23939a5a387d1da54`  
		Last Modified: Tue, 30 Dec 2025 03:48:53 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a259963f6a750d76c85f50b4a729093daf2b1543b7d7f0f56961c8853a9aa5`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-bullseye`

```console
$ docker pull haskell@sha256:cea76117ba2bf3e8110b9a849823e0d43deae6e2b2c39e3faf1e0c8475dcdcf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:00294c6703b73b9bbb558d5d65c71be1c7c0a17190a79f758f8b9896f5200698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659154185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5bcc4f528a3fedbe74d658c13e262c3a06ee98ee2127fc5d082318dd435683`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:37 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:19:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:17 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dd594824971fffd646434acd2f8cb944285d5662248793e7f5c1c652dd114`  
		Last Modified: Mon, 29 Dec 2025 23:20:52 GMT  
		Size: 133.8 MB (133759018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b890bf7f170ec3762847be6a1ba63596af0d5ff77f5c4c3780b95f3cb1e56e`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246a67688b8a1355ed3e249780619237cf63c0e6a4cfd98a22cd8a54c7685eca`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbd7e04f4d501c556cc4d1d45d8270f66600167280999f842ac8b88c68d8538`  
		Last Modified: Mon, 29 Dec 2025 23:21:45 GMT  
		Size: 441.8 MB (441805720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a52a1555c472e2ad5d8dcc7b60d8c34c075a152cd15a9b6374d3342373b0eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b55c9eb1d1092bc250758b0ae82591aec75e34fe61f4d6dd2d24e9050ebc2c`

```dockerfile
```

-	Layers:
	-	`sha256:d0371a3f0a3050fe378fe4d3fa46310837f121aad22e649c685ce8f50966d629`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffe3a711aa7b09bd9aaca3a75ad1409b4ddd813898dbdac1935e921fdfd9647`  
		Last Modified: Tue, 30 Dec 2025 03:48:55 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f3275e745ce464ed808e373238abbd4082b512a2c62b1efce4fa96d20ddef3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669448569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ac34b1c314183a7cc2c5e72cc03aab5cace727fa4948ff501a96cac069f2a9`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:16:57 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:59 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5280ec1a5df44236392d8b14bc966469c8c234eb70e8c65f31a370a3b097659`  
		Last Modified: Mon, 29 Dec 2025 23:20:19 GMT  
		Size: 129.2 MB (129240390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35c2ef41b84da2a8492d69e5fe7209cf5338d9a0010a204d06e87d088a687e`  
		Last Modified: Mon, 29 Dec 2025 23:20:09 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600ca497b466ab826688c761749af75c8e8a945a31f64e77480c3a540ec8b9b4`  
		Last Modified: Mon, 29 Dec 2025 23:20:08 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65a9628a3fd7f16cfbd6bf3b7c96b4c813428b9455cf994e163256726cf69d`  
		Last Modified: Mon, 29 Dec 2025 23:22:04 GMT  
		Size: 449.4 MB (449448901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:3add895d061fd10533b9ecead6bea7abf3dcf90882baf1a75c05a505860ea761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b560cd801061656c03e8103be090f777480bef3726076902616cf5fa5436c60b`

```dockerfile
```

-	Layers:
	-	`sha256:a28e7344b8f75cfff907d15034128ee3784f9afd291da7bdfeb2005b6efa857c`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01081a13d3bb59b97c2a776f3adb9bae72653eb9b007be9b36bb7919a286392`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26451 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:634cc56adaa1dd9f2321f640fb45fcbcb8363153ab37a977f971ee150247412f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:97b16c440c491654aba4c95e9c3132e1e4e1a065a709cce713390d160ca74f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774212235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92003b13829d688409aab1d1c244ff262fed57faa9d1acc3eb83a72f7c26fe35`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:53 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:53 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b04edbc0c4dfa46fafd245a2b2a0b057b91d4a81d0914d396de56028f15ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:59 GMT  
		Size: 124.4 MB (124406228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100a9279ba93680fbe144ea31c9310ac12a0b5045f9db11db3a1e983e6e881ff`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36999b209606621dff474cc3fab4ecd44dddd3fe5c75bc92e440b6bb2f440a7f`  
		Last Modified: Mon, 29 Dec 2025 23:21:27 GMT  
		Size: 591.7 MB (591749776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:eb0a2eb25660433b057a136f94dd660e17aef1f7a886387332d0a202a350b679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beba287c9837e41e99ff8f16de2652cc3d58080378e0357676dbe31c6b1daef4`

```dockerfile
```

-	Layers:
	-	`sha256:c8203cc4441763cf885e243f30d1630bc4c9a2a8c9759cba1c9a00acd995af77`  
		Last Modified: Tue, 30 Dec 2025 03:49:01 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd8ac24ce53a5207506ee8d7470313245cad1af0536175db5dc5110cfb18fca`  
		Last Modified: Tue, 30 Dec 2025 03:49:02 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:436435637aade026aa72bc34a8d91add8d7b32abe92f5e260d08cb85ff2388c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776710338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d149018b8046249b7e234dcd59bd0503f2c249b1da5ea71b9d7d07a34c78a14`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:58 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6377ba840a84af4c909b1eb1ef8792c6e8706b5e4320bfcf8c5e0ff25014fa`  
		Last Modified: Mon, 29 Dec 2025 23:22:01 GMT  
		Size: 118.5 MB (118483759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf44bd0db910fbbca8952d8094f8283bf8770a881423599b00480f8af3efa80`  
		Last Modified: Mon, 29 Dec 2025 23:21:55 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10d58ac69a8b25366852eb5b7a018d15122af20d6ca8d9d4bda3a25c4a50923`  
		Last Modified: Mon, 29 Dec 2025 23:21:53 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac8e82e01a1db4cc233e5dbd8d55fabe6d0bd6a1054f8d4de384afd7d6feb2`  
		Last Modified: Mon, 29 Dec 2025 23:22:02 GMT  
		Size: 591.6 MB (591626795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:e3d29985b25e02b3b6a90a7604a0f196bbebbb5a28627f5d3d227d44dbcd856d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1900668bc3a5e6c83a877a880e3cac853d615d7328cf7994004a6c9a031d80`

```dockerfile
```

-	Layers:
	-	`sha256:906ed3303f7f61337f39822b8214a83bf6701ce24504ab71585ca891197cfed1`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c16428de8f412befe040c1b5cb388bdd0663ecee5cc13bf70e7ddf78819791`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim-bookworm`

```console
$ docker pull haskell@sha256:634cc56adaa1dd9f2321f640fb45fcbcb8363153ab37a977f971ee150247412f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:97b16c440c491654aba4c95e9c3132e1e4e1a065a709cce713390d160ca74f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774212235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92003b13829d688409aab1d1c244ff262fed57faa9d1acc3eb83a72f7c26fe35`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:53 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:53 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b04edbc0c4dfa46fafd245a2b2a0b057b91d4a81d0914d396de56028f15ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:59 GMT  
		Size: 124.4 MB (124406228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100a9279ba93680fbe144ea31c9310ac12a0b5045f9db11db3a1e983e6e881ff`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36999b209606621dff474cc3fab4ecd44dddd3fe5c75bc92e440b6bb2f440a7f`  
		Last Modified: Mon, 29 Dec 2025 23:21:27 GMT  
		Size: 591.7 MB (591749776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:eb0a2eb25660433b057a136f94dd660e17aef1f7a886387332d0a202a350b679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beba287c9837e41e99ff8f16de2652cc3d58080378e0357676dbe31c6b1daef4`

```dockerfile
```

-	Layers:
	-	`sha256:c8203cc4441763cf885e243f30d1630bc4c9a2a8c9759cba1c9a00acd995af77`  
		Last Modified: Tue, 30 Dec 2025 03:49:01 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd8ac24ce53a5207506ee8d7470313245cad1af0536175db5dc5110cfb18fca`  
		Last Modified: Tue, 30 Dec 2025 03:49:02 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:436435637aade026aa72bc34a8d91add8d7b32abe92f5e260d08cb85ff2388c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776710338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d149018b8046249b7e234dcd59bd0503f2c249b1da5ea71b9d7d07a34c78a14`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:58 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6377ba840a84af4c909b1eb1ef8792c6e8706b5e4320bfcf8c5e0ff25014fa`  
		Last Modified: Mon, 29 Dec 2025 23:22:01 GMT  
		Size: 118.5 MB (118483759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf44bd0db910fbbca8952d8094f8283bf8770a881423599b00480f8af3efa80`  
		Last Modified: Mon, 29 Dec 2025 23:21:55 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10d58ac69a8b25366852eb5b7a018d15122af20d6ca8d9d4bda3a25c4a50923`  
		Last Modified: Mon, 29 Dec 2025 23:21:53 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac8e82e01a1db4cc233e5dbd8d55fabe6d0bd6a1054f8d4de384afd7d6feb2`  
		Last Modified: Mon, 29 Dec 2025 23:22:02 GMT  
		Size: 591.6 MB (591626795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:e3d29985b25e02b3b6a90a7604a0f196bbebbb5a28627f5d3d227d44dbcd856d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1900668bc3a5e6c83a877a880e3cac853d615d7328cf7994004a6c9a031d80`

```dockerfile
```

-	Layers:
	-	`sha256:906ed3303f7f61337f39822b8214a83bf6701ce24504ab71585ca891197cfed1`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c16428de8f412befe040c1b5cb388bdd0663ecee5cc13bf70e7ddf78819791`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim-bullseye`

```console
$ docker pull haskell@sha256:06fd4915fab64cc907db21681c6c2ee840dcd8041008577262b8c42121102213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim-bullseye` - linux; amd64

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

### `haskell:9-slim-bullseye` - unknown; unknown

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

### `haskell:9-slim-bullseye` - linux; arm64 variant v8

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

### `haskell:9-slim-bullseye` - unknown; unknown

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

## `haskell:9.10`

```console
$ docker pull haskell@sha256:cea76117ba2bf3e8110b9a849823e0d43deae6e2b2c39e3faf1e0c8475dcdcf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10` - linux; amd64

```console
$ docker pull haskell@sha256:00294c6703b73b9bbb558d5d65c71be1c7c0a17190a79f758f8b9896f5200698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659154185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5bcc4f528a3fedbe74d658c13e262c3a06ee98ee2127fc5d082318dd435683`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:37 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:19:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:17 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dd594824971fffd646434acd2f8cb944285d5662248793e7f5c1c652dd114`  
		Last Modified: Mon, 29 Dec 2025 23:20:52 GMT  
		Size: 133.8 MB (133759018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b890bf7f170ec3762847be6a1ba63596af0d5ff77f5c4c3780b95f3cb1e56e`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246a67688b8a1355ed3e249780619237cf63c0e6a4cfd98a22cd8a54c7685eca`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbd7e04f4d501c556cc4d1d45d8270f66600167280999f842ac8b88c68d8538`  
		Last Modified: Mon, 29 Dec 2025 23:21:45 GMT  
		Size: 441.8 MB (441805720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10` - unknown; unknown

```console
$ docker pull haskell@sha256:a52a1555c472e2ad5d8dcc7b60d8c34c075a152cd15a9b6374d3342373b0eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b55c9eb1d1092bc250758b0ae82591aec75e34fe61f4d6dd2d24e9050ebc2c`

```dockerfile
```

-	Layers:
	-	`sha256:d0371a3f0a3050fe378fe4d3fa46310837f121aad22e649c685ce8f50966d629`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffe3a711aa7b09bd9aaca3a75ad1409b4ddd813898dbdac1935e921fdfd9647`  
		Last Modified: Tue, 30 Dec 2025 03:48:55 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f3275e745ce464ed808e373238abbd4082b512a2c62b1efce4fa96d20ddef3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669448569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ac34b1c314183a7cc2c5e72cc03aab5cace727fa4948ff501a96cac069f2a9`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:16:57 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:59 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5280ec1a5df44236392d8b14bc966469c8c234eb70e8c65f31a370a3b097659`  
		Last Modified: Mon, 29 Dec 2025 23:20:19 GMT  
		Size: 129.2 MB (129240390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35c2ef41b84da2a8492d69e5fe7209cf5338d9a0010a204d06e87d088a687e`  
		Last Modified: Mon, 29 Dec 2025 23:20:09 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600ca497b466ab826688c761749af75c8e8a945a31f64e77480c3a540ec8b9b4`  
		Last Modified: Mon, 29 Dec 2025 23:20:08 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65a9628a3fd7f16cfbd6bf3b7c96b4c813428b9455cf994e163256726cf69d`  
		Last Modified: Mon, 29 Dec 2025 23:22:04 GMT  
		Size: 449.4 MB (449448901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10` - unknown; unknown

```console
$ docker pull haskell@sha256:3add895d061fd10533b9ecead6bea7abf3dcf90882baf1a75c05a505860ea761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b560cd801061656c03e8103be090f777480bef3726076902616cf5fa5436c60b`

```dockerfile
```

-	Layers:
	-	`sha256:a28e7344b8f75cfff907d15034128ee3784f9afd291da7bdfeb2005b6efa857c`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01081a13d3bb59b97c2a776f3adb9bae72653eb9b007be9b36bb7919a286392`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26451 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-bookworm`

```console
$ docker pull haskell@sha256:ff414d90dcd2ff179fc803d9fc3a85b13983be20274f8581136b9f13be230ccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:ef4391390604e36d66ae0a13cd55cf89ad03b9402366ebcdc9dca0e408f9c8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672787590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1178cff285dd4e70eef87e00457f8e650f98600c7bb69194bf9d56e690ff2a05`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:58 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:58 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:01 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:01 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:01 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:35 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a2749309fc51e616273f7f4b2fec8da9ce8458eb690a081bac91d99843296d`  
		Last Modified: Mon, 29 Dec 2025 23:20:23 GMT  
		Size: 152.4 MB (152360281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dc2c6e97370d8b3401b50a1e6dcb3ece64dc8be6ec9351cf3b84d0f051b81b`  
		Last Modified: Mon, 29 Dec 2025 23:20:07 GMT  
		Size: 22.2 MB (22220768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6fd8ad855480435b74e1875e7e2be1775be3be58fd5dc747257abbd2106dde`  
		Last Modified: Mon, 29 Dec 2025 23:20:06 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce57a1aa67bda45450161020082adb4ff1fa5c75b4499c22c60625e81077944`  
		Last Modified: Mon, 29 Dec 2025 23:21:14 GMT  
		Size: 442.1 MB (442118690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:bcd8e4e248646ff513a5def3d867428d5408a320f9e0b1f7dd3b619b70bd5933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834d69a70fecabe13404c6c2fb3e0a2ac0ea652e3d0f7463fb9cd5d5acbffd93`

```dockerfile
```

-	Layers:
	-	`sha256:e427f3dca1bdb34ec8aef686870d51ce8f8a9b6b155405bb70a969f9d83c0ced`  
		Last Modified: Tue, 30 Dec 2025 03:49:22 GMT  
		Size: 9.5 MB (9478462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b131ed4406b0e5050ead085c3863fc8c1b69c20bc594a21491b913595f1442cb`  
		Last Modified: Tue, 30 Dec 2025 03:49:23 GMT  
		Size: 25.4 KB (25354 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc94da0d0ecef5cc5a5d8afcee36f981cbc5713cc43aa4fd3acf230155d6eb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.7 MB (682746914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67ab599ba0d9a1c500253e2ff828ac580d3694e0d29120f9289b29315ca96f0`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:15:49 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:15:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:15:49 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:15:49 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:15:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:15:52 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:15:52 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:15:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:15:54 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:15:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:17:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:17:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:17:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef06fce84d20a74f1b516ede1991cffb34230509843f1cca42b7c54405dee2e`  
		Last Modified: Mon, 29 Dec 2025 23:19:12 GMT  
		Size: 146.4 MB (146441870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc5671be132e6de5d476541e4da042660610c28ca446698e6db1b0ddd3b9c2`  
		Last Modified: Mon, 29 Dec 2025 23:19:07 GMT  
		Size: 24.5 MB (24528556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98642ec65b5e9f2c65e33f46ccde5f2c5d84f48fd4ff43f49f7cf555cee37fdd`  
		Last Modified: Mon, 29 Dec 2025 23:19:06 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75016b0a3420941d3b17d3e69d67a168a3fc78be31dbf5957ecb8da75bd16b9b`  
		Last Modified: Mon, 29 Dec 2025 23:19:13 GMT  
		Size: 449.4 MB (449448319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:98fc5e693c8834dcc2be0283db4b46cfca9b8f405f7a8703d424c755161ec74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9531727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd07bf931d7b4b8983220e6ee0653533b13644c3cc6a6cf91d424dc9b08ae638`

```dockerfile
```

-	Layers:
	-	`sha256:a78e200148e9d3d1d0f611f3618f101073143b47c37ab8a89ae15ce711bf3c5d`  
		Last Modified: Tue, 30 Dec 2025 03:49:32 GMT  
		Size: 9.5 MB (9506246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:061a814c1b3680f9f76bc23e270a74947bc6afa20e60ccbf4f1f173403581614`  
		Last Modified: Tue, 30 Dec 2025 03:49:33 GMT  
		Size: 25.5 KB (25481 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-bullseye`

```console
$ docker pull haskell@sha256:cea76117ba2bf3e8110b9a849823e0d43deae6e2b2c39e3faf1e0c8475dcdcf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:00294c6703b73b9bbb558d5d65c71be1c7c0a17190a79f758f8b9896f5200698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659154185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5bcc4f528a3fedbe74d658c13e262c3a06ee98ee2127fc5d082318dd435683`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:37 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:19:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:17 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dd594824971fffd646434acd2f8cb944285d5662248793e7f5c1c652dd114`  
		Last Modified: Mon, 29 Dec 2025 23:20:52 GMT  
		Size: 133.8 MB (133759018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b890bf7f170ec3762847be6a1ba63596af0d5ff77f5c4c3780b95f3cb1e56e`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246a67688b8a1355ed3e249780619237cf63c0e6a4cfd98a22cd8a54c7685eca`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbd7e04f4d501c556cc4d1d45d8270f66600167280999f842ac8b88c68d8538`  
		Last Modified: Mon, 29 Dec 2025 23:21:45 GMT  
		Size: 441.8 MB (441805720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a52a1555c472e2ad5d8dcc7b60d8c34c075a152cd15a9b6374d3342373b0eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b55c9eb1d1092bc250758b0ae82591aec75e34fe61f4d6dd2d24e9050ebc2c`

```dockerfile
```

-	Layers:
	-	`sha256:d0371a3f0a3050fe378fe4d3fa46310837f121aad22e649c685ce8f50966d629`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffe3a711aa7b09bd9aaca3a75ad1409b4ddd813898dbdac1935e921fdfd9647`  
		Last Modified: Tue, 30 Dec 2025 03:48:55 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f3275e745ce464ed808e373238abbd4082b512a2c62b1efce4fa96d20ddef3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669448569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ac34b1c314183a7cc2c5e72cc03aab5cace727fa4948ff501a96cac069f2a9`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:16:57 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:59 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5280ec1a5df44236392d8b14bc966469c8c234eb70e8c65f31a370a3b097659`  
		Last Modified: Mon, 29 Dec 2025 23:20:19 GMT  
		Size: 129.2 MB (129240390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35c2ef41b84da2a8492d69e5fe7209cf5338d9a0010a204d06e87d088a687e`  
		Last Modified: Mon, 29 Dec 2025 23:20:09 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600ca497b466ab826688c761749af75c8e8a945a31f64e77480c3a540ec8b9b4`  
		Last Modified: Mon, 29 Dec 2025 23:20:08 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65a9628a3fd7f16cfbd6bf3b7c96b4c813428b9455cf994e163256726cf69d`  
		Last Modified: Mon, 29 Dec 2025 23:22:04 GMT  
		Size: 449.4 MB (449448901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:3add895d061fd10533b9ecead6bea7abf3dcf90882baf1a75c05a505860ea761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b560cd801061656c03e8103be090f777480bef3726076902616cf5fa5436c60b`

```dockerfile
```

-	Layers:
	-	`sha256:a28e7344b8f75cfff907d15034128ee3784f9afd291da7bdfeb2005b6efa857c`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01081a13d3bb59b97c2a776f3adb9bae72653eb9b007be9b36bb7919a286392`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26451 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-slim-bookworm`

```console
$ docker pull haskell@sha256:d897bd320156ede4c79e6de7263372d37480ba3068e4ee48ae4d2d869fcdde27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:0635e9e9541a194bb0c67d48bbf4d181e8569aef20db50af94b7191fab5f9db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.6 MB (624578952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4bfc8aa1722833a776705bc12374cb7a89ce866c337733b97d6450deb8f88c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:58 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:58 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:01 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:01 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:01 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a366a4ab777c56b0482b8e3930e460ba35085549b470558915dcd73c0395da`  
		Last Modified: Mon, 29 Dec 2025 23:20:30 GMT  
		Size: 124.4 MB (124405989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53e8714c8b1a6761e8187f57497c3f007c24c609477f742f556dd5d9c3cf8cf`  
		Last Modified: Mon, 29 Dec 2025 23:20:21 GMT  
		Size: 22.2 MB (22220755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6fd8ad855480435b74e1875e7e2be1775be3be58fd5dc747257abbd2106dde`  
		Last Modified: Mon, 29 Dec 2025 23:20:06 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9e35a1da32875c0fb1c548db1fd8ce25b5d1d8d5d00615e9cb30dfeff9f955`  
		Last Modified: Mon, 29 Dec 2025 23:20:29 GMT  
		Size: 442.1 MB (442116729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:82d99c472c017a882c24c4dedd305c4fe887e0fd495e93ff4f7cb69d33d78386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6595e4e3ce35fac8164a57bf3890e85acb5a18972397c82ef49a3af34aece8`

```dockerfile
```

-	Layers:
	-	`sha256:629a3beaeac7fa6da611f96b2b7369263e6a4c331f140194e973656d58fe222a`  
		Last Modified: Tue, 30 Dec 2025 03:49:32 GMT  
		Size: 6.6 MB (6606023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899ba3086646cb6207648d26e49148a6868262db4d0ab388d600970da13555d4`  
		Last Modified: Tue, 30 Dec 2025 03:49:33 GMT  
		Size: 25.4 KB (25397 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:758ed1a8d4e71324df535dd5a541898f9c11d0a26c465950bfb0ff466662228c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 MB (634532456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d8d7400123c7e7745841966d9f3c56688b01b5cc8154c96fe234b86ddd6329`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:27 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:27 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:27 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:29 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:29 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:31 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:16:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:01 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:01 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:01 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789d4e0999c7b36f9a51b8207ee4dafde60bc37447db853501689e22097319d1`  
		Last Modified: Mon, 29 Dec 2025 23:19:45 GMT  
		Size: 118.5 MB (118483985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e981c16461d144966fd980ffa4e3e491c41272e2533d26f70a904c87e3abae2d`  
		Last Modified: Mon, 29 Dec 2025 23:19:37 GMT  
		Size: 24.5 MB (24528542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f6287c49b89f8efdc3f1400d711d2b85670a8c0da04636762deb907435fc2b`  
		Last Modified: Mon, 29 Dec 2025 23:19:36 GMT  
		Size: 14.0 MB (13969025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbd4315529adc8be84f6b23eafed908917c3f34b0b62a2337f024794c63882a`  
		Last Modified: Mon, 29 Dec 2025 23:19:47 GMT  
		Size: 449.4 MB (449448694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:bb0e428fbb588edcaf046cb79e8e27d6ddc21aef478fefa448396ec7c68c952f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cf5c433d1839464e6443c03735392f1195f0b5cd2070add052b8b2e0fb9925`

```dockerfile
```

-	Layers:
	-	`sha256:e1fc6c7e6e4e6e707b92a587d45aaaf12b02aa837311e1f3070901c813467c3f`  
		Last Modified: Tue, 30 Dec 2025 03:49:39 GMT  
		Size: 6.6 MB (6634434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3058386c82156f470f65741017aa282ce112f5a413fc99616e3a71a368956c63`  
		Last Modified: Tue, 30 Dec 2025 03:50:05 GMT  
		Size: 25.5 KB (25524 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-slim-bullseye`

```console
$ docker pull haskell@sha256:06fd4915fab64cc907db21681c6c2ee840dcd8041008577262b8c42121102213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-slim-bullseye` - linux; amd64

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

### `haskell:9.10-slim-bullseye` - unknown; unknown

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

### `haskell:9.10-slim-bullseye` - linux; arm64 variant v8

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

### `haskell:9.10-slim-bullseye` - unknown; unknown

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

## `haskell:9.10.3`

```console
$ docker pull haskell@sha256:cea76117ba2bf3e8110b9a849823e0d43deae6e2b2c39e3faf1e0c8475dcdcf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3` - linux; amd64

```console
$ docker pull haskell@sha256:00294c6703b73b9bbb558d5d65c71be1c7c0a17190a79f758f8b9896f5200698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659154185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5bcc4f528a3fedbe74d658c13e262c3a06ee98ee2127fc5d082318dd435683`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:37 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:19:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:17 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dd594824971fffd646434acd2f8cb944285d5662248793e7f5c1c652dd114`  
		Last Modified: Mon, 29 Dec 2025 23:20:52 GMT  
		Size: 133.8 MB (133759018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b890bf7f170ec3762847be6a1ba63596af0d5ff77f5c4c3780b95f3cb1e56e`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246a67688b8a1355ed3e249780619237cf63c0e6a4cfd98a22cd8a54c7685eca`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbd7e04f4d501c556cc4d1d45d8270f66600167280999f842ac8b88c68d8538`  
		Last Modified: Mon, 29 Dec 2025 23:21:45 GMT  
		Size: 441.8 MB (441805720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3` - unknown; unknown

```console
$ docker pull haskell@sha256:a52a1555c472e2ad5d8dcc7b60d8c34c075a152cd15a9b6374d3342373b0eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b55c9eb1d1092bc250758b0ae82591aec75e34fe61f4d6dd2d24e9050ebc2c`

```dockerfile
```

-	Layers:
	-	`sha256:d0371a3f0a3050fe378fe4d3fa46310837f121aad22e649c685ce8f50966d629`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffe3a711aa7b09bd9aaca3a75ad1409b4ddd813898dbdac1935e921fdfd9647`  
		Last Modified: Tue, 30 Dec 2025 03:48:55 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f3275e745ce464ed808e373238abbd4082b512a2c62b1efce4fa96d20ddef3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669448569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ac34b1c314183a7cc2c5e72cc03aab5cace727fa4948ff501a96cac069f2a9`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:16:57 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:59 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5280ec1a5df44236392d8b14bc966469c8c234eb70e8c65f31a370a3b097659`  
		Last Modified: Mon, 29 Dec 2025 23:20:19 GMT  
		Size: 129.2 MB (129240390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35c2ef41b84da2a8492d69e5fe7209cf5338d9a0010a204d06e87d088a687e`  
		Last Modified: Mon, 29 Dec 2025 23:20:09 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600ca497b466ab826688c761749af75c8e8a945a31f64e77480c3a540ec8b9b4`  
		Last Modified: Mon, 29 Dec 2025 23:20:08 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65a9628a3fd7f16cfbd6bf3b7c96b4c813428b9455cf994e163256726cf69d`  
		Last Modified: Mon, 29 Dec 2025 23:22:04 GMT  
		Size: 449.4 MB (449448901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3` - unknown; unknown

```console
$ docker pull haskell@sha256:3add895d061fd10533b9ecead6bea7abf3dcf90882baf1a75c05a505860ea761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b560cd801061656c03e8103be090f777480bef3726076902616cf5fa5436c60b`

```dockerfile
```

-	Layers:
	-	`sha256:a28e7344b8f75cfff907d15034128ee3784f9afd291da7bdfeb2005b6efa857c`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01081a13d3bb59b97c2a776f3adb9bae72653eb9b007be9b36bb7919a286392`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26451 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-bookworm`

```console
$ docker pull haskell@sha256:ff414d90dcd2ff179fc803d9fc3a85b13983be20274f8581136b9f13be230ccd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:ef4391390604e36d66ae0a13cd55cf89ad03b9402366ebcdc9dca0e408f9c8e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672787590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1178cff285dd4e70eef87e00457f8e650f98600c7bb69194bf9d56e690ff2a05`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:58 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:58 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:01 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:01 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:01 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:35 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:35 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a2749309fc51e616273f7f4b2fec8da9ce8458eb690a081bac91d99843296d`  
		Last Modified: Mon, 29 Dec 2025 23:20:23 GMT  
		Size: 152.4 MB (152360281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dc2c6e97370d8b3401b50a1e6dcb3ece64dc8be6ec9351cf3b84d0f051b81b`  
		Last Modified: Mon, 29 Dec 2025 23:20:07 GMT  
		Size: 22.2 MB (22220768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6fd8ad855480435b74e1875e7e2be1775be3be58fd5dc747257abbd2106dde`  
		Last Modified: Mon, 29 Dec 2025 23:20:06 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce57a1aa67bda45450161020082adb4ff1fa5c75b4499c22c60625e81077944`  
		Last Modified: Mon, 29 Dec 2025 23:21:14 GMT  
		Size: 442.1 MB (442118690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:bcd8e4e248646ff513a5def3d867428d5408a320f9e0b1f7dd3b619b70bd5933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:834d69a70fecabe13404c6c2fb3e0a2ac0ea652e3d0f7463fb9cd5d5acbffd93`

```dockerfile
```

-	Layers:
	-	`sha256:e427f3dca1bdb34ec8aef686870d51ce8f8a9b6b155405bb70a969f9d83c0ced`  
		Last Modified: Tue, 30 Dec 2025 03:49:22 GMT  
		Size: 9.5 MB (9478462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b131ed4406b0e5050ead085c3863fc8c1b69c20bc594a21491b913595f1442cb`  
		Last Modified: Tue, 30 Dec 2025 03:49:23 GMT  
		Size: 25.4 KB (25354 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:dc94da0d0ecef5cc5a5d8afcee36f981cbc5713cc43aa4fd3acf230155d6eb50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.7 MB (682746914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a67ab599ba0d9a1c500253e2ff828ac580d3694e0d29120f9289b29315ca96f0`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:15:49 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:15:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:15:49 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:15:49 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:15:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:15:52 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:15:52 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:15:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:15:54 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:15:54 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:17:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:17:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:17:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef06fce84d20a74f1b516ede1991cffb34230509843f1cca42b7c54405dee2e`  
		Last Modified: Mon, 29 Dec 2025 23:19:12 GMT  
		Size: 146.4 MB (146441870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bc5671be132e6de5d476541e4da042660610c28ca446698e6db1b0ddd3b9c2`  
		Last Modified: Mon, 29 Dec 2025 23:19:07 GMT  
		Size: 24.5 MB (24528556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98642ec65b5e9f2c65e33f46ccde5f2c5d84f48fd4ff43f49f7cf555cee37fdd`  
		Last Modified: Mon, 29 Dec 2025 23:19:06 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75016b0a3420941d3b17d3e69d67a168a3fc78be31dbf5957ecb8da75bd16b9b`  
		Last Modified: Mon, 29 Dec 2025 23:19:13 GMT  
		Size: 449.4 MB (449448319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:98fc5e693c8834dcc2be0283db4b46cfca9b8f405f7a8703d424c755161ec74e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9531727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd07bf931d7b4b8983220e6ee0653533b13644c3cc6a6cf91d424dc9b08ae638`

```dockerfile
```

-	Layers:
	-	`sha256:a78e200148e9d3d1d0f611f3618f101073143b47c37ab8a89ae15ce711bf3c5d`  
		Last Modified: Tue, 30 Dec 2025 03:49:32 GMT  
		Size: 9.5 MB (9506246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:061a814c1b3680f9f76bc23e270a74947bc6afa20e60ccbf4f1f173403581614`  
		Last Modified: Tue, 30 Dec 2025 03:49:33 GMT  
		Size: 25.5 KB (25481 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-bullseye`

```console
$ docker pull haskell@sha256:cea76117ba2bf3e8110b9a849823e0d43deae6e2b2c39e3faf1e0c8475dcdcf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:00294c6703b73b9bbb558d5d65c71be1c7c0a17190a79f758f8b9896f5200698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659154185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5bcc4f528a3fedbe74d658c13e262c3a06ee98ee2127fc5d082318dd435683`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:37 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:19:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:17 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dd594824971fffd646434acd2f8cb944285d5662248793e7f5c1c652dd114`  
		Last Modified: Mon, 29 Dec 2025 23:20:52 GMT  
		Size: 133.8 MB (133759018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b890bf7f170ec3762847be6a1ba63596af0d5ff77f5c4c3780b95f3cb1e56e`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246a67688b8a1355ed3e249780619237cf63c0e6a4cfd98a22cd8a54c7685eca`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbd7e04f4d501c556cc4d1d45d8270f66600167280999f842ac8b88c68d8538`  
		Last Modified: Mon, 29 Dec 2025 23:21:45 GMT  
		Size: 441.8 MB (441805720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a52a1555c472e2ad5d8dcc7b60d8c34c075a152cd15a9b6374d3342373b0eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b55c9eb1d1092bc250758b0ae82591aec75e34fe61f4d6dd2d24e9050ebc2c`

```dockerfile
```

-	Layers:
	-	`sha256:d0371a3f0a3050fe378fe4d3fa46310837f121aad22e649c685ce8f50966d629`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffe3a711aa7b09bd9aaca3a75ad1409b4ddd813898dbdac1935e921fdfd9647`  
		Last Modified: Tue, 30 Dec 2025 03:48:55 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f3275e745ce464ed808e373238abbd4082b512a2c62b1efce4fa96d20ddef3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669448569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ac34b1c314183a7cc2c5e72cc03aab5cace727fa4948ff501a96cac069f2a9`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:16:57 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:59 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5280ec1a5df44236392d8b14bc966469c8c234eb70e8c65f31a370a3b097659`  
		Last Modified: Mon, 29 Dec 2025 23:20:19 GMT  
		Size: 129.2 MB (129240390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35c2ef41b84da2a8492d69e5fe7209cf5338d9a0010a204d06e87d088a687e`  
		Last Modified: Mon, 29 Dec 2025 23:20:09 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600ca497b466ab826688c761749af75c8e8a945a31f64e77480c3a540ec8b9b4`  
		Last Modified: Mon, 29 Dec 2025 23:20:08 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65a9628a3fd7f16cfbd6bf3b7c96b4c813428b9455cf994e163256726cf69d`  
		Last Modified: Mon, 29 Dec 2025 23:22:04 GMT  
		Size: 449.4 MB (449448901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:3add895d061fd10533b9ecead6bea7abf3dcf90882baf1a75c05a505860ea761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b560cd801061656c03e8103be090f777480bef3726076902616cf5fa5436c60b`

```dockerfile
```

-	Layers:
	-	`sha256:a28e7344b8f75cfff907d15034128ee3784f9afd291da7bdfeb2005b6efa857c`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01081a13d3bb59b97c2a776f3adb9bae72653eb9b007be9b36bb7919a286392`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26451 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-slim-bookworm`

```console
$ docker pull haskell@sha256:d897bd320156ede4c79e6de7263372d37480ba3068e4ee48ae4d2d869fcdde27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:0635e9e9541a194bb0c67d48bbf4d181e8569aef20db50af94b7191fab5f9db7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.6 MB (624578952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4bfc8aa1722833a776705bc12374cb7a89ce866c337733b97d6450deb8f88c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:58 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:58 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:58 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:00 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:00 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:01 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:01 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:01 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54a366a4ab777c56b0482b8e3930e460ba35085549b470558915dcd73c0395da`  
		Last Modified: Mon, 29 Dec 2025 23:20:30 GMT  
		Size: 124.4 MB (124405989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53e8714c8b1a6761e8187f57497c3f007c24c609477f742f556dd5d9c3cf8cf`  
		Last Modified: Mon, 29 Dec 2025 23:20:21 GMT  
		Size: 22.2 MB (22220755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6fd8ad855480435b74e1875e7e2be1775be3be58fd5dc747257abbd2106dde`  
		Last Modified: Mon, 29 Dec 2025 23:20:06 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9e35a1da32875c0fb1c548db1fd8ce25b5d1d8d5d00615e9cb30dfeff9f955`  
		Last Modified: Mon, 29 Dec 2025 23:20:29 GMT  
		Size: 442.1 MB (442116729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:82d99c472c017a882c24c4dedd305c4fe887e0fd495e93ff4f7cb69d33d78386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6595e4e3ce35fac8164a57bf3890e85acb5a18972397c82ef49a3af34aece8`

```dockerfile
```

-	Layers:
	-	`sha256:629a3beaeac7fa6da611f96b2b7369263e6a4c331f140194e973656d58fe222a`  
		Last Modified: Tue, 30 Dec 2025 03:49:32 GMT  
		Size: 6.6 MB (6606023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:899ba3086646cb6207648d26e49148a6868262db4d0ab388d600970da13555d4`  
		Last Modified: Tue, 30 Dec 2025 03:49:33 GMT  
		Size: 25.4 KB (25397 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:758ed1a8d4e71324df535dd5a541898f9c11d0a26c465950bfb0ff466662228c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 MB (634532456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2d8d7400123c7e7745841966d9f3c56688b01b5cc8154c96fe234b86ddd6329`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:27 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:27 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:27 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:27 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:29 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:29 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:31 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:16:31 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:01 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:01 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:01 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789d4e0999c7b36f9a51b8207ee4dafde60bc37447db853501689e22097319d1`  
		Last Modified: Mon, 29 Dec 2025 23:19:45 GMT  
		Size: 118.5 MB (118483985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e981c16461d144966fd980ffa4e3e491c41272e2533d26f70a904c87e3abae2d`  
		Last Modified: Mon, 29 Dec 2025 23:19:37 GMT  
		Size: 24.5 MB (24528542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f6287c49b89f8efdc3f1400d711d2b85670a8c0da04636762deb907435fc2b`  
		Last Modified: Mon, 29 Dec 2025 23:19:36 GMT  
		Size: 14.0 MB (13969025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbd4315529adc8be84f6b23eafed908917c3f34b0b62a2337f024794c63882a`  
		Last Modified: Mon, 29 Dec 2025 23:19:47 GMT  
		Size: 449.4 MB (449448694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:bb0e428fbb588edcaf046cb79e8e27d6ddc21aef478fefa448396ec7c68c952f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cf5c433d1839464e6443c03735392f1195f0b5cd2070add052b8b2e0fb9925`

```dockerfile
```

-	Layers:
	-	`sha256:e1fc6c7e6e4e6e707b92a587d45aaaf12b02aa837311e1f3070901c813467c3f`  
		Last Modified: Tue, 30 Dec 2025 03:49:39 GMT  
		Size: 6.6 MB (6634434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3058386c82156f470f65741017aa282ce112f5a413fc99616e3a71a368956c63`  
		Last Modified: Tue, 30 Dec 2025 03:50:05 GMT  
		Size: 25.5 KB (25524 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-slim-bullseye`

```console
$ docker pull haskell@sha256:06fd4915fab64cc907db21681c6c2ee840dcd8041008577262b8c42121102213
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-slim-bullseye` - linux; amd64

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

### `haskell:9.10.3-slim-bullseye` - unknown; unknown

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

### `haskell:9.10.3-slim-bullseye` - linux; arm64 variant v8

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

### `haskell:9.10.3-slim-bullseye` - unknown; unknown

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

## `haskell:9.12`

```console
$ docker pull haskell@sha256:590e9e9c918d1c7b0a87badb0a6449105732fa0b7152be87ecfc149576d09614
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12` - linux; amd64

```console
$ docker pull haskell@sha256:5906cacce760379bcdc745eb02f756846ca4a0fa213ad3b21604c4095c61403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822424053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5191a918085facf1d579e06d8b7976ae263fcec63b12d04d5114171e9b9bce1f`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851bd5b066c6bc5263113a72ba6b03f8cd26c0e11ec21b4faee09fd49138f9ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 152.4 MB (152360257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7702220116f89c51e73d9030008d264fb0d258f70cdeb0d47124192649a8a8b`  
		Last Modified: Mon, 29 Dec 2025 23:20:33 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d7dacad299c850062d8a60ca3d62f23a1fb27e132af8d6a96b6c5c092153f`  
		Last Modified: Mon, 29 Dec 2025 23:21:18 GMT  
		Size: 591.8 MB (591755193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12` - unknown; unknown

```console
$ docker pull haskell@sha256:c69dd9d58a2b4448bae5da7b44258efdf56f2b65fdfe2f1a425957c533faa84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620bcbc4e5d5426966bf9ea47bf486a0deef8d2b58e5aa9138e8c9a2d2277789`

```dockerfile
```

-	Layers:
	-	`sha256:a7c0c8cc14b721859c072fa36cd314b05d699933152bfe89930e04763ca67b65`  
		Last Modified: Tue, 30 Dec 2025 03:48:44 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da0a224b9700730cef9f784ff1c3bb008a0263ca3fdb5450e166255f06b420f`  
		Last Modified: Tue, 30 Dec 2025 03:48:45 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:bd4d7f122bfeb2b8ca0c8b666401862e03a7d2e91efd424f16f6e9687e765644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824926337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8255e5e92ffc6a0d411a4c3fdfa15b5a1aea3bec710d3ac9048714708a2483a1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c29931c3e00184d8309814c6bb94b8eae48b8d44cd8bb0b34c0a96704a32e1`  
		Last Modified: Mon, 29 Dec 2025 23:22:32 GMT  
		Size: 146.4 MB (146442606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd77a5299206d5e51acf0a90a31f30864e48172b41eeb9ee9efb392da0d93d6b`  
		Last Modified: Mon, 29 Dec 2025 23:21:52 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea94209ec2fd884df59dfdc57f9ffbe524964ff8aa73611e3e3e09146f5b027`  
		Last Modified: Mon, 29 Dec 2025 23:21:54 GMT  
		Size: 14.0 MB (13969019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e41e6094016ad14b3382f6e3587baeda522cea539bbf6ed42f7b692c200574`  
		Last Modified: Mon, 29 Dec 2025 23:22:26 GMT  
		Size: 591.6 MB (591627013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12` - unknown; unknown

```console
$ docker pull haskell@sha256:31602177a7c7a147780a5579401ae9cd255111cc88275dc22e9aa05020184ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802e3273d59f837cff1550dd346cfe9d8495d6eafd81ef3bb361eb4af81a7555`

```dockerfile
```

-	Layers:
	-	`sha256:31c781c3abc8afecf26acbe00ddba616277b794b7932b9a23939a5a387d1da54`  
		Last Modified: Tue, 30 Dec 2025 03:48:53 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a259963f6a750d76c85f50b4a729093daf2b1543b7d7f0f56961c8853a9aa5`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12-bookworm`

```console
$ docker pull haskell@sha256:590e9e9c918d1c7b0a87badb0a6449105732fa0b7152be87ecfc149576d09614
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:5906cacce760379bcdc745eb02f756846ca4a0fa213ad3b21604c4095c61403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822424053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5191a918085facf1d579e06d8b7976ae263fcec63b12d04d5114171e9b9bce1f`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851bd5b066c6bc5263113a72ba6b03f8cd26c0e11ec21b4faee09fd49138f9ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 152.4 MB (152360257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7702220116f89c51e73d9030008d264fb0d258f70cdeb0d47124192649a8a8b`  
		Last Modified: Mon, 29 Dec 2025 23:20:33 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d7dacad299c850062d8a60ca3d62f23a1fb27e132af8d6a96b6c5c092153f`  
		Last Modified: Mon, 29 Dec 2025 23:21:18 GMT  
		Size: 591.8 MB (591755193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:c69dd9d58a2b4448bae5da7b44258efdf56f2b65fdfe2f1a425957c533faa84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620bcbc4e5d5426966bf9ea47bf486a0deef8d2b58e5aa9138e8c9a2d2277789`

```dockerfile
```

-	Layers:
	-	`sha256:a7c0c8cc14b721859c072fa36cd314b05d699933152bfe89930e04763ca67b65`  
		Last Modified: Tue, 30 Dec 2025 03:48:44 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da0a224b9700730cef9f784ff1c3bb008a0263ca3fdb5450e166255f06b420f`  
		Last Modified: Tue, 30 Dec 2025 03:48:45 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:bd4d7f122bfeb2b8ca0c8b666401862e03a7d2e91efd424f16f6e9687e765644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824926337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8255e5e92ffc6a0d411a4c3fdfa15b5a1aea3bec710d3ac9048714708a2483a1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c29931c3e00184d8309814c6bb94b8eae48b8d44cd8bb0b34c0a96704a32e1`  
		Last Modified: Mon, 29 Dec 2025 23:22:32 GMT  
		Size: 146.4 MB (146442606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd77a5299206d5e51acf0a90a31f30864e48172b41eeb9ee9efb392da0d93d6b`  
		Last Modified: Mon, 29 Dec 2025 23:21:52 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea94209ec2fd884df59dfdc57f9ffbe524964ff8aa73611e3e3e09146f5b027`  
		Last Modified: Mon, 29 Dec 2025 23:21:54 GMT  
		Size: 14.0 MB (13969019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e41e6094016ad14b3382f6e3587baeda522cea539bbf6ed42f7b692c200574`  
		Last Modified: Mon, 29 Dec 2025 23:22:26 GMT  
		Size: 591.6 MB (591627013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:31602177a7c7a147780a5579401ae9cd255111cc88275dc22e9aa05020184ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802e3273d59f837cff1550dd346cfe9d8495d6eafd81ef3bb361eb4af81a7555`

```dockerfile
```

-	Layers:
	-	`sha256:31c781c3abc8afecf26acbe00ddba616277b794b7932b9a23939a5a387d1da54`  
		Last Modified: Tue, 30 Dec 2025 03:48:53 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a259963f6a750d76c85f50b4a729093daf2b1543b7d7f0f56961c8853a9aa5`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12-slim-bookworm`

```console
$ docker pull haskell@sha256:634cc56adaa1dd9f2321f640fb45fcbcb8363153ab37a977f971ee150247412f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:97b16c440c491654aba4c95e9c3132e1e4e1a065a709cce713390d160ca74f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774212235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92003b13829d688409aab1d1c244ff262fed57faa9d1acc3eb83a72f7c26fe35`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:53 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:53 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b04edbc0c4dfa46fafd245a2b2a0b057b91d4a81d0914d396de56028f15ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:59 GMT  
		Size: 124.4 MB (124406228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100a9279ba93680fbe144ea31c9310ac12a0b5045f9db11db3a1e983e6e881ff`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36999b209606621dff474cc3fab4ecd44dddd3fe5c75bc92e440b6bb2f440a7f`  
		Last Modified: Mon, 29 Dec 2025 23:21:27 GMT  
		Size: 591.7 MB (591749776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:eb0a2eb25660433b057a136f94dd660e17aef1f7a886387332d0a202a350b679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beba287c9837e41e99ff8f16de2652cc3d58080378e0357676dbe31c6b1daef4`

```dockerfile
```

-	Layers:
	-	`sha256:c8203cc4441763cf885e243f30d1630bc4c9a2a8c9759cba1c9a00acd995af77`  
		Last Modified: Tue, 30 Dec 2025 03:49:01 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd8ac24ce53a5207506ee8d7470313245cad1af0536175db5dc5110cfb18fca`  
		Last Modified: Tue, 30 Dec 2025 03:49:02 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:436435637aade026aa72bc34a8d91add8d7b32abe92f5e260d08cb85ff2388c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776710338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d149018b8046249b7e234dcd59bd0503f2c249b1da5ea71b9d7d07a34c78a14`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:58 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6377ba840a84af4c909b1eb1ef8792c6e8706b5e4320bfcf8c5e0ff25014fa`  
		Last Modified: Mon, 29 Dec 2025 23:22:01 GMT  
		Size: 118.5 MB (118483759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf44bd0db910fbbca8952d8094f8283bf8770a881423599b00480f8af3efa80`  
		Last Modified: Mon, 29 Dec 2025 23:21:55 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10d58ac69a8b25366852eb5b7a018d15122af20d6ca8d9d4bda3a25c4a50923`  
		Last Modified: Mon, 29 Dec 2025 23:21:53 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac8e82e01a1db4cc233e5dbd8d55fabe6d0bd6a1054f8d4de384afd7d6feb2`  
		Last Modified: Mon, 29 Dec 2025 23:22:02 GMT  
		Size: 591.6 MB (591626795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:e3d29985b25e02b3b6a90a7604a0f196bbebbb5a28627f5d3d227d44dbcd856d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1900668bc3a5e6c83a877a880e3cac853d615d7328cf7994004a6c9a031d80`

```dockerfile
```

-	Layers:
	-	`sha256:906ed3303f7f61337f39822b8214a83bf6701ce24504ab71585ca891197cfed1`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c16428de8f412befe040c1b5cb388bdd0663ecee5cc13bf70e7ddf78819791`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2`

```console
$ docker pull haskell@sha256:590e9e9c918d1c7b0a87badb0a6449105732fa0b7152be87ecfc149576d09614
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2` - linux; amd64

```console
$ docker pull haskell@sha256:5906cacce760379bcdc745eb02f756846ca4a0fa213ad3b21604c4095c61403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822424053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5191a918085facf1d579e06d8b7976ae263fcec63b12d04d5114171e9b9bce1f`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851bd5b066c6bc5263113a72ba6b03f8cd26c0e11ec21b4faee09fd49138f9ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 152.4 MB (152360257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7702220116f89c51e73d9030008d264fb0d258f70cdeb0d47124192649a8a8b`  
		Last Modified: Mon, 29 Dec 2025 23:20:33 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d7dacad299c850062d8a60ca3d62f23a1fb27e132af8d6a96b6c5c092153f`  
		Last Modified: Mon, 29 Dec 2025 23:21:18 GMT  
		Size: 591.8 MB (591755193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2` - unknown; unknown

```console
$ docker pull haskell@sha256:c69dd9d58a2b4448bae5da7b44258efdf56f2b65fdfe2f1a425957c533faa84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620bcbc4e5d5426966bf9ea47bf486a0deef8d2b58e5aa9138e8c9a2d2277789`

```dockerfile
```

-	Layers:
	-	`sha256:a7c0c8cc14b721859c072fa36cd314b05d699933152bfe89930e04763ca67b65`  
		Last Modified: Tue, 30 Dec 2025 03:48:44 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da0a224b9700730cef9f784ff1c3bb008a0263ca3fdb5450e166255f06b420f`  
		Last Modified: Tue, 30 Dec 2025 03:48:45 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:bd4d7f122bfeb2b8ca0c8b666401862e03a7d2e91efd424f16f6e9687e765644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824926337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8255e5e92ffc6a0d411a4c3fdfa15b5a1aea3bec710d3ac9048714708a2483a1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c29931c3e00184d8309814c6bb94b8eae48b8d44cd8bb0b34c0a96704a32e1`  
		Last Modified: Mon, 29 Dec 2025 23:22:32 GMT  
		Size: 146.4 MB (146442606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd77a5299206d5e51acf0a90a31f30864e48172b41eeb9ee9efb392da0d93d6b`  
		Last Modified: Mon, 29 Dec 2025 23:21:52 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea94209ec2fd884df59dfdc57f9ffbe524964ff8aa73611e3e3e09146f5b027`  
		Last Modified: Mon, 29 Dec 2025 23:21:54 GMT  
		Size: 14.0 MB (13969019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e41e6094016ad14b3382f6e3587baeda522cea539bbf6ed42f7b692c200574`  
		Last Modified: Mon, 29 Dec 2025 23:22:26 GMT  
		Size: 591.6 MB (591627013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2` - unknown; unknown

```console
$ docker pull haskell@sha256:31602177a7c7a147780a5579401ae9cd255111cc88275dc22e9aa05020184ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802e3273d59f837cff1550dd346cfe9d8495d6eafd81ef3bb361eb4af81a7555`

```dockerfile
```

-	Layers:
	-	`sha256:31c781c3abc8afecf26acbe00ddba616277b794b7932b9a23939a5a387d1da54`  
		Last Modified: Tue, 30 Dec 2025 03:48:53 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a259963f6a750d76c85f50b4a729093daf2b1543b7d7f0f56961c8853a9aa5`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2-bookworm`

```console
$ docker pull haskell@sha256:590e9e9c918d1c7b0a87badb0a6449105732fa0b7152be87ecfc149576d09614
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:5906cacce760379bcdc745eb02f756846ca4a0fa213ad3b21604c4095c61403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822424053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5191a918085facf1d579e06d8b7976ae263fcec63b12d04d5114171e9b9bce1f`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851bd5b066c6bc5263113a72ba6b03f8cd26c0e11ec21b4faee09fd49138f9ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 152.4 MB (152360257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7702220116f89c51e73d9030008d264fb0d258f70cdeb0d47124192649a8a8b`  
		Last Modified: Mon, 29 Dec 2025 23:20:33 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d7dacad299c850062d8a60ca3d62f23a1fb27e132af8d6a96b6c5c092153f`  
		Last Modified: Mon, 29 Dec 2025 23:21:18 GMT  
		Size: 591.8 MB (591755193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:c69dd9d58a2b4448bae5da7b44258efdf56f2b65fdfe2f1a425957c533faa84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620bcbc4e5d5426966bf9ea47bf486a0deef8d2b58e5aa9138e8c9a2d2277789`

```dockerfile
```

-	Layers:
	-	`sha256:a7c0c8cc14b721859c072fa36cd314b05d699933152bfe89930e04763ca67b65`  
		Last Modified: Tue, 30 Dec 2025 03:48:44 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da0a224b9700730cef9f784ff1c3bb008a0263ca3fdb5450e166255f06b420f`  
		Last Modified: Tue, 30 Dec 2025 03:48:45 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:bd4d7f122bfeb2b8ca0c8b666401862e03a7d2e91efd424f16f6e9687e765644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824926337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8255e5e92ffc6a0d411a4c3fdfa15b5a1aea3bec710d3ac9048714708a2483a1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c29931c3e00184d8309814c6bb94b8eae48b8d44cd8bb0b34c0a96704a32e1`  
		Last Modified: Mon, 29 Dec 2025 23:22:32 GMT  
		Size: 146.4 MB (146442606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd77a5299206d5e51acf0a90a31f30864e48172b41eeb9ee9efb392da0d93d6b`  
		Last Modified: Mon, 29 Dec 2025 23:21:52 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea94209ec2fd884df59dfdc57f9ffbe524964ff8aa73611e3e3e09146f5b027`  
		Last Modified: Mon, 29 Dec 2025 23:21:54 GMT  
		Size: 14.0 MB (13969019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e41e6094016ad14b3382f6e3587baeda522cea539bbf6ed42f7b692c200574`  
		Last Modified: Mon, 29 Dec 2025 23:22:26 GMT  
		Size: 591.6 MB (591627013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:31602177a7c7a147780a5579401ae9cd255111cc88275dc22e9aa05020184ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802e3273d59f837cff1550dd346cfe9d8495d6eafd81ef3bb361eb4af81a7555`

```dockerfile
```

-	Layers:
	-	`sha256:31c781c3abc8afecf26acbe00ddba616277b794b7932b9a23939a5a387d1da54`  
		Last Modified: Tue, 30 Dec 2025 03:48:53 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a259963f6a750d76c85f50b4a729093daf2b1543b7d7f0f56961c8853a9aa5`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2-slim-bookworm`

```console
$ docker pull haskell@sha256:634cc56adaa1dd9f2321f640fb45fcbcb8363153ab37a977f971ee150247412f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:97b16c440c491654aba4c95e9c3132e1e4e1a065a709cce713390d160ca74f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774212235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92003b13829d688409aab1d1c244ff262fed57faa9d1acc3eb83a72f7c26fe35`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:53 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:53 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b04edbc0c4dfa46fafd245a2b2a0b057b91d4a81d0914d396de56028f15ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:59 GMT  
		Size: 124.4 MB (124406228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100a9279ba93680fbe144ea31c9310ac12a0b5045f9db11db3a1e983e6e881ff`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36999b209606621dff474cc3fab4ecd44dddd3fe5c75bc92e440b6bb2f440a7f`  
		Last Modified: Mon, 29 Dec 2025 23:21:27 GMT  
		Size: 591.7 MB (591749776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:eb0a2eb25660433b057a136f94dd660e17aef1f7a886387332d0a202a350b679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beba287c9837e41e99ff8f16de2652cc3d58080378e0357676dbe31c6b1daef4`

```dockerfile
```

-	Layers:
	-	`sha256:c8203cc4441763cf885e243f30d1630bc4c9a2a8c9759cba1c9a00acd995af77`  
		Last Modified: Tue, 30 Dec 2025 03:49:01 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd8ac24ce53a5207506ee8d7470313245cad1af0536175db5dc5110cfb18fca`  
		Last Modified: Tue, 30 Dec 2025 03:49:02 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:436435637aade026aa72bc34a8d91add8d7b32abe92f5e260d08cb85ff2388c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776710338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d149018b8046249b7e234dcd59bd0503f2c249b1da5ea71b9d7d07a34c78a14`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:58 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6377ba840a84af4c909b1eb1ef8792c6e8706b5e4320bfcf8c5e0ff25014fa`  
		Last Modified: Mon, 29 Dec 2025 23:22:01 GMT  
		Size: 118.5 MB (118483759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf44bd0db910fbbca8952d8094f8283bf8770a881423599b00480f8af3efa80`  
		Last Modified: Mon, 29 Dec 2025 23:21:55 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10d58ac69a8b25366852eb5b7a018d15122af20d6ca8d9d4bda3a25c4a50923`  
		Last Modified: Mon, 29 Dec 2025 23:21:53 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac8e82e01a1db4cc233e5dbd8d55fabe6d0bd6a1054f8d4de384afd7d6feb2`  
		Last Modified: Mon, 29 Dec 2025 23:22:02 GMT  
		Size: 591.6 MB (591626795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:e3d29985b25e02b3b6a90a7604a0f196bbebbb5a28627f5d3d227d44dbcd856d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1900668bc3a5e6c83a877a880e3cac853d615d7328cf7994004a6c9a031d80`

```dockerfile
```

-	Layers:
	-	`sha256:906ed3303f7f61337f39822b8214a83bf6701ce24504ab71585ca891197cfed1`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c16428de8f412befe040c1b5cb388bdd0663ecee5cc13bf70e7ddf78819791`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6`

```console
$ docker pull haskell@sha256:ee197b2550916718a4acebbd6079cc21ac412a80da28533bf1b273a3bffab9fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6` - linux; amd64

```console
$ docker pull haskell@sha256:dcdc7a260adb186ea9a1d84bb37019398eaa2692a62120338e60d03e53ce7a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641572506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14581b42f2fa47aedf9940f56417ac44fdaa19cd9f8cd9e7de49a8f0d60a9c96`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:40 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:43 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:43 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:19:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:02 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:02 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc45b2751c0570d52e1ca630c74bb147dfea1e527c053ca9fef0923a01f9ada`  
		Last Modified: Mon, 29 Dec 2025 23:20:36 GMT  
		Size: 133.8 MB (133759795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aa0a080cc3e3a2d547b9e7820b821cf056c3adbf42a1d5f2f4a7a462988164`  
		Last Modified: Mon, 29 Dec 2025 23:20:25 GMT  
		Size: 22.2 MB (22220750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff6bfb2cb17a902b7bf12dac7b1eba8b38d0a7f1cb930f394cc45b06ced3c9`  
		Last Modified: Mon, 29 Dec 2025 23:20:24 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca189d8f8ebf2257244bcde1e3d7efc9f83971f121b0915ba710701981d3f333`  
		Last Modified: Mon, 29 Dec 2025 23:21:05 GMT  
		Size: 424.2 MB (424223281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6` - unknown; unknown

```console
$ docker pull haskell@sha256:6d8c45471ff831e3a0e3bfe4fa133ea736503e9a873c8ce6311b4e4204d533b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6bfbfa9bd6fc76fd3205a4a0a90c58171632b8470a65151a6b03f1cbda488f`

```dockerfile
```

-	Layers:
	-	`sha256:0b99232fdc3a72fa0953cb7045a58f70264c741589c48d8e6df34ca7de3897d4`  
		Last Modified: Tue, 30 Dec 2025 03:50:06 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eace2ac7ddff76f3386c458baaf117e6778408e8ee4ec10d0191cdc1e187b13`  
		Last Modified: Tue, 30 Dec 2025 03:50:06 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:ef48a9cb78e1f1ff8e1dec303bc8158b6f1a0b60f0fe8ef71c8f1ce30f2b083a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.4 MB (658350385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a06a3f1c536105de241fa361d6a6de337e3fd981b14d685f0263c1e44a36b2`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:10 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:10 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:13 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:13 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:13 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:18:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacd905a06452b63a81f81c7231e6e0e0e62f693fc89fc18d653e123683805b7`  
		Last Modified: Mon, 29 Dec 2025 23:20:27 GMT  
		Size: 129.2 MB (129241121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e89c89eca88f416e9e0e4fd85bc697bcc271db258f7b5eeddb7909b369f0f6d`  
		Last Modified: Mon, 29 Dec 2025 23:20:15 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490e717c00b85b32b044071d3c25461d7f4f99ca5875012df088f9591118ab05`  
		Last Modified: Mon, 29 Dec 2025 23:20:13 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2b18a5c6d65207f10fc6c17b220858889d87734da0680d321d435bf3b6e9f`  
		Last Modified: Mon, 29 Dec 2025 23:22:34 GMT  
		Size: 438.3 MB (438349984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6` - unknown; unknown

```console
$ docker pull haskell@sha256:d37cccfae3680bb88f3906e5587152bd9bcbb8fed8cfef473320ae43035ffa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38057dd915c60923426cec1a895f8ddee1c73ec92a159653c62cc5b32e921ad`

```dockerfile
```

-	Layers:
	-	`sha256:860da3a4237265d52546a7bafaedc1d84413506d53d69533efe3d21a1425c059`  
		Last Modified: Tue, 30 Dec 2025 03:50:15 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460c6758f664568a346a6062ca935932e825f21f4efe6ae09dc82ed8e27e6c11`  
		Last Modified: Tue, 30 Dec 2025 03:50:16 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-bullseye`

```console
$ docker pull haskell@sha256:ee197b2550916718a4acebbd6079cc21ac412a80da28533bf1b273a3bffab9fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:dcdc7a260adb186ea9a1d84bb37019398eaa2692a62120338e60d03e53ce7a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641572506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14581b42f2fa47aedf9940f56417ac44fdaa19cd9f8cd9e7de49a8f0d60a9c96`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:40 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:43 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:43 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:19:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:02 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:02 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc45b2751c0570d52e1ca630c74bb147dfea1e527c053ca9fef0923a01f9ada`  
		Last Modified: Mon, 29 Dec 2025 23:20:36 GMT  
		Size: 133.8 MB (133759795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aa0a080cc3e3a2d547b9e7820b821cf056c3adbf42a1d5f2f4a7a462988164`  
		Last Modified: Mon, 29 Dec 2025 23:20:25 GMT  
		Size: 22.2 MB (22220750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff6bfb2cb17a902b7bf12dac7b1eba8b38d0a7f1cb930f394cc45b06ced3c9`  
		Last Modified: Mon, 29 Dec 2025 23:20:24 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca189d8f8ebf2257244bcde1e3d7efc9f83971f121b0915ba710701981d3f333`  
		Last Modified: Mon, 29 Dec 2025 23:21:05 GMT  
		Size: 424.2 MB (424223281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:6d8c45471ff831e3a0e3bfe4fa133ea736503e9a873c8ce6311b4e4204d533b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6bfbfa9bd6fc76fd3205a4a0a90c58171632b8470a65151a6b03f1cbda488f`

```dockerfile
```

-	Layers:
	-	`sha256:0b99232fdc3a72fa0953cb7045a58f70264c741589c48d8e6df34ca7de3897d4`  
		Last Modified: Tue, 30 Dec 2025 03:50:06 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eace2ac7ddff76f3386c458baaf117e6778408e8ee4ec10d0191cdc1e187b13`  
		Last Modified: Tue, 30 Dec 2025 03:50:06 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:ef48a9cb78e1f1ff8e1dec303bc8158b6f1a0b60f0fe8ef71c8f1ce30f2b083a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.4 MB (658350385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a06a3f1c536105de241fa361d6a6de337e3fd981b14d685f0263c1e44a36b2`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:10 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:10 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:13 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:13 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:13 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:18:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacd905a06452b63a81f81c7231e6e0e0e62f693fc89fc18d653e123683805b7`  
		Last Modified: Mon, 29 Dec 2025 23:20:27 GMT  
		Size: 129.2 MB (129241121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e89c89eca88f416e9e0e4fd85bc697bcc271db258f7b5eeddb7909b369f0f6d`  
		Last Modified: Mon, 29 Dec 2025 23:20:15 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490e717c00b85b32b044071d3c25461d7f4f99ca5875012df088f9591118ab05`  
		Last Modified: Mon, 29 Dec 2025 23:20:13 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2b18a5c6d65207f10fc6c17b220858889d87734da0680d321d435bf3b6e9f`  
		Last Modified: Mon, 29 Dec 2025 23:22:34 GMT  
		Size: 438.3 MB (438349984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:d37cccfae3680bb88f3906e5587152bd9bcbb8fed8cfef473320ae43035ffa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38057dd915c60923426cec1a895f8ddee1c73ec92a159653c62cc5b32e921ad`

```dockerfile
```

-	Layers:
	-	`sha256:860da3a4237265d52546a7bafaedc1d84413506d53d69533efe3d21a1425c059`  
		Last Modified: Tue, 30 Dec 2025 03:50:15 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460c6758f664568a346a6062ca935932e825f21f4efe6ae09dc82ed8e27e6c11`  
		Last Modified: Tue, 30 Dec 2025 03:50:16 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-slim`

```console
$ docker pull haskell@sha256:24636d09ed520f5ae0c919032fc160991dd4a47c1636dde7e4fdbb5e2e2c34e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:45968c42b38a4bd69878982182cb0c1f2b54499b85988bd45edf468bb5d256fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590681249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd518015bc391188ffde0ee21c278225229b2b612872db45d2ac56ec3fc493`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:51 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:51 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:54 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:54 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:19:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfdefa8db4b518f339b8cbffb22d19d8a875325ff79fdbfe6fb75bf47432f69`  
		Last Modified: Mon, 29 Dec 2025 23:20:50 GMT  
		Size: 106.4 MB (106366833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8f8056a67c4f1d2b7640b58c78bc770c17b722667b3e9ba900bf30b19c1621`  
		Last Modified: Mon, 29 Dec 2025 23:20:44 GMT  
		Size: 22.2 MB (22220749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ed9d403b1ef83e23e939356068d228e162be38c7c4f3a4889f42d1c00a46e`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d7ed4ed3ffeba81308fff71e1b76fd08a869d1defc5a923cabae331280f46f`  
		Last Modified: Mon, 29 Dec 2025 23:21:48 GMT  
		Size: 424.2 MB (424222986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:82fa5d41bcd272a6f96319b6d6b0260b2e085cc8ac9723f3b7a7ca94e0b8ce3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b76cd6733294afa8a6eb27b6774c90c32599707ec28e88266d37073a1d4eeb`

```dockerfile
```

-	Layers:
	-	`sha256:389300bab508157259ffe8bfd3e5bfb1e5c00937ef96db414503f929748a03b9`  
		Last Modified: Tue, 30 Dec 2025 03:50:14 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d2d7ef0c8f192c153daf4ef8173c1d83b00d4d1d36768621714ea26ef099707`  
		Last Modified: Tue, 30 Dec 2025 03:50:15 GMT  
		Size: 26.0 KB (25995 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d60491158b2b43a3c733bd878052c6bf2575c7f70cb7dda0c377944481cc10a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607458442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bfd1c1dcaded071189926d51ad205048e7ad327bc2248775d0de2700167759`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:06 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:18:34 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:34 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:34 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a683c1a51be9b8cfc1bb45aaae0d179abb74083546557e36b29c278ffd9b4`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 101.9 MB (101863815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefa63d33cf7e1e31ef551f770986e0aea97cfb935160d297371a4d686889822`  
		Last Modified: Mon, 29 Dec 2025 23:20:13 GMT  
		Size: 24.5 MB (24528545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f766a135c6fc61150e3f3dcdf2ea3b05917587b132d31887ad973aa0f6c74e8`  
		Last Modified: Mon, 29 Dec 2025 23:20:07 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1976bbe72d9568527a5052c78fc39db0585d94d0596fe43dd737e5a0e52d4924`  
		Last Modified: Mon, 29 Dec 2025 23:20:25 GMT  
		Size: 438.3 MB (438344660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:59be18ed887bebadd676a1ed116de555b3b07a5ff33209feeb70292c333b4e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06aff08305d5585988e8a506e113ad705ab77d6e975c50f17d7c674449fbe9d`

```dockerfile
```

-	Layers:
	-	`sha256:d85e9a54de99e1fa1e1af1fc1b43c63b7c41c3fe9dc17e2f13e76c283bd858f1`  
		Last Modified: Tue, 30 Dec 2025 03:50:21 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6620d47f157e9c0eea4da54f9f0363d35440ff7f754190d42c35594f8501be4`  
		Last Modified: Tue, 30 Dec 2025 03:50:22 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-slim-bullseye`

```console
$ docker pull haskell@sha256:24636d09ed520f5ae0c919032fc160991dd4a47c1636dde7e4fdbb5e2e2c34e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:45968c42b38a4bd69878982182cb0c1f2b54499b85988bd45edf468bb5d256fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590681249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd518015bc391188ffde0ee21c278225229b2b612872db45d2ac56ec3fc493`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:51 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:51 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:54 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:54 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:19:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfdefa8db4b518f339b8cbffb22d19d8a875325ff79fdbfe6fb75bf47432f69`  
		Last Modified: Mon, 29 Dec 2025 23:20:50 GMT  
		Size: 106.4 MB (106366833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8f8056a67c4f1d2b7640b58c78bc770c17b722667b3e9ba900bf30b19c1621`  
		Last Modified: Mon, 29 Dec 2025 23:20:44 GMT  
		Size: 22.2 MB (22220749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ed9d403b1ef83e23e939356068d228e162be38c7c4f3a4889f42d1c00a46e`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d7ed4ed3ffeba81308fff71e1b76fd08a869d1defc5a923cabae331280f46f`  
		Last Modified: Mon, 29 Dec 2025 23:21:48 GMT  
		Size: 424.2 MB (424222986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:82fa5d41bcd272a6f96319b6d6b0260b2e085cc8ac9723f3b7a7ca94e0b8ce3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b76cd6733294afa8a6eb27b6774c90c32599707ec28e88266d37073a1d4eeb`

```dockerfile
```

-	Layers:
	-	`sha256:389300bab508157259ffe8bfd3e5bfb1e5c00937ef96db414503f929748a03b9`  
		Last Modified: Tue, 30 Dec 2025 03:50:14 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d2d7ef0c8f192c153daf4ef8173c1d83b00d4d1d36768621714ea26ef099707`  
		Last Modified: Tue, 30 Dec 2025 03:50:15 GMT  
		Size: 26.0 KB (25995 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d60491158b2b43a3c733bd878052c6bf2575c7f70cb7dda0c377944481cc10a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607458442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bfd1c1dcaded071189926d51ad205048e7ad327bc2248775d0de2700167759`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:06 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:18:34 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:34 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:34 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a683c1a51be9b8cfc1bb45aaae0d179abb74083546557e36b29c278ffd9b4`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 101.9 MB (101863815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefa63d33cf7e1e31ef551f770986e0aea97cfb935160d297371a4d686889822`  
		Last Modified: Mon, 29 Dec 2025 23:20:13 GMT  
		Size: 24.5 MB (24528545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f766a135c6fc61150e3f3dcdf2ea3b05917587b132d31887ad973aa0f6c74e8`  
		Last Modified: Mon, 29 Dec 2025 23:20:07 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1976bbe72d9568527a5052c78fc39db0585d94d0596fe43dd737e5a0e52d4924`  
		Last Modified: Mon, 29 Dec 2025 23:20:25 GMT  
		Size: 438.3 MB (438344660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:59be18ed887bebadd676a1ed116de555b3b07a5ff33209feeb70292c333b4e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06aff08305d5585988e8a506e113ad705ab77d6e975c50f17d7c674449fbe9d`

```dockerfile
```

-	Layers:
	-	`sha256:d85e9a54de99e1fa1e1af1fc1b43c63b7c41c3fe9dc17e2f13e76c283bd858f1`  
		Last Modified: Tue, 30 Dec 2025 03:50:21 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6620d47f157e9c0eea4da54f9f0363d35440ff7f754190d42c35594f8501be4`  
		Last Modified: Tue, 30 Dec 2025 03:50:22 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7`

```console
$ docker pull haskell@sha256:ee197b2550916718a4acebbd6079cc21ac412a80da28533bf1b273a3bffab9fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7` - linux; amd64

```console
$ docker pull haskell@sha256:dcdc7a260adb186ea9a1d84bb37019398eaa2692a62120338e60d03e53ce7a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641572506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14581b42f2fa47aedf9940f56417ac44fdaa19cd9f8cd9e7de49a8f0d60a9c96`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:40 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:43 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:43 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:19:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:02 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:02 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc45b2751c0570d52e1ca630c74bb147dfea1e527c053ca9fef0923a01f9ada`  
		Last Modified: Mon, 29 Dec 2025 23:20:36 GMT  
		Size: 133.8 MB (133759795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aa0a080cc3e3a2d547b9e7820b821cf056c3adbf42a1d5f2f4a7a462988164`  
		Last Modified: Mon, 29 Dec 2025 23:20:25 GMT  
		Size: 22.2 MB (22220750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff6bfb2cb17a902b7bf12dac7b1eba8b38d0a7f1cb930f394cc45b06ced3c9`  
		Last Modified: Mon, 29 Dec 2025 23:20:24 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca189d8f8ebf2257244bcde1e3d7efc9f83971f121b0915ba710701981d3f333`  
		Last Modified: Mon, 29 Dec 2025 23:21:05 GMT  
		Size: 424.2 MB (424223281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7` - unknown; unknown

```console
$ docker pull haskell@sha256:6d8c45471ff831e3a0e3bfe4fa133ea736503e9a873c8ce6311b4e4204d533b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6bfbfa9bd6fc76fd3205a4a0a90c58171632b8470a65151a6b03f1cbda488f`

```dockerfile
```

-	Layers:
	-	`sha256:0b99232fdc3a72fa0953cb7045a58f70264c741589c48d8e6df34ca7de3897d4`  
		Last Modified: Tue, 30 Dec 2025 03:50:06 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eace2ac7ddff76f3386c458baaf117e6778408e8ee4ec10d0191cdc1e187b13`  
		Last Modified: Tue, 30 Dec 2025 03:50:06 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:ef48a9cb78e1f1ff8e1dec303bc8158b6f1a0b60f0fe8ef71c8f1ce30f2b083a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.4 MB (658350385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a06a3f1c536105de241fa361d6a6de337e3fd981b14d685f0263c1e44a36b2`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:10 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:10 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:13 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:13 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:13 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:18:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacd905a06452b63a81f81c7231e6e0e0e62f693fc89fc18d653e123683805b7`  
		Last Modified: Mon, 29 Dec 2025 23:20:27 GMT  
		Size: 129.2 MB (129241121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e89c89eca88f416e9e0e4fd85bc697bcc271db258f7b5eeddb7909b369f0f6d`  
		Last Modified: Mon, 29 Dec 2025 23:20:15 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490e717c00b85b32b044071d3c25461d7f4f99ca5875012df088f9591118ab05`  
		Last Modified: Mon, 29 Dec 2025 23:20:13 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2b18a5c6d65207f10fc6c17b220858889d87734da0680d321d435bf3b6e9f`  
		Last Modified: Mon, 29 Dec 2025 23:22:34 GMT  
		Size: 438.3 MB (438349984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7` - unknown; unknown

```console
$ docker pull haskell@sha256:d37cccfae3680bb88f3906e5587152bd9bcbb8fed8cfef473320ae43035ffa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38057dd915c60923426cec1a895f8ddee1c73ec92a159653c62cc5b32e921ad`

```dockerfile
```

-	Layers:
	-	`sha256:860da3a4237265d52546a7bafaedc1d84413506d53d69533efe3d21a1425c059`  
		Last Modified: Tue, 30 Dec 2025 03:50:15 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460c6758f664568a346a6062ca935932e825f21f4efe6ae09dc82ed8e27e6c11`  
		Last Modified: Tue, 30 Dec 2025 03:50:16 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-bullseye`

```console
$ docker pull haskell@sha256:ee197b2550916718a4acebbd6079cc21ac412a80da28533bf1b273a3bffab9fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:dcdc7a260adb186ea9a1d84bb37019398eaa2692a62120338e60d03e53ce7a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641572506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14581b42f2fa47aedf9940f56417ac44fdaa19cd9f8cd9e7de49a8f0d60a9c96`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:40 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:40 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:40 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:43 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:43 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:19:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:02 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:02 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc45b2751c0570d52e1ca630c74bb147dfea1e527c053ca9fef0923a01f9ada`  
		Last Modified: Mon, 29 Dec 2025 23:20:36 GMT  
		Size: 133.8 MB (133759795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57aa0a080cc3e3a2d547b9e7820b821cf056c3adbf42a1d5f2f4a7a462988164`  
		Last Modified: Mon, 29 Dec 2025 23:20:25 GMT  
		Size: 22.2 MB (22220750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faff6bfb2cb17a902b7bf12dac7b1eba8b38d0a7f1cb930f394cc45b06ced3c9`  
		Last Modified: Mon, 29 Dec 2025 23:20:24 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca189d8f8ebf2257244bcde1e3d7efc9f83971f121b0915ba710701981d3f333`  
		Last Modified: Mon, 29 Dec 2025 23:21:05 GMT  
		Size: 424.2 MB (424223281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:6d8c45471ff831e3a0e3bfe4fa133ea736503e9a873c8ce6311b4e4204d533b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6bfbfa9bd6fc76fd3205a4a0a90c58171632b8470a65151a6b03f1cbda488f`

```dockerfile
```

-	Layers:
	-	`sha256:0b99232fdc3a72fa0953cb7045a58f70264c741589c48d8e6df34ca7de3897d4`  
		Last Modified: Tue, 30 Dec 2025 03:50:06 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eace2ac7ddff76f3386c458baaf117e6778408e8ee4ec10d0191cdc1e187b13`  
		Last Modified: Tue, 30 Dec 2025 03:50:06 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:ef48a9cb78e1f1ff8e1dec303bc8158b6f1a0b60f0fe8ef71c8f1ce30f2b083a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.4 MB (658350385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a06a3f1c536105de241fa361d6a6de337e3fd981b14d685f0263c1e44a36b2`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:10 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:10 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:13 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:13 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:13 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:18:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:39 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:39 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eacd905a06452b63a81f81c7231e6e0e0e62f693fc89fc18d653e123683805b7`  
		Last Modified: Mon, 29 Dec 2025 23:20:27 GMT  
		Size: 129.2 MB (129241121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e89c89eca88f416e9e0e4fd85bc697bcc271db258f7b5eeddb7909b369f0f6d`  
		Last Modified: Mon, 29 Dec 2025 23:20:15 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490e717c00b85b32b044071d3c25461d7f4f99ca5875012df088f9591118ab05`  
		Last Modified: Mon, 29 Dec 2025 23:20:13 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edf2b18a5c6d65207f10fc6c17b220858889d87734da0680d321d435bf3b6e9f`  
		Last Modified: Mon, 29 Dec 2025 23:22:34 GMT  
		Size: 438.3 MB (438349984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:d37cccfae3680bb88f3906e5587152bd9bcbb8fed8cfef473320ae43035ffa37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c38057dd915c60923426cec1a895f8ddee1c73ec92a159653c62cc5b32e921ad`

```dockerfile
```

-	Layers:
	-	`sha256:860da3a4237265d52546a7bafaedc1d84413506d53d69533efe3d21a1425c059`  
		Last Modified: Tue, 30 Dec 2025 03:50:15 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460c6758f664568a346a6062ca935932e825f21f4efe6ae09dc82ed8e27e6c11`  
		Last Modified: Tue, 30 Dec 2025 03:50:16 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-slim`

```console
$ docker pull haskell@sha256:24636d09ed520f5ae0c919032fc160991dd4a47c1636dde7e4fdbb5e2e2c34e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-slim` - linux; amd64

```console
$ docker pull haskell@sha256:45968c42b38a4bd69878982182cb0c1f2b54499b85988bd45edf468bb5d256fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590681249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd518015bc391188ffde0ee21c278225229b2b612872db45d2ac56ec3fc493`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:51 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:51 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:54 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:54 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:19:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfdefa8db4b518f339b8cbffb22d19d8a875325ff79fdbfe6fb75bf47432f69`  
		Last Modified: Mon, 29 Dec 2025 23:20:50 GMT  
		Size: 106.4 MB (106366833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8f8056a67c4f1d2b7640b58c78bc770c17b722667b3e9ba900bf30b19c1621`  
		Last Modified: Mon, 29 Dec 2025 23:20:44 GMT  
		Size: 22.2 MB (22220749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ed9d403b1ef83e23e939356068d228e162be38c7c4f3a4889f42d1c00a46e`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d7ed4ed3ffeba81308fff71e1b76fd08a869d1defc5a923cabae331280f46f`  
		Last Modified: Mon, 29 Dec 2025 23:21:48 GMT  
		Size: 424.2 MB (424222986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:82fa5d41bcd272a6f96319b6d6b0260b2e085cc8ac9723f3b7a7ca94e0b8ce3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b76cd6733294afa8a6eb27b6774c90c32599707ec28e88266d37073a1d4eeb`

```dockerfile
```

-	Layers:
	-	`sha256:389300bab508157259ffe8bfd3e5bfb1e5c00937ef96db414503f929748a03b9`  
		Last Modified: Tue, 30 Dec 2025 03:50:14 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d2d7ef0c8f192c153daf4ef8173c1d83b00d4d1d36768621714ea26ef099707`  
		Last Modified: Tue, 30 Dec 2025 03:50:15 GMT  
		Size: 26.0 KB (25995 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d60491158b2b43a3c733bd878052c6bf2575c7f70cb7dda0c377944481cc10a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607458442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bfd1c1dcaded071189926d51ad205048e7ad327bc2248775d0de2700167759`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:06 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:18:34 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:34 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:34 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a683c1a51be9b8cfc1bb45aaae0d179abb74083546557e36b29c278ffd9b4`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 101.9 MB (101863815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefa63d33cf7e1e31ef551f770986e0aea97cfb935160d297371a4d686889822`  
		Last Modified: Mon, 29 Dec 2025 23:20:13 GMT  
		Size: 24.5 MB (24528545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f766a135c6fc61150e3f3dcdf2ea3b05917587b132d31887ad973aa0f6c74e8`  
		Last Modified: Mon, 29 Dec 2025 23:20:07 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1976bbe72d9568527a5052c78fc39db0585d94d0596fe43dd737e5a0e52d4924`  
		Last Modified: Mon, 29 Dec 2025 23:20:25 GMT  
		Size: 438.3 MB (438344660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:59be18ed887bebadd676a1ed116de555b3b07a5ff33209feeb70292c333b4e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06aff08305d5585988e8a506e113ad705ab77d6e975c50f17d7c674449fbe9d`

```dockerfile
```

-	Layers:
	-	`sha256:d85e9a54de99e1fa1e1af1fc1b43c63b7c41c3fe9dc17e2f13e76c283bd858f1`  
		Last Modified: Tue, 30 Dec 2025 03:50:21 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6620d47f157e9c0eea4da54f9f0363d35440ff7f754190d42c35594f8501be4`  
		Last Modified: Tue, 30 Dec 2025 03:50:22 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-slim-bullseye`

```console
$ docker pull haskell@sha256:24636d09ed520f5ae0c919032fc160991dd4a47c1636dde7e4fdbb5e2e2c34e9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:45968c42b38a4bd69878982182cb0c1f2b54499b85988bd45edf468bb5d256fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590681249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6fd518015bc391188ffde0ee21c278225229b2b612872db45d2ac56ec3fc493`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:51 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:51 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:54 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:54 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:19:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:20 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:20 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bfdefa8db4b518f339b8cbffb22d19d8a875325ff79fdbfe6fb75bf47432f69`  
		Last Modified: Mon, 29 Dec 2025 23:20:50 GMT  
		Size: 106.4 MB (106366833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8f8056a67c4f1d2b7640b58c78bc770c17b722667b3e9ba900bf30b19c1621`  
		Last Modified: Mon, 29 Dec 2025 23:20:44 GMT  
		Size: 22.2 MB (22220749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062ed9d403b1ef83e23e939356068d228e162be38c7c4f3a4889f42d1c00a46e`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d7ed4ed3ffeba81308fff71e1b76fd08a869d1defc5a923cabae331280f46f`  
		Last Modified: Mon, 29 Dec 2025 23:21:48 GMT  
		Size: 424.2 MB (424222986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:82fa5d41bcd272a6f96319b6d6b0260b2e085cc8ac9723f3b7a7ca94e0b8ce3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b76cd6733294afa8a6eb27b6774c90c32599707ec28e88266d37073a1d4eeb`

```dockerfile
```

-	Layers:
	-	`sha256:389300bab508157259ffe8bfd3e5bfb1e5c00937ef96db414503f929748a03b9`  
		Last Modified: Tue, 30 Dec 2025 03:50:14 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d2d7ef0c8f192c153daf4ef8173c1d83b00d4d1d36768621714ea26ef099707`  
		Last Modified: Tue, 30 Dec 2025 03:50:15 GMT  
		Size: 26.0 KB (25995 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d60491158b2b43a3c733bd878052c6bf2575c7f70cb7dda0c377944481cc10a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607458442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bfd1c1dcaded071189926d51ad205048e7ad327bc2248775d0de2700167759`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:06 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC=9.6.7
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Mon, 29 Dec 2025 23:18:34 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:34 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:34 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60a683c1a51be9b8cfc1bb45aaae0d179abb74083546557e36b29c278ffd9b4`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 101.9 MB (101863815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefa63d33cf7e1e31ef551f770986e0aea97cfb935160d297371a4d686889822`  
		Last Modified: Mon, 29 Dec 2025 23:20:13 GMT  
		Size: 24.5 MB (24528545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f766a135c6fc61150e3f3dcdf2ea3b05917587b132d31887ad973aa0f6c74e8`  
		Last Modified: Mon, 29 Dec 2025 23:20:07 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1976bbe72d9568527a5052c78fc39db0585d94d0596fe43dd737e5a0e52d4924`  
		Last Modified: Mon, 29 Dec 2025 23:20:25 GMT  
		Size: 438.3 MB (438344660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:59be18ed887bebadd676a1ed116de555b3b07a5ff33209feeb70292c333b4e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f06aff08305d5585988e8a506e113ad705ab77d6e975c50f17d7c674449fbe9d`

```dockerfile
```

-	Layers:
	-	`sha256:d85e9a54de99e1fa1e1af1fc1b43c63b7c41c3fe9dc17e2f13e76c283bd858f1`  
		Last Modified: Tue, 30 Dec 2025 03:50:21 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6620d47f157e9c0eea4da54f9f0363d35440ff7f754190d42c35594f8501be4`  
		Last Modified: Tue, 30 Dec 2025 03:50:22 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8`

```console
$ docker pull haskell@sha256:68394d0ec62abe61eb411ab1623bb6fa574a594fee7f28a5df4111ba4c20a16f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8` - linux; amd64

```console
$ docker pull haskell@sha256:3dbd8e72f90ca3564e5deac36c1bd41201293060e587bda12d02a19625256697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653562347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c56d1ffff3ab0633dfb3bfc9f1fd67f82f1652ac5b75ce6ed431b299170a8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:38 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:38 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:40 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d588c577afc2a96a7780369b0a9e3c23fb3df82a79f5932ea96b24d6b09c351`  
		Last Modified: Mon, 29 Dec 2025 23:21:12 GMT  
		Size: 133.8 MB (133758659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a345c14d0d3204033fca6ef0e5939932aad0666fb862d59408ceb7bd933c2c09`  
		Last Modified: Mon, 29 Dec 2025 23:20:49 GMT  
		Size: 22.2 MB (22220729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a63c328c90e31d05c9d86d74fcfab3a1a95f5cf2ec821663ea3fcb40ca735`  
		Last Modified: Mon, 29 Dec 2025 23:20:48 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ccb98eef8d13d746fba81dd0be85e36acc678df20f8e2e05131fe4256a5b4`  
		Last Modified: Mon, 29 Dec 2025 23:21:11 GMT  
		Size: 436.2 MB (436214276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8` - unknown; unknown

```console
$ docker pull haskell@sha256:6ae2f8ba1198823cd06de5a3a8196cff9e5414fc4c36690f7643b9792f914465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc10ca1c9b6bd3889ac29577fa85fcd8e1b42187028db71f6b149f49a0e5404`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9b16ca44ffaacf9e5b37df1b9b8d753d53df6defec38d04b2850b3633686e`  
		Last Modified: Tue, 30 Dec 2025 03:50:32 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7493a35686cc05dbc67c3a46c8bd37f758e9ac153c403d6ae65cf6739e6a331`  
		Last Modified: Tue, 30 Dec 2025 03:50:33 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:85780ba5150b58dd2414b92cee8e848a3f35da642b712b597d98d9e9bed6fade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663797220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad395e1833b5e4cabee9a889460c0b7c8e76e028de4ca7b604f8e0cdf8cec78`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:09 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:09 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:12 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:12 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8f09569995691473a0f640469d641107ce98823e448cbb4e554313d66c6c3a`  
		Last Modified: Mon, 29 Dec 2025 23:21:36 GMT  
		Size: 129.2 MB (129240461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44769ef818fe4b8e31d6d49a7d51e4382b95f4d258155d6ae5db86aecc1fc8d5`  
		Last Modified: Mon, 29 Dec 2025 23:21:09 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a413bbd7cd0b473d11232a45f59aae06af24f370b84807230f9724ad96a839ec`  
		Last Modified: Mon, 29 Dec 2025 23:21:09 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a721030ded20e88c901cb5742e3ca9e96ff28b23b6973bece84b7800b5225009`  
		Last Modified: Mon, 29 Dec 2025 23:21:20 GMT  
		Size: 443.8 MB (443797478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8` - unknown; unknown

```console
$ docker pull haskell@sha256:3cafbc5aa9053084855e6e6bd6468b6080e4f4baeaa4aebed4ec37a2c744bb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f694995826b6fe4822395efc31cac3494457d7625fc05113ac7eed6129830e`

```dockerfile
```

-	Layers:
	-	`sha256:97e915cb05d0ca30693f7fbe91a3f2af12139a50c56dbfe8e6eadc20a54497db`  
		Last Modified: Tue, 30 Dec 2025 03:50:40 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c20aa5428be614bed3d97de7949cd1f8fd63026ab6049e0e2bb2e3914c1d0f`  
		Last Modified: Tue, 30 Dec 2025 03:50:40 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-bullseye`

```console
$ docker pull haskell@sha256:68394d0ec62abe61eb411ab1623bb6fa574a594fee7f28a5df4111ba4c20a16f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:3dbd8e72f90ca3564e5deac36c1bd41201293060e587bda12d02a19625256697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653562347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c56d1ffff3ab0633dfb3bfc9f1fd67f82f1652ac5b75ce6ed431b299170a8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:38 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:38 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:40 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d588c577afc2a96a7780369b0a9e3c23fb3df82a79f5932ea96b24d6b09c351`  
		Last Modified: Mon, 29 Dec 2025 23:21:12 GMT  
		Size: 133.8 MB (133758659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a345c14d0d3204033fca6ef0e5939932aad0666fb862d59408ceb7bd933c2c09`  
		Last Modified: Mon, 29 Dec 2025 23:20:49 GMT  
		Size: 22.2 MB (22220729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a63c328c90e31d05c9d86d74fcfab3a1a95f5cf2ec821663ea3fcb40ca735`  
		Last Modified: Mon, 29 Dec 2025 23:20:48 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ccb98eef8d13d746fba81dd0be85e36acc678df20f8e2e05131fe4256a5b4`  
		Last Modified: Mon, 29 Dec 2025 23:21:11 GMT  
		Size: 436.2 MB (436214276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:6ae2f8ba1198823cd06de5a3a8196cff9e5414fc4c36690f7643b9792f914465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc10ca1c9b6bd3889ac29577fa85fcd8e1b42187028db71f6b149f49a0e5404`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9b16ca44ffaacf9e5b37df1b9b8d753d53df6defec38d04b2850b3633686e`  
		Last Modified: Tue, 30 Dec 2025 03:50:32 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7493a35686cc05dbc67c3a46c8bd37f758e9ac153c403d6ae65cf6739e6a331`  
		Last Modified: Tue, 30 Dec 2025 03:50:33 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:85780ba5150b58dd2414b92cee8e848a3f35da642b712b597d98d9e9bed6fade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663797220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad395e1833b5e4cabee9a889460c0b7c8e76e028de4ca7b604f8e0cdf8cec78`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:09 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:09 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:12 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:12 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8f09569995691473a0f640469d641107ce98823e448cbb4e554313d66c6c3a`  
		Last Modified: Mon, 29 Dec 2025 23:21:36 GMT  
		Size: 129.2 MB (129240461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44769ef818fe4b8e31d6d49a7d51e4382b95f4d258155d6ae5db86aecc1fc8d5`  
		Last Modified: Mon, 29 Dec 2025 23:21:09 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a413bbd7cd0b473d11232a45f59aae06af24f370b84807230f9724ad96a839ec`  
		Last Modified: Mon, 29 Dec 2025 23:21:09 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a721030ded20e88c901cb5742e3ca9e96ff28b23b6973bece84b7800b5225009`  
		Last Modified: Mon, 29 Dec 2025 23:21:20 GMT  
		Size: 443.8 MB (443797478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:3cafbc5aa9053084855e6e6bd6468b6080e4f4baeaa4aebed4ec37a2c744bb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f694995826b6fe4822395efc31cac3494457d7625fc05113ac7eed6129830e`

```dockerfile
```

-	Layers:
	-	`sha256:97e915cb05d0ca30693f7fbe91a3f2af12139a50c56dbfe8e6eadc20a54497db`  
		Last Modified: Tue, 30 Dec 2025 03:50:40 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c20aa5428be614bed3d97de7949cd1f8fd63026ab6049e0e2bb2e3914c1d0f`  
		Last Modified: Tue, 30 Dec 2025 03:50:40 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-slim`

```console
$ docker pull haskell@sha256:6e9f3b24cde7887cb83ac5edf7e30c011174d127586cb7980f14c444599bf9e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:5b53996dda26808343ffcfaa7e75521074b2e4d4e35819a70c31cdbc8416dd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602671056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bd572deb730a5fee23645a21bb9baa3f23c5d28c6ff0b7b461d9fe389d4876`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:39 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:39 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c79223b899ccd723c9453a2b17cac04fba292798a5101387eeda3a99246d28`  
		Last Modified: Mon, 29 Dec 2025 23:21:00 GMT  
		Size: 106.4 MB (106366699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915c51849a535b4c8b7e133ae3d2e3379e3f1f8c02ee30ebfad413224794f197`  
		Last Modified: Mon, 29 Dec 2025 23:20:48 GMT  
		Size: 22.2 MB (22220768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850fa59e92869b1dfc4781790debfe1cca748ef63c2e6b61d080527c2aec11c9`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bc71accd462a16278319a7b9b03f25dcf78a0318eb80b32d1f689e6e896d84`  
		Last Modified: Mon, 29 Dec 2025 23:21:10 GMT  
		Size: 436.2 MB (436212908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:e8c19afc5d2c8de347fb12844b121cb521f8e0aab3947c4533b5e00adc06c2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cd2e760cb58aebc41aa936c2c04b283d9f0a23ba902f98640c8b6a5d5593ba`

```dockerfile
```

-	Layers:
	-	`sha256:868e84ff26de88a94af9d462e5c065c0442399d1b1aa5ebeb28d35222411c0fa`  
		Last Modified: Tue, 30 Dec 2025 03:50:43 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb56571b530949e7db473dc9b5a77ef4140e001fd52995692eeb0e93c6bfb0f8`  
		Last Modified: Tue, 30 Dec 2025 03:50:43 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7a661bcfb7b17e887774d85150c1b46dc5e8629ceeae25afb80c2477d44eb222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612910610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edda5cf2a4c0c0b34fb0d8cd83143e78de23f44a58884fb89bed09548d46cbdc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:06 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd10bd9ba69f49919bcf9e0287134cc68847b8511b5d57a26c02cf027bafab8b`  
		Last Modified: Mon, 29 Dec 2025 23:21:12 GMT  
		Size: 101.9 MB (101863845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9ab60cabf8e12219217bcbae48160a7e3ea61a58cca4a7f2b51c844f217782`  
		Last Modified: Mon, 29 Dec 2025 23:21:06 GMT  
		Size: 24.5 MB (24528545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f766a135c6fc61150e3f3dcdf2ea3b05917587b132d31887ad973aa0f6c74e8`  
		Last Modified: Mon, 29 Dec 2025 23:20:07 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28852afef0eea61b1121834b3e0fce9f75863c26d587be958e9ecbcad800a38d`  
		Last Modified: Mon, 29 Dec 2025 23:21:53 GMT  
		Size: 443.8 MB (443796798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:94b8d1f17ddab209abdaea07dd0430ef71f785899cc937814fe69b993247c1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d16f568e17c66a139ccee1d72f69430ecb6c8a198586b68946fb5bdf31910c`

```dockerfile
```

-	Layers:
	-	`sha256:56dc56746d2064417f72327f5dde8be74ac1e0eba26179e511e2b8ddd129b8e8`  
		Last Modified: Tue, 30 Dec 2025 03:50:49 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8238ebcb6217d1a5c2665f1a0cc625f1bbaa44a2c3fb7414de096394caaf0732`  
		Last Modified: Tue, 30 Dec 2025 03:50:50 GMT  
		Size: 25.9 KB (25867 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-slim-bullseye`

```console
$ docker pull haskell@sha256:6e9f3b24cde7887cb83ac5edf7e30c011174d127586cb7980f14c444599bf9e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:5b53996dda26808343ffcfaa7e75521074b2e4d4e35819a70c31cdbc8416dd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602671056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bd572deb730a5fee23645a21bb9baa3f23c5d28c6ff0b7b461d9fe389d4876`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:39 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:39 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c79223b899ccd723c9453a2b17cac04fba292798a5101387eeda3a99246d28`  
		Last Modified: Mon, 29 Dec 2025 23:21:00 GMT  
		Size: 106.4 MB (106366699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915c51849a535b4c8b7e133ae3d2e3379e3f1f8c02ee30ebfad413224794f197`  
		Last Modified: Mon, 29 Dec 2025 23:20:48 GMT  
		Size: 22.2 MB (22220768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850fa59e92869b1dfc4781790debfe1cca748ef63c2e6b61d080527c2aec11c9`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bc71accd462a16278319a7b9b03f25dcf78a0318eb80b32d1f689e6e896d84`  
		Last Modified: Mon, 29 Dec 2025 23:21:10 GMT  
		Size: 436.2 MB (436212908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:e8c19afc5d2c8de347fb12844b121cb521f8e0aab3947c4533b5e00adc06c2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cd2e760cb58aebc41aa936c2c04b283d9f0a23ba902f98640c8b6a5d5593ba`

```dockerfile
```

-	Layers:
	-	`sha256:868e84ff26de88a94af9d462e5c065c0442399d1b1aa5ebeb28d35222411c0fa`  
		Last Modified: Tue, 30 Dec 2025 03:50:43 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb56571b530949e7db473dc9b5a77ef4140e001fd52995692eeb0e93c6bfb0f8`  
		Last Modified: Tue, 30 Dec 2025 03:50:43 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7a661bcfb7b17e887774d85150c1b46dc5e8629ceeae25afb80c2477d44eb222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612910610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edda5cf2a4c0c0b34fb0d8cd83143e78de23f44a58884fb89bed09548d46cbdc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:06 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd10bd9ba69f49919bcf9e0287134cc68847b8511b5d57a26c02cf027bafab8b`  
		Last Modified: Mon, 29 Dec 2025 23:21:12 GMT  
		Size: 101.9 MB (101863845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9ab60cabf8e12219217bcbae48160a7e3ea61a58cca4a7f2b51c844f217782`  
		Last Modified: Mon, 29 Dec 2025 23:21:06 GMT  
		Size: 24.5 MB (24528545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f766a135c6fc61150e3f3dcdf2ea3b05917587b132d31887ad973aa0f6c74e8`  
		Last Modified: Mon, 29 Dec 2025 23:20:07 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28852afef0eea61b1121834b3e0fce9f75863c26d587be958e9ecbcad800a38d`  
		Last Modified: Mon, 29 Dec 2025 23:21:53 GMT  
		Size: 443.8 MB (443796798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:94b8d1f17ddab209abdaea07dd0430ef71f785899cc937814fe69b993247c1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d16f568e17c66a139ccee1d72f69430ecb6c8a198586b68946fb5bdf31910c`

```dockerfile
```

-	Layers:
	-	`sha256:56dc56746d2064417f72327f5dde8be74ac1e0eba26179e511e2b8ddd129b8e8`  
		Last Modified: Tue, 30 Dec 2025 03:50:49 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8238ebcb6217d1a5c2665f1a0cc625f1bbaa44a2c3fb7414de096394caaf0732`  
		Last Modified: Tue, 30 Dec 2025 03:50:50 GMT  
		Size: 25.9 KB (25867 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4`

```console
$ docker pull haskell@sha256:68394d0ec62abe61eb411ab1623bb6fa574a594fee7f28a5df4111ba4c20a16f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4` - linux; amd64

```console
$ docker pull haskell@sha256:3dbd8e72f90ca3564e5deac36c1bd41201293060e587bda12d02a19625256697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653562347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c56d1ffff3ab0633dfb3bfc9f1fd67f82f1652ac5b75ce6ed431b299170a8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:38 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:38 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:40 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d588c577afc2a96a7780369b0a9e3c23fb3df82a79f5932ea96b24d6b09c351`  
		Last Modified: Mon, 29 Dec 2025 23:21:12 GMT  
		Size: 133.8 MB (133758659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a345c14d0d3204033fca6ef0e5939932aad0666fb862d59408ceb7bd933c2c09`  
		Last Modified: Mon, 29 Dec 2025 23:20:49 GMT  
		Size: 22.2 MB (22220729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a63c328c90e31d05c9d86d74fcfab3a1a95f5cf2ec821663ea3fcb40ca735`  
		Last Modified: Mon, 29 Dec 2025 23:20:48 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ccb98eef8d13d746fba81dd0be85e36acc678df20f8e2e05131fe4256a5b4`  
		Last Modified: Mon, 29 Dec 2025 23:21:11 GMT  
		Size: 436.2 MB (436214276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4` - unknown; unknown

```console
$ docker pull haskell@sha256:6ae2f8ba1198823cd06de5a3a8196cff9e5414fc4c36690f7643b9792f914465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc10ca1c9b6bd3889ac29577fa85fcd8e1b42187028db71f6b149f49a0e5404`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9b16ca44ffaacf9e5b37df1b9b8d753d53df6defec38d04b2850b3633686e`  
		Last Modified: Tue, 30 Dec 2025 03:50:32 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7493a35686cc05dbc67c3a46c8bd37f758e9ac153c403d6ae65cf6739e6a331`  
		Last Modified: Tue, 30 Dec 2025 03:50:33 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:85780ba5150b58dd2414b92cee8e848a3f35da642b712b597d98d9e9bed6fade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663797220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad395e1833b5e4cabee9a889460c0b7c8e76e028de4ca7b604f8e0cdf8cec78`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:09 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:09 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:12 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:12 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8f09569995691473a0f640469d641107ce98823e448cbb4e554313d66c6c3a`  
		Last Modified: Mon, 29 Dec 2025 23:21:36 GMT  
		Size: 129.2 MB (129240461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44769ef818fe4b8e31d6d49a7d51e4382b95f4d258155d6ae5db86aecc1fc8d5`  
		Last Modified: Mon, 29 Dec 2025 23:21:09 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a413bbd7cd0b473d11232a45f59aae06af24f370b84807230f9724ad96a839ec`  
		Last Modified: Mon, 29 Dec 2025 23:21:09 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a721030ded20e88c901cb5742e3ca9e96ff28b23b6973bece84b7800b5225009`  
		Last Modified: Mon, 29 Dec 2025 23:21:20 GMT  
		Size: 443.8 MB (443797478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4` - unknown; unknown

```console
$ docker pull haskell@sha256:3cafbc5aa9053084855e6e6bd6468b6080e4f4baeaa4aebed4ec37a2c744bb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f694995826b6fe4822395efc31cac3494457d7625fc05113ac7eed6129830e`

```dockerfile
```

-	Layers:
	-	`sha256:97e915cb05d0ca30693f7fbe91a3f2af12139a50c56dbfe8e6eadc20a54497db`  
		Last Modified: Tue, 30 Dec 2025 03:50:40 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c20aa5428be614bed3d97de7949cd1f8fd63026ab6049e0e2bb2e3914c1d0f`  
		Last Modified: Tue, 30 Dec 2025 03:50:40 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-bullseye`

```console
$ docker pull haskell@sha256:68394d0ec62abe61eb411ab1623bb6fa574a594fee7f28a5df4111ba4c20a16f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:3dbd8e72f90ca3564e5deac36c1bd41201293060e587bda12d02a19625256697
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.6 MB (653562347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352c56d1ffff3ab0633dfb3bfc9f1fd67f82f1652ac5b75ce6ed431b299170a8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:38 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:38 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:38 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:40 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:14 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d588c577afc2a96a7780369b0a9e3c23fb3df82a79f5932ea96b24d6b09c351`  
		Last Modified: Mon, 29 Dec 2025 23:21:12 GMT  
		Size: 133.8 MB (133758659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a345c14d0d3204033fca6ef0e5939932aad0666fb862d59408ceb7bd933c2c09`  
		Last Modified: Mon, 29 Dec 2025 23:20:49 GMT  
		Size: 22.2 MB (22220729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211a63c328c90e31d05c9d86d74fcfab3a1a95f5cf2ec821663ea3fcb40ca735`  
		Last Modified: Mon, 29 Dec 2025 23:20:48 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22ccb98eef8d13d746fba81dd0be85e36acc678df20f8e2e05131fe4256a5b4`  
		Last Modified: Mon, 29 Dec 2025 23:21:11 GMT  
		Size: 436.2 MB (436214276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:6ae2f8ba1198823cd06de5a3a8196cff9e5414fc4c36690f7643b9792f914465
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fc10ca1c9b6bd3889ac29577fa85fcd8e1b42187028db71f6b149f49a0e5404`

```dockerfile
```

-	Layers:
	-	`sha256:9fc9b16ca44ffaacf9e5b37df1b9b8d753d53df6defec38d04b2850b3633686e`  
		Last Modified: Tue, 30 Dec 2025 03:50:32 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7493a35686cc05dbc67c3a46c8bd37f758e9ac153c403d6ae65cf6739e6a331`  
		Last Modified: Tue, 30 Dec 2025 03:50:33 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:85780ba5150b58dd2414b92cee8e848a3f35da642b712b597d98d9e9bed6fade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663797220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad395e1833b5e4cabee9a889460c0b7c8e76e028de4ca7b604f8e0cdf8cec78`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:09 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:09 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:12 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:12 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8f09569995691473a0f640469d641107ce98823e448cbb4e554313d66c6c3a`  
		Last Modified: Mon, 29 Dec 2025 23:21:36 GMT  
		Size: 129.2 MB (129240461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44769ef818fe4b8e31d6d49a7d51e4382b95f4d258155d6ae5db86aecc1fc8d5`  
		Last Modified: Mon, 29 Dec 2025 23:21:09 GMT  
		Size: 24.5 MB (24528550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a413bbd7cd0b473d11232a45f59aae06af24f370b84807230f9724ad96a839ec`  
		Last Modified: Mon, 29 Dec 2025 23:21:09 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a721030ded20e88c901cb5742e3ca9e96ff28b23b6973bece84b7800b5225009`  
		Last Modified: Mon, 29 Dec 2025 23:21:20 GMT  
		Size: 443.8 MB (443797478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:3cafbc5aa9053084855e6e6bd6468b6080e4f4baeaa4aebed4ec37a2c744bb71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6f694995826b6fe4822395efc31cac3494457d7625fc05113ac7eed6129830e`

```dockerfile
```

-	Layers:
	-	`sha256:97e915cb05d0ca30693f7fbe91a3f2af12139a50c56dbfe8e6eadc20a54497db`  
		Last Modified: Tue, 30 Dec 2025 03:50:40 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c20aa5428be614bed3d97de7949cd1f8fd63026ab6049e0e2bb2e3914c1d0f`  
		Last Modified: Tue, 30 Dec 2025 03:50:40 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-slim`

```console
$ docker pull haskell@sha256:6e9f3b24cde7887cb83ac5edf7e30c011174d127586cb7980f14c444599bf9e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-slim` - linux; amd64

```console
$ docker pull haskell@sha256:5b53996dda26808343ffcfaa7e75521074b2e4d4e35819a70c31cdbc8416dd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602671056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bd572deb730a5fee23645a21bb9baa3f23c5d28c6ff0b7b461d9fe389d4876`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:39 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:39 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c79223b899ccd723c9453a2b17cac04fba292798a5101387eeda3a99246d28`  
		Last Modified: Mon, 29 Dec 2025 23:21:00 GMT  
		Size: 106.4 MB (106366699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915c51849a535b4c8b7e133ae3d2e3379e3f1f8c02ee30ebfad413224794f197`  
		Last Modified: Mon, 29 Dec 2025 23:20:48 GMT  
		Size: 22.2 MB (22220768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850fa59e92869b1dfc4781790debfe1cca748ef63c2e6b61d080527c2aec11c9`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bc71accd462a16278319a7b9b03f25dcf78a0318eb80b32d1f689e6e896d84`  
		Last Modified: Mon, 29 Dec 2025 23:21:10 GMT  
		Size: 436.2 MB (436212908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:e8c19afc5d2c8de347fb12844b121cb521f8e0aab3947c4533b5e00adc06c2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cd2e760cb58aebc41aa936c2c04b283d9f0a23ba902f98640c8b6a5d5593ba`

```dockerfile
```

-	Layers:
	-	`sha256:868e84ff26de88a94af9d462e5c065c0442399d1b1aa5ebeb28d35222411c0fa`  
		Last Modified: Tue, 30 Dec 2025 03:50:43 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb56571b530949e7db473dc9b5a77ef4140e001fd52995692eeb0e93c6bfb0f8`  
		Last Modified: Tue, 30 Dec 2025 03:50:43 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7a661bcfb7b17e887774d85150c1b46dc5e8629ceeae25afb80c2477d44eb222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612910610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edda5cf2a4c0c0b34fb0d8cd83143e78de23f44a58884fb89bed09548d46cbdc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:06 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd10bd9ba69f49919bcf9e0287134cc68847b8511b5d57a26c02cf027bafab8b`  
		Last Modified: Mon, 29 Dec 2025 23:21:12 GMT  
		Size: 101.9 MB (101863845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9ab60cabf8e12219217bcbae48160a7e3ea61a58cca4a7f2b51c844f217782`  
		Last Modified: Mon, 29 Dec 2025 23:21:06 GMT  
		Size: 24.5 MB (24528545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f766a135c6fc61150e3f3dcdf2ea3b05917587b132d31887ad973aa0f6c74e8`  
		Last Modified: Mon, 29 Dec 2025 23:20:07 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28852afef0eea61b1121834b3e0fce9f75863c26d587be958e9ecbcad800a38d`  
		Last Modified: Mon, 29 Dec 2025 23:21:53 GMT  
		Size: 443.8 MB (443796798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:94b8d1f17ddab209abdaea07dd0430ef71f785899cc937814fe69b993247c1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d16f568e17c66a139ccee1d72f69430ecb6c8a198586b68946fb5bdf31910c`

```dockerfile
```

-	Layers:
	-	`sha256:56dc56746d2064417f72327f5dde8be74ac1e0eba26179e511e2b8ddd129b8e8`  
		Last Modified: Tue, 30 Dec 2025 03:50:49 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8238ebcb6217d1a5c2665f1a0cc625f1bbaa44a2c3fb7414de096394caaf0732`  
		Last Modified: Tue, 30 Dec 2025 03:50:50 GMT  
		Size: 25.9 KB (25867 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-slim-bullseye`

```console
$ docker pull haskell@sha256:6e9f3b24cde7887cb83ac5edf7e30c011174d127586cb7980f14c444599bf9e3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:5b53996dda26808343ffcfaa7e75521074b2e4d4e35819a70c31cdbc8416dd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602671056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04bd572deb730a5fee23645a21bb9baa3f23c5d28c6ff0b7b461d9fe389d4876`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:39 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:39 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:42 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:42 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:16 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:37b52eae712b138ea3c9639c687f975153ccba96801de3dc69883975843edb35`  
		Last Modified: Mon, 29 Dec 2025 22:27:47 GMT  
		Size: 30.3 MB (30258441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c79223b899ccd723c9453a2b17cac04fba292798a5101387eeda3a99246d28`  
		Last Modified: Mon, 29 Dec 2025 23:21:00 GMT  
		Size: 106.4 MB (106366699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915c51849a535b4c8b7e133ae3d2e3379e3f1f8c02ee30ebfad413224794f197`  
		Last Modified: Mon, 29 Dec 2025 23:20:48 GMT  
		Size: 22.2 MB (22220768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850fa59e92869b1dfc4781790debfe1cca748ef63c2e6b61d080527c2aec11c9`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3bc71accd462a16278319a7b9b03f25dcf78a0318eb80b32d1f689e6e896d84`  
		Last Modified: Mon, 29 Dec 2025 23:21:10 GMT  
		Size: 436.2 MB (436212908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:e8c19afc5d2c8de347fb12844b121cb521f8e0aab3947c4533b5e00adc06c2de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cd2e760cb58aebc41aa936c2c04b283d9f0a23ba902f98640c8b6a5d5593ba`

```dockerfile
```

-	Layers:
	-	`sha256:868e84ff26de88a94af9d462e5c065c0442399d1b1aa5ebeb28d35222411c0fa`  
		Last Modified: Tue, 30 Dec 2025 03:50:43 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb56571b530949e7db473dc9b5a77ef4140e001fd52995692eeb0e93c6bfb0f8`  
		Last Modified: Tue, 30 Dec 2025 03:50:43 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7a661bcfb7b17e887774d85150c1b46dc5e8629ceeae25afb80c2477d44eb222
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612910610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edda5cf2a4c0c0b34fb0d8cd83143e78de23f44a58884fb89bed09548d46cbdc`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:06 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC=9.8.4
# Mon, 29 Dec 2025 23:17:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:33 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:33 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:33 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:2b952d66bc8c719b5ca92eacb4307075591731bdc405a12ebd6fa840a24375b7`  
		Last Modified: Mon, 29 Dec 2025 22:27:18 GMT  
		Size: 28.7 MB (28748462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd10bd9ba69f49919bcf9e0287134cc68847b8511b5d57a26c02cf027bafab8b`  
		Last Modified: Mon, 29 Dec 2025 23:21:12 GMT  
		Size: 101.9 MB (101863845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9ab60cabf8e12219217bcbae48160a7e3ea61a58cca4a7f2b51c844f217782`  
		Last Modified: Mon, 29 Dec 2025 23:21:06 GMT  
		Size: 24.5 MB (24528545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f766a135c6fc61150e3f3dcdf2ea3b05917587b132d31887ad973aa0f6c74e8`  
		Last Modified: Mon, 29 Dec 2025 23:20:07 GMT  
		Size: 14.0 MB (13972960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28852afef0eea61b1121834b3e0fce9f75863c26d587be958e9ecbcad800a38d`  
		Last Modified: Mon, 29 Dec 2025 23:21:53 GMT  
		Size: 443.8 MB (443796798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:94b8d1f17ddab209abdaea07dd0430ef71f785899cc937814fe69b993247c1ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9d16f568e17c66a139ccee1d72f69430ecb6c8a198586b68946fb5bdf31910c`

```dockerfile
```

-	Layers:
	-	`sha256:56dc56746d2064417f72327f5dde8be74ac1e0eba26179e511e2b8ddd129b8e8`  
		Last Modified: Tue, 30 Dec 2025 03:50:49 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8238ebcb6217d1a5c2665f1a0cc625f1bbaa44a2c3fb7414de096394caaf0732`  
		Last Modified: Tue, 30 Dec 2025 03:50:50 GMT  
		Size: 25.9 KB (25867 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:bookworm`

```console
$ docker pull haskell@sha256:590e9e9c918d1c7b0a87badb0a6449105732fa0b7152be87ecfc149576d09614
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:5906cacce760379bcdc745eb02f756846ca4a0fa213ad3b21604c4095c61403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822424053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5191a918085facf1d579e06d8b7976ae263fcec63b12d04d5114171e9b9bce1f`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851bd5b066c6bc5263113a72ba6b03f8cd26c0e11ec21b4faee09fd49138f9ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 152.4 MB (152360257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7702220116f89c51e73d9030008d264fb0d258f70cdeb0d47124192649a8a8b`  
		Last Modified: Mon, 29 Dec 2025 23:20:33 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d7dacad299c850062d8a60ca3d62f23a1fb27e132af8d6a96b6c5c092153f`  
		Last Modified: Mon, 29 Dec 2025 23:21:18 GMT  
		Size: 591.8 MB (591755193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:c69dd9d58a2b4448bae5da7b44258efdf56f2b65fdfe2f1a425957c533faa84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620bcbc4e5d5426966bf9ea47bf486a0deef8d2b58e5aa9138e8c9a2d2277789`

```dockerfile
```

-	Layers:
	-	`sha256:a7c0c8cc14b721859c072fa36cd314b05d699933152bfe89930e04763ca67b65`  
		Last Modified: Tue, 30 Dec 2025 03:48:44 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da0a224b9700730cef9f784ff1c3bb008a0263ca3fdb5450e166255f06b420f`  
		Last Modified: Tue, 30 Dec 2025 03:48:45 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:bd4d7f122bfeb2b8ca0c8b666401862e03a7d2e91efd424f16f6e9687e765644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824926337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8255e5e92ffc6a0d411a4c3fdfa15b5a1aea3bec710d3ac9048714708a2483a1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c29931c3e00184d8309814c6bb94b8eae48b8d44cd8bb0b34c0a96704a32e1`  
		Last Modified: Mon, 29 Dec 2025 23:22:32 GMT  
		Size: 146.4 MB (146442606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd77a5299206d5e51acf0a90a31f30864e48172b41eeb9ee9efb392da0d93d6b`  
		Last Modified: Mon, 29 Dec 2025 23:21:52 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea94209ec2fd884df59dfdc57f9ffbe524964ff8aa73611e3e3e09146f5b027`  
		Last Modified: Mon, 29 Dec 2025 23:21:54 GMT  
		Size: 14.0 MB (13969019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e41e6094016ad14b3382f6e3587baeda522cea539bbf6ed42f7b692c200574`  
		Last Modified: Mon, 29 Dec 2025 23:22:26 GMT  
		Size: 591.6 MB (591627013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:31602177a7c7a147780a5579401ae9cd255111cc88275dc22e9aa05020184ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802e3273d59f837cff1550dd346cfe9d8495d6eafd81ef3bb361eb4af81a7555`

```dockerfile
```

-	Layers:
	-	`sha256:31c781c3abc8afecf26acbe00ddba616277b794b7932b9a23939a5a387d1da54`  
		Last Modified: Tue, 30 Dec 2025 03:48:53 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a259963f6a750d76c85f50b4a729093daf2b1543b7d7f0f56961c8853a9aa5`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:bullseye`

```console
$ docker pull haskell@sha256:cea76117ba2bf3e8110b9a849823e0d43deae6e2b2c39e3faf1e0c8475dcdcf0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:00294c6703b73b9bbb558d5d65c71be1c7c0a17190a79f758f8b9896f5200698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.2 MB (659154185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5bcc4f528a3fedbe74d658c13e262c3a06ee98ee2127fc5d082318dd435683`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:17:37 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:17:37 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:17:37 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:17:39 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:17:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:40 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:19:17 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:17 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:17 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:81c5fe73ee38995b42041f20ff8af640cf790ab264e1dc7316c4c1de7eceb4f1`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 53.8 MB (53756440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e03dd594824971fffd646434acd2f8cb944285d5662248793e7f5c1c652dd114`  
		Last Modified: Mon, 29 Dec 2025 23:20:52 GMT  
		Size: 133.8 MB (133759018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b890bf7f170ec3762847be6a1ba63596af0d5ff77f5c4c3780b95f3cb1e56e`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246a67688b8a1355ed3e249780619237cf63c0e6a4cfd98a22cd8a54c7685eca`  
		Last Modified: Mon, 29 Dec 2025 23:20:46 GMT  
		Size: 7.6 MB (7612240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbd7e04f4d501c556cc4d1d45d8270f66600167280999f842ac8b88c68d8538`  
		Last Modified: Mon, 29 Dec 2025 23:21:45 GMT  
		Size: 441.8 MB (441805720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a52a1555c472e2ad5d8dcc7b60d8c34c075a152cd15a9b6374d3342373b0eee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b55c9eb1d1092bc250758b0ae82591aec75e34fe61f4d6dd2d24e9050ebc2c`

```dockerfile
```

-	Layers:
	-	`sha256:d0371a3f0a3050fe378fe4d3fa46310837f121aad22e649c685ce8f50966d629`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffe3a711aa7b09bd9aaca3a75ad1409b4ddd813898dbdac1935e921fdfd9647`  
		Last Modified: Tue, 30 Dec 2025 03:48:55 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:f3275e745ce464ed808e373238abbd4082b512a2c62b1efce4fa96d20ddef3fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669448569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00ac34b1c314183a7cc2c5e72cc03aab5cace727fa4948ff501a96cac069f2a9`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1766966400'
# Mon, 29 Dec 2025 23:16:57 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:57 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:57 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:59 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:59 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:17:00 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC=9.10.3
# Mon, 29 Dec 2025 23:17:00 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Dec 2025 23:18:31 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:31 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:31 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:9cc7bc8e086c95eb3e992d2c623bd505740ab0a6afcbc89656d0bb477878489f`  
		Last Modified: Mon, 29 Dec 2025 22:27:00 GMT  
		Size: 52.3 MB (52257770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5280ec1a5df44236392d8b14bc966469c8c234eb70e8c65f31a370a3b097659`  
		Last Modified: Mon, 29 Dec 2025 23:20:19 GMT  
		Size: 129.2 MB (129240390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f35c2ef41b84da2a8492d69e5fe7209cf5338d9a0010a204d06e87d088a687e`  
		Last Modified: Mon, 29 Dec 2025 23:20:09 GMT  
		Size: 24.5 MB (24528547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:600ca497b466ab826688c761749af75c8e8a945a31f64e77480c3a540ec8b9b4`  
		Last Modified: Mon, 29 Dec 2025 23:20:08 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65a9628a3fd7f16cfbd6bf3b7c96b4c813428b9455cf994e163256726cf69d`  
		Last Modified: Mon, 29 Dec 2025 23:22:04 GMT  
		Size: 449.4 MB (449448901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:3add895d061fd10533b9ecead6bea7abf3dcf90882baf1a75c05a505860ea761
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b560cd801061656c03e8103be090f777480bef3726076902616cf5fa5436c60b`

```dockerfile
```

-	Layers:
	-	`sha256:a28e7344b8f75cfff907d15034128ee3784f9afd291da7bdfeb2005b6efa857c`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f01081a13d3bb59b97c2a776f3adb9bae72653eb9b007be9b36bb7919a286392`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26451 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:latest`

```console
$ docker pull haskell@sha256:590e9e9c918d1c7b0a87badb0a6449105732fa0b7152be87ecfc149576d09614
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:5906cacce760379bcdc745eb02f756846ca4a0fa213ad3b21604c4095c61403f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822424053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5191a918085facf1d579e06d8b7976ae263fcec63b12d04d5114171e9b9bce1f`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851bd5b066c6bc5263113a72ba6b03f8cd26c0e11ec21b4faee09fd49138f9ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:43 GMT  
		Size: 152.4 MB (152360257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7702220116f89c51e73d9030008d264fb0d258f70cdeb0d47124192649a8a8b`  
		Last Modified: Mon, 29 Dec 2025 23:20:33 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02d7dacad299c850062d8a60ca3d62f23a1fb27e132af8d6a96b6c5c092153f`  
		Last Modified: Mon, 29 Dec 2025 23:21:18 GMT  
		Size: 591.8 MB (591755193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:c69dd9d58a2b4448bae5da7b44258efdf56f2b65fdfe2f1a425957c533faa84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:620bcbc4e5d5426966bf9ea47bf486a0deef8d2b58e5aa9138e8c9a2d2277789`

```dockerfile
```

-	Layers:
	-	`sha256:a7c0c8cc14b721859c072fa36cd314b05d699933152bfe89930e04763ca67b65`  
		Last Modified: Tue, 30 Dec 2025 03:48:44 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9da0a224b9700730cef9f784ff1c3bb008a0263ca3fdb5450e166255f06b420f`  
		Last Modified: Tue, 30 Dec 2025 03:48:45 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:bd4d7f122bfeb2b8ca0c8b666401862e03a7d2e91efd424f16f6e9687e765644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824926337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8255e5e92ffc6a0d411a4c3fdfa15b5a1aea3bec710d3ac9048714708a2483a1`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:11 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c29931c3e00184d8309814c6bb94b8eae48b8d44cd8bb0b34c0a96704a32e1`  
		Last Modified: Mon, 29 Dec 2025 23:22:32 GMT  
		Size: 146.4 MB (146442606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd77a5299206d5e51acf0a90a31f30864e48172b41eeb9ee9efb392da0d93d6b`  
		Last Modified: Mon, 29 Dec 2025 23:21:52 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea94209ec2fd884df59dfdc57f9ffbe524964ff8aa73611e3e3e09146f5b027`  
		Last Modified: Mon, 29 Dec 2025 23:21:54 GMT  
		Size: 14.0 MB (13969019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e41e6094016ad14b3382f6e3587baeda522cea539bbf6ed42f7b692c200574`  
		Last Modified: Mon, 29 Dec 2025 23:22:26 GMT  
		Size: 591.6 MB (591627013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:31602177a7c7a147780a5579401ae9cd255111cc88275dc22e9aa05020184ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802e3273d59f837cff1550dd346cfe9d8495d6eafd81ef3bb361eb4af81a7555`

```dockerfile
```

-	Layers:
	-	`sha256:31c781c3abc8afecf26acbe00ddba616277b794b7932b9a23939a5a387d1da54`  
		Last Modified: Tue, 30 Dec 2025 03:48:53 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0a259963f6a750d76c85f50b4a729093daf2b1543b7d7f0f56961c8853a9aa5`  
		Last Modified: Tue, 30 Dec 2025 03:48:54 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim`

```console
$ docker pull haskell@sha256:634cc56adaa1dd9f2321f640fb45fcbcb8363153ab37a977f971ee150247412f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:97b16c440c491654aba4c95e9c3132e1e4e1a065a709cce713390d160ca74f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774212235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92003b13829d688409aab1d1c244ff262fed57faa9d1acc3eb83a72f7c26fe35`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:53 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:53 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b04edbc0c4dfa46fafd245a2b2a0b057b91d4a81d0914d396de56028f15ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:59 GMT  
		Size: 124.4 MB (124406228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100a9279ba93680fbe144ea31c9310ac12a0b5045f9db11db3a1e983e6e881ff`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36999b209606621dff474cc3fab4ecd44dddd3fe5c75bc92e440b6bb2f440a7f`  
		Last Modified: Mon, 29 Dec 2025 23:21:27 GMT  
		Size: 591.7 MB (591749776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim` - unknown; unknown

```console
$ docker pull haskell@sha256:eb0a2eb25660433b057a136f94dd660e17aef1f7a886387332d0a202a350b679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beba287c9837e41e99ff8f16de2652cc3d58080378e0357676dbe31c6b1daef4`

```dockerfile
```

-	Layers:
	-	`sha256:c8203cc4441763cf885e243f30d1630bc4c9a2a8c9759cba1c9a00acd995af77`  
		Last Modified: Tue, 30 Dec 2025 03:49:01 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd8ac24ce53a5207506ee8d7470313245cad1af0536175db5dc5110cfb18fca`  
		Last Modified: Tue, 30 Dec 2025 03:49:02 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:436435637aade026aa72bc34a8d91add8d7b32abe92f5e260d08cb85ff2388c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776710338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d149018b8046249b7e234dcd59bd0503f2c249b1da5ea71b9d7d07a34c78a14`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:58 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6377ba840a84af4c909b1eb1ef8792c6e8706b5e4320bfcf8c5e0ff25014fa`  
		Last Modified: Mon, 29 Dec 2025 23:22:01 GMT  
		Size: 118.5 MB (118483759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf44bd0db910fbbca8952d8094f8283bf8770a881423599b00480f8af3efa80`  
		Last Modified: Mon, 29 Dec 2025 23:21:55 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10d58ac69a8b25366852eb5b7a018d15122af20d6ca8d9d4bda3a25c4a50923`  
		Last Modified: Mon, 29 Dec 2025 23:21:53 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac8e82e01a1db4cc233e5dbd8d55fabe6d0bd6a1054f8d4de384afd7d6feb2`  
		Last Modified: Mon, 29 Dec 2025 23:22:02 GMT  
		Size: 591.6 MB (591626795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim` - unknown; unknown

```console
$ docker pull haskell@sha256:e3d29985b25e02b3b6a90a7604a0f196bbebbb5a28627f5d3d227d44dbcd856d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1900668bc3a5e6c83a877a880e3cac853d615d7328cf7994004a6c9a031d80`

```dockerfile
```

-	Layers:
	-	`sha256:906ed3303f7f61337f39822b8214a83bf6701ce24504ab71585ca891197cfed1`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c16428de8f412befe040c1b5cb388bdd0663ecee5cc13bf70e7ddf78819791`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim-bookworm`

```console
$ docker pull haskell@sha256:634cc56adaa1dd9f2321f640fb45fcbcb8363153ab37a977f971ee150247412f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:97b16c440c491654aba4c95e9c3132e1e4e1a065a709cce713390d160ca74f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774212235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92003b13829d688409aab1d1c244ff262fed57faa9d1acc3eb83a72f7c26fe35`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:44 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:44 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:44 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:46 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:48 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:18:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:18:53 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:18:53 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065b04edbc0c4dfa46fafd245a2b2a0b057b91d4a81d0914d396de56028f15ef`  
		Last Modified: Mon, 29 Dec 2025 23:20:59 GMT  
		Size: 124.4 MB (124406228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:100a9279ba93680fbe144ea31c9310ac12a0b5045f9db11db3a1e983e6e881ff`  
		Last Modified: Mon, 29 Dec 2025 23:20:47 GMT  
		Size: 22.2 MB (22220751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02bad5e61117345a500b24ddda8bb642e492b23635c361430292621f12700ac6`  
		Last Modified: Mon, 29 Dec 2025 23:20:32 GMT  
		Size: 7.6 MB (7607056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36999b209606621dff474cc3fab4ecd44dddd3fe5c75bc92e440b6bb2f440a7f`  
		Last Modified: Mon, 29 Dec 2025 23:21:27 GMT  
		Size: 591.7 MB (591749776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:eb0a2eb25660433b057a136f94dd660e17aef1f7a886387332d0a202a350b679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beba287c9837e41e99ff8f16de2652cc3d58080378e0357676dbe31c6b1daef4`

```dockerfile
```

-	Layers:
	-	`sha256:c8203cc4441763cf885e243f30d1630bc4c9a2a8c9759cba1c9a00acd995af77`  
		Last Modified: Tue, 30 Dec 2025 03:49:01 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd8ac24ce53a5207506ee8d7470313245cad1af0536175db5dc5110cfb18fca`  
		Last Modified: Tue, 30 Dec 2025 03:49:02 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:436435637aade026aa72bc34a8d91add8d7b32abe92f5e260d08cb85ff2388c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776710338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d149018b8046249b7e234dcd59bd0503f2c249b1da5ea71b9d7d07a34c78a14`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:07 GMT
ENV LANG=C.UTF-8
# Mon, 29 Dec 2025 23:16:07 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK=3.3.1
# Mon, 29 Dec 2025 23:16:07 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 29 Dec 2025 23:16:09 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL=3.14.1.1
# Mon, 29 Dec 2025 23:16:09 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Dec 2025 23:16:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC=9.12.2
# Mon, 29 Dec 2025 23:16:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Mon, 29 Dec 2025 23:19:58 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Mon, 29 Dec 2025 23:19:58 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Dec 2025 23:19:58 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6377ba840a84af4c909b1eb1ef8792c6e8706b5e4320bfcf8c5e0ff25014fa`  
		Last Modified: Mon, 29 Dec 2025 23:22:01 GMT  
		Size: 118.5 MB (118483759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf44bd0db910fbbca8952d8094f8283bf8770a881423599b00480f8af3efa80`  
		Last Modified: Mon, 29 Dec 2025 23:21:55 GMT  
		Size: 24.5 MB (24528552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10d58ac69a8b25366852eb5b7a018d15122af20d6ca8d9d4bda3a25c4a50923`  
		Last Modified: Mon, 29 Dec 2025 23:21:53 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac8e82e01a1db4cc233e5dbd8d55fabe6d0bd6a1054f8d4de384afd7d6feb2`  
		Last Modified: Mon, 29 Dec 2025 23:22:02 GMT  
		Size: 591.6 MB (591626795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:e3d29985b25e02b3b6a90a7604a0f196bbebbb5a28627f5d3d227d44dbcd856d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1900668bc3a5e6c83a877a880e3cac853d615d7328cf7994004a6c9a031d80`

```dockerfile
```

-	Layers:
	-	`sha256:906ed3303f7f61337f39822b8214a83bf6701ce24504ab71585ca891197cfed1`  
		Last Modified: Tue, 30 Dec 2025 03:49:07 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c16428de8f412befe040c1b5cb388bdd0663ecee5cc13bf70e7ddf78819791`  
		Last Modified: Tue, 30 Dec 2025 03:49:08 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

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
