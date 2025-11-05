## `haskell:9-bullseye`

```console
$ docker pull haskell@sha256:4ffc51ccedd616a59ad63c3b04323ea98cdffe36a6f217fe9a10db9322891d8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `haskell:9-bullseye` - linux; amd64

```console
$ docker pull haskell@sha256:6a36db5b32b02037cb55b3d8dd8bf7b8f5e45ea9eb22182cdb2fb443c1dd105a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.0 MB (658023988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0829b07e2f4dfd063bcbfbbb232657e3b20b54be33de2ae3899f8ad0610360f`
-	Default Command: `["ghci"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:16:59 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 00:16:59 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dpkg-dev         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libnuma-dev         libtinfo-dev         make         netbase         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:16:59 GMT
ARG STACK=3.3.1
# Tue, 04 Nov 2025 00:16:59 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 04 Nov 2025 00:17:01 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     STACK_URL="https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-$ARCH.tar.gz";     case "$ARCH" in         'aarch64')             STACK_SHA256='bdd618ea5a9c921417727011f2ecd78987dffa5cee5e741108baf65a9b5b58ab';             ;;         'x86_64')             STACK_SHA256='88d7e517342c125b0a098d9d578fe53e590618ae4b2427283a27408a1ebd06d8';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$STACK_URL" -o stack.tar.gz;     echo "$STACK_SHA256 stack.tar.gz" | sha256sum --strict --check;         curl -sSL "$STACK_URL.asc" -o stack.tar.gz.asc;     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$STACK_RELEASE_KEY";     gpg --batch --verify stack.tar.gz.asc stack.tar.gz;     gpgconf --kill all;         tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 "stack-$STACK-linux-$ARCH/stack";     stack config set system-ghc --global true;     stack config set install-ghc --global false;         rm -rf /tmp/*;         stack --version; # buildkit
# Tue, 04 Nov 2025 00:17:01 GMT
ARG CABAL_INSTALL=3.12.1.0
# Tue, 04 Nov 2025 00:17:01 GMT
ARG CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
# Tue, 04 Nov 2025 00:17:02 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.12.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     CABAL_INSTALL_TAR="cabal-install-$CABAL_INSTALL-$ARCH-linux-deb11.tar.xz";     CABAL_INSTALL_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/$CABAL_INSTALL_TAR";     CABAL_INSTALL_SHA256SUMS_URL="https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS";     case "$ARCH" in         'aarch64')             CABAL_INSTALL_SHA256='c14e8198407f37f7276c77b5cefef60ee6a929b4c22d7316577ce8e2301a758e';             ;;         'x86_64')             CABAL_INSTALL_SHA256='4f60cf1c72f4ad4d82d668839ac61ae15ae4faf6c4b809395799e8a3ee622051';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'"; exit 1 ;;     esac;     curl -fSL "$CABAL_INSTALL_URL" -o cabal-install.tar.gz;     echo "$CABAL_INSTALL_SHA256 cabal-install.tar.gz" | sha256sum --strict --check;         curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL";     curl -sSLO "$CABAL_INSTALL_SHA256SUMS_URL.sig";     GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$CABAL_INSTALL_RELEASE_KEY";     gpg --batch --verify SHA256SUMS.sig SHA256SUMS;     grep "$CABAL_INSTALL_SHA256  $CABAL_INSTALL_TAR" SHA256SUMS;     gpgconf --kill all;         tar -xf cabal-install.tar.gz -C /usr/local/bin;         rm -rf /tmp/*;         cabal --version # buildkit
# Tue, 04 Nov 2025 00:17:02 GMT
ARG GHC=9.10.2
# Tue, 04 Nov 2025 00:17:02 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Tue, 04 Nov 2025 00:18:48 GMT
# ARGS: STACK=3.3.1 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 CABAL_INSTALL=3.12.1.0 CABAL_INSTALL_RELEASE_KEY=1E07C9A1A3088BAD47F74A3E227EE1942B0BDB95 GHC=9.10.2 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
RUN set -eux;     cd /tmp;     ARCH="$(dpkg-architecture --query DEB_BUILD_GNU_CPU)";     GHC_URL="https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-$ARCH-deb11-linux.tar.xz";     case "$ARCH" in         'aarch64')             GHC_SHA256='0188ca098abdaf71eb0804d0f35311f405da489137d8d438bfaa43b8d1e3f1b0';             ;;         'x86_64')             GHC_SHA256='2fe2c3e0a07e4782530e8bf83eeda8ff6935e40d5450c1809abcdc6182c9c848';             ;;         *) echo >&2 "error: unsupported architecture '$ARCH'" ; exit 1 ;;     esac;     curl -sSL "$GHC_URL" -o ghc.tar.xz;     echo "$GHC_SHA256 ghc.tar.xz" | sha256sum --strict --check;         GNUPGHOME="$(mktemp -d)"; export GNUPGHOME;     curl -sSL "$GHC_URL.sig" -o ghc.tar.xz.sig;     gpg --batch --keyserver keyserver.ubuntu.com --receive-keys "$GHC_RELEASE_KEY";     gpg --batch --verify ghc.tar.xz.sig ghc.tar.xz;     gpgconf --kill all;         tar xf ghc.tar.xz;     cd "ghc-$GHC-$ARCH-unknown-linux";     ./configure --prefix "/opt/ghc/$GHC";     make install;         rm -rf /tmp/*;         "/opt/ghc/$GHC/bin/ghc" --version # buildkit
# Tue, 04 Nov 2025 00:18:48 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.10.2/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:18:48 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8374320bd95b65d1348c5565c8e85ebe467e16d6a706fd824864656d1b57a568`  
		Last Modified: Tue, 04 Nov 2025 13:39:28 GMT  
		Size: 133.7 MB (133737039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd72423f281c6a8707a417175f390d6608e5d05697070ee9b4dcb7ec9da12b3f`  
		Last Modified: Tue, 04 Nov 2025 00:20:29 GMT  
		Size: 22.2 MB (22220761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c9efa2179d6e898851b9282b26de9bd02f1e57ebc697b17e1b3e04772f8a55`  
		Last Modified: Tue, 04 Nov 2025 00:20:28 GMT  
		Size: 7.2 MB (7181380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a2099d2af17f925ea746b21883f9440541e54aba294d83b08f0a4896aad0bc`  
		Last Modified: Tue, 04 Nov 2025 13:39:29 GMT  
		Size: 441.1 MB (441128114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `haskell:9-bullseye` - unknown; unknown

```console
$ docker pull haskell@sha256:0e10a0d220c65e64192e091150b832f1e0a0f9b55d474c6541c005de36a26cba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9425812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2467af9e701a266b9778910ed4d5fd76c4414a0e549eee0b1cb8ae4384dfe5e6`

```dockerfile
```

-	Layers:
	-	`sha256:3ac3a8fb58a5e1148c83c8d99a10ac1d9175737330682d592931414faf9326b0`  
		Last Modified: Tue, 04 Nov 2025 09:48:27 GMT  
		Size: 9.4 MB (9399610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28ca4fda54567ec8f3b997432c8e981298f2298c3c17aac868186423ef6aa694`  
		Last Modified: Tue, 04 Nov 2025 09:48:28 GMT  
		Size: 26.2 KB (26202 bytes)  
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
