## `haskell:9-slim-bullseye`

```console
$ docker pull haskell@sha256:323f93d1ac614ad94416019d1c81cf0a5b70ad0ecdd523119588357a535651ed
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-slim-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:5a2fbb57276d0909430280bd20aa6641d0babe15adfe46d099eed4549acca500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.3 MB (604288957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb37c8f4823bcb0711aabedee2a72120ab5269d7af4f22cdb8ce220d6fbc582`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 18 Dec 2024 07:09:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
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
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3777c42b2fdf15ce40369958cfeeef1ca331257ef1942ac764fae187846a22`  
		Last Modified: Mon, 17 Mar 2025 23:15:38 GMT  
		Size: 106.2 MB (106163060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f59aaa0d34f6b75f30464951fbbbac9c400b56093e57a03520d13c48fa41538`  
		Last Modified: Mon, 17 Mar 2025 23:15:37 GMT  
		Size: 21.6 MB (21635304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edfc0adecc78a61e0c2c3e14d9d46381256ceac380f6e61b9964b97f1366e325`  
		Last Modified: Mon, 17 Mar 2025 23:15:37 GMT  
		Size: 7.2 MB (7181375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9142b07e781ae318be23ec37fd0333717db6f1b9a0a6867350c08d9d0b2136f0`  
		Last Modified: Mon, 17 Mar 2025 23:15:45 GMT  
		Size: 439.1 MB (439055382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:f6de760664b41996a9a45293d161b8ef965b065e1cdda87c0796e153491b809b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6592444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5705818aa9a8f67e9325221e24c27b3b3c801e7cb45167d58eff36dad7d700`

```dockerfile
```

-	Layers:
	-	`sha256:68620ae6ae7f50dc39a3dc2406d4559973c32e8165bb3b17dedeed92ede79d12`  
		Last Modified: Mon, 17 Mar 2025 23:15:37 GMT  
		Size: 6.6 MB (6566140 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32eed7c08a3c42883306b98410d4f457b5050f9d4655b94bb033bde090b2cadf`  
		Last Modified: Mon, 17 Mar 2025 23:15:37 GMT  
		Size: 26.3 KB (26304 bytes)  
		MIME: application/vnd.in-toto+json

### `haskell:9-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull haskell@sha256:a24328862d8716e1cb9c418770e14f8c1aec715b14ee2528d0aac94a8c11534e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **614.5 MB (614507530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e462a60e0202c3ac9e9c30b7215c3b4ab81a778ceb2fa94c9f6119426f0686ae`
-	Default Command: `["ghci"]`

```dockerfile
# Wed, 18 Dec 2024 07:09:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ec20109db6cd142be5101f424ddad9454e518a16d56c1c66e524d5237c7547`  
		Last Modified: Tue, 25 Feb 2025 02:33:12 GMT  
		Size: 101.7 MB (101659347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6961e8982a63559f7994dc88dcede523f2cc98f49f1ef237cddee9e5e9db70c5`  
		Last Modified: Tue, 25 Feb 2025 02:33:11 GMT  
		Size: 23.9 MB (23858438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4841a798cbd62c22efbc5ebeb9f252528652288ebb21d4fc12601b361bacbf74`  
		Last Modified: Tue, 25 Feb 2025 02:33:09 GMT  
		Size: 13.8 MB (13762115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdc188463256273413ba93e59afeda9e37e5a65f251d907b9e96ab45f95b33e`  
		Last Modified: Tue, 25 Feb 2025 02:33:19 GMT  
		Size: 446.5 MB (446481643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-slim-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:799188a093f1eee749f7acbc155d91ed178f01229a575d81e1f74a6bf40a736b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6595442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:165e226d1e479bb5b3e84c2e57350557df3eb8540b4e5b64c6ca813ba6406296`

```dockerfile
```

-	Layers:
	-	`sha256:2449eaeeb2eb992c831b68c1ba9004c87c3cdeebb1cf6ee4d5e964ea1ee6433e`  
		Last Modified: Tue, 25 Feb 2025 02:33:09 GMT  
		Size: 6.6 MB (6568963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:577922511996936690c64f29e4cf96bd498f2ea01a36bc30dcb45ffc2a3ec0ed`  
		Last Modified: Tue, 25 Feb 2025 02:33:09 GMT  
		Size: 26.5 KB (26479 bytes)  
		MIME: application/vnd.in-toto+json
