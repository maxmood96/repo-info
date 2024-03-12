## `haskell:9-slim-buster`

```console
$ docker pull haskell@sha256:c9f458686de098b431e01b2a802466b0451c72d05381f4aebbe72a5ae245f92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:a8f4371fda7264c0ce654448ede13b93cbfdfe5608d557275239f6c406aca136
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.7 MB (447652940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636d47e5b490af201cd956bf12239e2afcdd48ec4ac620bb14ac36c984692629`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:45 GMT
ADD file:e64f92c07598d7a1e58a8116342198e837ea4ed870cac2c252323c261b270566 in / 
# Tue, 12 Mar 2024 01:21:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 09:01:24 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 09:01:50 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 09:01:51 GMT
ARG STACK=2.15.1
# Tue, 12 Mar 2024 09:01:51 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 12 Mar 2024 09:01:54 GMT
# ARGS: STACK=2.15.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='450126245044aa37ea8ba33f70c3c5bad331a3b4d3138f7b7ad0dee2a4ca1613';             ;;         'x86_64')             STACK_SHA256='3e8d85c4c9d24905498edc8c0ec0b4fa207093d9817f281d842c203f33ad9f5e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 12 Mar 2024 09:01:55 GMT
ARG CABAL_INSTALL=3.10.2.0
# Tue, 12 Mar 2024 09:01:55 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 12 Mar 2024 09:01:57 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 12 Mar 2024 09:01:57 GMT
ARG GHC=9.8.2
# Tue, 12 Mar 2024 09:01:57 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 12 Mar 2024 09:03:37 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 12 Mar 2024 09:03:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 09:03:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:4a21b857313366ffd622f19e31c4300a81dce92b023b4ff6583ca167179804ac`  
		Last Modified: Tue, 12 Mar 2024 01:26:59 GMT  
		Size: 27.2 MB (27188304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b7132a505ed26b97d44a19f8c791127b3b651f3a69ef312efe582a2799fd43`  
		Last Modified: Tue, 12 Mar 2024 09:19:22 GMT  
		Size: 94.0 MB (94045079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d174ad6ce725da67388511e3866bf630f27a7c1a29b9f8587ac749188368014f`  
		Last Modified: Tue, 12 Mar 2024 09:19:11 GMT  
		Size: 21.4 MB (21436614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d0a3ed398350c8a6645ef554b2ed98f0d12d3a1a83f2d6a2988a49597241e1`  
		Last Modified: Tue, 12 Mar 2024 09:19:08 GMT  
		Size: 8.0 MB (7999456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb776e84bd44ca2da631600cc3f296e03647673871d4421af704226d1287231`  
		Last Modified: Tue, 12 Mar 2024 09:19:57 GMT  
		Size: 297.0 MB (296983487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:d80d7458b0644fd2763898f8582e881041613d4eb46dc5670834934861dcd081
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.5 MB (451489265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c33f58b227d1b5a1cd88c4cc2fa02cf9457e53b622b9dc53e5af5925d46cb0`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:05 GMT
ADD file:01e6303e5bd3d7bb8200a616ab1d931421cd756c837936b3f897727814cb89c3 in / 
# Tue, 12 Mar 2024 00:46:06 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:27:04 GMT
ENV LANG=C.UTF-8
# Tue, 12 Mar 2024 02:27:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:27:21 GMT
ARG STACK=2.15.1
# Tue, 12 Mar 2024 02:27:21 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 12 Mar 2024 02:27:24 GMT
# ARGS: STACK=2.15.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='450126245044aa37ea8ba33f70c3c5bad331a3b4d3138f7b7ad0dee2a4ca1613';             ;;         'x86_64')             STACK_SHA256='3e8d85c4c9d24905498edc8c0ec0b4fa207093d9817f281d842c203f33ad9f5e';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Tue, 12 Mar 2024 02:27:25 GMT
ARG CABAL_INSTALL=3.10.2.0
# Tue, 12 Mar 2024 02:27:25 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Tue, 12 Mar 2024 02:27:27 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='004ed4a7ca890fadee23f58f9cb606c066236a43e16b34be2532b177b231b06d';             ;;         'x86_64')             CABAL_INSTALL_SHA256='bdeb27c008b09c3b86f8a2768018d62a1aee02565304d123fda87ed432549418';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Tue, 12 Mar 2024 02:27:27 GMT
ARG GHC=9.8.2
# Tue, 12 Mar 2024 02:27:27 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 12 Mar 2024 02:28:55 GMT
# ARGS: CABAL_INSTALL=3.10.2.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Tue, 12 Mar 2024 02:29:06 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Mar 2024 02:29:06 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:f109bca8a22fa25fc80b89d2ad693f6f3e7832d4386218a35d068f3b37b0e808`  
		Last Modified: Tue, 12 Mar 2024 00:50:11 GMT  
		Size: 26.0 MB (25970589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423479e962c133f62edb999fc509d246a177db39cf8ed9c1c5b2b4c38235dd0f`  
		Last Modified: Tue, 12 Mar 2024 02:44:06 GMT  
		Size: 88.1 MB (88055032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9a6098845d3652853d057deaf2cabd9ad85068a14e812bc3717e774af99389`  
		Last Modified: Tue, 12 Mar 2024 02:43:58 GMT  
		Size: 23.7 MB (23745268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c38163335ac58480a356921f67ce05e54595e393ee4dbb11fa54f1c3dd35a5`  
		Last Modified: Tue, 12 Mar 2024 02:43:57 GMT  
		Size: 10.1 MB (10112976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350b1321f68e33a2fe194ccd31c4742ca9d408fdb60955cfe4b0382bfd6da465`  
		Last Modified: Tue, 12 Mar 2024 02:45:43 GMT  
		Size: 303.6 MB (303605400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
