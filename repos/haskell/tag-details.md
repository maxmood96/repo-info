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
$ docker pull haskell@sha256:78c823f5c5723101cd3a50139ccc247d916d1bea7480c6aabd38eff59e28e647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:a41bf6877d1b1c87c421f94a4638eba7df8218bb2cbad0f71fef0e70c92602b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822417895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6aa04b16cabf65b9d6d22c021edde2947d51f1ac99f7ea60c9ff2a66ecdaf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 00:58:45 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 00:58:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 00:58:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 00:58:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:00:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:00:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:00:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74e79de258e3316172835a71c06df1674203435ce381ddb37305408e4d8730`  
		Last Modified: Wed, 05 Nov 2025 04:13:29 GMT  
		Size: 152.4 MB (152350699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553b1f0dd1e197cbbe3f0463774823e46927db001afa401edd276a3b99489d30`  
		Last Modified: Wed, 05 Nov 2025 01:02:51 GMT  
		Size: 22.2 MB (22220772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd0d14b3991f9f0aebe9120fa0a7204e23303c50fc1a8f5af5f3738c20f88b`  
		Last Modified: Wed, 05 Nov 2025 01:02:56 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd2b0e9ae55c4f5be104cd2eedef25c4289355a15a18cfaec59f5ba30f280d`  
		Last Modified: Wed, 05 Nov 2025 04:14:02 GMT  
		Size: 591.8 MB (591758313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9` - unknown; unknown

```console
$ docker pull haskell@sha256:458e9b22beeb9921367aefa61ed3d13dd8a57d4f32a4f5d9bf110ac9dcadd790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14e893bb39433aadd3fbed2ded5e11e67866c9e8a69c7f68baeadb53a586067`

```dockerfile
```

-	Layers:
	-	`sha256:3192e5864311a3b4d24424073b8bd90e596f8710e6a70e7d14fc2527780434f7`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43221b79dcf6f8d53e8a9c4d6c37c39c1f7bb2e76922487e0fb0cb8432ff84af`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7fd9839058ccbb571a8e2d0d0a5893bbe11fb7ae709fc10082f993febdba6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824914239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142829b70e18729d3f9677cc8adbaca4536552fd98b3e9c517fd6d4dd3d8c10e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce95fd68f2b36a165ba3ad3e35396590889fb3e4056830890a496db707cf348`  
		Last Modified: Wed, 05 Nov 2025 02:50:44 GMT  
		Size: 146.4 MB (146430422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48665fd90cd640558ea256bbd3e5c928979d6e482f935f4c34d851c1efe4b4`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ffee524ac5f20f017307ec386b9e5d9c2626ffa50ba57f8803695768046f38`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c2a5bf9e7458376d169214655aff5fed34472997e6bdb214d76466ef72931`  
		Last Modified: Wed, 05 Nov 2025 02:51:25 GMT  
		Size: 591.6 MB (591626752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9` - unknown; unknown

```console
$ docker pull haskell@sha256:733ae5fb5d3735a1be1196b14601606d235545c4ed86a7f75bf912dcb67daf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a81146c4e4b94307c4afb5035ddb5ad5bee3eb364f569f36482536eca91fd5`

```dockerfile
```

-	Layers:
	-	`sha256:ac0049f8b5386b8a7aaef447204d3098e0db4e28e1ef34c66bc13c3480601908`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b59f5afbc59dba62205816d52797470ff0bf9edb8a603bedfba451414f5994`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-bookworm`

```console
$ docker pull haskell@sha256:78c823f5c5723101cd3a50139ccc247d916d1bea7480c6aabd38eff59e28e647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:a41bf6877d1b1c87c421f94a4638eba7df8218bb2cbad0f71fef0e70c92602b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822417895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6aa04b16cabf65b9d6d22c021edde2947d51f1ac99f7ea60c9ff2a66ecdaf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 00:58:45 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 00:58:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 00:58:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 00:58:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:00:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:00:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:00:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74e79de258e3316172835a71c06df1674203435ce381ddb37305408e4d8730`  
		Last Modified: Wed, 05 Nov 2025 04:13:29 GMT  
		Size: 152.4 MB (152350699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553b1f0dd1e197cbbe3f0463774823e46927db001afa401edd276a3b99489d30`  
		Last Modified: Wed, 05 Nov 2025 01:02:51 GMT  
		Size: 22.2 MB (22220772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd0d14b3991f9f0aebe9120fa0a7204e23303c50fc1a8f5af5f3738c20f88b`  
		Last Modified: Wed, 05 Nov 2025 01:02:56 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd2b0e9ae55c4f5be104cd2eedef25c4289355a15a18cfaec59f5ba30f280d`  
		Last Modified: Wed, 05 Nov 2025 04:14:02 GMT  
		Size: 591.8 MB (591758313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:458e9b22beeb9921367aefa61ed3d13dd8a57d4f32a4f5d9bf110ac9dcadd790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14e893bb39433aadd3fbed2ded5e11e67866c9e8a69c7f68baeadb53a586067`

```dockerfile
```

-	Layers:
	-	`sha256:3192e5864311a3b4d24424073b8bd90e596f8710e6a70e7d14fc2527780434f7`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43221b79dcf6f8d53e8a9c4d6c37c39c1f7bb2e76922487e0fb0cb8432ff84af`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7fd9839058ccbb571a8e2d0d0a5893bbe11fb7ae709fc10082f993febdba6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824914239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142829b70e18729d3f9677cc8adbaca4536552fd98b3e9c517fd6d4dd3d8c10e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce95fd68f2b36a165ba3ad3e35396590889fb3e4056830890a496db707cf348`  
		Last Modified: Wed, 05 Nov 2025 02:50:44 GMT  
		Size: 146.4 MB (146430422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48665fd90cd640558ea256bbd3e5c928979d6e482f935f4c34d851c1efe4b4`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ffee524ac5f20f017307ec386b9e5d9c2626ffa50ba57f8803695768046f38`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c2a5bf9e7458376d169214655aff5fed34472997e6bdb214d76466ef72931`  
		Last Modified: Wed, 05 Nov 2025 02:51:25 GMT  
		Size: 591.6 MB (591626752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:733ae5fb5d3735a1be1196b14601606d235545c4ed86a7f75bf912dcb67daf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a81146c4e4b94307c4afb5035ddb5ad5bee3eb364f569f36482536eca91fd5`

```dockerfile
```

-	Layers:
	-	`sha256:ac0049f8b5386b8a7aaef447204d3098e0db4e28e1ef34c66bc13c3480601908`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b59f5afbc59dba62205816d52797470ff0bf9edb8a603bedfba451414f5994`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-bullseye`

```console
$ docker pull haskell@sha256:dd81ed941a848ffb0eced55b63e85f2b8986d82578b64f44636b602ddb521610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:81a86e1ea160f85082562f10e1928a59a0c9ab8987aca9feb7a9a1987740f290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659125300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9387a429a5d5704c5ef75bd2051dafc8168966a1746cd4939de77e87cef6aca`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:02:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dffd0aee3bf7bbe35a7b471cef359eeefa13932dbd4df53017ba1f4307c844`  
		Last Modified: Wed, 05 Nov 2025 06:48:41 GMT  
		Size: 133.7 MB (133737186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045be5b92248b3d9bd5effb953305a0912cfea45e2d0a718e4e07b4f45643d3c`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0f78eeb3db594d1db2c288857f115a46a17204edf96119a5b6432088628d9`  
		Last Modified: Wed, 05 Nov 2025 01:04:45 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0900a9b4accb5d08271764254a00f9ae17937fa2ed3c65bd1b4ee01e7f9db6e`  
		Last Modified: Wed, 05 Nov 2025 06:48:51 GMT  
		Size: 441.8 MB (441798409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:7c9f9e34fe9c803e250b12ef12d39fbcf840f817a88d62983f4c0a7b7b980297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c01f7c7feef3ff0514632720135dfe5d8aa28e70104a9c252e023a5a89b963`

```dockerfile
```

-	Layers:
	-	`sha256:1d39ab4b5cbea0dd076770c00259350040057f3f1fb3ee893a983db7f135a9ba`  
		Last Modified: Wed, 05 Nov 2025 03:48:24 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3e9b3aa3a9ed7bde2a358779c5416b443af533319e267402593ae6dd7dc6ac`  
		Last Modified: Wed, 05 Nov 2025 03:48:25 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8d73683c844837d5df96b274c017588f5e304e505a4a82f52bb0f6d1d04071d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669436520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7015f6723d585232346cd27459b66255821f3481dab0165c2e987e7e15578af8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896b69b58297e59a819a754d1e990f5d5ad269382647d19ea7d2aa668a5f7dfd`  
		Last Modified: Tue, 04 Nov 2025 23:25:22 GMT  
		Size: 129.2 MB (129224321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12a3c165fda31a17180ab1d45a2568d86791617546c97974383027ac7b80ad1`  
		Last Modified: Tue, 04 Nov 2025 23:25:47 GMT  
		Size: 24.5 MB (24528595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fa173cb85a42b8185c9bb59004594f75717dcabc5952241d81e1d300698619`  
		Last Modified: Tue, 04 Nov 2025 23:25:46 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ef4e39dd7279c474796198d827f6eb2fe0943f03c5139be85df71245042b9b`  
		Last Modified: Tue, 04 Nov 2025 23:25:38 GMT  
		Size: 449.5 MB (449452674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:58b8f891da64e3f0776e1ee1c6be2fdc69f6fdf994740cc9d9587ab0087b4c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997597fa5f7ab7d0a4367631f13242b49e245acb41b5da7e45e02402ecfed3cf`

```dockerfile
```

-	Layers:
	-	`sha256:1c7af5b1988122c9eb842a9c4af1dbcc8a74ea4227340c3b8958d12b12146add`  
		Last Modified: Wed, 05 Nov 2025 00:48:43 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170f7fda7578f769f8289b3c507d4becdbf308b131256b716dee71cbc6c1f07d`  
		Last Modified: Wed, 05 Nov 2025 00:48:44 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim`

```console
$ docker pull haskell@sha256:fb2bda3959b5c4571312a9449c69854eec11ec15cc6f1bc15b54c44595cd9f4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:6661f83b6d9612b7ee355aed52957acd2dcb22cfa1168f375a624d2a07b46890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774226835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f4c09f9d50ce6b07424304779854802bac7a82f4c7dd3cec4a3b2e167f6ed4`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 01:00:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:00:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:00:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:00:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:02:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8271a965164bc23e31a9ddc248acd56dc871d237df6cc16e874a150569eb6bb7`  
		Last Modified: Wed, 05 Nov 2025 01:04:57 GMT  
		Size: 124.4 MB (124406092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d291c4dad79d17a29c3070282e992374454228cd4f0a8e2ff72e502e31456d24`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba317e1a05fa997b78d6cc5fd1590cd99192bd8f5909a91bbfea0a74e0d2d2a`  
		Last Modified: Wed, 05 Nov 2025 01:04:48 GMT  
		Size: 7.6 MB (7607061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f57245b6c97717b46d25fa4b02c34ac804e6c463ccc00f25644b5b3eb3d12`  
		Last Modified: Wed, 05 Nov 2025 04:41:27 GMT  
		Size: 591.8 MB (591764340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:b7d82e0f1f51b7d13f302097cc8e888935740cdacd5da61700eff68fac593d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46f9f3507602fe823509b330fbf15659afab945a1878bc5073ff44f325c31c2`

```dockerfile
```

-	Layers:
	-	`sha256:3c6cfa885e60075b0c7ec2e259343e3075a93afb5f61b3a939ef1c5304c2ad9b`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9454075c4b79dba3e00b3fb64ab2d514a25e318ea3914abb34adedabdeef073`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:428c38c35848ae20da237bb4c2e9a3660800fe96a93a37ec33e6d26dd5a12cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776707214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf631611acadbab9fc2f73bb9d7b518d15bf2e7478ccaac9cfdd8c0923999b5`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd10243405c62faa4120f029da948bde716bfe5475ad9e3559253bd0925ffa`  
		Last Modified: Tue, 04 Nov 2025 23:26:28 GMT  
		Size: 118.5 MB (118483733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c5c5a35659575c20b89d69badcf9aa3374cedbfda46a8d3b7b833b02ff6f8`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9fa47c2d351040977a11cd8fb7cbff5bf5a2667ff33e7fe33cbd02d540304`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8155cd34b96433ff8496257790a2ddfd1c8b9f2295601acb8a12baecf1a8765a`  
		Last Modified: Tue, 04 Nov 2025 23:25:59 GMT  
		Size: 591.6 MB (591623479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:176bb96490f2f6215b29823180e44df23adcaf8b4f257f02965957b5401322d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f404b57cb062f3f8b0be0d26974da9218b9852ec75070e382b144b6f5da0cc`

```dockerfile
```

-	Layers:
	-	`sha256:bd037653b5928dfb4a639ce168667ebfc3edf471756dda6f8e41feaea3b71b5e`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4933ebfa06d93dd61896b287216f2341093ff3c290b5980c745a0d66995084b`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim-bookworm`

```console
$ docker pull haskell@sha256:fb2bda3959b5c4571312a9449c69854eec11ec15cc6f1bc15b54c44595cd9f4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:6661f83b6d9612b7ee355aed52957acd2dcb22cfa1168f375a624d2a07b46890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774226835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f4c09f9d50ce6b07424304779854802bac7a82f4c7dd3cec4a3b2e167f6ed4`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 01:00:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:00:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:00:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:00:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:02:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8271a965164bc23e31a9ddc248acd56dc871d237df6cc16e874a150569eb6bb7`  
		Last Modified: Wed, 05 Nov 2025 01:04:57 GMT  
		Size: 124.4 MB (124406092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d291c4dad79d17a29c3070282e992374454228cd4f0a8e2ff72e502e31456d24`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba317e1a05fa997b78d6cc5fd1590cd99192bd8f5909a91bbfea0a74e0d2d2a`  
		Last Modified: Wed, 05 Nov 2025 01:04:48 GMT  
		Size: 7.6 MB (7607061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f57245b6c97717b46d25fa4b02c34ac804e6c463ccc00f25644b5b3eb3d12`  
		Last Modified: Wed, 05 Nov 2025 04:41:27 GMT  
		Size: 591.8 MB (591764340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:b7d82e0f1f51b7d13f302097cc8e888935740cdacd5da61700eff68fac593d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46f9f3507602fe823509b330fbf15659afab945a1878bc5073ff44f325c31c2`

```dockerfile
```

-	Layers:
	-	`sha256:3c6cfa885e60075b0c7ec2e259343e3075a93afb5f61b3a939ef1c5304c2ad9b`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9454075c4b79dba3e00b3fb64ab2d514a25e318ea3914abb34adedabdeef073`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:428c38c35848ae20da237bb4c2e9a3660800fe96a93a37ec33e6d26dd5a12cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776707214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf631611acadbab9fc2f73bb9d7b518d15bf2e7478ccaac9cfdd8c0923999b5`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd10243405c62faa4120f029da948bde716bfe5475ad9e3559253bd0925ffa`  
		Last Modified: Tue, 04 Nov 2025 23:26:28 GMT  
		Size: 118.5 MB (118483733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c5c5a35659575c20b89d69badcf9aa3374cedbfda46a8d3b7b833b02ff6f8`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9fa47c2d351040977a11cd8fb7cbff5bf5a2667ff33e7fe33cbd02d540304`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8155cd34b96433ff8496257790a2ddfd1c8b9f2295601acb8a12baecf1a8765a`  
		Last Modified: Tue, 04 Nov 2025 23:25:59 GMT  
		Size: 591.6 MB (591623479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:176bb96490f2f6215b29823180e44df23adcaf8b4f257f02965957b5401322d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f404b57cb062f3f8b0be0d26974da9218b9852ec75070e382b144b6f5da0cc`

```dockerfile
```

-	Layers:
	-	`sha256:bd037653b5928dfb4a639ce168667ebfc3edf471756dda6f8e41feaea3b71b5e`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4933ebfa06d93dd61896b287216f2341093ff3c290b5980c745a0d66995084b`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9-slim-bullseye`

```console
$ docker pull haskell@sha256:415e263078684c25a11918122c8173f671f05b6f4809c3321bd8e813ed414c5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f3ab4f23ec881de6220a2b68b599406140cef1ed63fc60c2de649d35f24a5e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608258987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdc26fd61aeddbe576dd48a9595f1beba39f8a0b04fe1a8dc065c94b58d574c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:26 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:26 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:30 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:03:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923f781df5b8a5c4299278e3418c8167b0755e231951fad172068cef8d708870`  
		Last Modified: Wed, 05 Nov 2025 01:04:38 GMT  
		Size: 106.4 MB (106366669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295a975b946c68a39b8fa62e02be53316c8932176eac7227b6b0bc86b95148a0`  
		Last Modified: Wed, 05 Nov 2025 01:04:28 GMT  
		Size: 22.2 MB (22220774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084d0d48b3516b6c62cd1a7ca37708fc2d5aa8454ff1398a6eb68baff6597d99`  
		Last Modified: Wed, 05 Nov 2025 01:04:26 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14992ee7da922ef406db6cf1542f4cb2619512aa477d189bb6b568536233e7ca`  
		Last Modified: Wed, 05 Nov 2025 06:58:18 GMT  
		Size: 441.8 MB (441800705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:4f01384a4a590600f239c8daf1e0269803ff098779e1726b0bdd85bb745dfc4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ebc71cba910e7c4ffc7bf31b6643dfbca8abd8fc5e3457ef9737b5a7f4e160`

```dockerfile
```

-	Layers:
	-	`sha256:d49c2acab03cbb152b37481eca7475af2446bfa5d70ae4c03d1cbbd65984be15`  
		Last Modified: Wed, 05 Nov 2025 03:48:36 GMT  
		Size: 6.8 MB (6750929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8dfdca42123fdcddcd45976dc302fd49052d6c7d91b2128d2dae3c2198230cb`  
		Last Modified: Wed, 05 Nov 2025 03:48:37 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:4c155d54fb64720b4a09291dd911e1a8cdc9d64b062258a9a591de4c379974c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618570950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57691ad02377bce23fb606584a35a7b0e855d4452482e09e7279bd9515541a0`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:16 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:19 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:19 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:20 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d275ddfa41ee2d9ccfc71507f0292da1aba94bd2f501c5ddfd430907b4dc50`  
		Last Modified: Tue, 04 Nov 2025 23:25:29 GMT  
		Size: 101.9 MB (101863502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd2b3f08398c1bfe2ef3c048abc27c058f7a6fcba39580a722e21bec8ad343b`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46140ed114cae7d7b0b71a188690513fe284c7320050bb4dba82f025b8f68258`  
		Last Modified: Tue, 04 Nov 2025 23:25:23 GMT  
		Size: 14.0 MB (13972958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dd63d00101136020b2a86961bdf45b99f7cf0d3fc0362b559d2dc080561e80`  
		Last Modified: Tue, 04 Nov 2025 23:25:15 GMT  
		Size: 449.5 MB (449457387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:1084beeb40a2a5530f4f1fe6ca4ff5c39130aeae6205de0dff0d411c4f681e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e3c86c3ae0c45dcf954bb7443da4384fed2e7e868430588319acef4cd3a506`

```dockerfile
```

-	Layers:
	-	`sha256:70296bae1d0c5102672799af1c2caf71d4fb7e46af35ccf067f5300e0b6fb0a7`  
		Last Modified: Wed, 05 Nov 2025 00:48:52 GMT  
		Size: 6.8 MB (6753439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4b054ea1508bde495c990515594f0b04af77f5c1df839aae61e2a0056793990`  
		Last Modified: Wed, 05 Nov 2025 00:48:53 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10`

```console
$ docker pull haskell@sha256:dd81ed941a848ffb0eced55b63e85f2b8986d82578b64f44636b602ddb521610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10` - linux; amd64

```console
$ docker pull haskell@sha256:81a86e1ea160f85082562f10e1928a59a0c9ab8987aca9feb7a9a1987740f290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659125300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9387a429a5d5704c5ef75bd2051dafc8168966a1746cd4939de77e87cef6aca`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:02:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dffd0aee3bf7bbe35a7b471cef359eeefa13932dbd4df53017ba1f4307c844`  
		Last Modified: Wed, 05 Nov 2025 06:48:41 GMT  
		Size: 133.7 MB (133737186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045be5b92248b3d9bd5effb953305a0912cfea45e2d0a718e4e07b4f45643d3c`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0f78eeb3db594d1db2c288857f115a46a17204edf96119a5b6432088628d9`  
		Last Modified: Wed, 05 Nov 2025 01:04:45 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0900a9b4accb5d08271764254a00f9ae17937fa2ed3c65bd1b4ee01e7f9db6e`  
		Last Modified: Wed, 05 Nov 2025 06:48:51 GMT  
		Size: 441.8 MB (441798409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10` - unknown; unknown

```console
$ docker pull haskell@sha256:7c9f9e34fe9c803e250b12ef12d39fbcf840f817a88d62983f4c0a7b7b980297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c01f7c7feef3ff0514632720135dfe5d8aa28e70104a9c252e023a5a89b963`

```dockerfile
```

-	Layers:
	-	`sha256:1d39ab4b5cbea0dd076770c00259350040057f3f1fb3ee893a983db7f135a9ba`  
		Last Modified: Wed, 05 Nov 2025 03:48:24 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3e9b3aa3a9ed7bde2a358779c5416b443af533319e267402593ae6dd7dc6ac`  
		Last Modified: Wed, 05 Nov 2025 03:48:25 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8d73683c844837d5df96b274c017588f5e304e505a4a82f52bb0f6d1d04071d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669436520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7015f6723d585232346cd27459b66255821f3481dab0165c2e987e7e15578af8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896b69b58297e59a819a754d1e990f5d5ad269382647d19ea7d2aa668a5f7dfd`  
		Last Modified: Tue, 04 Nov 2025 23:25:22 GMT  
		Size: 129.2 MB (129224321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12a3c165fda31a17180ab1d45a2568d86791617546c97974383027ac7b80ad1`  
		Last Modified: Tue, 04 Nov 2025 23:25:47 GMT  
		Size: 24.5 MB (24528595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fa173cb85a42b8185c9bb59004594f75717dcabc5952241d81e1d300698619`  
		Last Modified: Tue, 04 Nov 2025 23:25:46 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ef4e39dd7279c474796198d827f6eb2fe0943f03c5139be85df71245042b9b`  
		Last Modified: Tue, 04 Nov 2025 23:25:38 GMT  
		Size: 449.5 MB (449452674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10` - unknown; unknown

```console
$ docker pull haskell@sha256:58b8f891da64e3f0776e1ee1c6be2fdc69f6fdf994740cc9d9587ab0087b4c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997597fa5f7ab7d0a4367631f13242b49e245acb41b5da7e45e02402ecfed3cf`

```dockerfile
```

-	Layers:
	-	`sha256:1c7af5b1988122c9eb842a9c4af1dbcc8a74ea4227340c3b8958d12b12146add`  
		Last Modified: Wed, 05 Nov 2025 00:48:43 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170f7fda7578f769f8289b3c507d4becdbf308b131256b716dee71cbc6c1f07d`  
		Last Modified: Wed, 05 Nov 2025 00:48:44 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-bookworm`

```console
$ docker pull haskell@sha256:d83036d9bbe82cd21ecdd78a872c029c3cdb06980329da2f33bb20bcd1cd60f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:d3c4d8a24888c4e217ff22400aff51b79914cbd87426be06719125b8dfa3db90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672776357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2698ad5456b6eb38b494492a59f4c8e9225595ed5c297c78672709c0a5d0ed2`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 01:01:03 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:03 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:03 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:05 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:07 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:02:45 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:45 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e373b7f712e78e5715c63f4a6b2eacef73814251fcb0076aeb4d8d7dee86e55d`  
		Last Modified: Wed, 05 Nov 2025 06:39:58 GMT  
		Size: 152.4 MB (152350630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb49f70db680ece953f55aea331a7f0bbf9dbdd9ba1dd4d2090325fb95731f4`  
		Last Modified: Wed, 05 Nov 2025 01:04:27 GMT  
		Size: 22.2 MB (22220766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d79705fa256dc0a20e12ba34ee873567b70b2b10fd46fbf8c457fb960d9aee`  
		Last Modified: Wed, 05 Nov 2025 01:04:27 GMT  
		Size: 7.6 MB (7607051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1860ed18f447c17a06950413a60cc01c02f48941187331e5eb8e436248a6bd`  
		Last Modified: Wed, 05 Nov 2025 06:40:02 GMT  
		Size: 442.1 MB (442116854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:e8f066f7e9103b351dc255520e5ca0ba07a572a14cfd193f519f0167879e7a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188cd376afe6de97b92884a8ebcd23493d15a1755b648f55671a9a0f53b7247d`

```dockerfile
```

-	Layers:
	-	`sha256:5e0e2392cd37627596da4061517f3ccc152ea2800d16a0b54380a3d2a65904c0`  
		Last Modified: Wed, 05 Nov 2025 03:48:43 GMT  
		Size: 9.5 MB (9478462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ec54a248f8b1856493631ccbe63c58db4926b0776878382acd8d9120f8dc48`  
		Last Modified: Wed, 05 Nov 2025 03:48:44 GMT  
		Size: 25.4 KB (25354 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:2a67d4ac55e36e4cbad3b28397fae12748ce37b9c0fcf626a2637af02915fa57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.7 MB (682735483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5561cea3cea22188c380a78746cb0c613d8a754c8594816822159ea35c84dddd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:16 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:16 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:40 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:40 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd427febe62e8d07726b1d34c46b42cda18280846c91bd6076f610a60aa81c3e`  
		Last Modified: Tue, 04 Nov 2025 23:25:04 GMT  
		Size: 146.4 MB (146430286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f37339d36a6ed12a12f4c5da3602ff2430a07e3fc0ea0bfcd7ae0af6edd8a`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481416619574b664be42d99c63a38f91844fe0e5ddd0c8ba7c8e319a77a0fc89`  
		Last Modified: Tue, 04 Nov 2025 23:25:23 GMT  
		Size: 14.0 MB (13969029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5303524c160a35357df9a815d36750c25fe0093b4f00977604cb0d069127de`  
		Last Modified: Tue, 04 Nov 2025 23:25:15 GMT  
		Size: 449.4 MB (449448087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:58ca1fa7c9d810d04eed58ab299c0e84110cbdd5d0096ff463f208557c5737cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9531727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145676a649d79ef54282cd803ccfc4ef2adecf75efa1e17f68e8d3c7eda1fe77`

```dockerfile
```

-	Layers:
	-	`sha256:cb9936cbaa7aa9d56f1240be22ef15968011ccaf168bcb8b9f1859fc5136119e`  
		Last Modified: Wed, 05 Nov 2025 00:48:55 GMT  
		Size: 9.5 MB (9506246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07c4579db390c634071c4ade5c88c96d828dd4ffb585f3eaccd6d4bf1b3c1346`  
		Last Modified: Wed, 05 Nov 2025 00:48:56 GMT  
		Size: 25.5 KB (25481 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-bullseye`

```console
$ docker pull haskell@sha256:dd81ed941a848ffb0eced55b63e85f2b8986d82578b64f44636b602ddb521610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:81a86e1ea160f85082562f10e1928a59a0c9ab8987aca9feb7a9a1987740f290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659125300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9387a429a5d5704c5ef75bd2051dafc8168966a1746cd4939de77e87cef6aca`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:02:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dffd0aee3bf7bbe35a7b471cef359eeefa13932dbd4df53017ba1f4307c844`  
		Last Modified: Wed, 05 Nov 2025 06:48:41 GMT  
		Size: 133.7 MB (133737186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045be5b92248b3d9bd5effb953305a0912cfea45e2d0a718e4e07b4f45643d3c`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0f78eeb3db594d1db2c288857f115a46a17204edf96119a5b6432088628d9`  
		Last Modified: Wed, 05 Nov 2025 01:04:45 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0900a9b4accb5d08271764254a00f9ae17937fa2ed3c65bd1b4ee01e7f9db6e`  
		Last Modified: Wed, 05 Nov 2025 06:48:51 GMT  
		Size: 441.8 MB (441798409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:7c9f9e34fe9c803e250b12ef12d39fbcf840f817a88d62983f4c0a7b7b980297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c01f7c7feef3ff0514632720135dfe5d8aa28e70104a9c252e023a5a89b963`

```dockerfile
```

-	Layers:
	-	`sha256:1d39ab4b5cbea0dd076770c00259350040057f3f1fb3ee893a983db7f135a9ba`  
		Last Modified: Wed, 05 Nov 2025 03:48:24 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3e9b3aa3a9ed7bde2a358779c5416b443af533319e267402593ae6dd7dc6ac`  
		Last Modified: Wed, 05 Nov 2025 03:48:25 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8d73683c844837d5df96b274c017588f5e304e505a4a82f52bb0f6d1d04071d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669436520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7015f6723d585232346cd27459b66255821f3481dab0165c2e987e7e15578af8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896b69b58297e59a819a754d1e990f5d5ad269382647d19ea7d2aa668a5f7dfd`  
		Last Modified: Tue, 04 Nov 2025 23:25:22 GMT  
		Size: 129.2 MB (129224321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12a3c165fda31a17180ab1d45a2568d86791617546c97974383027ac7b80ad1`  
		Last Modified: Tue, 04 Nov 2025 23:25:47 GMT  
		Size: 24.5 MB (24528595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fa173cb85a42b8185c9bb59004594f75717dcabc5952241d81e1d300698619`  
		Last Modified: Tue, 04 Nov 2025 23:25:46 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ef4e39dd7279c474796198d827f6eb2fe0943f03c5139be85df71245042b9b`  
		Last Modified: Tue, 04 Nov 2025 23:25:38 GMT  
		Size: 449.5 MB (449452674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:58b8f891da64e3f0776e1ee1c6be2fdc69f6fdf994740cc9d9587ab0087b4c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997597fa5f7ab7d0a4367631f13242b49e245acb41b5da7e45e02402ecfed3cf`

```dockerfile
```

-	Layers:
	-	`sha256:1c7af5b1988122c9eb842a9c4af1dbcc8a74ea4227340c3b8958d12b12146add`  
		Last Modified: Wed, 05 Nov 2025 00:48:43 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170f7fda7578f769f8289b3c507d4becdbf308b131256b716dee71cbc6c1f07d`  
		Last Modified: Wed, 05 Nov 2025 00:48:44 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-slim-bookworm`

```console
$ docker pull haskell@sha256:67579232a5346dd114fc17cf4109dfdba1f3a2250d9662c7c5daa323c352b3ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:27781eae38b527ffc0ae170b7e2ad6a7a5c3d8a619e8e1bbad94fcfc320c7ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.6 MB (624579717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d3f7bd94f5aeb01273e36a9ecdd6e653002a57954f1fb4f13fc1140c7db584`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 01:01:09 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:09 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:11 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:12 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:12 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:02:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:36 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d838d000155ef723ee0e175ff5a7dd5fe048061c9e6cfceb72ef2d2ac21be8`  
		Last Modified: Wed, 05 Nov 2025 01:04:18 GMT  
		Size: 124.4 MB (124405989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056eceb9e7ff8b2f183775c286594a1249ef0f408e37e0f8cadec66ab3b75b1f`  
		Last Modified: Wed, 05 Nov 2025 01:04:07 GMT  
		Size: 22.2 MB (22220772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3fccfa699336382612528b5645405486947fac39fccaeab51d8baaf3c8bcc6`  
		Last Modified: Wed, 05 Nov 2025 01:04:06 GMT  
		Size: 7.6 MB (7607051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28de024af9eccd259f232441212a6c2a8ad11b0bfc506a6bc0834ff0d3f8cbb`  
		Last Modified: Wed, 05 Nov 2025 06:44:25 GMT  
		Size: 442.1 MB (442117338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:e791b0139286d2375f5c86655b6d88bc3d25d20de16a833aa525132ddf1408f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48cb63323d26c756c7169d0d7ff19f1217cb724305d995491f715d90b5401ab`

```dockerfile
```

-	Layers:
	-	`sha256:6748dd9e58e1a726311c5ee561d29c90d50eb14c2a024fffacbdcd2f48d27b74`  
		Last Modified: Wed, 05 Nov 2025 03:48:50 GMT  
		Size: 6.6 MB (6606023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8c22c62340afb4b03dee2eea3f220e293bd581a50edc9d8f0d680ad6f47742`  
		Last Modified: Wed, 05 Nov 2025 03:48:51 GMT  
		Size: 25.4 KB (25397 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:5bfe0b4c1d79a08ba161c7c050cf3850e384a8a161a94a3368c4e8797b159d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 MB (634532768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2e4d976470b40fb50e912ebff4af25483b99274519f111564b4861b33fea20`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:14 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:14 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:16 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:16 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:18 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:44 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:44 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32721fb00b278628e1be9f155a9645697a282507b2067aa1e422de48fe4be265`  
		Last Modified: Tue, 04 Nov 2025 23:25:26 GMT  
		Size: 118.5 MB (118483646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d22db0861ea87794af6681f1071c21daac1fad3279ea4c69f1c18141c77b35`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128bf50a9c1af9ec74b15ce055dc2cef06fb9cb03a008c7d8badca8301c35638`  
		Last Modified: Tue, 04 Nov 2025 23:25:17 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4965971a20019165dce18044a8938b29416bbf926a608a2222f94d5cd8ecd0a`  
		Last Modified: Tue, 04 Nov 2025 23:25:12 GMT  
		Size: 449.4 MB (449449129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:5b0ddc33081618bd4d192d60cda48cef95129b19733aefb6a69792d4e813e4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72c4eec988beff99759892482c92d84779aba2899071e06ebd989f7367c4f6e`

```dockerfile
```

-	Layers:
	-	`sha256:486b763cfd64d3a8fb706cfd0333583ac25b821da6e00750ced5eb5d4f6d3fdf`  
		Last Modified: Wed, 05 Nov 2025 00:49:06 GMT  
		Size: 6.6 MB (6634434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88927610c2512caf01a8cc284efc30a90597af8e8a06158928a33b59295b08bf`  
		Last Modified: Wed, 05 Nov 2025 00:49:07 GMT  
		Size: 25.5 KB (25523 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10-slim-bullseye`

```console
$ docker pull haskell@sha256:415e263078684c25a11918122c8173f671f05b6f4809c3321bd8e813ed414c5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f3ab4f23ec881de6220a2b68b599406140cef1ed63fc60c2de649d35f24a5e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608258987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdc26fd61aeddbe576dd48a9595f1beba39f8a0b04fe1a8dc065c94b58d574c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:26 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:26 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:30 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:03:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923f781df5b8a5c4299278e3418c8167b0755e231951fad172068cef8d708870`  
		Last Modified: Wed, 05 Nov 2025 01:04:38 GMT  
		Size: 106.4 MB (106366669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295a975b946c68a39b8fa62e02be53316c8932176eac7227b6b0bc86b95148a0`  
		Last Modified: Wed, 05 Nov 2025 01:04:28 GMT  
		Size: 22.2 MB (22220774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084d0d48b3516b6c62cd1a7ca37708fc2d5aa8454ff1398a6eb68baff6597d99`  
		Last Modified: Wed, 05 Nov 2025 01:04:26 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14992ee7da922ef406db6cf1542f4cb2619512aa477d189bb6b568536233e7ca`  
		Last Modified: Wed, 05 Nov 2025 06:58:18 GMT  
		Size: 441.8 MB (441800705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:4f01384a4a590600f239c8daf1e0269803ff098779e1726b0bdd85bb745dfc4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ebc71cba910e7c4ffc7bf31b6643dfbca8abd8fc5e3457ef9737b5a7f4e160`

```dockerfile
```

-	Layers:
	-	`sha256:d49c2acab03cbb152b37481eca7475af2446bfa5d70ae4c03d1cbbd65984be15`  
		Last Modified: Wed, 05 Nov 2025 03:48:36 GMT  
		Size: 6.8 MB (6750929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8dfdca42123fdcddcd45976dc302fd49052d6c7d91b2128d2dae3c2198230cb`  
		Last Modified: Wed, 05 Nov 2025 03:48:37 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:4c155d54fb64720b4a09291dd911e1a8cdc9d64b062258a9a591de4c379974c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618570950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57691ad02377bce23fb606584a35a7b0e855d4452482e09e7279bd9515541a0`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:16 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:19 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:19 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:20 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d275ddfa41ee2d9ccfc71507f0292da1aba94bd2f501c5ddfd430907b4dc50`  
		Last Modified: Tue, 04 Nov 2025 23:25:29 GMT  
		Size: 101.9 MB (101863502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd2b3f08398c1bfe2ef3c048abc27c058f7a6fcba39580a722e21bec8ad343b`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46140ed114cae7d7b0b71a188690513fe284c7320050bb4dba82f025b8f68258`  
		Last Modified: Tue, 04 Nov 2025 23:25:23 GMT  
		Size: 14.0 MB (13972958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dd63d00101136020b2a86961bdf45b99f7cf0d3fc0362b559d2dc080561e80`  
		Last Modified: Tue, 04 Nov 2025 23:25:15 GMT  
		Size: 449.5 MB (449457387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:1084beeb40a2a5530f4f1fe6ca4ff5c39130aeae6205de0dff0d411c4f681e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e3c86c3ae0c45dcf954bb7443da4384fed2e7e868430588319acef4cd3a506`

```dockerfile
```

-	Layers:
	-	`sha256:70296bae1d0c5102672799af1c2caf71d4fb7e46af35ccf067f5300e0b6fb0a7`  
		Last Modified: Wed, 05 Nov 2025 00:48:52 GMT  
		Size: 6.8 MB (6753439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4b054ea1508bde495c990515594f0b04af77f5c1df839aae61e2a0056793990`  
		Last Modified: Wed, 05 Nov 2025 00:48:53 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3`

```console
$ docker pull haskell@sha256:dd81ed941a848ffb0eced55b63e85f2b8986d82578b64f44636b602ddb521610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3` - linux; amd64

```console
$ docker pull haskell@sha256:81a86e1ea160f85082562f10e1928a59a0c9ab8987aca9feb7a9a1987740f290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659125300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9387a429a5d5704c5ef75bd2051dafc8168966a1746cd4939de77e87cef6aca`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:02:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dffd0aee3bf7bbe35a7b471cef359eeefa13932dbd4df53017ba1f4307c844`  
		Last Modified: Wed, 05 Nov 2025 06:48:41 GMT  
		Size: 133.7 MB (133737186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045be5b92248b3d9bd5effb953305a0912cfea45e2d0a718e4e07b4f45643d3c`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0f78eeb3db594d1db2c288857f115a46a17204edf96119a5b6432088628d9`  
		Last Modified: Wed, 05 Nov 2025 01:04:45 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0900a9b4accb5d08271764254a00f9ae17937fa2ed3c65bd1b4ee01e7f9db6e`  
		Last Modified: Wed, 05 Nov 2025 06:48:51 GMT  
		Size: 441.8 MB (441798409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3` - unknown; unknown

```console
$ docker pull haskell@sha256:7c9f9e34fe9c803e250b12ef12d39fbcf840f817a88d62983f4c0a7b7b980297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c01f7c7feef3ff0514632720135dfe5d8aa28e70104a9c252e023a5a89b963`

```dockerfile
```

-	Layers:
	-	`sha256:1d39ab4b5cbea0dd076770c00259350040057f3f1fb3ee893a983db7f135a9ba`  
		Last Modified: Wed, 05 Nov 2025 03:48:24 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3e9b3aa3a9ed7bde2a358779c5416b443af533319e267402593ae6dd7dc6ac`  
		Last Modified: Wed, 05 Nov 2025 03:48:25 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8d73683c844837d5df96b274c017588f5e304e505a4a82f52bb0f6d1d04071d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669436520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7015f6723d585232346cd27459b66255821f3481dab0165c2e987e7e15578af8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896b69b58297e59a819a754d1e990f5d5ad269382647d19ea7d2aa668a5f7dfd`  
		Last Modified: Tue, 04 Nov 2025 23:25:22 GMT  
		Size: 129.2 MB (129224321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12a3c165fda31a17180ab1d45a2568d86791617546c97974383027ac7b80ad1`  
		Last Modified: Tue, 04 Nov 2025 23:25:47 GMT  
		Size: 24.5 MB (24528595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fa173cb85a42b8185c9bb59004594f75717dcabc5952241d81e1d300698619`  
		Last Modified: Tue, 04 Nov 2025 23:25:46 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ef4e39dd7279c474796198d827f6eb2fe0943f03c5139be85df71245042b9b`  
		Last Modified: Tue, 04 Nov 2025 23:25:38 GMT  
		Size: 449.5 MB (449452674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3` - unknown; unknown

```console
$ docker pull haskell@sha256:58b8f891da64e3f0776e1ee1c6be2fdc69f6fdf994740cc9d9587ab0087b4c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997597fa5f7ab7d0a4367631f13242b49e245acb41b5da7e45e02402ecfed3cf`

```dockerfile
```

-	Layers:
	-	`sha256:1c7af5b1988122c9eb842a9c4af1dbcc8a74ea4227340c3b8958d12b12146add`  
		Last Modified: Wed, 05 Nov 2025 00:48:43 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170f7fda7578f769f8289b3c507d4becdbf308b131256b716dee71cbc6c1f07d`  
		Last Modified: Wed, 05 Nov 2025 00:48:44 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-bookworm`

```console
$ docker pull haskell@sha256:d83036d9bbe82cd21ecdd78a872c029c3cdb06980329da2f33bb20bcd1cd60f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:d3c4d8a24888c4e217ff22400aff51b79914cbd87426be06719125b8dfa3db90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **672.8 MB (672776357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2698ad5456b6eb38b494492a59f4c8e9225595ed5c297c78672709c0a5d0ed2`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 01:01:03 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:03 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:03 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:03 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:05 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:05 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:07 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:07 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:02:45 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:45 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:45 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e373b7f712e78e5715c63f4a6b2eacef73814251fcb0076aeb4d8d7dee86e55d`  
		Last Modified: Wed, 05 Nov 2025 06:39:58 GMT  
		Size: 152.4 MB (152350630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb49f70db680ece953f55aea331a7f0bbf9dbdd9ba1dd4d2090325fb95731f4`  
		Last Modified: Wed, 05 Nov 2025 01:04:27 GMT  
		Size: 22.2 MB (22220766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d79705fa256dc0a20e12ba34ee873567b70b2b10fd46fbf8c457fb960d9aee`  
		Last Modified: Wed, 05 Nov 2025 01:04:27 GMT  
		Size: 7.6 MB (7607051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1860ed18f447c17a06950413a60cc01c02f48941187331e5eb8e436248a6bd`  
		Last Modified: Wed, 05 Nov 2025 06:40:02 GMT  
		Size: 442.1 MB (442116854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:e8f066f7e9103b351dc255520e5ca0ba07a572a14cfd193f519f0167879e7a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9503816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188cd376afe6de97b92884a8ebcd23493d15a1755b648f55671a9a0f53b7247d`

```dockerfile
```

-	Layers:
	-	`sha256:5e0e2392cd37627596da4061517f3ccc152ea2800d16a0b54380a3d2a65904c0`  
		Last Modified: Wed, 05 Nov 2025 03:48:43 GMT  
		Size: 9.5 MB (9478462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ec54a248f8b1856493631ccbe63c58db4926b0776878382acd8d9120f8dc48`  
		Last Modified: Wed, 05 Nov 2025 03:48:44 GMT  
		Size: 25.4 KB (25354 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:2a67d4ac55e36e4cbad3b28397fae12748ce37b9c0fcf626a2637af02915fa57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **682.7 MB (682735483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5561cea3cea22188c380a78746cb0c613d8a754c8594816822159ea35c84dddd`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:16 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:16 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:40 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:40 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:40 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd427febe62e8d07726b1d34c46b42cda18280846c91bd6076f610a60aa81c3e`  
		Last Modified: Tue, 04 Nov 2025 23:25:04 GMT  
		Size: 146.4 MB (146430286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5f37339d36a6ed12a12f4c5da3602ff2430a07e3fc0ea0bfcd7ae0af6edd8a`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481416619574b664be42d99c63a38f91844fe0e5ddd0c8ba7c8e319a77a0fc89`  
		Last Modified: Tue, 04 Nov 2025 23:25:23 GMT  
		Size: 14.0 MB (13969029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5303524c160a35357df9a815d36750c25fe0093b4f00977604cb0d069127de`  
		Last Modified: Tue, 04 Nov 2025 23:25:15 GMT  
		Size: 449.4 MB (449448087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:58ca1fa7c9d810d04eed58ab299c0e84110cbdd5d0096ff463f208557c5737cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9531727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:145676a649d79ef54282cd803ccfc4ef2adecf75efa1e17f68e8d3c7eda1fe77`

```dockerfile
```

-	Layers:
	-	`sha256:cb9936cbaa7aa9d56f1240be22ef15968011ccaf168bcb8b9f1859fc5136119e`  
		Last Modified: Wed, 05 Nov 2025 00:48:55 GMT  
		Size: 9.5 MB (9506246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07c4579db390c634071c4ade5c88c96d828dd4ffb585f3eaccd6d4bf1b3c1346`  
		Last Modified: Wed, 05 Nov 2025 00:48:56 GMT  
		Size: 25.5 KB (25481 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-bullseye`

```console
$ docker pull haskell@sha256:dd81ed941a848ffb0eced55b63e85f2b8986d82578b64f44636b602ddb521610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:81a86e1ea160f85082562f10e1928a59a0c9ab8987aca9feb7a9a1987740f290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659125300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9387a429a5d5704c5ef75bd2051dafc8168966a1746cd4939de77e87cef6aca`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:02:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dffd0aee3bf7bbe35a7b471cef359eeefa13932dbd4df53017ba1f4307c844`  
		Last Modified: Wed, 05 Nov 2025 06:48:41 GMT  
		Size: 133.7 MB (133737186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045be5b92248b3d9bd5effb953305a0912cfea45e2d0a718e4e07b4f45643d3c`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0f78eeb3db594d1db2c288857f115a46a17204edf96119a5b6432088628d9`  
		Last Modified: Wed, 05 Nov 2025 01:04:45 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0900a9b4accb5d08271764254a00f9ae17937fa2ed3c65bd1b4ee01e7f9db6e`  
		Last Modified: Wed, 05 Nov 2025 06:48:51 GMT  
		Size: 441.8 MB (441798409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:7c9f9e34fe9c803e250b12ef12d39fbcf840f817a88d62983f4c0a7b7b980297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c01f7c7feef3ff0514632720135dfe5d8aa28e70104a9c252e023a5a89b963`

```dockerfile
```

-	Layers:
	-	`sha256:1d39ab4b5cbea0dd076770c00259350040057f3f1fb3ee893a983db7f135a9ba`  
		Last Modified: Wed, 05 Nov 2025 03:48:24 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3e9b3aa3a9ed7bde2a358779c5416b443af533319e267402593ae6dd7dc6ac`  
		Last Modified: Wed, 05 Nov 2025 03:48:25 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8d73683c844837d5df96b274c017588f5e304e505a4a82f52bb0f6d1d04071d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669436520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7015f6723d585232346cd27459b66255821f3481dab0165c2e987e7e15578af8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896b69b58297e59a819a754d1e990f5d5ad269382647d19ea7d2aa668a5f7dfd`  
		Last Modified: Tue, 04 Nov 2025 23:25:22 GMT  
		Size: 129.2 MB (129224321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12a3c165fda31a17180ab1d45a2568d86791617546c97974383027ac7b80ad1`  
		Last Modified: Tue, 04 Nov 2025 23:25:47 GMT  
		Size: 24.5 MB (24528595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fa173cb85a42b8185c9bb59004594f75717dcabc5952241d81e1d300698619`  
		Last Modified: Tue, 04 Nov 2025 23:25:46 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ef4e39dd7279c474796198d827f6eb2fe0943f03c5139be85df71245042b9b`  
		Last Modified: Tue, 04 Nov 2025 23:25:38 GMT  
		Size: 449.5 MB (449452674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:58b8f891da64e3f0776e1ee1c6be2fdc69f6fdf994740cc9d9587ab0087b4c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997597fa5f7ab7d0a4367631f13242b49e245acb41b5da7e45e02402ecfed3cf`

```dockerfile
```

-	Layers:
	-	`sha256:1c7af5b1988122c9eb842a9c4af1dbcc8a74ea4227340c3b8958d12b12146add`  
		Last Modified: Wed, 05 Nov 2025 00:48:43 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170f7fda7578f769f8289b3c507d4becdbf308b131256b716dee71cbc6c1f07d`  
		Last Modified: Wed, 05 Nov 2025 00:48:44 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-slim-bookworm`

```console
$ docker pull haskell@sha256:67579232a5346dd114fc17cf4109dfdba1f3a2250d9662c7c5daa323c352b3ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:27781eae38b527ffc0ae170b7e2ad6a7a5c3d8a619e8e1bbad94fcfc320c7ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **624.6 MB (624579717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9d3f7bd94f5aeb01273e36a9ecdd6e653002a57954f1fb4f13fc1140c7db584`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 01:01:09 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:09 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:09 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:11 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:11 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:12 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:12 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:02:36 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:36 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:36 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d838d000155ef723ee0e175ff5a7dd5fe048061c9e6cfceb72ef2d2ac21be8`  
		Last Modified: Wed, 05 Nov 2025 01:04:18 GMT  
		Size: 124.4 MB (124405989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056eceb9e7ff8b2f183775c286594a1249ef0f408e37e0f8cadec66ab3b75b1f`  
		Last Modified: Wed, 05 Nov 2025 01:04:07 GMT  
		Size: 22.2 MB (22220772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3fccfa699336382612528b5645405486947fac39fccaeab51d8baaf3c8bcc6`  
		Last Modified: Wed, 05 Nov 2025 01:04:06 GMT  
		Size: 7.6 MB (7607051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28de024af9eccd259f232441212a6c2a8ad11b0bfc506a6bc0834ff0d3f8cbb`  
		Last Modified: Wed, 05 Nov 2025 06:44:25 GMT  
		Size: 442.1 MB (442117338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:e791b0139286d2375f5c86655b6d88bc3d25d20de16a833aa525132ddf1408f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6631420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48cb63323d26c756c7169d0d7ff19f1217cb724305d995491f715d90b5401ab`

```dockerfile
```

-	Layers:
	-	`sha256:6748dd9e58e1a726311c5ee561d29c90d50eb14c2a024fffacbdcd2f48d27b74`  
		Last Modified: Wed, 05 Nov 2025 03:48:50 GMT  
		Size: 6.6 MB (6606023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c8c22c62340afb4b03dee2eea3f220e293bd581a50edc9d8f0d680ad6f47742`  
		Last Modified: Wed, 05 Nov 2025 03:48:51 GMT  
		Size: 25.4 KB (25397 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:5bfe0b4c1d79a08ba161c7c050cf3850e384a8a161a94a3368c4e8797b159d53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **634.5 MB (634532768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2e4d976470b40fb50e912ebff4af25483b99274519f111564b4861b33fea20`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:14 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:14 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:14 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:14 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:16 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:16 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:16 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:18 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:18 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:44 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             GHC_URL='https://downloads.haskell.org/~ghc/9.10.3/ghc-9.10.3-aarch64-deb11-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='1ac63f04eac0ad551d45cbde38f27e0e3f43ceefd98833fae1fa3f2dbd042367';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:44 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:44 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32721fb00b278628e1be9f155a9645697a282507b2067aa1e422de48fe4be265`  
		Last Modified: Tue, 04 Nov 2025 23:25:26 GMT  
		Size: 118.5 MB (118483646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d22db0861ea87794af6681f1071c21daac1fad3279ea4c69f1c18141c77b35`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128bf50a9c1af9ec74b15ce055dc2cef06fb9cb03a008c7d8badca8301c35638`  
		Last Modified: Tue, 04 Nov 2025 23:25:17 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4965971a20019165dce18044a8938b29416bbf926a608a2222f94d5cd8ecd0a`  
		Last Modified: Tue, 04 Nov 2025 23:25:12 GMT  
		Size: 449.4 MB (449449129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:5b0ddc33081618bd4d192d60cda48cef95129b19733aefb6a69792d4e813e4b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6659957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f72c4eec988beff99759892482c92d84779aba2899071e06ebd989f7367c4f6e`

```dockerfile
```

-	Layers:
	-	`sha256:486b763cfd64d3a8fb706cfd0333583ac25b821da6e00750ced5eb5d4f6d3fdf`  
		Last Modified: Wed, 05 Nov 2025 00:49:06 GMT  
		Size: 6.6 MB (6634434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88927610c2512caf01a8cc284efc30a90597af8e8a06158928a33b59295b08bf`  
		Last Modified: Wed, 05 Nov 2025 00:49:07 GMT  
		Size: 25.5 KB (25523 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.10.3-slim-bullseye`

```console
$ docker pull haskell@sha256:415e263078684c25a11918122c8173f671f05b6f4809c3321bd8e813ed414c5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.10.3-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f3ab4f23ec881de6220a2b68b599406140cef1ed63fc60c2de649d35f24a5e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608258987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdc26fd61aeddbe576dd48a9595f1beba39f8a0b04fe1a8dc065c94b58d574c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:26 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:26 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:30 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:03:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923f781df5b8a5c4299278e3418c8167b0755e231951fad172068cef8d708870`  
		Last Modified: Wed, 05 Nov 2025 01:04:38 GMT  
		Size: 106.4 MB (106366669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295a975b946c68a39b8fa62e02be53316c8932176eac7227b6b0bc86b95148a0`  
		Last Modified: Wed, 05 Nov 2025 01:04:28 GMT  
		Size: 22.2 MB (22220774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084d0d48b3516b6c62cd1a7ca37708fc2d5aa8454ff1398a6eb68baff6597d99`  
		Last Modified: Wed, 05 Nov 2025 01:04:26 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14992ee7da922ef406db6cf1542f4cb2619512aa477d189bb6b568536233e7ca`  
		Last Modified: Wed, 05 Nov 2025 06:58:18 GMT  
		Size: 441.8 MB (441800705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:4f01384a4a590600f239c8daf1e0269803ff098779e1726b0bdd85bb745dfc4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ebc71cba910e7c4ffc7bf31b6643dfbca8abd8fc5e3457ef9737b5a7f4e160`

```dockerfile
```

-	Layers:
	-	`sha256:d49c2acab03cbb152b37481eca7475af2446bfa5d70ae4c03d1cbbd65984be15`  
		Last Modified: Wed, 05 Nov 2025 03:48:36 GMT  
		Size: 6.8 MB (6750929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8dfdca42123fdcddcd45976dc302fd49052d6c7d91b2128d2dae3c2198230cb`  
		Last Modified: Wed, 05 Nov 2025 03:48:37 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.10.3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:4c155d54fb64720b4a09291dd911e1a8cdc9d64b062258a9a591de4c379974c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618570950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57691ad02377bce23fb606584a35a7b0e855d4452482e09e7279bd9515541a0`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:16 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:19 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:19 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:20 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d275ddfa41ee2d9ccfc71507f0292da1aba94bd2f501c5ddfd430907b4dc50`  
		Last Modified: Tue, 04 Nov 2025 23:25:29 GMT  
		Size: 101.9 MB (101863502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd2b3f08398c1bfe2ef3c048abc27c058f7a6fcba39580a722e21bec8ad343b`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46140ed114cae7d7b0b71a188690513fe284c7320050bb4dba82f025b8f68258`  
		Last Modified: Tue, 04 Nov 2025 23:25:23 GMT  
		Size: 14.0 MB (13972958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dd63d00101136020b2a86961bdf45b99f7cf0d3fc0362b559d2dc080561e80`  
		Last Modified: Tue, 04 Nov 2025 23:25:15 GMT  
		Size: 449.5 MB (449457387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.10.3-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:1084beeb40a2a5530f4f1fe6ca4ff5c39130aeae6205de0dff0d411c4f681e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e3c86c3ae0c45dcf954bb7443da4384fed2e7e868430588319acef4cd3a506`

```dockerfile
```

-	Layers:
	-	`sha256:70296bae1d0c5102672799af1c2caf71d4fb7e46af35ccf067f5300e0b6fb0a7`  
		Last Modified: Wed, 05 Nov 2025 00:48:52 GMT  
		Size: 6.8 MB (6753439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4b054ea1508bde495c990515594f0b04af77f5c1df839aae61e2a0056793990`  
		Last Modified: Wed, 05 Nov 2025 00:48:53 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12`

```console
$ docker pull haskell@sha256:78c823f5c5723101cd3a50139ccc247d916d1bea7480c6aabd38eff59e28e647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12` - linux; amd64

```console
$ docker pull haskell@sha256:a41bf6877d1b1c87c421f94a4638eba7df8218bb2cbad0f71fef0e70c92602b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822417895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6aa04b16cabf65b9d6d22c021edde2947d51f1ac99f7ea60c9ff2a66ecdaf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 00:58:45 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 00:58:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 00:58:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 00:58:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:00:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:00:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:00:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74e79de258e3316172835a71c06df1674203435ce381ddb37305408e4d8730`  
		Last Modified: Wed, 05 Nov 2025 04:13:29 GMT  
		Size: 152.4 MB (152350699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553b1f0dd1e197cbbe3f0463774823e46927db001afa401edd276a3b99489d30`  
		Last Modified: Wed, 05 Nov 2025 01:02:51 GMT  
		Size: 22.2 MB (22220772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd0d14b3991f9f0aebe9120fa0a7204e23303c50fc1a8f5af5f3738c20f88b`  
		Last Modified: Wed, 05 Nov 2025 01:02:56 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd2b0e9ae55c4f5be104cd2eedef25c4289355a15a18cfaec59f5ba30f280d`  
		Last Modified: Wed, 05 Nov 2025 04:14:02 GMT  
		Size: 591.8 MB (591758313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12` - unknown; unknown

```console
$ docker pull haskell@sha256:458e9b22beeb9921367aefa61ed3d13dd8a57d4f32a4f5d9bf110ac9dcadd790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14e893bb39433aadd3fbed2ded5e11e67866c9e8a69c7f68baeadb53a586067`

```dockerfile
```

-	Layers:
	-	`sha256:3192e5864311a3b4d24424073b8bd90e596f8710e6a70e7d14fc2527780434f7`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43221b79dcf6f8d53e8a9c4d6c37c39c1f7bb2e76922487e0fb0cb8432ff84af`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7fd9839058ccbb571a8e2d0d0a5893bbe11fb7ae709fc10082f993febdba6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824914239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142829b70e18729d3f9677cc8adbaca4536552fd98b3e9c517fd6d4dd3d8c10e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce95fd68f2b36a165ba3ad3e35396590889fb3e4056830890a496db707cf348`  
		Last Modified: Wed, 05 Nov 2025 02:50:44 GMT  
		Size: 146.4 MB (146430422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48665fd90cd640558ea256bbd3e5c928979d6e482f935f4c34d851c1efe4b4`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ffee524ac5f20f017307ec386b9e5d9c2626ffa50ba57f8803695768046f38`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c2a5bf9e7458376d169214655aff5fed34472997e6bdb214d76466ef72931`  
		Last Modified: Wed, 05 Nov 2025 02:51:25 GMT  
		Size: 591.6 MB (591626752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12` - unknown; unknown

```console
$ docker pull haskell@sha256:733ae5fb5d3735a1be1196b14601606d235545c4ed86a7f75bf912dcb67daf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a81146c4e4b94307c4afb5035ddb5ad5bee3eb364f569f36482536eca91fd5`

```dockerfile
```

-	Layers:
	-	`sha256:ac0049f8b5386b8a7aaef447204d3098e0db4e28e1ef34c66bc13c3480601908`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b59f5afbc59dba62205816d52797470ff0bf9edb8a603bedfba451414f5994`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12-bookworm`

```console
$ docker pull haskell@sha256:78c823f5c5723101cd3a50139ccc247d916d1bea7480c6aabd38eff59e28e647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:a41bf6877d1b1c87c421f94a4638eba7df8218bb2cbad0f71fef0e70c92602b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822417895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6aa04b16cabf65b9d6d22c021edde2947d51f1ac99f7ea60c9ff2a66ecdaf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 00:58:45 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 00:58:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 00:58:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 00:58:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:00:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:00:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:00:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74e79de258e3316172835a71c06df1674203435ce381ddb37305408e4d8730`  
		Last Modified: Wed, 05 Nov 2025 04:13:29 GMT  
		Size: 152.4 MB (152350699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553b1f0dd1e197cbbe3f0463774823e46927db001afa401edd276a3b99489d30`  
		Last Modified: Wed, 05 Nov 2025 01:02:51 GMT  
		Size: 22.2 MB (22220772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd0d14b3991f9f0aebe9120fa0a7204e23303c50fc1a8f5af5f3738c20f88b`  
		Last Modified: Wed, 05 Nov 2025 01:02:56 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd2b0e9ae55c4f5be104cd2eedef25c4289355a15a18cfaec59f5ba30f280d`  
		Last Modified: Wed, 05 Nov 2025 04:14:02 GMT  
		Size: 591.8 MB (591758313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:458e9b22beeb9921367aefa61ed3d13dd8a57d4f32a4f5d9bf110ac9dcadd790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14e893bb39433aadd3fbed2ded5e11e67866c9e8a69c7f68baeadb53a586067`

```dockerfile
```

-	Layers:
	-	`sha256:3192e5864311a3b4d24424073b8bd90e596f8710e6a70e7d14fc2527780434f7`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43221b79dcf6f8d53e8a9c4d6c37c39c1f7bb2e76922487e0fb0cb8432ff84af`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7fd9839058ccbb571a8e2d0d0a5893bbe11fb7ae709fc10082f993febdba6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824914239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142829b70e18729d3f9677cc8adbaca4536552fd98b3e9c517fd6d4dd3d8c10e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce95fd68f2b36a165ba3ad3e35396590889fb3e4056830890a496db707cf348`  
		Last Modified: Wed, 05 Nov 2025 02:50:44 GMT  
		Size: 146.4 MB (146430422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48665fd90cd640558ea256bbd3e5c928979d6e482f935f4c34d851c1efe4b4`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ffee524ac5f20f017307ec386b9e5d9c2626ffa50ba57f8803695768046f38`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c2a5bf9e7458376d169214655aff5fed34472997e6bdb214d76466ef72931`  
		Last Modified: Wed, 05 Nov 2025 02:51:25 GMT  
		Size: 591.6 MB (591626752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:733ae5fb5d3735a1be1196b14601606d235545c4ed86a7f75bf912dcb67daf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a81146c4e4b94307c4afb5035ddb5ad5bee3eb364f569f36482536eca91fd5`

```dockerfile
```

-	Layers:
	-	`sha256:ac0049f8b5386b8a7aaef447204d3098e0db4e28e1ef34c66bc13c3480601908`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b59f5afbc59dba62205816d52797470ff0bf9edb8a603bedfba451414f5994`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12-slim-bookworm`

```console
$ docker pull haskell@sha256:fb2bda3959b5c4571312a9449c69854eec11ec15cc6f1bc15b54c44595cd9f4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:6661f83b6d9612b7ee355aed52957acd2dcb22cfa1168f375a624d2a07b46890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774226835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f4c09f9d50ce6b07424304779854802bac7a82f4c7dd3cec4a3b2e167f6ed4`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 01:00:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:00:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:00:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:00:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:02:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8271a965164bc23e31a9ddc248acd56dc871d237df6cc16e874a150569eb6bb7`  
		Last Modified: Wed, 05 Nov 2025 01:04:57 GMT  
		Size: 124.4 MB (124406092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d291c4dad79d17a29c3070282e992374454228cd4f0a8e2ff72e502e31456d24`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba317e1a05fa997b78d6cc5fd1590cd99192bd8f5909a91bbfea0a74e0d2d2a`  
		Last Modified: Wed, 05 Nov 2025 01:04:48 GMT  
		Size: 7.6 MB (7607061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f57245b6c97717b46d25fa4b02c34ac804e6c463ccc00f25644b5b3eb3d12`  
		Last Modified: Wed, 05 Nov 2025 04:41:27 GMT  
		Size: 591.8 MB (591764340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:b7d82e0f1f51b7d13f302097cc8e888935740cdacd5da61700eff68fac593d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46f9f3507602fe823509b330fbf15659afab945a1878bc5073ff44f325c31c2`

```dockerfile
```

-	Layers:
	-	`sha256:3c6cfa885e60075b0c7ec2e259343e3075a93afb5f61b3a939ef1c5304c2ad9b`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9454075c4b79dba3e00b3fb64ab2d514a25e318ea3914abb34adedabdeef073`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:428c38c35848ae20da237bb4c2e9a3660800fe96a93a37ec33e6d26dd5a12cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776707214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf631611acadbab9fc2f73bb9d7b518d15bf2e7478ccaac9cfdd8c0923999b5`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd10243405c62faa4120f029da948bde716bfe5475ad9e3559253bd0925ffa`  
		Last Modified: Tue, 04 Nov 2025 23:26:28 GMT  
		Size: 118.5 MB (118483733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c5c5a35659575c20b89d69badcf9aa3374cedbfda46a8d3b7b833b02ff6f8`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9fa47c2d351040977a11cd8fb7cbff5bf5a2667ff33e7fe33cbd02d540304`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8155cd34b96433ff8496257790a2ddfd1c8b9f2295601acb8a12baecf1a8765a`  
		Last Modified: Tue, 04 Nov 2025 23:25:59 GMT  
		Size: 591.6 MB (591623479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:176bb96490f2f6215b29823180e44df23adcaf8b4f257f02965957b5401322d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f404b57cb062f3f8b0be0d26974da9218b9852ec75070e382b144b6f5da0cc`

```dockerfile
```

-	Layers:
	-	`sha256:bd037653b5928dfb4a639ce168667ebfc3edf471756dda6f8e41feaea3b71b5e`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4933ebfa06d93dd61896b287216f2341093ff3c290b5980c745a0d66995084b`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2`

```console
$ docker pull haskell@sha256:78c823f5c5723101cd3a50139ccc247d916d1bea7480c6aabd38eff59e28e647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2` - linux; amd64

```console
$ docker pull haskell@sha256:a41bf6877d1b1c87c421f94a4638eba7df8218bb2cbad0f71fef0e70c92602b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822417895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6aa04b16cabf65b9d6d22c021edde2947d51f1ac99f7ea60c9ff2a66ecdaf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 00:58:45 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 00:58:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 00:58:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 00:58:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:00:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:00:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:00:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74e79de258e3316172835a71c06df1674203435ce381ddb37305408e4d8730`  
		Last Modified: Wed, 05 Nov 2025 04:13:29 GMT  
		Size: 152.4 MB (152350699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553b1f0dd1e197cbbe3f0463774823e46927db001afa401edd276a3b99489d30`  
		Last Modified: Wed, 05 Nov 2025 01:02:51 GMT  
		Size: 22.2 MB (22220772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd0d14b3991f9f0aebe9120fa0a7204e23303c50fc1a8f5af5f3738c20f88b`  
		Last Modified: Wed, 05 Nov 2025 01:02:56 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd2b0e9ae55c4f5be104cd2eedef25c4289355a15a18cfaec59f5ba30f280d`  
		Last Modified: Wed, 05 Nov 2025 04:14:02 GMT  
		Size: 591.8 MB (591758313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2` - unknown; unknown

```console
$ docker pull haskell@sha256:458e9b22beeb9921367aefa61ed3d13dd8a57d4f32a4f5d9bf110ac9dcadd790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14e893bb39433aadd3fbed2ded5e11e67866c9e8a69c7f68baeadb53a586067`

```dockerfile
```

-	Layers:
	-	`sha256:3192e5864311a3b4d24424073b8bd90e596f8710e6a70e7d14fc2527780434f7`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43221b79dcf6f8d53e8a9c4d6c37c39c1f7bb2e76922487e0fb0cb8432ff84af`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7fd9839058ccbb571a8e2d0d0a5893bbe11fb7ae709fc10082f993febdba6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824914239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142829b70e18729d3f9677cc8adbaca4536552fd98b3e9c517fd6d4dd3d8c10e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce95fd68f2b36a165ba3ad3e35396590889fb3e4056830890a496db707cf348`  
		Last Modified: Wed, 05 Nov 2025 02:50:44 GMT  
		Size: 146.4 MB (146430422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48665fd90cd640558ea256bbd3e5c928979d6e482f935f4c34d851c1efe4b4`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ffee524ac5f20f017307ec386b9e5d9c2626ffa50ba57f8803695768046f38`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c2a5bf9e7458376d169214655aff5fed34472997e6bdb214d76466ef72931`  
		Last Modified: Wed, 05 Nov 2025 02:51:25 GMT  
		Size: 591.6 MB (591626752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2` - unknown; unknown

```console
$ docker pull haskell@sha256:733ae5fb5d3735a1be1196b14601606d235545c4ed86a7f75bf912dcb67daf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a81146c4e4b94307c4afb5035ddb5ad5bee3eb364f569f36482536eca91fd5`

```dockerfile
```

-	Layers:
	-	`sha256:ac0049f8b5386b8a7aaef447204d3098e0db4e28e1ef34c66bc13c3480601908`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b59f5afbc59dba62205816d52797470ff0bf9edb8a603bedfba451414f5994`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2-bookworm`

```console
$ docker pull haskell@sha256:78c823f5c5723101cd3a50139ccc247d916d1bea7480c6aabd38eff59e28e647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:a41bf6877d1b1c87c421f94a4638eba7df8218bb2cbad0f71fef0e70c92602b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822417895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6aa04b16cabf65b9d6d22c021edde2947d51f1ac99f7ea60c9ff2a66ecdaf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 00:58:45 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 00:58:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 00:58:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 00:58:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:00:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:00:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:00:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74e79de258e3316172835a71c06df1674203435ce381ddb37305408e4d8730`  
		Last Modified: Wed, 05 Nov 2025 04:13:29 GMT  
		Size: 152.4 MB (152350699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553b1f0dd1e197cbbe3f0463774823e46927db001afa401edd276a3b99489d30`  
		Last Modified: Wed, 05 Nov 2025 01:02:51 GMT  
		Size: 22.2 MB (22220772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd0d14b3991f9f0aebe9120fa0a7204e23303c50fc1a8f5af5f3738c20f88b`  
		Last Modified: Wed, 05 Nov 2025 01:02:56 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd2b0e9ae55c4f5be104cd2eedef25c4289355a15a18cfaec59f5ba30f280d`  
		Last Modified: Wed, 05 Nov 2025 04:14:02 GMT  
		Size: 591.8 MB (591758313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:458e9b22beeb9921367aefa61ed3d13dd8a57d4f32a4f5d9bf110ac9dcadd790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14e893bb39433aadd3fbed2ded5e11e67866c9e8a69c7f68baeadb53a586067`

```dockerfile
```

-	Layers:
	-	`sha256:3192e5864311a3b4d24424073b8bd90e596f8710e6a70e7d14fc2527780434f7`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43221b79dcf6f8d53e8a9c4d6c37c39c1f7bb2e76922487e0fb0cb8432ff84af`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7fd9839058ccbb571a8e2d0d0a5893bbe11fb7ae709fc10082f993febdba6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824914239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142829b70e18729d3f9677cc8adbaca4536552fd98b3e9c517fd6d4dd3d8c10e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce95fd68f2b36a165ba3ad3e35396590889fb3e4056830890a496db707cf348`  
		Last Modified: Wed, 05 Nov 2025 02:50:44 GMT  
		Size: 146.4 MB (146430422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48665fd90cd640558ea256bbd3e5c928979d6e482f935f4c34d851c1efe4b4`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ffee524ac5f20f017307ec386b9e5d9c2626ffa50ba57f8803695768046f38`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c2a5bf9e7458376d169214655aff5fed34472997e6bdb214d76466ef72931`  
		Last Modified: Wed, 05 Nov 2025 02:51:25 GMT  
		Size: 591.6 MB (591626752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:733ae5fb5d3735a1be1196b14601606d235545c4ed86a7f75bf912dcb67daf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a81146c4e4b94307c4afb5035ddb5ad5bee3eb364f569f36482536eca91fd5`

```dockerfile
```

-	Layers:
	-	`sha256:ac0049f8b5386b8a7aaef447204d3098e0db4e28e1ef34c66bc13c3480601908`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b59f5afbc59dba62205816d52797470ff0bf9edb8a603bedfba451414f5994`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.12.2-slim-bookworm`

```console
$ docker pull haskell@sha256:fb2bda3959b5c4571312a9449c69854eec11ec15cc6f1bc15b54c44595cd9f4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.12.2-slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:6661f83b6d9612b7ee355aed52957acd2dcb22cfa1168f375a624d2a07b46890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774226835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f4c09f9d50ce6b07424304779854802bac7a82f4c7dd3cec4a3b2e167f6ed4`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 01:00:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:00:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:00:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:00:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:02:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8271a965164bc23e31a9ddc248acd56dc871d237df6cc16e874a150569eb6bb7`  
		Last Modified: Wed, 05 Nov 2025 01:04:57 GMT  
		Size: 124.4 MB (124406092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d291c4dad79d17a29c3070282e992374454228cd4f0a8e2ff72e502e31456d24`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba317e1a05fa997b78d6cc5fd1590cd99192bd8f5909a91bbfea0a74e0d2d2a`  
		Last Modified: Wed, 05 Nov 2025 01:04:48 GMT  
		Size: 7.6 MB (7607061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f57245b6c97717b46d25fa4b02c34ac804e6c463ccc00f25644b5b3eb3d12`  
		Last Modified: Wed, 05 Nov 2025 04:41:27 GMT  
		Size: 591.8 MB (591764340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:b7d82e0f1f51b7d13f302097cc8e888935740cdacd5da61700eff68fac593d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46f9f3507602fe823509b330fbf15659afab945a1878bc5073ff44f325c31c2`

```dockerfile
```

-	Layers:
	-	`sha256:3c6cfa885e60075b0c7ec2e259343e3075a93afb5f61b3a939ef1c5304c2ad9b`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9454075c4b79dba3e00b3fb64ab2d514a25e318ea3914abb34adedabdeef073`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.12.2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:428c38c35848ae20da237bb4c2e9a3660800fe96a93a37ec33e6d26dd5a12cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776707214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf631611acadbab9fc2f73bb9d7b518d15bf2e7478ccaac9cfdd8c0923999b5`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd10243405c62faa4120f029da948bde716bfe5475ad9e3559253bd0925ffa`  
		Last Modified: Tue, 04 Nov 2025 23:26:28 GMT  
		Size: 118.5 MB (118483733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c5c5a35659575c20b89d69badcf9aa3374cedbfda46a8d3b7b833b02ff6f8`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9fa47c2d351040977a11cd8fb7cbff5bf5a2667ff33e7fe33cbd02d540304`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8155cd34b96433ff8496257790a2ddfd1c8b9f2295601acb8a12baecf1a8765a`  
		Last Modified: Tue, 04 Nov 2025 23:25:59 GMT  
		Size: 591.6 MB (591623479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.12.2-slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:176bb96490f2f6215b29823180e44df23adcaf8b4f257f02965957b5401322d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f404b57cb062f3f8b0be0d26974da9218b9852ec75070e382b144b6f5da0cc`

```dockerfile
```

-	Layers:
	-	`sha256:bd037653b5928dfb4a639ce168667ebfc3edf471756dda6f8e41feaea3b71b5e`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4933ebfa06d93dd61896b287216f2341093ff3c290b5980c745a0d66995084b`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6`

```console
$ docker pull haskell@sha256:d0b0282163e131b177b4b14a6022334ff96c058b7d09f0802b8ad73a185abfeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6` - linux; amd64

```console
$ docker pull haskell@sha256:5d51daa58b73b133b0c002b31e86727ad064752d3e11be18b6fe7734d77beecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641554471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f287aa18302eb4324877e9647db5e00097a0bc307622ed1fa461f5668da8a0`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:46 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:46 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:46 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:49 GMT
ARG GHC=9.6.7
# Wed, 05 Nov 2025 01:01:49 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Wed, 05 Nov 2025 01:03:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd353de69382164817f65f8772fe5d476bc3f339c097dbe47afbc8d459706b8c`  
		Last Modified: Wed, 05 Nov 2025 03:55:48 GMT  
		Size: 133.7 MB (133737434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb356732994aed268a6ed2de37cfb845452c263ea9b9bdb5a248a5fb85674c`  
		Last Modified: Wed, 05 Nov 2025 01:04:55 GMT  
		Size: 22.2 MB (22220773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28feef3aafb5a98cc214441b6cf2dba72389e89e78764345df0d2bd91a62cde`  
		Last Modified: Wed, 05 Nov 2025 01:04:54 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc35fa997cb739420901a7c9db8973fa0cec3b8675c1cf55b0f1b1e703a2d87f`  
		Last Modified: Wed, 05 Nov 2025 03:56:16 GMT  
		Size: 424.2 MB (424227327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6` - unknown; unknown

```console
$ docker pull haskell@sha256:5c9632a8f79c84a0b7076c128a8a7306b11fec0b11d3426c59ffb90a887a849b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df7db158f56eb683a218244ead2693d691ef05497a8e86eca2582a244210e3e`

```dockerfile
```

-	Layers:
	-	`sha256:5cffa6f3028b1c0a6845c266c48bfc0fa41dbe510b95caac45df5671e2d3786a`  
		Last Modified: Wed, 05 Nov 2025 03:49:31 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e85988ef1583e2a54dfe93f7f6d454835116b871190ada8c8212e39cfc6eed8`  
		Last Modified: Wed, 05 Nov 2025 03:49:32 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d285bb39f6c80a8a0ff25de5f79c3031242b5b930019f2bfa4140b411e90cf39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.3 MB (658324274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a66fc530193324143ea7e25bc1e50e84855423441373d24cacce6606987951`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:24 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:26 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:28 GMT
ARG GHC=9.6.7
# Tue, 04 Nov 2025 23:22:28 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 04 Nov 2025 23:23:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196f036893c1b1973f9375ea0a6f028079cf64dc612a43158ebd64768a4052a8`  
		Last Modified: Tue, 04 Nov 2025 23:25:11 GMT  
		Size: 129.2 MB (129223967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cce136fc26055d3fd90b9055c261a96152301ab023dd5f1822e1404e00008b`  
		Last Modified: Tue, 04 Nov 2025 23:25:27 GMT  
		Size: 24.5 MB (24528570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf9e4c36920e4bf642a38fa2d19ca5b068f723455cd04243d165f85e1f79f57`  
		Last Modified: Tue, 04 Nov 2025 23:25:26 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42ed9714ed8f49ba3ea4cd3475a08d6c630e871dde96f4842162fb6a95adc27`  
		Last Modified: Wed, 05 Nov 2025 07:29:33 GMT  
		Size: 438.3 MB (438340809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6` - unknown; unknown

```console
$ docker pull haskell@sha256:a34188813a0de5c138f90913011d32bd9a8606fc39dc7c5522f59f58c1c0af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2a8490c64051c982e7dd53417cec005e17a98b6a614003136f3757f268de57`

```dockerfile
```

-	Layers:
	-	`sha256:6470a47f0f60aac51d9abc4fef961155dc6de17eed6f97efdc11ccf1533ea8a0`  
		Last Modified: Wed, 05 Nov 2025 00:49:39 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d18120c68b37bc5b0e6563532fa452bb706cb47b22562cacf5fa95ff98a56bd`  
		Last Modified: Wed, 05 Nov 2025 00:49:39 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-bullseye`

```console
$ docker pull haskell@sha256:d0b0282163e131b177b4b14a6022334ff96c058b7d09f0802b8ad73a185abfeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:5d51daa58b73b133b0c002b31e86727ad064752d3e11be18b6fe7734d77beecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641554471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f287aa18302eb4324877e9647db5e00097a0bc307622ed1fa461f5668da8a0`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:46 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:46 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:46 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:49 GMT
ARG GHC=9.6.7
# Wed, 05 Nov 2025 01:01:49 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Wed, 05 Nov 2025 01:03:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd353de69382164817f65f8772fe5d476bc3f339c097dbe47afbc8d459706b8c`  
		Last Modified: Wed, 05 Nov 2025 03:55:48 GMT  
		Size: 133.7 MB (133737434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb356732994aed268a6ed2de37cfb845452c263ea9b9bdb5a248a5fb85674c`  
		Last Modified: Wed, 05 Nov 2025 01:04:55 GMT  
		Size: 22.2 MB (22220773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28feef3aafb5a98cc214441b6cf2dba72389e89e78764345df0d2bd91a62cde`  
		Last Modified: Wed, 05 Nov 2025 01:04:54 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc35fa997cb739420901a7c9db8973fa0cec3b8675c1cf55b0f1b1e703a2d87f`  
		Last Modified: Wed, 05 Nov 2025 03:56:16 GMT  
		Size: 424.2 MB (424227327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:5c9632a8f79c84a0b7076c128a8a7306b11fec0b11d3426c59ffb90a887a849b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df7db158f56eb683a218244ead2693d691ef05497a8e86eca2582a244210e3e`

```dockerfile
```

-	Layers:
	-	`sha256:5cffa6f3028b1c0a6845c266c48bfc0fa41dbe510b95caac45df5671e2d3786a`  
		Last Modified: Wed, 05 Nov 2025 03:49:31 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e85988ef1583e2a54dfe93f7f6d454835116b871190ada8c8212e39cfc6eed8`  
		Last Modified: Wed, 05 Nov 2025 03:49:32 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d285bb39f6c80a8a0ff25de5f79c3031242b5b930019f2bfa4140b411e90cf39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.3 MB (658324274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a66fc530193324143ea7e25bc1e50e84855423441373d24cacce6606987951`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:24 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:26 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:28 GMT
ARG GHC=9.6.7
# Tue, 04 Nov 2025 23:22:28 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 04 Nov 2025 23:23:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196f036893c1b1973f9375ea0a6f028079cf64dc612a43158ebd64768a4052a8`  
		Last Modified: Tue, 04 Nov 2025 23:25:11 GMT  
		Size: 129.2 MB (129223967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cce136fc26055d3fd90b9055c261a96152301ab023dd5f1822e1404e00008b`  
		Last Modified: Tue, 04 Nov 2025 23:25:27 GMT  
		Size: 24.5 MB (24528570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf9e4c36920e4bf642a38fa2d19ca5b068f723455cd04243d165f85e1f79f57`  
		Last Modified: Tue, 04 Nov 2025 23:25:26 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42ed9714ed8f49ba3ea4cd3475a08d6c630e871dde96f4842162fb6a95adc27`  
		Last Modified: Wed, 05 Nov 2025 07:29:33 GMT  
		Size: 438.3 MB (438340809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a34188813a0de5c138f90913011d32bd9a8606fc39dc7c5522f59f58c1c0af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2a8490c64051c982e7dd53417cec005e17a98b6a614003136f3757f268de57`

```dockerfile
```

-	Layers:
	-	`sha256:6470a47f0f60aac51d9abc4fef961155dc6de17eed6f97efdc11ccf1533ea8a0`  
		Last Modified: Wed, 05 Nov 2025 00:49:39 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d18120c68b37bc5b0e6563532fa452bb706cb47b22562cacf5fa95ff98a56bd`  
		Last Modified: Wed, 05 Nov 2025 00:49:39 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-slim`

```console
$ docker pull haskell@sha256:b27c56b30c870d2dd3abeffd1aeaf65ff52e548d5fcc0f4358907cebbacc1a97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-slim` - linux; amd64

```console
$ docker pull haskell@sha256:feb213a60716162568487a0cc4e43f7f15a78cd1d2036c0425c8c97c78ee7f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590681567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf699625af9fde8ce3c666428c5dbc31c87e2e468bc1f09351a78bb9cf0a7ca`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:53 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:56 GMT
ARG GHC=9.6.7
# Wed, 05 Nov 2025 01:01:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Wed, 05 Nov 2025 01:03:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf3d873033515409b739b351e4d77fc2534abd3e2f46a3316e2ff81dfd183c8`  
		Last Modified: Wed, 05 Nov 2025 01:05:01 GMT  
		Size: 106.4 MB (106366664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c207fcdecf425c4dacfdea19e1f37212c0b6eacc828577955b216483cd8bc7`  
		Last Modified: Wed, 05 Nov 2025 01:04:56 GMT  
		Size: 22.2 MB (22220770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f20b6a137d27d5d27d4a274239a168904cd0e4ec081fb595a45174fadfda69`  
		Last Modified: Wed, 05 Nov 2025 01:04:54 GMT  
		Size: 7.6 MB (7612241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9336d9ff2afd6703889926f4a83aa0fb3c01f3ea51bb2dfe3997204f113cd7`  
		Last Modified: Wed, 05 Nov 2025 04:36:24 GMT  
		Size: 424.2 MB (424223296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:317606ba1f12315ba3e5d206e293e8f6852a922e66e055e831347d9ae2211ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953782a198f7b008d1d5760cac4534e8c4174990ac714fa019de1b54bb5c8944`

```dockerfile
```

-	Layers:
	-	`sha256:2916b61f3dd4c91e4619303b548ea22b1b4b4dfff50780d6981bc0dac6b89c60`  
		Last Modified: Wed, 05 Nov 2025 03:49:37 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb05b00b5585879a07d79b2ce4a59390bf322d13353e944ecec1b95f61641a3c`  
		Last Modified: Wed, 05 Nov 2025 03:49:38 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:2ae524ec283906b1b16b70cacb68a4eb202482b59d9382bc0c8bc1f2ff1fabdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607455930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3742a25940db94134432650d11ef91997a4aea2423c945d2f1cbb89da968022a`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:22 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:24 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:24 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:26 GMT
ARG GHC=9.6.7
# Tue, 04 Nov 2025 23:22:26 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 04 Nov 2025 23:23:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39761fbbae3128eecb1d16537e952d4a9b343e291c6889154dd2a263539da5b5`  
		Last Modified: Tue, 04 Nov 2025 23:25:27 GMT  
		Size: 101.9 MB (101863592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097cff993e9e6140385a05850784bde29029470a1c1e36f8d3d45c44642354d2`  
		Last Modified: Tue, 04 Nov 2025 23:25:17 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72ba20d9d84f826c0123fa0aa30a8e2961566fa9cba041926e390155e00e46e`  
		Last Modified: Tue, 04 Nov 2025 23:25:18 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95458b4f5262690cd75fcd6eba50ec1e124122ae7ffa799d768000e9f9d2999`  
		Last Modified: Tue, 04 Nov 2025 23:25:10 GMT  
		Size: 438.3 MB (438342224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:b228fa086c4b2e68b8ba8fa36a359cc6191207eeca836f5588cc8b78b73fdeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5a3715e7acb971ded8c489da637e365ad0eb21f79ddb4ab9ac08786d6a0222`

```dockerfile
```

-	Layers:
	-	`sha256:ee23cdc0534d5dabd0b02626f2a32eb8fbc65cd4482f82dde1522538c567b33a`  
		Last Modified: Wed, 05 Nov 2025 00:49:40 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d2b610c297f97e64a9065631f6fee72188cf80cab144fc5fe246dc11c9507b`  
		Last Modified: Wed, 05 Nov 2025 00:49:41 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6-slim-bullseye`

```console
$ docker pull haskell@sha256:b27c56b30c870d2dd3abeffd1aeaf65ff52e548d5fcc0f4358907cebbacc1a97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:feb213a60716162568487a0cc4e43f7f15a78cd1d2036c0425c8c97c78ee7f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590681567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf699625af9fde8ce3c666428c5dbc31c87e2e468bc1f09351a78bb9cf0a7ca`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:53 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:56 GMT
ARG GHC=9.6.7
# Wed, 05 Nov 2025 01:01:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Wed, 05 Nov 2025 01:03:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf3d873033515409b739b351e4d77fc2534abd3e2f46a3316e2ff81dfd183c8`  
		Last Modified: Wed, 05 Nov 2025 01:05:01 GMT  
		Size: 106.4 MB (106366664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c207fcdecf425c4dacfdea19e1f37212c0b6eacc828577955b216483cd8bc7`  
		Last Modified: Wed, 05 Nov 2025 01:04:56 GMT  
		Size: 22.2 MB (22220770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f20b6a137d27d5d27d4a274239a168904cd0e4ec081fb595a45174fadfda69`  
		Last Modified: Wed, 05 Nov 2025 01:04:54 GMT  
		Size: 7.6 MB (7612241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9336d9ff2afd6703889926f4a83aa0fb3c01f3ea51bb2dfe3997204f113cd7`  
		Last Modified: Wed, 05 Nov 2025 04:36:24 GMT  
		Size: 424.2 MB (424223296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:317606ba1f12315ba3e5d206e293e8f6852a922e66e055e831347d9ae2211ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953782a198f7b008d1d5760cac4534e8c4174990ac714fa019de1b54bb5c8944`

```dockerfile
```

-	Layers:
	-	`sha256:2916b61f3dd4c91e4619303b548ea22b1b4b4dfff50780d6981bc0dac6b89c60`  
		Last Modified: Wed, 05 Nov 2025 03:49:37 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb05b00b5585879a07d79b2ce4a59390bf322d13353e944ecec1b95f61641a3c`  
		Last Modified: Wed, 05 Nov 2025 03:49:38 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:2ae524ec283906b1b16b70cacb68a4eb202482b59d9382bc0c8bc1f2ff1fabdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607455930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3742a25940db94134432650d11ef91997a4aea2423c945d2f1cbb89da968022a`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:22 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:24 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:24 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:26 GMT
ARG GHC=9.6.7
# Tue, 04 Nov 2025 23:22:26 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 04 Nov 2025 23:23:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39761fbbae3128eecb1d16537e952d4a9b343e291c6889154dd2a263539da5b5`  
		Last Modified: Tue, 04 Nov 2025 23:25:27 GMT  
		Size: 101.9 MB (101863592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097cff993e9e6140385a05850784bde29029470a1c1e36f8d3d45c44642354d2`  
		Last Modified: Tue, 04 Nov 2025 23:25:17 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72ba20d9d84f826c0123fa0aa30a8e2961566fa9cba041926e390155e00e46e`  
		Last Modified: Tue, 04 Nov 2025 23:25:18 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95458b4f5262690cd75fcd6eba50ec1e124122ae7ffa799d768000e9f9d2999`  
		Last Modified: Tue, 04 Nov 2025 23:25:10 GMT  
		Size: 438.3 MB (438342224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b228fa086c4b2e68b8ba8fa36a359cc6191207eeca836f5588cc8b78b73fdeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5a3715e7acb971ded8c489da637e365ad0eb21f79ddb4ab9ac08786d6a0222`

```dockerfile
```

-	Layers:
	-	`sha256:ee23cdc0534d5dabd0b02626f2a32eb8fbc65cd4482f82dde1522538c567b33a`  
		Last Modified: Wed, 05 Nov 2025 00:49:40 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d2b610c297f97e64a9065631f6fee72188cf80cab144fc5fe246dc11c9507b`  
		Last Modified: Wed, 05 Nov 2025 00:49:41 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7`

```console
$ docker pull haskell@sha256:d0b0282163e131b177b4b14a6022334ff96c058b7d09f0802b8ad73a185abfeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7` - linux; amd64

```console
$ docker pull haskell@sha256:5d51daa58b73b133b0c002b31e86727ad064752d3e11be18b6fe7734d77beecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641554471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f287aa18302eb4324877e9647db5e00097a0bc307622ed1fa461f5668da8a0`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:46 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:46 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:46 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:49 GMT
ARG GHC=9.6.7
# Wed, 05 Nov 2025 01:01:49 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Wed, 05 Nov 2025 01:03:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd353de69382164817f65f8772fe5d476bc3f339c097dbe47afbc8d459706b8c`  
		Last Modified: Wed, 05 Nov 2025 03:55:48 GMT  
		Size: 133.7 MB (133737434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb356732994aed268a6ed2de37cfb845452c263ea9b9bdb5a248a5fb85674c`  
		Last Modified: Wed, 05 Nov 2025 01:04:55 GMT  
		Size: 22.2 MB (22220773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28feef3aafb5a98cc214441b6cf2dba72389e89e78764345df0d2bd91a62cde`  
		Last Modified: Wed, 05 Nov 2025 01:04:54 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc35fa997cb739420901a7c9db8973fa0cec3b8675c1cf55b0f1b1e703a2d87f`  
		Last Modified: Wed, 05 Nov 2025 03:56:16 GMT  
		Size: 424.2 MB (424227327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7` - unknown; unknown

```console
$ docker pull haskell@sha256:5c9632a8f79c84a0b7076c128a8a7306b11fec0b11d3426c59ffb90a887a849b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df7db158f56eb683a218244ead2693d691ef05497a8e86eca2582a244210e3e`

```dockerfile
```

-	Layers:
	-	`sha256:5cffa6f3028b1c0a6845c266c48bfc0fa41dbe510b95caac45df5671e2d3786a`  
		Last Modified: Wed, 05 Nov 2025 03:49:31 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e85988ef1583e2a54dfe93f7f6d454835116b871190ada8c8212e39cfc6eed8`  
		Last Modified: Wed, 05 Nov 2025 03:49:32 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d285bb39f6c80a8a0ff25de5f79c3031242b5b930019f2bfa4140b411e90cf39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.3 MB (658324274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a66fc530193324143ea7e25bc1e50e84855423441373d24cacce6606987951`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:24 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:26 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:28 GMT
ARG GHC=9.6.7
# Tue, 04 Nov 2025 23:22:28 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 04 Nov 2025 23:23:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196f036893c1b1973f9375ea0a6f028079cf64dc612a43158ebd64768a4052a8`  
		Last Modified: Tue, 04 Nov 2025 23:25:11 GMT  
		Size: 129.2 MB (129223967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cce136fc26055d3fd90b9055c261a96152301ab023dd5f1822e1404e00008b`  
		Last Modified: Tue, 04 Nov 2025 23:25:27 GMT  
		Size: 24.5 MB (24528570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf9e4c36920e4bf642a38fa2d19ca5b068f723455cd04243d165f85e1f79f57`  
		Last Modified: Tue, 04 Nov 2025 23:25:26 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42ed9714ed8f49ba3ea4cd3475a08d6c630e871dde96f4842162fb6a95adc27`  
		Last Modified: Wed, 05 Nov 2025 07:29:33 GMT  
		Size: 438.3 MB (438340809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7` - unknown; unknown

```console
$ docker pull haskell@sha256:a34188813a0de5c138f90913011d32bd9a8606fc39dc7c5522f59f58c1c0af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2a8490c64051c982e7dd53417cec005e17a98b6a614003136f3757f268de57`

```dockerfile
```

-	Layers:
	-	`sha256:6470a47f0f60aac51d9abc4fef961155dc6de17eed6f97efdc11ccf1533ea8a0`  
		Last Modified: Wed, 05 Nov 2025 00:49:39 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d18120c68b37bc5b0e6563532fa452bb706cb47b22562cacf5fa95ff98a56bd`  
		Last Modified: Wed, 05 Nov 2025 00:49:39 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-bullseye`

```console
$ docker pull haskell@sha256:d0b0282163e131b177b4b14a6022334ff96c058b7d09f0802b8ad73a185abfeb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:5d51daa58b73b133b0c002b31e86727ad064752d3e11be18b6fe7734d77beecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **641.6 MB (641554471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f287aa18302eb4324877e9647db5e00097a0bc307622ed1fa461f5668da8a0`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:46 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:46 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:46 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:46 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:49 GMT
ARG GHC=9.6.7
# Wed, 05 Nov 2025 01:01:49 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Wed, 05 Nov 2025 01:03:18 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:18 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:18 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd353de69382164817f65f8772fe5d476bc3f339c097dbe47afbc8d459706b8c`  
		Last Modified: Wed, 05 Nov 2025 03:55:48 GMT  
		Size: 133.7 MB (133737434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb356732994aed268a6ed2de37cfb845452c263ea9b9bdb5a248a5fb85674c`  
		Last Modified: Wed, 05 Nov 2025 01:04:55 GMT  
		Size: 22.2 MB (22220773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28feef3aafb5a98cc214441b6cf2dba72389e89e78764345df0d2bd91a62cde`  
		Last Modified: Wed, 05 Nov 2025 01:04:54 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc35fa997cb739420901a7c9db8973fa0cec3b8675c1cf55b0f1b1e703a2d87f`  
		Last Modified: Wed, 05 Nov 2025 03:56:16 GMT  
		Size: 424.2 MB (424227327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:5c9632a8f79c84a0b7076c128a8a7306b11fec0b11d3426c59ffb90a887a849b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df7db158f56eb683a218244ead2693d691ef05497a8e86eca2582a244210e3e`

```dockerfile
```

-	Layers:
	-	`sha256:5cffa6f3028b1c0a6845c266c48bfc0fa41dbe510b95caac45df5671e2d3786a`  
		Last Modified: Wed, 05 Nov 2025 03:49:31 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e85988ef1583e2a54dfe93f7f6d454835116b871190ada8c8212e39cfc6eed8`  
		Last Modified: Wed, 05 Nov 2025 03:49:32 GMT  
		Size: 25.9 KB (25933 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d285bb39f6c80a8a0ff25de5f79c3031242b5b930019f2bfa4140b411e90cf39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.3 MB (658324274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a66fc530193324143ea7e25bc1e50e84855423441373d24cacce6606987951`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:24 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:24 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:24 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:24 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:26 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:26 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:28 GMT
ARG GHC=9.6.7
# Tue, 04 Nov 2025 23:22:28 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 04 Nov 2025 23:23:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196f036893c1b1973f9375ea0a6f028079cf64dc612a43158ebd64768a4052a8`  
		Last Modified: Tue, 04 Nov 2025 23:25:11 GMT  
		Size: 129.2 MB (129223967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cce136fc26055d3fd90b9055c261a96152301ab023dd5f1822e1404e00008b`  
		Last Modified: Tue, 04 Nov 2025 23:25:27 GMT  
		Size: 24.5 MB (24528570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf9e4c36920e4bf642a38fa2d19ca5b068f723455cd04243d165f85e1f79f57`  
		Last Modified: Tue, 04 Nov 2025 23:25:26 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42ed9714ed8f49ba3ea4cd3475a08d6c630e871dde96f4842162fb6a95adc27`  
		Last Modified: Wed, 05 Nov 2025 07:29:33 GMT  
		Size: 438.3 MB (438340809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:a34188813a0de5c138f90913011d32bd9a8606fc39dc7c5522f59f58c1c0af16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2a8490c64051c982e7dd53417cec005e17a98b6a614003136f3757f268de57`

```dockerfile
```

-	Layers:
	-	`sha256:6470a47f0f60aac51d9abc4fef961155dc6de17eed6f97efdc11ccf1533ea8a0`  
		Last Modified: Wed, 05 Nov 2025 00:49:39 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d18120c68b37bc5b0e6563532fa452bb706cb47b22562cacf5fa95ff98a56bd`  
		Last Modified: Wed, 05 Nov 2025 00:49:39 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-slim`

```console
$ docker pull haskell@sha256:b27c56b30c870d2dd3abeffd1aeaf65ff52e548d5fcc0f4358907cebbacc1a97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-slim` - linux; amd64

```console
$ docker pull haskell@sha256:feb213a60716162568487a0cc4e43f7f15a78cd1d2036c0425c8c97c78ee7f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590681567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf699625af9fde8ce3c666428c5dbc31c87e2e468bc1f09351a78bb9cf0a7ca`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:53 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:56 GMT
ARG GHC=9.6.7
# Wed, 05 Nov 2025 01:01:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Wed, 05 Nov 2025 01:03:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf3d873033515409b739b351e4d77fc2534abd3e2f46a3316e2ff81dfd183c8`  
		Last Modified: Wed, 05 Nov 2025 01:05:01 GMT  
		Size: 106.4 MB (106366664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c207fcdecf425c4dacfdea19e1f37212c0b6eacc828577955b216483cd8bc7`  
		Last Modified: Wed, 05 Nov 2025 01:04:56 GMT  
		Size: 22.2 MB (22220770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f20b6a137d27d5d27d4a274239a168904cd0e4ec081fb595a45174fadfda69`  
		Last Modified: Wed, 05 Nov 2025 01:04:54 GMT  
		Size: 7.6 MB (7612241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9336d9ff2afd6703889926f4a83aa0fb3c01f3ea51bb2dfe3997204f113cd7`  
		Last Modified: Wed, 05 Nov 2025 04:36:24 GMT  
		Size: 424.2 MB (424223296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:317606ba1f12315ba3e5d206e293e8f6852a922e66e055e831347d9ae2211ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953782a198f7b008d1d5760cac4534e8c4174990ac714fa019de1b54bb5c8944`

```dockerfile
```

-	Layers:
	-	`sha256:2916b61f3dd4c91e4619303b548ea22b1b4b4dfff50780d6981bc0dac6b89c60`  
		Last Modified: Wed, 05 Nov 2025 03:49:37 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb05b00b5585879a07d79b2ce4a59390bf322d13353e944ecec1b95f61641a3c`  
		Last Modified: Wed, 05 Nov 2025 03:49:38 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:2ae524ec283906b1b16b70cacb68a4eb202482b59d9382bc0c8bc1f2ff1fabdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607455930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3742a25940db94134432650d11ef91997a4aea2423c945d2f1cbb89da968022a`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:22 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:24 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:24 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:26 GMT
ARG GHC=9.6.7
# Tue, 04 Nov 2025 23:22:26 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 04 Nov 2025 23:23:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39761fbbae3128eecb1d16537e952d4a9b343e291c6889154dd2a263539da5b5`  
		Last Modified: Tue, 04 Nov 2025 23:25:27 GMT  
		Size: 101.9 MB (101863592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097cff993e9e6140385a05850784bde29029470a1c1e36f8d3d45c44642354d2`  
		Last Modified: Tue, 04 Nov 2025 23:25:17 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72ba20d9d84f826c0123fa0aa30a8e2961566fa9cba041926e390155e00e46e`  
		Last Modified: Tue, 04 Nov 2025 23:25:18 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95458b4f5262690cd75fcd6eba50ec1e124122ae7ffa799d768000e9f9d2999`  
		Last Modified: Tue, 04 Nov 2025 23:25:10 GMT  
		Size: 438.3 MB (438342224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:b228fa086c4b2e68b8ba8fa36a359cc6191207eeca836f5588cc8b78b73fdeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5a3715e7acb971ded8c489da637e365ad0eb21f79ddb4ab9ac08786d6a0222`

```dockerfile
```

-	Layers:
	-	`sha256:ee23cdc0534d5dabd0b02626f2a32eb8fbc65cd4482f82dde1522538c567b33a`  
		Last Modified: Wed, 05 Nov 2025 00:49:40 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d2b610c297f97e64a9065631f6fee72188cf80cab144fc5fe246dc11c9507b`  
		Last Modified: Wed, 05 Nov 2025 00:49:41 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.6.7-slim-bullseye`

```console
$ docker pull haskell@sha256:b27c56b30c870d2dd3abeffd1aeaf65ff52e548d5fcc0f4358907cebbacc1a97
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.6.7-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:feb213a60716162568487a0cc4e43f7f15a78cd1d2036c0425c8c97c78ee7f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 MB (590681567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf699625af9fde8ce3c666428c5dbc31c87e2e468bc1f09351a78bb9cf0a7ca`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:53 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:53 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:53 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:53 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:55 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:56 GMT
ARG GHC=9.6.7
# Wed, 05 Nov 2025 01:01:56 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Wed, 05 Nov 2025 01:03:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:21 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:21 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf3d873033515409b739b351e4d77fc2534abd3e2f46a3316e2ff81dfd183c8`  
		Last Modified: Wed, 05 Nov 2025 01:05:01 GMT  
		Size: 106.4 MB (106366664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c207fcdecf425c4dacfdea19e1f37212c0b6eacc828577955b216483cd8bc7`  
		Last Modified: Wed, 05 Nov 2025 01:04:56 GMT  
		Size: 22.2 MB (22220770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f20b6a137d27d5d27d4a274239a168904cd0e4ec081fb595a45174fadfda69`  
		Last Modified: Wed, 05 Nov 2025 01:04:54 GMT  
		Size: 7.6 MB (7612241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd9336d9ff2afd6703889926f4a83aa0fb3c01f3ea51bb2dfe3997204f113cd7`  
		Last Modified: Wed, 05 Nov 2025 04:36:24 GMT  
		Size: 424.2 MB (424223296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:317606ba1f12315ba3e5d206e293e8f6852a922e66e055e831347d9ae2211ee7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953782a198f7b008d1d5760cac4534e8c4174990ac714fa019de1b54bb5c8944`

```dockerfile
```

-	Layers:
	-	`sha256:2916b61f3dd4c91e4619303b548ea22b1b4b4dfff50780d6981bc0dac6b89c60`  
		Last Modified: Wed, 05 Nov 2025 03:49:37 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb05b00b5585879a07d79b2ce4a59390bf322d13353e944ecec1b95f61641a3c`  
		Last Modified: Wed, 05 Nov 2025 03:49:38 GMT  
		Size: 26.0 KB (25996 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.6.7-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:2ae524ec283906b1b16b70cacb68a4eb202482b59d9382bc0c8bc1f2ff1fabdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **607.5 MB (607455930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3742a25940db94134432650d11ef91997a4aea2423c945d2f1cbb89da968022a`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:22 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:22 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:22 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:24 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:24 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:24 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:26 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:26 GMT
ARG GHC=9.6.7
# Tue, 04 Nov 2025 23:22:26 GMT
ARG GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
# Tue, 04 Nov 2025 23:23:46 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.6.7 GHC_RELEASE_KEY=8C961469C8FDC968718D6245AC7DE836C5DF907D
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='3cfa843687856de304a946dbe849a497c4fdad021f0275628b8ca7b55ccf8082';             GHC_URL='https://downloads.haskell.org/~ghc/9.6.7/ghc-9.6.7-aarch64-deb10-linux.tar.xz';             ;;         'x86_64')             GHC_SHA256='fc6a6247d1831745c67b27d6212f6911c35a933043f3b6851724e2e01484d077';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:46 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39761fbbae3128eecb1d16537e952d4a9b343e291c6889154dd2a263539da5b5`  
		Last Modified: Tue, 04 Nov 2025 23:25:27 GMT  
		Size: 101.9 MB (101863592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097cff993e9e6140385a05850784bde29029470a1c1e36f8d3d45c44642354d2`  
		Last Modified: Tue, 04 Nov 2025 23:25:17 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72ba20d9d84f826c0123fa0aa30a8e2961566fa9cba041926e390155e00e46e`  
		Last Modified: Tue, 04 Nov 2025 23:25:18 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95458b4f5262690cd75fcd6eba50ec1e124122ae7ffa799d768000e9f9d2999`  
		Last Modified: Tue, 04 Nov 2025 23:25:10 GMT  
		Size: 438.3 MB (438342224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.6.7-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b228fa086c4b2e68b8ba8fa36a359cc6191207eeca836f5588cc8b78b73fdeaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5a3715e7acb971ded8c489da637e365ad0eb21f79ddb4ab9ac08786d6a0222`

```dockerfile
```

-	Layers:
	-	`sha256:ee23cdc0534d5dabd0b02626f2a32eb8fbc65cd4482f82dde1522538c567b33a`  
		Last Modified: Wed, 05 Nov 2025 00:49:40 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d2b610c297f97e64a9065631f6fee72188cf80cab144fc5fe246dc11c9507b`  
		Last Modified: Wed, 05 Nov 2025 00:49:41 GMT  
		Size: 26.1 KB (26147 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8`

```console
$ docker pull haskell@sha256:75f1e960168e39037368573d65a5a7e8a9a6b82900126fdf3de25e69ea05c880
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8` - linux; amd64

```console
$ docker pull haskell@sha256:a1d43c167bb702d864de74c1c775f258ad52640e6d7eadc541586ff88240ca10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.5 MB (653541458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633d3f2689310704164c96c262254c20b2c29989f87b48bd0fc878df2bf09365`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:39 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:39 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:43 GMT
ARG GHC=9.8.4
# Wed, 05 Nov 2025 01:01:43 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:03:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f04a9e6e60b9a6b934d520adfbba79295d41e173fee6b961e3cf1faf953ca9`  
		Last Modified: Wed, 05 Nov 2025 06:46:02 GMT  
		Size: 133.7 MB (133736642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929b9e81b1ea6a09f373c3b23cf4ffc925f242ade5ec5e1fbc4e00089a3160b1`  
		Last Modified: Wed, 05 Nov 2025 01:04:47 GMT  
		Size: 22.2 MB (22220773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30a07350dacfb54a8621c84b8f0de66bb2d7cdca57cf7f6965d70008ba2fec`  
		Last Modified: Wed, 05 Nov 2025 01:04:45 GMT  
		Size: 7.6 MB (7612246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e53eafba036b4ac48f448851846711861262ebd59af107ac9e7b943968ddfd`  
		Last Modified: Wed, 05 Nov 2025 06:46:49 GMT  
		Size: 436.2 MB (436215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8` - unknown; unknown

```console
$ docker pull haskell@sha256:b249321b5c33ef1b9df5f903c0a77fb7e1499a78e081611ea33e1b27389c1eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3fddad215781cefc61b5e1f78df47541629877e012071ad79e7f8e59489b75`

```dockerfile
```

-	Layers:
	-	`sha256:ccd7fda4ef37723486efa06dd9af4234fca1fc72fe4ce15f92e970da04e1f477`  
		Last Modified: Wed, 05 Nov 2025 03:49:47 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8173b8b8856597ebd49acf3a8e54d00f3580cbac8f4160651c6cd28732f2ba78`  
		Last Modified: Wed, 05 Nov 2025 03:49:48 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:596034a02adb08f510456ad23c162369c6ba37f42e15c9e8e0a12a81a726d615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663783354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771938d06120c4a8cfa87534db9f6fe27180bd65a2666f8c35d264b754f9ae16`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:19 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:21 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG GHC=9.8.4
# Tue, 04 Nov 2025 23:22:22 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:23:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8abe994dd29ae941b15603f985161afa352a57b7757d4a1502f960bedf73fdd`  
		Last Modified: Wed, 05 Nov 2025 08:28:45 GMT  
		Size: 129.2 MB (129223813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c5c226019037a7f288f2093d02f7a9322063f51a406729b677e9264d10afd1`  
		Last Modified: Tue, 04 Nov 2025 23:25:22 GMT  
		Size: 24.5 MB (24528559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5221832edfc801f3ecf984fd33e62dd03503f754340594577c268c85d4f622`  
		Last Modified: Tue, 04 Nov 2025 23:25:17 GMT  
		Size: 14.0 MB (13972958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47eb18b2bd0e593bc463d1d177b29b7fc59d4b541679b4dc1bd525eada7ed2c`  
		Last Modified: Wed, 05 Nov 2025 08:30:12 GMT  
		Size: 443.8 MB (443800055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8` - unknown; unknown

```console
$ docker pull haskell@sha256:68c98fac4dabd709ca1800f98fcafce11d6048ea8d1f115a5f4552297f4a7522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12d22e9e5dab49b22eefdefe6d4cedda18d34b0de2087410eb94644a1c103cf`

```dockerfile
```

-	Layers:
	-	`sha256:4dcf1efdeff2ab9c45cd02f33fb33f312641cd0a75dce3c161aaf0000467997d`  
		Last Modified: Wed, 05 Nov 2025 00:49:58 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c02a10ee6af9479b3fbe1132242f0f7cdb72892d9b2616faaf4adf8d348376`  
		Last Modified: Wed, 05 Nov 2025 00:49:59 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-bullseye`

```console
$ docker pull haskell@sha256:75f1e960168e39037368573d65a5a7e8a9a6b82900126fdf3de25e69ea05c880
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:a1d43c167bb702d864de74c1c775f258ad52640e6d7eadc541586ff88240ca10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.5 MB (653541458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633d3f2689310704164c96c262254c20b2c29989f87b48bd0fc878df2bf09365`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:39 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:39 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:43 GMT
ARG GHC=9.8.4
# Wed, 05 Nov 2025 01:01:43 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:03:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f04a9e6e60b9a6b934d520adfbba79295d41e173fee6b961e3cf1faf953ca9`  
		Last Modified: Wed, 05 Nov 2025 06:46:02 GMT  
		Size: 133.7 MB (133736642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929b9e81b1ea6a09f373c3b23cf4ffc925f242ade5ec5e1fbc4e00089a3160b1`  
		Last Modified: Wed, 05 Nov 2025 01:04:47 GMT  
		Size: 22.2 MB (22220773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30a07350dacfb54a8621c84b8f0de66bb2d7cdca57cf7f6965d70008ba2fec`  
		Last Modified: Wed, 05 Nov 2025 01:04:45 GMT  
		Size: 7.6 MB (7612246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e53eafba036b4ac48f448851846711861262ebd59af107ac9e7b943968ddfd`  
		Last Modified: Wed, 05 Nov 2025 06:46:49 GMT  
		Size: 436.2 MB (436215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b249321b5c33ef1b9df5f903c0a77fb7e1499a78e081611ea33e1b27389c1eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3fddad215781cefc61b5e1f78df47541629877e012071ad79e7f8e59489b75`

```dockerfile
```

-	Layers:
	-	`sha256:ccd7fda4ef37723486efa06dd9af4234fca1fc72fe4ce15f92e970da04e1f477`  
		Last Modified: Wed, 05 Nov 2025 03:49:47 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8173b8b8856597ebd49acf3a8e54d00f3580cbac8f4160651c6cd28732f2ba78`  
		Last Modified: Wed, 05 Nov 2025 03:49:48 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:596034a02adb08f510456ad23c162369c6ba37f42e15c9e8e0a12a81a726d615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663783354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771938d06120c4a8cfa87534db9f6fe27180bd65a2666f8c35d264b754f9ae16`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:19 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:21 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG GHC=9.8.4
# Tue, 04 Nov 2025 23:22:22 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:23:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8abe994dd29ae941b15603f985161afa352a57b7757d4a1502f960bedf73fdd`  
		Last Modified: Wed, 05 Nov 2025 08:28:45 GMT  
		Size: 129.2 MB (129223813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c5c226019037a7f288f2093d02f7a9322063f51a406729b677e9264d10afd1`  
		Last Modified: Tue, 04 Nov 2025 23:25:22 GMT  
		Size: 24.5 MB (24528559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5221832edfc801f3ecf984fd33e62dd03503f754340594577c268c85d4f622`  
		Last Modified: Tue, 04 Nov 2025 23:25:17 GMT  
		Size: 14.0 MB (13972958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47eb18b2bd0e593bc463d1d177b29b7fc59d4b541679b4dc1bd525eada7ed2c`  
		Last Modified: Wed, 05 Nov 2025 08:30:12 GMT  
		Size: 443.8 MB (443800055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:68c98fac4dabd709ca1800f98fcafce11d6048ea8d1f115a5f4552297f4a7522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12d22e9e5dab49b22eefdefe6d4cedda18d34b0de2087410eb94644a1c103cf`

```dockerfile
```

-	Layers:
	-	`sha256:4dcf1efdeff2ab9c45cd02f33fb33f312641cd0a75dce3c161aaf0000467997d`  
		Last Modified: Wed, 05 Nov 2025 00:49:58 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c02a10ee6af9479b3fbe1132242f0f7cdb72892d9b2616faaf4adf8d348376`  
		Last Modified: Wed, 05 Nov 2025 00:49:59 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-slim`

```console
$ docker pull haskell@sha256:380ba0b82d8c1f9ded39f172ef323ee9672c88d2c56dc40c3e3d8733dc0ac28b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-slim` - linux; amd64

```console
$ docker pull haskell@sha256:e37fd5e94b73298e0918acfc70d437890a4de1bc9b30126cb84f024a3a58fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602673495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7c619a9c16b329ef1e89b2499e8fff9a54016f47cedd13500522268cd98f93`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:33 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:33 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:37 GMT
ARG GHC=9.8.4
# Wed, 05 Nov 2025 01:01:37 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:03:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4fa84202d68a8bd7cc72e7273aefdb4aad334bcf903d7ca2c54589c5bbfe05`  
		Last Modified: Wed, 05 Nov 2025 01:04:22 GMT  
		Size: 106.4 MB (106367056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb9f548ac4e3b76118fe45e9a581e820c524eb21eb6fd8d51eb10b42785c83e`  
		Last Modified: Wed, 05 Nov 2025 01:04:18 GMT  
		Size: 22.2 MB (22220776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aa7288fe8af570fd1203e1f1dd554ceae1eb5c2180e8e9ad50ad5ed42e68bb`  
		Last Modified: Wed, 05 Nov 2025 01:04:17 GMT  
		Size: 7.6 MB (7612246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2ec286115bf1db0982901d4d02fc7520f7c67920080b3bc30816bc2e6cb7d0`  
		Last Modified: Wed, 05 Nov 2025 01:04:28 GMT  
		Size: 436.2 MB (436214821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:b8ce02886828bafb797aac2843f8e7347cd1309d90c922310a3fe71d3ad5ff71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47898658959e476efc9e1b93ddd15d314c419217461b93b2afb5e65a7c223220`

```dockerfile
```

-	Layers:
	-	`sha256:791b0a4446cf2f9f1b5f87b07074af9c0115a9688248310a54a6ae46349b6839`  
		Last Modified: Wed, 05 Nov 2025 03:49:55 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4360fbb44d1a2f0bc2af427200e59f19247f1e6e79c4466eda48e6bd95e403f4`  
		Last Modified: Wed, 05 Nov 2025 03:49:56 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6dab2a0514bccc282094420b62eb1bfd8b0ad830ae36aaeb97f4474872c1578f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612915009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5536ea4369adbf7c286f3ab32e8805951bffb6f35a5b767abf55c63c58aa94`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:20 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:20 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:23 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:23 GMT
ARG GHC=9.8.4
# Tue, 04 Nov 2025 23:22:23 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:23:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9e8c1f6afdcfe15e879c5f60bb4f084afade6245689986ae2204e37d7a2ca7`  
		Last Modified: Tue, 04 Nov 2025 23:25:31 GMT  
		Size: 101.9 MB (101863852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1bb57a7bd072a84a6033176c1488f4242eee32bea32746f327f7046848ab8e`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b862be86ba3074c1cc18733c3ea738a050aa18cb9de25245daf63fd0bdb886`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae6017e6e9ab74ba71c4e52a19fbd36dcd789706f7f5e4666d90928ec5cef9b`  
		Last Modified: Tue, 04 Nov 2025 23:25:14 GMT  
		Size: 443.8 MB (443801023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:3ecb68170f55226420b3a84c1441215c1e97e45a2af698c3c8216259a82298ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528f9c7bd02ec72103a7d6ef16c17cac75eb25fd06939c119c6e440594a0b292`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3f0f597e5d89c818c909c34bd1c06a2ec7283093094e6de81404f003a6bbe`  
		Last Modified: Wed, 05 Nov 2025 00:50:05 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2b9a176516f5b99682bccd4df9c5fe9a36354d8b80f8b82ddbef904c8b512b`  
		Last Modified: Wed, 05 Nov 2025 00:50:06 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8-slim-bullseye`

```console
$ docker pull haskell@sha256:380ba0b82d8c1f9ded39f172ef323ee9672c88d2c56dc40c3e3d8733dc0ac28b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:e37fd5e94b73298e0918acfc70d437890a4de1bc9b30126cb84f024a3a58fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602673495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7c619a9c16b329ef1e89b2499e8fff9a54016f47cedd13500522268cd98f93`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:33 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:33 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:37 GMT
ARG GHC=9.8.4
# Wed, 05 Nov 2025 01:01:37 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:03:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4fa84202d68a8bd7cc72e7273aefdb4aad334bcf903d7ca2c54589c5bbfe05`  
		Last Modified: Wed, 05 Nov 2025 01:04:22 GMT  
		Size: 106.4 MB (106367056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb9f548ac4e3b76118fe45e9a581e820c524eb21eb6fd8d51eb10b42785c83e`  
		Last Modified: Wed, 05 Nov 2025 01:04:18 GMT  
		Size: 22.2 MB (22220776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aa7288fe8af570fd1203e1f1dd554ceae1eb5c2180e8e9ad50ad5ed42e68bb`  
		Last Modified: Wed, 05 Nov 2025 01:04:17 GMT  
		Size: 7.6 MB (7612246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2ec286115bf1db0982901d4d02fc7520f7c67920080b3bc30816bc2e6cb7d0`  
		Last Modified: Wed, 05 Nov 2025 01:04:28 GMT  
		Size: 436.2 MB (436214821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b8ce02886828bafb797aac2843f8e7347cd1309d90c922310a3fe71d3ad5ff71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47898658959e476efc9e1b93ddd15d314c419217461b93b2afb5e65a7c223220`

```dockerfile
```

-	Layers:
	-	`sha256:791b0a4446cf2f9f1b5f87b07074af9c0115a9688248310a54a6ae46349b6839`  
		Last Modified: Wed, 05 Nov 2025 03:49:55 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4360fbb44d1a2f0bc2af427200e59f19247f1e6e79c4466eda48e6bd95e403f4`  
		Last Modified: Wed, 05 Nov 2025 03:49:56 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6dab2a0514bccc282094420b62eb1bfd8b0ad830ae36aaeb97f4474872c1578f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612915009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5536ea4369adbf7c286f3ab32e8805951bffb6f35a5b767abf55c63c58aa94`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:20 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:20 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:23 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:23 GMT
ARG GHC=9.8.4
# Tue, 04 Nov 2025 23:22:23 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:23:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9e8c1f6afdcfe15e879c5f60bb4f084afade6245689986ae2204e37d7a2ca7`  
		Last Modified: Tue, 04 Nov 2025 23:25:31 GMT  
		Size: 101.9 MB (101863852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1bb57a7bd072a84a6033176c1488f4242eee32bea32746f327f7046848ab8e`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b862be86ba3074c1cc18733c3ea738a050aa18cb9de25245daf63fd0bdb886`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae6017e6e9ab74ba71c4e52a19fbd36dcd789706f7f5e4666d90928ec5cef9b`  
		Last Modified: Tue, 04 Nov 2025 23:25:14 GMT  
		Size: 443.8 MB (443801023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:3ecb68170f55226420b3a84c1441215c1e97e45a2af698c3c8216259a82298ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528f9c7bd02ec72103a7d6ef16c17cac75eb25fd06939c119c6e440594a0b292`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3f0f597e5d89c818c909c34bd1c06a2ec7283093094e6de81404f003a6bbe`  
		Last Modified: Wed, 05 Nov 2025 00:50:05 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2b9a176516f5b99682bccd4df9c5fe9a36354d8b80f8b82ddbef904c8b512b`  
		Last Modified: Wed, 05 Nov 2025 00:50:06 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4`

```console
$ docker pull haskell@sha256:75f1e960168e39037368573d65a5a7e8a9a6b82900126fdf3de25e69ea05c880
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4` - linux; amd64

```console
$ docker pull haskell@sha256:a1d43c167bb702d864de74c1c775f258ad52640e6d7eadc541586ff88240ca10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.5 MB (653541458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633d3f2689310704164c96c262254c20b2c29989f87b48bd0fc878df2bf09365`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:39 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:39 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:43 GMT
ARG GHC=9.8.4
# Wed, 05 Nov 2025 01:01:43 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:03:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f04a9e6e60b9a6b934d520adfbba79295d41e173fee6b961e3cf1faf953ca9`  
		Last Modified: Wed, 05 Nov 2025 06:46:02 GMT  
		Size: 133.7 MB (133736642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929b9e81b1ea6a09f373c3b23cf4ffc925f242ade5ec5e1fbc4e00089a3160b1`  
		Last Modified: Wed, 05 Nov 2025 01:04:47 GMT  
		Size: 22.2 MB (22220773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30a07350dacfb54a8621c84b8f0de66bb2d7cdca57cf7f6965d70008ba2fec`  
		Last Modified: Wed, 05 Nov 2025 01:04:45 GMT  
		Size: 7.6 MB (7612246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e53eafba036b4ac48f448851846711861262ebd59af107ac9e7b943968ddfd`  
		Last Modified: Wed, 05 Nov 2025 06:46:49 GMT  
		Size: 436.2 MB (436215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4` - unknown; unknown

```console
$ docker pull haskell@sha256:b249321b5c33ef1b9df5f903c0a77fb7e1499a78e081611ea33e1b27389c1eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3fddad215781cefc61b5e1f78df47541629877e012071ad79e7f8e59489b75`

```dockerfile
```

-	Layers:
	-	`sha256:ccd7fda4ef37723486efa06dd9af4234fca1fc72fe4ce15f92e970da04e1f477`  
		Last Modified: Wed, 05 Nov 2025 03:49:47 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8173b8b8856597ebd49acf3a8e54d00f3580cbac8f4160651c6cd28732f2ba78`  
		Last Modified: Wed, 05 Nov 2025 03:49:48 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:596034a02adb08f510456ad23c162369c6ba37f42e15c9e8e0a12a81a726d615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663783354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771938d06120c4a8cfa87534db9f6fe27180bd65a2666f8c35d264b754f9ae16`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:19 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:21 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG GHC=9.8.4
# Tue, 04 Nov 2025 23:22:22 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:23:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8abe994dd29ae941b15603f985161afa352a57b7757d4a1502f960bedf73fdd`  
		Last Modified: Wed, 05 Nov 2025 08:28:45 GMT  
		Size: 129.2 MB (129223813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c5c226019037a7f288f2093d02f7a9322063f51a406729b677e9264d10afd1`  
		Last Modified: Tue, 04 Nov 2025 23:25:22 GMT  
		Size: 24.5 MB (24528559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5221832edfc801f3ecf984fd33e62dd03503f754340594577c268c85d4f622`  
		Last Modified: Tue, 04 Nov 2025 23:25:17 GMT  
		Size: 14.0 MB (13972958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47eb18b2bd0e593bc463d1d177b29b7fc59d4b541679b4dc1bd525eada7ed2c`  
		Last Modified: Wed, 05 Nov 2025 08:30:12 GMT  
		Size: 443.8 MB (443800055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4` - unknown; unknown

```console
$ docker pull haskell@sha256:68c98fac4dabd709ca1800f98fcafce11d6048ea8d1f115a5f4552297f4a7522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12d22e9e5dab49b22eefdefe6d4cedda18d34b0de2087410eb94644a1c103cf`

```dockerfile
```

-	Layers:
	-	`sha256:4dcf1efdeff2ab9c45cd02f33fb33f312641cd0a75dce3c161aaf0000467997d`  
		Last Modified: Wed, 05 Nov 2025 00:49:58 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c02a10ee6af9479b3fbe1132242f0f7cdb72892d9b2616faaf4adf8d348376`  
		Last Modified: Wed, 05 Nov 2025 00:49:59 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-bullseye`

```console
$ docker pull haskell@sha256:75f1e960168e39037368573d65a5a7e8a9a6b82900126fdf3de25e69ea05c880
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:a1d43c167bb702d864de74c1c775f258ad52640e6d7eadc541586ff88240ca10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **653.5 MB (653541458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633d3f2689310704164c96c262254c20b2c29989f87b48bd0fc878df2bf09365`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:39 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:39 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:39 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:39 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:41 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:41 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:41 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:43 GMT
ARG GHC=9.8.4
# Wed, 05 Nov 2025 01:01:43 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:03:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f04a9e6e60b9a6b934d520adfbba79295d41e173fee6b961e3cf1faf953ca9`  
		Last Modified: Wed, 05 Nov 2025 06:46:02 GMT  
		Size: 133.7 MB (133736642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929b9e81b1ea6a09f373c3b23cf4ffc925f242ade5ec5e1fbc4e00089a3160b1`  
		Last Modified: Wed, 05 Nov 2025 01:04:47 GMT  
		Size: 22.2 MB (22220773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b30a07350dacfb54a8621c84b8f0de66bb2d7cdca57cf7f6965d70008ba2fec`  
		Last Modified: Wed, 05 Nov 2025 01:04:45 GMT  
		Size: 7.6 MB (7612246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e53eafba036b4ac48f448851846711861262ebd59af107ac9e7b943968ddfd`  
		Last Modified: Wed, 05 Nov 2025 06:46:49 GMT  
		Size: 436.2 MB (436215103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b249321b5c33ef1b9df5f903c0a77fb7e1499a78e081611ea33e1b27389c1eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9426047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3fddad215781cefc61b5e1f78df47541629877e012071ad79e7f8e59489b75`

```dockerfile
```

-	Layers:
	-	`sha256:ccd7fda4ef37723486efa06dd9af4234fca1fc72fe4ce15f92e970da04e1f477`  
		Last Modified: Wed, 05 Nov 2025 03:49:47 GMT  
		Size: 9.4 MB (9400393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8173b8b8856597ebd49acf3a8e54d00f3580cbac8f4160651c6cd28732f2ba78`  
		Last Modified: Wed, 05 Nov 2025 03:49:48 GMT  
		Size: 25.7 KB (25654 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:596034a02adb08f510456ad23c162369c6ba37f42e15c9e8e0a12a81a726d615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **663.8 MB (663783354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:771938d06120c4a8cfa87534db9f6fe27180bd65a2666f8c35d264b754f9ae16`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:19 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:19 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:19 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:21 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG GHC=9.8.4
# Tue, 04 Nov 2025 23:22:22 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:23:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8abe994dd29ae941b15603f985161afa352a57b7757d4a1502f960bedf73fdd`  
		Last Modified: Wed, 05 Nov 2025 08:28:45 GMT  
		Size: 129.2 MB (129223813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c5c226019037a7f288f2093d02f7a9322063f51a406729b677e9264d10afd1`  
		Last Modified: Tue, 04 Nov 2025 23:25:22 GMT  
		Size: 24.5 MB (24528559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5221832edfc801f3ecf984fd33e62dd03503f754340594577c268c85d4f622`  
		Last Modified: Tue, 04 Nov 2025 23:25:17 GMT  
		Size: 14.0 MB (13972958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47eb18b2bd0e593bc463d1d177b29b7fc59d4b541679b4dc1bd525eada7ed2c`  
		Last Modified: Wed, 05 Nov 2025 08:30:12 GMT  
		Size: 443.8 MB (443800055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:68c98fac4dabd709ca1800f98fcafce11d6048ea8d1f115a5f4552297f4a7522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d12d22e9e5dab49b22eefdefe6d4cedda18d34b0de2087410eb94644a1c103cf`

```dockerfile
```

-	Layers:
	-	`sha256:4dcf1efdeff2ab9c45cd02f33fb33f312641cd0a75dce3c161aaf0000467997d`  
		Last Modified: Wed, 05 Nov 2025 00:49:58 GMT  
		Size: 9.4 MB (9401641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37c02a10ee6af9479b3fbe1132242f0f7cdb72892d9b2616faaf4adf8d348376`  
		Last Modified: Wed, 05 Nov 2025 00:49:59 GMT  
		Size: 25.8 KB (25805 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-slim`

```console
$ docker pull haskell@sha256:380ba0b82d8c1f9ded39f172ef323ee9672c88d2c56dc40c3e3d8733dc0ac28b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-slim` - linux; amd64

```console
$ docker pull haskell@sha256:e37fd5e94b73298e0918acfc70d437890a4de1bc9b30126cb84f024a3a58fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602673495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7c619a9c16b329ef1e89b2499e8fff9a54016f47cedd13500522268cd98f93`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:33 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:33 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:37 GMT
ARG GHC=9.8.4
# Wed, 05 Nov 2025 01:01:37 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:03:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4fa84202d68a8bd7cc72e7273aefdb4aad334bcf903d7ca2c54589c5bbfe05`  
		Last Modified: Wed, 05 Nov 2025 01:04:22 GMT  
		Size: 106.4 MB (106367056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb9f548ac4e3b76118fe45e9a581e820c524eb21eb6fd8d51eb10b42785c83e`  
		Last Modified: Wed, 05 Nov 2025 01:04:18 GMT  
		Size: 22.2 MB (22220776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aa7288fe8af570fd1203e1f1dd554ceae1eb5c2180e8e9ad50ad5ed42e68bb`  
		Last Modified: Wed, 05 Nov 2025 01:04:17 GMT  
		Size: 7.6 MB (7612246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2ec286115bf1db0982901d4d02fc7520f7c67920080b3bc30816bc2e6cb7d0`  
		Last Modified: Wed, 05 Nov 2025 01:04:28 GMT  
		Size: 436.2 MB (436214821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:b8ce02886828bafb797aac2843f8e7347cd1309d90c922310a3fe71d3ad5ff71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47898658959e476efc9e1b93ddd15d314c419217461b93b2afb5e65a7c223220`

```dockerfile
```

-	Layers:
	-	`sha256:791b0a4446cf2f9f1b5f87b07074af9c0115a9688248310a54a6ae46349b6839`  
		Last Modified: Wed, 05 Nov 2025 03:49:55 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4360fbb44d1a2f0bc2af427200e59f19247f1e6e79c4466eda48e6bd95e403f4`  
		Last Modified: Wed, 05 Nov 2025 03:49:56 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6dab2a0514bccc282094420b62eb1bfd8b0ad830ae36aaeb97f4474872c1578f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612915009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5536ea4369adbf7c286f3ab32e8805951bffb6f35a5b767abf55c63c58aa94`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:20 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:20 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:23 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:23 GMT
ARG GHC=9.8.4
# Tue, 04 Nov 2025 23:22:23 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:23:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9e8c1f6afdcfe15e879c5f60bb4f084afade6245689986ae2204e37d7a2ca7`  
		Last Modified: Tue, 04 Nov 2025 23:25:31 GMT  
		Size: 101.9 MB (101863852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1bb57a7bd072a84a6033176c1488f4242eee32bea32746f327f7046848ab8e`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b862be86ba3074c1cc18733c3ea738a050aa18cb9de25245daf63fd0bdb886`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae6017e6e9ab74ba71c4e52a19fbd36dcd789706f7f5e4666d90928ec5cef9b`  
		Last Modified: Tue, 04 Nov 2025 23:25:14 GMT  
		Size: 443.8 MB (443801023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim` - unknown; unknown

```console
$ docker pull haskell@sha256:3ecb68170f55226420b3a84c1441215c1e97e45a2af698c3c8216259a82298ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528f9c7bd02ec72103a7d6ef16c17cac75eb25fd06939c119c6e440594a0b292`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3f0f597e5d89c818c909c34bd1c06a2ec7283093094e6de81404f003a6bbe`  
		Last Modified: Wed, 05 Nov 2025 00:50:05 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2b9a176516f5b99682bccd4df9c5fe9a36354d8b80f8b82ddbef904c8b512b`  
		Last Modified: Wed, 05 Nov 2025 00:50:06 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:9.8.4-slim-bullseye`

```console
$ docker pull haskell@sha256:380ba0b82d8c1f9ded39f172ef323ee9672c88d2c56dc40c3e3d8733dc0ac28b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9.8.4-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:e37fd5e94b73298e0918acfc70d437890a4de1bc9b30126cb84f024a3a58fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.7 MB (602673495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7c619a9c16b329ef1e89b2499e8fff9a54016f47cedd13500522268cd98f93`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:33 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:33 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:33 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:33 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:35 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:35 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:35 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:37 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:37 GMT
ARG GHC=9.8.4
# Wed, 05 Nov 2025 01:01:37 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:03:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4fa84202d68a8bd7cc72e7273aefdb4aad334bcf903d7ca2c54589c5bbfe05`  
		Last Modified: Wed, 05 Nov 2025 01:04:22 GMT  
		Size: 106.4 MB (106367056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb9f548ac4e3b76118fe45e9a581e820c524eb21eb6fd8d51eb10b42785c83e`  
		Last Modified: Wed, 05 Nov 2025 01:04:18 GMT  
		Size: 22.2 MB (22220776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59aa7288fe8af570fd1203e1f1dd554ceae1eb5c2180e8e9ad50ad5ed42e68bb`  
		Last Modified: Wed, 05 Nov 2025 01:04:17 GMT  
		Size: 7.6 MB (7612246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2ec286115bf1db0982901d4d02fc7520f7c67920080b3bc30816bc2e6cb7d0`  
		Last Modified: Wed, 05 Nov 2025 01:04:28 GMT  
		Size: 436.2 MB (436214821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:b8ce02886828bafb797aac2843f8e7347cd1309d90c922310a3fe71d3ad5ff71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6778025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47898658959e476efc9e1b93ddd15d314c419217461b93b2afb5e65a7c223220`

```dockerfile
```

-	Layers:
	-	`sha256:791b0a4446cf2f9f1b5f87b07074af9c0115a9688248310a54a6ae46349b6839`  
		Last Modified: Wed, 05 Nov 2025 03:49:55 GMT  
		Size: 6.8 MB (6752308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4360fbb44d1a2f0bc2af427200e59f19247f1e6e79c4466eda48e6bd95e403f4`  
		Last Modified: Wed, 05 Nov 2025 03:49:56 GMT  
		Size: 25.7 KB (25717 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9.8.4-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:6dab2a0514bccc282094420b62eb1bfd8b0ad830ae36aaeb97f4474872c1578f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **612.9 MB (612915009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5536ea4369adbf7c286f3ab32e8805951bffb6f35a5b767abf55c63c58aa94`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:20 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:20 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:22 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:22 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:22 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:23 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:23 GMT
ARG GHC=9.8.4
# Tue, 04 Nov 2025 23:22:23 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:23:47 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.4 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='310204daf2df6ad16087be94b3498ca414a0953b29e94e8ec8eb4a5c9bf603d3';             ;;         'x86_64')             GHC_SHA256='af151db8682b8c763f5a44f960f65453d794c95b60f151abc82dbdefcbe6f8ad';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:47 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9e8c1f6afdcfe15e879c5f60bb4f084afade6245689986ae2204e37d7a2ca7`  
		Last Modified: Tue, 04 Nov 2025 23:25:31 GMT  
		Size: 101.9 MB (101863852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db1bb57a7bd072a84a6033176c1488f4242eee32bea32746f327f7046848ab8e`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b862be86ba3074c1cc18733c3ea738a050aa18cb9de25245daf63fd0bdb886`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 14.0 MB (13972959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae6017e6e9ab74ba71c4e52a19fbd36dcd789706f7f5e4666d90928ec5cef9b`  
		Last Modified: Tue, 04 Nov 2025 23:25:14 GMT  
		Size: 443.8 MB (443801023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9.8.4-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:3ecb68170f55226420b3a84c1441215c1e97e45a2af698c3c8216259a82298ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6780686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528f9c7bd02ec72103a7d6ef16c17cac75eb25fd06939c119c6e440594a0b292`

```dockerfile
```

-	Layers:
	-	`sha256:d9e3f0f597e5d89c818c909c34bd1c06a2ec7283093094e6de81404f003a6bbe`  
		Last Modified: Wed, 05 Nov 2025 00:50:05 GMT  
		Size: 6.8 MB (6754818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee2b9a176516f5b99682bccd4df9c5fe9a36354d8b80f8b82ddbef904c8b512b`  
		Last Modified: Wed, 05 Nov 2025 00:50:06 GMT  
		Size: 25.9 KB (25868 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:bookworm`

```console
$ docker pull haskell@sha256:78c823f5c5723101cd3a50139ccc247d916d1bea7480c6aabd38eff59e28e647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:a41bf6877d1b1c87c421f94a4638eba7df8218bb2cbad0f71fef0e70c92602b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822417895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6aa04b16cabf65b9d6d22c021edde2947d51f1ac99f7ea60c9ff2a66ecdaf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 00:58:45 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 00:58:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 00:58:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 00:58:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:00:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:00:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:00:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74e79de258e3316172835a71c06df1674203435ce381ddb37305408e4d8730`  
		Last Modified: Wed, 05 Nov 2025 04:13:29 GMT  
		Size: 152.4 MB (152350699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553b1f0dd1e197cbbe3f0463774823e46927db001afa401edd276a3b99489d30`  
		Last Modified: Wed, 05 Nov 2025 01:02:51 GMT  
		Size: 22.2 MB (22220772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd0d14b3991f9f0aebe9120fa0a7204e23303c50fc1a8f5af5f3738c20f88b`  
		Last Modified: Wed, 05 Nov 2025 01:02:56 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd2b0e9ae55c4f5be104cd2eedef25c4289355a15a18cfaec59f5ba30f280d`  
		Last Modified: Wed, 05 Nov 2025 04:14:02 GMT  
		Size: 591.8 MB (591758313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:458e9b22beeb9921367aefa61ed3d13dd8a57d4f32a4f5d9bf110ac9dcadd790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14e893bb39433aadd3fbed2ded5e11e67866c9e8a69c7f68baeadb53a586067`

```dockerfile
```

-	Layers:
	-	`sha256:3192e5864311a3b4d24424073b8bd90e596f8710e6a70e7d14fc2527780434f7`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43221b79dcf6f8d53e8a9c4d6c37c39c1f7bb2e76922487e0fb0cb8432ff84af`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7fd9839058ccbb571a8e2d0d0a5893bbe11fb7ae709fc10082f993febdba6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824914239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142829b70e18729d3f9677cc8adbaca4536552fd98b3e9c517fd6d4dd3d8c10e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce95fd68f2b36a165ba3ad3e35396590889fb3e4056830890a496db707cf348`  
		Last Modified: Wed, 05 Nov 2025 02:50:44 GMT  
		Size: 146.4 MB (146430422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48665fd90cd640558ea256bbd3e5c928979d6e482f935f4c34d851c1efe4b4`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ffee524ac5f20f017307ec386b9e5d9c2626ffa50ba57f8803695768046f38`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c2a5bf9e7458376d169214655aff5fed34472997e6bdb214d76466ef72931`  
		Last Modified: Wed, 05 Nov 2025 02:51:25 GMT  
		Size: 591.6 MB (591626752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:733ae5fb5d3735a1be1196b14601606d235545c4ed86a7f75bf912dcb67daf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a81146c4e4b94307c4afb5035ddb5ad5bee3eb364f569f36482536eca91fd5`

```dockerfile
```

-	Layers:
	-	`sha256:ac0049f8b5386b8a7aaef447204d3098e0db4e28e1ef34c66bc13c3480601908`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b59f5afbc59dba62205816d52797470ff0bf9edb8a603bedfba451414f5994`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:bullseye`

```console
$ docker pull haskell@sha256:dd81ed941a848ffb0eced55b63e85f2b8986d82578b64f44636b602ddb521610
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:81a86e1ea160f85082562f10e1928a59a0c9ab8987aca9feb7a9a1987740f290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **659.1 MB (659125300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9387a429a5d5704c5ef75bd2051dafc8168966a1746cd4939de77e87cef6aca`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:10 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:10 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:12 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:12 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:14 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:02:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:54 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:54 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8dffd0aee3bf7bbe35a7b471cef359eeefa13932dbd4df53017ba1f4307c844`  
		Last Modified: Wed, 05 Nov 2025 06:48:41 GMT  
		Size: 133.7 MB (133737186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045be5b92248b3d9bd5effb953305a0912cfea45e2d0a718e4e07b4f45643d3c`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e0f78eeb3db594d1db2c288857f115a46a17204edf96119a5b6432088628d9`  
		Last Modified: Wed, 05 Nov 2025 01:04:45 GMT  
		Size: 7.6 MB (7612245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0900a9b4accb5d08271764254a00f9ae17937fa2ed3c65bd1b4ee01e7f9db6e`  
		Last Modified: Wed, 05 Nov 2025 06:48:51 GMT  
		Size: 441.8 MB (441798409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:7c9f9e34fe9c803e250b12ef12d39fbcf840f817a88d62983f4c0a7b7b980297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c01f7c7feef3ff0514632720135dfe5d8aa28e70104a9c252e023a5a89b963`

```dockerfile
```

-	Layers:
	-	`sha256:1d39ab4b5cbea0dd076770c00259350040057f3f1fb3ee893a983db7f135a9ba`  
		Last Modified: Wed, 05 Nov 2025 03:48:24 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a3e9b3aa3a9ed7bde2a358779c5416b443af533319e267402593ae6dd7dc6ac`  
		Last Modified: Wed, 05 Nov 2025 03:48:25 GMT  
		Size: 26.3 KB (26277 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:8d73683c844837d5df96b274c017588f5e304e505a4a82f52bb0f6d1d04071d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.4 MB (669436520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7015f6723d585232346cd27459b66255821f3481dab0165c2e987e7e15578af8`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:17 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:17 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:20 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:21 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:21 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:55 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:55 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:55 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:896b69b58297e59a819a754d1e990f5d5ad269382647d19ea7d2aa668a5f7dfd`  
		Last Modified: Tue, 04 Nov 2025 23:25:22 GMT  
		Size: 129.2 MB (129224321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12a3c165fda31a17180ab1d45a2568d86791617546c97974383027ac7b80ad1`  
		Last Modified: Tue, 04 Nov 2025 23:25:47 GMT  
		Size: 24.5 MB (24528595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fa173cb85a42b8185c9bb59004594f75717dcabc5952241d81e1d300698619`  
		Last Modified: Tue, 04 Nov 2025 23:25:46 GMT  
		Size: 14.0 MB (13972961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ef4e39dd7279c474796198d827f6eb2fe0943f03c5139be85df71245042b9b`  
		Last Modified: Tue, 04 Nov 2025 23:25:38 GMT  
		Size: 449.5 MB (449452674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:58b8f891da64e3f0776e1ee1c6be2fdc69f6fdf994740cc9d9587ab0087b4c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9427334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997597fa5f7ab7d0a4367631f13242b49e245acb41b5da7e45e02402ecfed3cf`

```dockerfile
```

-	Layers:
	-	`sha256:1c7af5b1988122c9eb842a9c4af1dbcc8a74ea4227340c3b8958d12b12146add`  
		Last Modified: Wed, 05 Nov 2025 00:48:43 GMT  
		Size: 9.4 MB (9400882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170f7fda7578f769f8289b3c507d4becdbf308b131256b716dee71cbc6c1f07d`  
		Last Modified: Wed, 05 Nov 2025 00:48:44 GMT  
		Size: 26.5 KB (26452 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:latest`

```console
$ docker pull haskell@sha256:78c823f5c5723101cd3a50139ccc247d916d1bea7480c6aabd38eff59e28e647
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:a41bf6877d1b1c87c421f94a4638eba7df8218bb2cbad0f71fef0e70c92602b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822417895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e6aa04b16cabf65b9d6d22c021edde2947d51f1ac99f7ea60c9ff2a66ecdaf`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 00:58:45 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 00:58:45 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 00:58:45 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 00:58:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 00:58:48 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 00:58:49 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 00:58:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:00:43 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:00:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:00:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c74e79de258e3316172835a71c06df1674203435ce381ddb37305408e4d8730`  
		Last Modified: Wed, 05 Nov 2025 04:13:29 GMT  
		Size: 152.4 MB (152350699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553b1f0dd1e197cbbe3f0463774823e46927db001afa401edd276a3b99489d30`  
		Last Modified: Wed, 05 Nov 2025 01:02:51 GMT  
		Size: 22.2 MB (22220772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18dd0d14b3991f9f0aebe9120fa0a7204e23303c50fc1a8f5af5f3738c20f88b`  
		Last Modified: Wed, 05 Nov 2025 01:02:56 GMT  
		Size: 7.6 MB (7607055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3dd2b0e9ae55c4f5be104cd2eedef25c4289355a15a18cfaec59f5ba30f280d`  
		Last Modified: Wed, 05 Nov 2025 04:14:02 GMT  
		Size: 591.8 MB (591758313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:458e9b22beeb9921367aefa61ed3d13dd8a57d4f32a4f5d9bf110ac9dcadd790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14e893bb39433aadd3fbed2ded5e11e67866c9e8a69c7f68baeadb53a586067`

```dockerfile
```

-	Layers:
	-	`sha256:3192e5864311a3b4d24424073b8bd90e596f8710e6a70e7d14fc2527780434f7`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43221b79dcf6f8d53e8a9c4d6c37c39c1f7bb2e76922487e0fb0cb8432ff84af`  
		Last Modified: Wed, 05 Nov 2025 03:48:17 GMT  
		Size: 26.9 KB (26867 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7fd9839058ccbb571a8e2d0d0a5893bbe11fb7ae709fc10082f993febdba6998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824914239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142829b70e18729d3f9677cc8adbaca4536552fd98b3e9c517fd6d4dd3d8c10e`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:06 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:06 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:06 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:08 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:08 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:10 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:10 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:05 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:05 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:05 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bce95fd68f2b36a165ba3ad3e35396590889fb3e4056830890a496db707cf348`  
		Last Modified: Wed, 05 Nov 2025 02:50:44 GMT  
		Size: 146.4 MB (146430422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db48665fd90cd640558ea256bbd3e5c928979d6e482f935f4c34d851c1efe4b4`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ffee524ac5f20f017307ec386b9e5d9c2626ffa50ba57f8803695768046f38`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:454c2a5bf9e7458376d169214655aff5fed34472997e6bdb214d76466ef72931`  
		Last Modified: Wed, 05 Nov 2025 02:51:25 GMT  
		Size: 591.6 MB (591626752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:733ae5fb5d3735a1be1196b14601606d235545c4ed86a7f75bf912dcb67daf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a81146c4e4b94307c4afb5035ddb5ad5bee3eb364f569f36482536eca91fd5`

```dockerfile
```

-	Layers:
	-	`sha256:ac0049f8b5386b8a7aaef447204d3098e0db4e28e1ef34c66bc13c3480601908`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81b59f5afbc59dba62205816d52797470ff0bf9edb8a603bedfba451414f5994`  
		Last Modified: Wed, 05 Nov 2025 00:48:35 GMT  
		Size: 27.1 KB (27066 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim`

```console
$ docker pull haskell@sha256:fb2bda3959b5c4571312a9449c69854eec11ec15cc6f1bc15b54c44595cd9f4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim` - linux; amd64

```console
$ docker pull haskell@sha256:6661f83b6d9612b7ee355aed52957acd2dcb22cfa1168f375a624d2a07b46890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774226835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f4c09f9d50ce6b07424304779854802bac7a82f4c7dd3cec4a3b2e167f6ed4`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 01:00:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:00:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:00:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:00:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:02:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8271a965164bc23e31a9ddc248acd56dc871d237df6cc16e874a150569eb6bb7`  
		Last Modified: Wed, 05 Nov 2025 01:04:57 GMT  
		Size: 124.4 MB (124406092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d291c4dad79d17a29c3070282e992374454228cd4f0a8e2ff72e502e31456d24`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba317e1a05fa997b78d6cc5fd1590cd99192bd8f5909a91bbfea0a74e0d2d2a`  
		Last Modified: Wed, 05 Nov 2025 01:04:48 GMT  
		Size: 7.6 MB (7607061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f57245b6c97717b46d25fa4b02c34ac804e6c463ccc00f25644b5b3eb3d12`  
		Last Modified: Wed, 05 Nov 2025 04:41:27 GMT  
		Size: 591.8 MB (591764340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim` - unknown; unknown

```console
$ docker pull haskell@sha256:b7d82e0f1f51b7d13f302097cc8e888935740cdacd5da61700eff68fac593d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46f9f3507602fe823509b330fbf15659afab945a1878bc5073ff44f325c31c2`

```dockerfile
```

-	Layers:
	-	`sha256:3c6cfa885e60075b0c7ec2e259343e3075a93afb5f61b3a939ef1c5304c2ad9b`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9454075c4b79dba3e00b3fb64ab2d514a25e318ea3914abb34adedabdeef073`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:428c38c35848ae20da237bb4c2e9a3660800fe96a93a37ec33e6d26dd5a12cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776707214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf631611acadbab9fc2f73bb9d7b518d15bf2e7478ccaac9cfdd8c0923999b5`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd10243405c62faa4120f029da948bde716bfe5475ad9e3559253bd0925ffa`  
		Last Modified: Tue, 04 Nov 2025 23:26:28 GMT  
		Size: 118.5 MB (118483733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c5c5a35659575c20b89d69badcf9aa3374cedbfda46a8d3b7b833b02ff6f8`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9fa47c2d351040977a11cd8fb7cbff5bf5a2667ff33e7fe33cbd02d540304`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8155cd34b96433ff8496257790a2ddfd1c8b9f2295601acb8a12baecf1a8765a`  
		Last Modified: Tue, 04 Nov 2025 23:25:59 GMT  
		Size: 591.6 MB (591623479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim` - unknown; unknown

```console
$ docker pull haskell@sha256:176bb96490f2f6215b29823180e44df23adcaf8b4f257f02965957b5401322d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f404b57cb062f3f8b0be0d26974da9218b9852ec75070e382b144b6f5da0cc`

```dockerfile
```

-	Layers:
	-	`sha256:bd037653b5928dfb4a639ce168667ebfc3edf471756dda6f8e41feaea3b71b5e`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4933ebfa06d93dd61896b287216f2341093ff3c290b5980c745a0d66995084b`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim-bookworm`

```console
$ docker pull haskell@sha256:fb2bda3959b5c4571312a9449c69854eec11ec15cc6f1bc15b54c44595cd9f4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim-bookworm` - linux; amd64

```console
$ docker pull haskell@sha256:6661f83b6d9612b7ee355aed52957acd2dcb22cfa1168f375a624d2a07b46890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.2 MB (774226835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8f4c09f9d50ce6b07424304779854802bac7a82f4c7dd3cec4a3b2e167f6ed4`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Wed, 05 Nov 2025 01:00:54 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:00:54 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:00:54 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:00:56 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:00:56 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:00:57 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC=9.12.2
# Wed, 05 Nov 2025 01:00:57 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 05 Nov 2025 01:02:52 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:02:52 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:02:52 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8271a965164bc23e31a9ddc248acd56dc871d237df6cc16e874a150569eb6bb7`  
		Last Modified: Wed, 05 Nov 2025 01:04:57 GMT  
		Size: 124.4 MB (124406092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d291c4dad79d17a29c3070282e992374454228cd4f0a8e2ff72e502e31456d24`  
		Last Modified: Wed, 05 Nov 2025 01:04:46 GMT  
		Size: 22.2 MB (22220775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ba317e1a05fa997b78d6cc5fd1590cd99192bd8f5909a91bbfea0a74e0d2d2a`  
		Last Modified: Wed, 05 Nov 2025 01:04:48 GMT  
		Size: 7.6 MB (7607061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64f57245b6c97717b46d25fa4b02c34ac804e6c463ccc00f25644b5b3eb3d12`  
		Last Modified: Wed, 05 Nov 2025 04:41:27 GMT  
		Size: 591.8 MB (591764340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:b7d82e0f1f51b7d13f302097cc8e888935740cdacd5da61700eff68fac593d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46f9f3507602fe823509b330fbf15659afab945a1878bc5073ff44f325c31c2`

```dockerfile
```

-	Layers:
	-	`sha256:3c6cfa885e60075b0c7ec2e259343e3075a93afb5f61b3a939ef1c5304c2ad9b`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 6.6 MB (6605748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9454075c4b79dba3e00b3fb64ab2d514a25e318ea3914abb34adedabdeef073`  
		Last Modified: Wed, 05 Nov 2025 03:48:28 GMT  
		Size: 26.3 KB (26340 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:428c38c35848ae20da237bb4c2e9a3660800fe96a93a37ec33e6d26dd5a12cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **776.7 MB (776707214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf631611acadbab9fc2f73bb9d7b518d15bf2e7478ccaac9cfdd8c0923999b5`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 23:22:12 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:12 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:12 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:14 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:14 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:15 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 23:22:15 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 23:24:07 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:24:07 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:24:07 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7cd10243405c62faa4120f029da948bde716bfe5475ad9e3559253bd0925ffa`  
		Last Modified: Tue, 04 Nov 2025 23:26:28 GMT  
		Size: 118.5 MB (118483733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4c5c5a35659575c20b89d69badcf9aa3374cedbfda46a8d3b7b833b02ff6f8`  
		Last Modified: Tue, 04 Nov 2025 23:26:06 GMT  
		Size: 24.5 MB (24528603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da9fa47c2d351040977a11cd8fb7cbff5bf5a2667ff33e7fe33cbd02d540304`  
		Last Modified: Tue, 04 Nov 2025 23:26:05 GMT  
		Size: 14.0 MB (13969023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8155cd34b96433ff8496257790a2ddfd1c8b9f2295601acb8a12baecf1a8765a`  
		Last Modified: Tue, 04 Nov 2025 23:25:59 GMT  
		Size: 591.6 MB (591623479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bookworm` - unknown; unknown

```console
$ docker pull haskell@sha256:176bb96490f2f6215b29823180e44df23adcaf8b4f257f02965957b5401322d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6660722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f404b57cb062f3f8b0be0d26974da9218b9852ec75070e382b144b6f5da0cc`

```dockerfile
```

-	Layers:
	-	`sha256:bd037653b5928dfb4a639ce168667ebfc3edf471756dda6f8e41feaea3b71b5e`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 6.6 MB (6634207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4933ebfa06d93dd61896b287216f2341093ff3c290b5980c745a0d66995084b`  
		Last Modified: Wed, 05 Nov 2025 00:48:45 GMT  
		Size: 26.5 KB (26515 bytes)  
		MIME: application/vnd.in-toto+json

## `haskell:slim-bullseye`

```console
$ docker pull haskell@sha256:415e263078684c25a11918122c8173f671f05b6f4809c3321bd8e813ed414c5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:f3ab4f23ec881de6220a2b68b599406140cef1ed63fc60c2de649d35f24a5e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **608.3 MB (608258987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdc26fd61aeddbe576dd48a9595f1beba39f8a0b04fe1a8dc065c94b58d574c`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Wed, 05 Nov 2025 01:01:26 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:01:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Nov 2025 01:01:26 GMT
ARG STACK=3.3.1
# Wed, 05 Nov 2025 01:01:26 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 05 Nov 2025 01:01:28 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 05 Nov 2025 01:01:28 GMT
ARG CABAL_INSTALL=3.14.1.1
# Wed, 05 Nov 2025 01:01:28 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Wed, 05 Nov 2025 01:01:30 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 05 Nov 2025 01:01:30 GMT
ARG GHC=9.10.3
# Wed, 05 Nov 2025 01:01:30 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Wed, 05 Nov 2025 01:03:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 05 Nov 2025 01:03:04 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Nov 2025 01:03:04 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923f781df5b8a5c4299278e3418c8167b0755e231951fad172068cef8d708870`  
		Last Modified: Wed, 05 Nov 2025 01:04:38 GMT  
		Size: 106.4 MB (106366669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295a975b946c68a39b8fa62e02be53316c8932176eac7227b6b0bc86b95148a0`  
		Last Modified: Wed, 05 Nov 2025 01:04:28 GMT  
		Size: 22.2 MB (22220774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084d0d48b3516b6c62cd1a7ca37708fc2d5aa8454ff1398a6eb68baff6597d99`  
		Last Modified: Wed, 05 Nov 2025 01:04:26 GMT  
		Size: 7.6 MB (7612243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14992ee7da922ef406db6cf1542f4cb2619512aa477d189bb6b568536233e7ca`  
		Last Modified: Wed, 05 Nov 2025 06:58:18 GMT  
		Size: 441.8 MB (441800705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:4f01384a4a590600f239c8daf1e0269803ff098779e1726b0bdd85bb745dfc4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6776673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ebc71cba910e7c4ffc7bf31b6643dfbca8abd8fc5e3457ef9737b5a7f4e160`

```dockerfile
```

-	Layers:
	-	`sha256:d49c2acab03cbb152b37481eca7475af2446bfa5d70ae4c03d1cbbd65984be15`  
		Last Modified: Wed, 05 Nov 2025 03:48:36 GMT  
		Size: 6.8 MB (6750929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8dfdca42123fdcddcd45976dc302fd49052d6c7d91b2128d2dae3c2198230cb`  
		Last Modified: Wed, 05 Nov 2025 03:48:37 GMT  
		Size: 25.7 KB (25744 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:4c155d54fb64720b4a09291dd911e1a8cdc9d64b062258a9a591de4c379974c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **618.6 MB (618570950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d57691ad02377bce23fb606584a35a7b0e855d4452482e09e7279bd9515541a0`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 23:22:16 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:22:16 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 23:22:16 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 23:22:16 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 23:22:19 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)";     export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 23:22:19 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 23:22:19 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 23:22:20 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='5e8c47a055d5b744741039a7061ee43ec7d080d1251784e7a4cd836403e42523';             ;;         'x86_64')             CABAL_INSTALL_SHA256='41b85bb25fa654e4b79169014b9142fe696ff35e002e043caa0e52d65204ba8a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 23:22:20 GMT
ARG GHC=9.10.3
# Tue, 04 Nov 2025 23:22:20 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 23:23:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.10.3 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='052789dfe7f6fba6dc3822de0da272e8a5bd358c37adae17d8e82cff39bc1008';             ;;         'x86_64')             GHC_SHA256='b6bbd3514e0cdb9db350812a003bb7c670c58d99779086fbe41092b019548924';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 23:23:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 23:23:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d275ddfa41ee2d9ccfc71507f0292da1aba94bd2f501c5ddfd430907b4dc50`  
		Last Modified: Tue, 04 Nov 2025 23:25:29 GMT  
		Size: 101.9 MB (101863502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd2b3f08398c1bfe2ef3c048abc27c058f7a6fcba39580a722e21bec8ad343b`  
		Last Modified: Tue, 04 Nov 2025 23:25:24 GMT  
		Size: 24.5 MB (24528551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46140ed114cae7d7b0b71a188690513fe284c7320050bb4dba82f025b8f68258`  
		Last Modified: Tue, 04 Nov 2025 23:25:23 GMT  
		Size: 14.0 MB (13972958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0dd63d00101136020b2a86961bdf45b99f7cf0d3fc0362b559d2dc080561e80`  
		Last Modified: Tue, 04 Nov 2025 23:25:15 GMT  
		Size: 449.5 MB (449457387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:1084beeb40a2a5530f4f1fe6ca4ff5c39130aeae6205de0dff0d411c4f681e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6779334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e3c86c3ae0c45dcf954bb7443da4384fed2e7e868430588319acef4cd3a506`

```dockerfile
```

-	Layers:
	-	`sha256:70296bae1d0c5102672799af1c2caf71d4fb7e46af35ccf067f5300e0b6fb0a7`  
		Last Modified: Wed, 05 Nov 2025 00:48:52 GMT  
		Size: 6.8 MB (6753439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4b054ea1508bde495c990515594f0b04af77f5c1df839aae61e2a0056793990`  
		Last Modified: Wed, 05 Nov 2025 00:48:53 GMT  
		Size: 25.9 KB (25895 bytes)  
		MIME: application/vnd.in-toto+json
