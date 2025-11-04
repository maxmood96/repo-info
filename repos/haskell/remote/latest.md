## `haskell:latest`

```console
$ docker pull haskell@sha256:959738aa548fcfe073058463f3e0c56f349bd627f39559006af7b290f734110e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:bfb338741ce9d1ee5af7d7396c9a06776797b27a1d0a13447fd5081e4eb9ab5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **822.4 MB (822424858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5334dcd5b2f32a667b133477c51e21bd02e2b8bbf6820d3274e0d0d2a12715ec`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:16:51 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:16:51 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:51 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 00:16:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 00:16:53 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 00:16:53 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 00:16:53 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 00:16:54 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 00:16:54 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 00:16:54 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 00:18:50 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 00:18:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:18:50 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c127189757d6727401624cfa3591d2759a10972de9c70f68bb0506481ebb343`  
		Last Modified: Tue, 04 Nov 2025 09:50:26 GMT  
		Size: 152.4 MB (152350288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08f03b61fdba6cdccbf7ca4a4eede5faf298dba9372c59b28b8e4f31cb5332a6`  
		Last Modified: Tue, 04 Nov 2025 00:20:42 GMT  
		Size: 22.2 MB (22220767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701cf9879e02a272ef2359ff406b9b2929b2f45dad581f4d322fbb871747e116`  
		Last Modified: Tue, 04 Nov 2025 00:20:34 GMT  
		Size: 7.6 MB (7607047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47880a60eb608920ecbe30fef3fe1d3553076eed98353dec89489776dfad93c1`  
		Last Modified: Tue, 04 Nov 2025 09:50:36 GMT  
		Size: 591.8 MB (591765700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:4da06618bb15a8663ed17d2b914c18338afb17d69203a5af0d35042fca5fe2ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9505549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee13b8fdaaf915142afd1d48e3b4530158ee3d5f652f8aa62ffdb984098f9a9`

```dockerfile
```

-	Layers:
	-	`sha256:4a3df4c7ccbbfdb14ef3ca3b5cfceec0adbe9724d28fe8b7a3b8541840207df5`  
		Last Modified: Tue, 04 Nov 2025 09:48:17 GMT  
		Size: 9.5 MB (9478757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1221931ad957abd5f7f5e0a294ebfc24834f34778958bf8561dc80d9c1939fef`  
		Last Modified: Tue, 04 Nov 2025 09:48:17 GMT  
		Size: 26.8 KB (26792 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:latest` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:1ca9f94fd1001819a1f576e60d1e7588595c33f7555a03387920c052b3161f09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **824.9 MB (824914217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6cd0054b61f6d48f5f6b99fe8f9d9227e831c467327e61330321cd57202ac53`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:17:00 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:17:00 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:17:00 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 00:17:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 00:17:03 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 00:17:03 GMT
ARG CABAL_INSTALL=3.14.1.1
# Tue, 04 Nov 2025 00:17:03 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 04 Nov 2025 00:17:04 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb12.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='f763fb2af2bc1ff174b7361a7d51109a585954f87a0e14f86d144f3bce28f7a9';             ;;         'x86_64')             CABAL_INSTALL_SHA256='73a463306c771e18ca22c0a9469176ffab0138ec5925adb5364ef47174e1adc5';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 00:17:04 GMT
ARG GHC=9.12.2
# Tue, 04 Nov 2025 00:17:04 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Tue, 04 Nov 2025 00:20:29 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.14.1.1 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.12.2 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb12-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='bee95bc91a621d8a2e9a9d86dac28ff839605e87316518dae12c779709bd58f1';             ;;         'x86_64')             GHC_SHA256='447ec2fcc773ae9ebc3f39766c719641631274f9b765d7426a8cbe9241677c9f';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 00:20:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.12.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:20:29 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a1f050b3db97bf0fb4bb95458b2f9adc3acc756c0bf7291a6d9e1bf2b25605`  
		Last Modified: Tue, 04 Nov 2025 14:15:49 GMT  
		Size: 146.4 MB (146430785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214dfa0dcf05744bd0dc9333fb4b29da68bc64c3e633996bc8bb23cfb403e702`  
		Last Modified: Tue, 04 Nov 2025 00:22:33 GMT  
		Size: 24.5 MB (24528554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eef0c2c6e73e3505187fbb3c7984d49bb31c2a75754f24151cc90f97ff7e8ed`  
		Last Modified: Tue, 04 Nov 2025 00:22:30 GMT  
		Size: 14.0 MB (13969022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc84eccf9e1d8833968f4e0d80a8bbbbafc77d17474c5aea27f77fcea94c659d`  
		Last Modified: Tue, 04 Nov 2025 14:15:53 GMT  
		Size: 591.6 MB (591626378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:latest` - unknown; unknown

```console
$ docker pull haskell@sha256:fece9939c2a3ba81332660dbe676f6e53ba7525d1c174efff6891059332bbc30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 MB (9533604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7e310ca2188160c35731551b2b3d895ebae39719437a611d3c07a2371103f33`

```dockerfile
```

-	Layers:
	-	`sha256:d12e278f881f9eab4fa8ab5a8340165a9778903a28aeda9d8e0989bbd0c8433a`  
		Last Modified: Tue, 04 Nov 2025 09:48:28 GMT  
		Size: 9.5 MB (9506613 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1753a47e934112d3ca2303796afe11e9845ef301a31665ac6cccfdb8301d3f7`  
		Last Modified: Tue, 04 Nov 2025 09:48:28 GMT  
		Size: 27.0 KB (26991 bytes)  
		MIME: application/vnd.in-toto+json
