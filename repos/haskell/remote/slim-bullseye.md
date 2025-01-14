## `haskell:slim-bullseye`

```console
$ docker pull haskell@sha256:cee59af9d625377acb3c362877f5c63aebf645e07bb562417477263bc24c43ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:160a09eac2b716f46e5f64094ca12419526eb7024061e9311525075a8ecb2b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.3 MB (604289663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c017b49b54445eea507015e179341aadd7f63861cc45b6b64239f6b2d6bdaae`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 18 Dec 2024 07:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Wed, 18 Dec 2024 07:09:49 GMT
ENV LANG=C.UTF-8
# Wed, 18 Dec 2024 07:09:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Dec 2024 07:09:49 GMT
ARG STACK=3.1.1
# Wed, 18 Dec 2024 07:09:49 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 18 Dec 2024 07:09:49 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 18 Dec 2024 07:09:49 GMT
ARG CABAL_INSTALL=3.12.1.0
# Wed, 18 Dec 2024 07:09:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Wed, 18 Dec 2024 07:09:49 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.12.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c14e8198407f37f7276c77b5cefef60ee6a929b4c22d7316577ce8e2301a758e';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4f60cf1c72f4ad4d82d668839ac61ae15ae4faf6c4b809395799e8a3ee622051';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 18 Dec 2024 07:09:49 GMT
ARG GHC=9.10.1
# Wed, 18 Dec 2024 07:09:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 18 Dec 2024 07:09:49 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.12.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 18 Dec 2024 07:09:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Dec 2024 07:09:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:803cbf9f433165d879999b9a53b4744673405bf04a1dfe8738c523fa2c79f42b`  
		Last Modified: Tue, 14 Jan 2025 02:19:14 GMT  
		Size: 106.2 MB (106165581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f3ea5aed6607ad10063139eabe62c9d141aeacd38361ccd6042375af4aa52e`  
		Last Modified: Tue, 14 Jan 2025 02:19:12 GMT  
		Size: 21.6 MB (21635311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b70605383c7ca3ce388fa506c109b8e6b7e960fdea846670210db6ed98acf09`  
		Last Modified: Tue, 14 Jan 2025 02:19:12 GMT  
		Size: 7.2 MB (7181372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8d3cbefa56c4c2bba015e3f68a02f237f3a31c0ac75e6af106c839cd08a4ec`  
		Last Modified: Tue, 14 Jan 2025 02:19:22 GMT  
		Size: 439.1 MB (439054734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:8f7c9fb56a97e3875aff00c75fec00ac14cafb9c7110d8ea48e0dbcd2323cce9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6592444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f77b8c82f42691740b5e45e634b7eb3384f401401fc51465b75495e6f8a682c`

```dockerfile
```

-	Layers:
	-	`sha256:0cb9c9331200e0bac3817a68aefbacfc858d3dd97ea37af1cd83e5ba506b7b42`  
		Last Modified: Tue, 14 Jan 2025 02:19:11 GMT  
		Size: 6.6 MB (6566140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac267863e3169e61fd3c02b67ff4b67c06861e2209e40f93808e0c3eadbb20a9`  
		Last Modified: Tue, 14 Jan 2025 02:19:11 GMT  
		Size: 26.3 KB (26304 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:7b112221fe38830a36ef4d694acff7a7100636e159397d7a6eb954567ecfb5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.5 MB (614502172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1383affbfc51d4214090d1cc8e95be72cbb7722831b890f1f3692470d0323f82`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 18 Dec 2024 07:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Wed, 18 Dec 2024 07:09:49 GMT
ENV LANG=C.UTF-8
# Wed, 18 Dec 2024 07:09:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 18 Dec 2024 07:09:49 GMT
ARG STACK=3.1.1
# Wed, 18 Dec 2024 07:09:49 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Wed, 18 Dec 2024 07:09:49 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='033cb75bad3a5299b522c99e8056915bd081879f5df312e6d44d7511fc567455';             ;;         'x86_64')             STACK_SHA256='d096125ea3d987a55d17f7d4f8599ee2fd96bd2d0f033566e28ddfe248f730f9';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Wed, 18 Dec 2024 07:09:49 GMT
ARG CABAL_INSTALL=3.12.1.0
# Wed, 18 Dec 2024 07:09:49 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Wed, 18 Dec 2024 07:09:49 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.12.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c14e8198407f37f7276c77b5cefef60ee6a929b4c22d7316577ce8e2301a758e';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4f60cf1c72f4ad4d82d668839ac61ae15ae4faf6c4b809395799e8a3ee622051';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Wed, 18 Dec 2024 07:09:49 GMT
ARG GHC=9.10.1
# Wed, 18 Dec 2024 07:09:49 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Wed, 18 Dec 2024 07:09:49 GMT
# ARGS: STACK=3.1.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.12.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.10.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='1db449c445d34779d4deaba22341576f7b512a05b6c2b5cb64f3846d1509714e';             ;;         'x86_64')             GHC_SHA256='78975575b8125ecf1f50f78b1016b14ea6e87abbf1fc39797af469d029c5d737';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Wed, 18 Dec 2024 07:09:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Dec 2024 07:09:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 20:33:33 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c52baea4caf428eee2f956bc5e7bb3fd4eb846c5fc757cc49ff346633f1c0df`  
		Last Modified: Tue, 14 Jan 2025 02:41:43 GMT  
		Size: 101.7 MB (101659074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a2f51c317af655520ba7ce9648ca63fff4734509f6928860856541eff9d951`  
		Last Modified: Tue, 14 Jan 2025 02:41:41 GMT  
		Size: 23.9 MB (23858433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d632750a946e1b9f574e4e02c5aef69e1476335309a99350b737796eed4ed3f6`  
		Last Modified: Tue, 14 Jan 2025 02:41:41 GMT  
		Size: 13.8 MB (13762115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775acefaa4be8cc5ed15c5607c2bc2e91738eec59072fc5f2c897b025d4d0d90`  
		Last Modified: Tue, 14 Jan 2025 02:41:50 GMT  
		Size: 446.5 MB (446477637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:6ba6f1f62981d8ebdc48992f29e884503bbc6aa6068775a4e0f0037ce8da5b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6595442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac79f252fa3cd0b67b1ac73af49b79928bc6f118c928aa973fcfc60c1710637`

```dockerfile
```

-	Layers:
	-	`sha256:ab2f021c043f2b222e8161df2b39307cd2e85196950b253aee68225971a5208f`  
		Last Modified: Tue, 14 Jan 2025 02:41:41 GMT  
		Size: 6.6 MB (6568963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a11031b3332b00cd31177b05ca255405bba45beeb2eb14478b648f574222c87`  
		Last Modified: Tue, 14 Jan 2025 02:41:40 GMT  
		Size: 26.5 KB (26479 bytes)  
		MIME: application/vnd.in-toto+json
