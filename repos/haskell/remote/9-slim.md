## `haskell:9-slim`

```console
$ docker pull haskell@sha256:5548ba78c59d05d727223855d117c7f64f4f22e291d1fb81cd43130ec9a28a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `haskell:9-slim` - linux; amd64

```console
$ docker pull haskell@sha256:a667d63e538b3fe80138665681ea592a3abde302aad48db570b2158970760e32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.4 MB (427372341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1fa61331b18ea8be888c9457d778b53065b01508512a529c143f445ee5cee8e`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:35 GMT
ADD file:04482e1456288a566d216ed1cea383eabd946f66656da78e1e151056edf936d1 in / 
# Wed, 11 Oct 2023 18:35:35 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 20:06:28 GMT
ENV LANG=C.UTF-8
# Wed, 11 Oct 2023 20:06:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:07:00 GMT
ARG STACK=2.11.1
# Wed, 11 Oct 2023 20:07:00 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 11 Oct 2023 20:07:03 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 11 Oct 2023 20:07:03 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 11 Oct 2023 20:07:04 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 11 Oct 2023 20:07:06 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 11 Oct 2023 20:07:06 GMT
ARG GHC=9.6.3
# Wed, 11 Oct 2023 20:07:06 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Wed, 11 Oct 2023 20:08:41 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 11 Oct 2023 20:08:46 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 20:08:47 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:b70638ed4228556f5f57f76a636b1668fe301e86662437141774e61963da1b4f`  
		Last Modified: Wed, 11 Oct 2023 18:41:01 GMT  
		Size: 27.2 MB (27187490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ced24644a2add9a3304a700fc1b7f61d907ea6464919e662cd29edee0905702`  
		Last Modified: Wed, 11 Oct 2023 20:14:08 GMT  
		Size: 94.0 MB (94044368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfd24f0256bd1a42d1f892682bc4aabc2eaa97b40c3329fb8a401f056fa6b50`  
		Last Modified: Wed, 11 Oct 2023 20:13:58 GMT  
		Size: 15.4 MB (15359956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d6cd6508b074b1fc0563d4da5731a3334fb1d2576314fa2fd1b4b931e0998f`  
		Last Modified: Wed, 11 Oct 2023 20:13:57 GMT  
		Size: 7.8 MB (7838353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a39875de8fea1acd7ae2e9ce6ff90d5639161595fef37abb634738ac0eabf98`  
		Last Modified: Wed, 11 Oct 2023 20:14:44 GMT  
		Size: 282.9 MB (282942174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `haskell:9-slim` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:9cfab74d0de6df74ba2e25c6948261c5352001ec7a655fade88f4a6226836522
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.7 MB (433697134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d441dfe54e42fb9b9928afb61a7cc4423e24bfeca866e82e2e4db351589c5f1`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:21 GMT
ADD file:013dd6e1187d63722cbaddc725f44bc6789ce42a75e2ae86456088763728139c in / 
# Wed, 11 Oct 2023 18:25:21 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 22:56:16 GMT
ENV LANG=C.UTF-8
# Wed, 11 Oct 2023 22:56:34 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 22:56:36 GMT
ARG STACK=2.11.1
# Wed, 11 Oct 2023 22:56:36 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 11 Oct 2023 22:56:39 GMT
# ARGS: STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='c7733d07ed78d6f4d82e0ebf6d260eb693c6c9df2208003d60caba69766f9c15';             ;;         'x86_64')             STACK_SHA256='408a120e824ed6e6b24c548a2ff6f210fcb0eed246f204a280ed4c75af0517e7';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version;
# Wed, 11 Oct 2023 22:56:39 GMT
ARG CABAL_INSTALL=3.8.1.0
# Wed, 11 Oct 2023 22:56:39 GMT
ARG CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C
# Wed, 11 Oct 2023 22:56:41 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb10.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c7fa9029f2f829432dd9dcf764e58605fbb7431db79234feb3e46684a9b37214';             ;;         'x86_64')             CABAL_INSTALL_SHA256='c71a1a46fd42d235bb86be968660815c24950e5da2d1ff4640da025ab520424b';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version
# Wed, 11 Oct 2023 22:56:42 GMT
ARG GHC=9.6.3
# Wed, 11 Oct 2023 22:56:42 GMT
ARG GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB
# Wed, 11 Oct 2023 22:58:14 GMT
# ARGS: CABAL_INSTALL=3.8.1.0 CABAL_INSTALL_RELEASE_KEY=E9EC5616017C3EE26B33468CCE1ED8AE0B011D8C GHC=9.6.3 GHC_RELEASE_KEY=33C3A599DB85EA9B8BAA1866B202264020068BFB STACK=2.11.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb10-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='03c389859319f09452081310fc13af7525063ea8930830ef76be2a14b312271e';             ;;         'x86_64')             GHC_SHA256='9ba0458c84efdbba69509c3c57497e22ad03743f816eb9c8b024abc13f7aacaa';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;     find "/opt/ghc/$GHC/" \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version
# Wed, 11 Oct 2023 22:58:24 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.6.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 22:58:25 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:466d0c81a91b4dea612f4d4bcbd480b8ee299558a2d50e93104c98a012e7975e`  
		Last Modified: Wed, 11 Oct 2023 18:29:47 GMT  
		Size: 26.0 MB (25967816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d69d78315d2f6e5c6ef6165d462362a14ced4f3f3a8ad726295460c75441426`  
		Last Modified: Wed, 11 Oct 2023 23:10:02 GMT  
		Size: 88.1 MB (88053657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abded56f07ca7ef82fea74a56a88ecad5c99fc0070f5fc9bb1933f39e1f01cd8`  
		Last Modified: Wed, 11 Oct 2023 23:09:52 GMT  
		Size: 17.2 MB (17230060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d869dfc3085940cb64260e2b8890d10d500fc98b7c9d7f142c24b562e9bbe56f`  
		Last Modified: Wed, 11 Oct 2023 23:09:52 GMT  
		Size: 12.4 MB (12373177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8fafdd1d75fb43326718e68eef5e397c8e3bf4b8713af3aec81320bcaa8807`  
		Last Modified: Wed, 11 Oct 2023 23:10:33 GMT  
		Size: 290.1 MB (290072424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
