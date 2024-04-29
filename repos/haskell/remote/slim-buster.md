## `haskell:slim-buster`

```console
$ docker pull haskell@sha256:211b65a92cacec6232af9ded4ee0a3ca15d04c9903bf68643ff971f2f8e9057e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:slim-buster` - linux; amd64

```console
$ docker pull haskell@sha256:0b7c87871f940a3b129a9bfa5602dbc1de154502d9bba55974549e362e426f37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **447.8 MB (447815309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870a00ea17bfe83fb3eb359c48226baf10278b2059f96e250fe5a28c38586725`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:50 GMT
ADD file:9b846fb660cf816c4e731c6f547b8e389343bc05aa2ec510b1dfc2bddd4d1c8a in / 
# Wed, 24 Apr 2024 03:28:51 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:34:51 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:35:10 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:35:11 GMT
ARG STACK=2.15.5
# Wed, 24 Apr 2024 04:35:11 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 24 Apr 2024 04:35:15 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Fri, 26 Apr 2024 22:11:49 GMT
ARG CABAL_INSTALL=3.10.3.0
# Fri, 26 Apr 2024 22:11:50 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Fri, 26 Apr 2024 22:11:52 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='92d341620c60294535f03098bff796ef6de2701de0c4fcba249cde18a2923013';             ;;         'x86_64')             CABAL_INSTALL_SHA256='1d7a7131402295b01f25be5373fde095a404c45f9b5a5508fb7474bb0d3d057a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Fri, 26 Apr 2024 22:11:52 GMT
ARG GHC=9.8.2
# Fri, 26 Apr 2024 22:11:53 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Fri, 26 Apr 2024 22:13:35 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Fri, 26 Apr 2024 22:13:41 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Apr 2024 22:13:41 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:74ff537ac401802b30ae451fd049f6337b6ed0ee93f7f7e1b00cc09b9ae7f2af`  
		Last Modified: Wed, 24 Apr 2024 03:33:56 GMT  
		Size: 27.3 MB (27337575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff9592dd87b246fac3ba36b3683c97b67d3281a31b7174f67e43cbabc137bce`  
		Last Modified: Wed, 24 Apr 2024 04:52:49 GMT  
		Size: 94.0 MB (94043841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0e508509841e6ef472fa07934e48844a79e4e4620cce636456daeac016f236`  
		Last Modified: Wed, 24 Apr 2024 04:52:39 GMT  
		Size: 21.4 MB (21443418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d847294f430b2e9c64e689682f6dde9ea8f22e0b581b822354769a302a40b1`  
		Last Modified: Fri, 26 Apr 2024 22:23:30 GMT  
		Size: 8.0 MB (8009669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235f59d25e57f8059b2a56f3ceb964370b90a29d96c1453781568dff99002834`  
		Last Modified: Fri, 26 Apr 2024 22:24:18 GMT  
		Size: 297.0 MB (296980806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:slim-buster` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:27a410926572c407c6b18d1fe465fa3f11047d62e6a64c193700c7f5abfd8c86
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **451.6 MB (451640769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7713489943d4791b35ed31e83ac386aef5fc10a9591c1f4291cc695f36714d4`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 24 Apr 2024 04:11:06 GMT
ADD file:bd84662eb5c566f361c169149ba683475c50ddc528270daf67d40c8e98ed12a7 in / 
# Wed, 24 Apr 2024 04:11:07 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:50:41 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 08:50:56 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:50:58 GMT
ARG STACK=2.15.5
# Wed, 24 Apr 2024 08:50:58 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 24 Apr 2024 08:51:01 GMT
# ARGS: STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='52cd9d9c2ee4dbf2841bba856f5fca15fbf6ba23fced7256aa3f7c8b76381c91';             ;;         'x86_64')             STACK_SHA256='d55f8554932aad23f7b1198e0d5ebe332073d73fe60e3f324d0b315c156d8c43';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Mon, 29 Apr 2024 20:02:01 GMT
ARG CABAL_INSTALL=3.10.3.0
# Mon, 29 Apr 2024 20:02:01 GMT
ARG CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF
# Mon, 29 Apr 2024 20:02:04 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='92d341620c60294535f03098bff796ef6de2701de0c4fcba249cde18a2923013';             ;;         'x86_64')             CABAL_INSTALL_SHA256='1d7a7131402295b01f25be5373fde095a404c45f9b5a5508fb7474bb0d3d057a';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Mon, 29 Apr 2024 20:02:04 GMT
ARG GHC=9.8.2
# Mon, 29 Apr 2024 20:02:04 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Mon, 29 Apr 2024 20:03:30 GMT
# ARGS: CABAL_INSTALL=3.10.3.0 CABAL_INSTALL_RELEASE_KEY=EAF2A9A722C0C96F2B431CA511AAD8CEDEE0CAEF GHC=9.8.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 STACK=2.15.5 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='9a3776fd8dc02f95b751f0e44823d6727dea2c212857e2c5c5f6a38a034d1575';             ;;         'x86_64')             GHC_SHA256='7449e1c8ef351ec326f36d9eba2885ba7b75d9900df35b2069c4d6fd151b09eb';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Mon, 29 Apr 2024 20:03:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.8.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 29 Apr 2024 20:03:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:57c62469eb2b8cb9a971714401ad24a78c171e2f6dab20314e1c5f0dab7a8639`  
		Last Modified: Wed, 24 Apr 2024 04:15:23 GMT  
		Size: 26.1 MB (26109830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a1461f8a980239fb62e99e87f008b6219d9f0e507f58cdcae93a2367f7ddad`  
		Last Modified: Wed, 24 Apr 2024 09:08:29 GMT  
		Size: 88.1 MB (88057126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebd2cb7bddf5e3dd2de5827e881c68ffceb78a27ae7b584056126811834a21c`  
		Last Modified: Wed, 24 Apr 2024 09:08:21 GMT  
		Size: 23.7 MB (23749362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c2a2f05fb724d7aac93c27411f3fe0b2c18966e8aeee8f70b46cc8dd76c263`  
		Last Modified: Mon, 29 Apr 2024 20:12:57 GMT  
		Size: 10.1 MB (10118932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e450a9005f2418d28e9b38caca00e4125d32fda539ad966762528dfab93efe56`  
		Last Modified: Mon, 29 Apr 2024 20:13:40 GMT  
		Size: 303.6 MB (303605519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
