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
