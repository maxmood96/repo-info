<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:8`](#haskell8)
-	[`haskell:8-buster`](#haskell8-buster)
-	[`haskell:8-stretch`](#haskell8-stretch)
-	[`haskell:8.10`](#haskell810)
-	[`haskell:8.10-buster`](#haskell810-buster)
-	[`haskell:8.10-stretch`](#haskell810-stretch)
-	[`haskell:8.10.7`](#haskell8107)
-	[`haskell:8.10.7-buster`](#haskell8107-buster)
-	[`haskell:8.10.7-stretch`](#haskell8107-stretch)
-	[`haskell:9`](#haskell9)
-	[`haskell:9-buster`](#haskell9-buster)
-	[`haskell:9-stretch`](#haskell9-stretch)
-	[`haskell:9.0`](#haskell90)
-	[`haskell:9.0-buster`](#haskell90-buster)
-	[`haskell:9.0-stretch`](#haskell90-stretch)
-	[`haskell:9.0.1`](#haskell901)
-	[`haskell:9.0.1-buster`](#haskell901-buster)
-	[`haskell:9.0.1-stretch`](#haskell901-stretch)
-	[`haskell:buster`](#haskellbuster)
-	[`haskell:latest`](#haskelllatest)
-	[`haskell:stretch`](#haskellstretch)

## `haskell:8`

```console
$ docker pull haskell@sha256:23a6ea47691a1987942597e73d1c71358de01bac91b5b1e5a993b4647a3b00d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8` - linux; amd64

```console
$ docker pull haskell@sha256:f2e9f7baab27cd125a6a545fce515b7d8324e0e00037cde5404838dadcfb1a19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.7 MB (409675846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad8f24e3fc9bede6b1474e29231a94050ae71b3256ebec39ed20eb99f0011ef`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:18:54 GMT
ARG GHC=8.10.7
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
# Thu, 07 Oct 2021 22:20:15 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 588764FBE22D19C4 --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:20:29 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:20:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151af84d1987a730fd7e453f1680c1a1eee6f0dcc6cc0ad88fb59d1fd29ae4f4`  
		Last Modified: Thu, 07 Oct 2021 22:32:20 GMT  
		Size: 214.5 MB (214534774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f43b9a5c404b33db104a2a96febce09803661c5e439d811c19cfc4922f38104`  
		Last Modified: Thu, 07 Oct 2021 22:31:40 GMT  
		Size: 17.9 MB (17901263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-buster`

```console
$ docker pull haskell@sha256:23a6ea47691a1987942597e73d1c71358de01bac91b5b1e5a993b4647a3b00d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:f2e9f7baab27cd125a6a545fce515b7d8324e0e00037cde5404838dadcfb1a19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.7 MB (409675846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad8f24e3fc9bede6b1474e29231a94050ae71b3256ebec39ed20eb99f0011ef`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:18:54 GMT
ARG GHC=8.10.7
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
# Thu, 07 Oct 2021 22:20:15 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 588764FBE22D19C4 --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:20:29 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:20:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151af84d1987a730fd7e453f1680c1a1eee6f0dcc6cc0ad88fb59d1fd29ae4f4`  
		Last Modified: Thu, 07 Oct 2021 22:32:20 GMT  
		Size: 214.5 MB (214534774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f43b9a5c404b33db104a2a96febce09803661c5e439d811c19cfc4922f38104`  
		Last Modified: Thu, 07 Oct 2021 22:31:40 GMT  
		Size: 17.9 MB (17901263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-stretch`

```console
$ docker pull haskell@sha256:8a4035bc06440fd2cc34471f37d02f3e395bbcc4e7d6c64fa6cb49a852e6661e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:e24b1fcc2f8b9c9f5a596aef4caede2242d3065fd47e2def51141b9a4c37191c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379724202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f630cea36f75d0ff631be2bd6e7e64932c3afe6a7a6a17e55802c4481d51f51`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:17:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:17:30 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:20:35 GMT
ARG GHC=8.10.7
# Thu, 07 Oct 2021 22:20:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 07 Oct 2021 22:20:35 GMT
ARG GHC_RELEASE_SHA256=CED9870EA351AF64FB48274B81A664CDB6A9266775F1598A79CBB6FDD5770A23
# Thu, 07 Oct 2021 22:21:44 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=CED9870EA351AF64FB48274B81A664CDB6A9266775F1598A79CBB6FDD5770A23
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 588764FBE22D19C4 --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:21:48 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:21:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:21:48 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:21:57 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=CED9870EA351AF64FB48274B81A664CDB6A9266775F1598A79CBB6FDD5770A23 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:21:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:21:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297dd1ce1133542b9eca73f903c96abe7e387481fe266cc10c66326bb44042e1`  
		Last Modified: Thu, 07 Oct 2021 22:30:56 GMT  
		Size: 97.4 MB (97444753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5ebe044929da629f395ac3d5643bcb7beb2c58f2def117f9a5df6753e83178`  
		Last Modified: Thu, 07 Oct 2021 22:30:41 GMT  
		Size: 9.8 MB (9816048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b48ba0d8a8cf35da8f7b8dd3f378d5e1ebbc21d159d911973076129dc676d2`  
		Last Modified: Thu, 07 Oct 2021 22:33:21 GMT  
		Size: 209.2 MB (209182522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26d60349a189af61f2f4097e033ddec413e4c9e2110b6f7df1a0f217d99ee60`  
		Last Modified: Thu, 07 Oct 2021 22:32:43 GMT  
		Size: 17.9 MB (17901225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10`

```console
$ docker pull haskell@sha256:23a6ea47691a1987942597e73d1c71358de01bac91b5b1e5a993b4647a3b00d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10` - linux; amd64

```console
$ docker pull haskell@sha256:f2e9f7baab27cd125a6a545fce515b7d8324e0e00037cde5404838dadcfb1a19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.7 MB (409675846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad8f24e3fc9bede6b1474e29231a94050ae71b3256ebec39ed20eb99f0011ef`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:18:54 GMT
ARG GHC=8.10.7
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
# Thu, 07 Oct 2021 22:20:15 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 588764FBE22D19C4 --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:20:29 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:20:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151af84d1987a730fd7e453f1680c1a1eee6f0dcc6cc0ad88fb59d1fd29ae4f4`  
		Last Modified: Thu, 07 Oct 2021 22:32:20 GMT  
		Size: 214.5 MB (214534774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f43b9a5c404b33db104a2a96febce09803661c5e439d811c19cfc4922f38104`  
		Last Modified: Thu, 07 Oct 2021 22:31:40 GMT  
		Size: 17.9 MB (17901263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-buster`

```console
$ docker pull haskell@sha256:23a6ea47691a1987942597e73d1c71358de01bac91b5b1e5a993b4647a3b00d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10-buster` - linux; amd64

```console
$ docker pull haskell@sha256:f2e9f7baab27cd125a6a545fce515b7d8324e0e00037cde5404838dadcfb1a19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.7 MB (409675846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad8f24e3fc9bede6b1474e29231a94050ae71b3256ebec39ed20eb99f0011ef`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:18:54 GMT
ARG GHC=8.10.7
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
# Thu, 07 Oct 2021 22:20:15 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 588764FBE22D19C4 --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:20:29 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:20:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151af84d1987a730fd7e453f1680c1a1eee6f0dcc6cc0ad88fb59d1fd29ae4f4`  
		Last Modified: Thu, 07 Oct 2021 22:32:20 GMT  
		Size: 214.5 MB (214534774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f43b9a5c404b33db104a2a96febce09803661c5e439d811c19cfc4922f38104`  
		Last Modified: Thu, 07 Oct 2021 22:31:40 GMT  
		Size: 17.9 MB (17901263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-stretch`

```console
$ docker pull haskell@sha256:8a4035bc06440fd2cc34471f37d02f3e395bbcc4e7d6c64fa6cb49a852e6661e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:e24b1fcc2f8b9c9f5a596aef4caede2242d3065fd47e2def51141b9a4c37191c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379724202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f630cea36f75d0ff631be2bd6e7e64932c3afe6a7a6a17e55802c4481d51f51`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:17:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:17:30 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:20:35 GMT
ARG GHC=8.10.7
# Thu, 07 Oct 2021 22:20:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 07 Oct 2021 22:20:35 GMT
ARG GHC_RELEASE_SHA256=CED9870EA351AF64FB48274B81A664CDB6A9266775F1598A79CBB6FDD5770A23
# Thu, 07 Oct 2021 22:21:44 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=CED9870EA351AF64FB48274B81A664CDB6A9266775F1598A79CBB6FDD5770A23
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 588764FBE22D19C4 --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:21:48 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:21:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:21:48 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:21:57 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=CED9870EA351AF64FB48274B81A664CDB6A9266775F1598A79CBB6FDD5770A23 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:21:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:21:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297dd1ce1133542b9eca73f903c96abe7e387481fe266cc10c66326bb44042e1`  
		Last Modified: Thu, 07 Oct 2021 22:30:56 GMT  
		Size: 97.4 MB (97444753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5ebe044929da629f395ac3d5643bcb7beb2c58f2def117f9a5df6753e83178`  
		Last Modified: Thu, 07 Oct 2021 22:30:41 GMT  
		Size: 9.8 MB (9816048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b48ba0d8a8cf35da8f7b8dd3f378d5e1ebbc21d159d911973076129dc676d2`  
		Last Modified: Thu, 07 Oct 2021 22:33:21 GMT  
		Size: 209.2 MB (209182522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26d60349a189af61f2f4097e033ddec413e4c9e2110b6f7df1a0f217d99ee60`  
		Last Modified: Thu, 07 Oct 2021 22:32:43 GMT  
		Size: 17.9 MB (17901225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7`

```console
$ docker pull haskell@sha256:23a6ea47691a1987942597e73d1c71358de01bac91b5b1e5a993b4647a3b00d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10.7` - linux; amd64

```console
$ docker pull haskell@sha256:f2e9f7baab27cd125a6a545fce515b7d8324e0e00037cde5404838dadcfb1a19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.7 MB (409675846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad8f24e3fc9bede6b1474e29231a94050ae71b3256ebec39ed20eb99f0011ef`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:18:54 GMT
ARG GHC=8.10.7
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
# Thu, 07 Oct 2021 22:20:15 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 588764FBE22D19C4 --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:20:29 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:20:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151af84d1987a730fd7e453f1680c1a1eee6f0dcc6cc0ad88fb59d1fd29ae4f4`  
		Last Modified: Thu, 07 Oct 2021 22:32:20 GMT  
		Size: 214.5 MB (214534774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f43b9a5c404b33db104a2a96febce09803661c5e439d811c19cfc4922f38104`  
		Last Modified: Thu, 07 Oct 2021 22:31:40 GMT  
		Size: 17.9 MB (17901263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7-buster`

```console
$ docker pull haskell@sha256:23a6ea47691a1987942597e73d1c71358de01bac91b5b1e5a993b4647a3b00d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10.7-buster` - linux; amd64

```console
$ docker pull haskell@sha256:f2e9f7baab27cd125a6a545fce515b7d8324e0e00037cde5404838dadcfb1a19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.7 MB (409675846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad8f24e3fc9bede6b1474e29231a94050ae71b3256ebec39ed20eb99f0011ef`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:18:54 GMT
ARG GHC=8.10.7
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 07 Oct 2021 22:18:55 GMT
ARG GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
# Thu, 07 Oct 2021 22:20:15 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 588764FBE22D19C4 --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:20:19 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:20:29 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=A13719BCA87A0D3AC0C7D4157A4E60887009A7F1A8DBE95C4759EC413E086D30 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:20:29 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:20:30 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151af84d1987a730fd7e453f1680c1a1eee6f0dcc6cc0ad88fb59d1fd29ae4f4`  
		Last Modified: Thu, 07 Oct 2021 22:32:20 GMT  
		Size: 214.5 MB (214534774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f43b9a5c404b33db104a2a96febce09803661c5e439d811c19cfc4922f38104`  
		Last Modified: Thu, 07 Oct 2021 22:31:40 GMT  
		Size: 17.9 MB (17901263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.7-stretch`

```console
$ docker pull haskell@sha256:8a4035bc06440fd2cc34471f37d02f3e395bbcc4e7d6c64fa6cb49a852e6661e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10.7-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:e24b1fcc2f8b9c9f5a596aef4caede2242d3065fd47e2def51141b9a4c37191c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.7 MB (379724202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f630cea36f75d0ff631be2bd6e7e64932c3afe6a7a6a17e55802c4481d51f51`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:17:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:17:30 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:20:35 GMT
ARG GHC=8.10.7
# Thu, 07 Oct 2021 22:20:35 GMT
ARG GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4
# Thu, 07 Oct 2021 22:20:35 GMT
ARG GHC_RELEASE_SHA256=CED9870EA351AF64FB48274B81A664CDB6A9266775F1598A79CBB6FDD5770A23
# Thu, 07 Oct 2021 22:21:44 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=CED9870EA351AF64FB48274B81A664CDB6A9266775F1598A79CBB6FDD5770A23
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 588764FBE22D19C4 --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:21:48 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:21:48 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:21:48 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:21:57 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=8.10.7 GHC_RELEASE_KEY=88B57FCF7DB53B4DB3BFA4B1588764FBE22D19C4 GHC_RELEASE_SHA256=CED9870EA351AF64FB48274B81A664CDB6A9266775F1598A79CBB6FDD5770A23 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:21:57 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/8.10.7/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:21:57 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297dd1ce1133542b9eca73f903c96abe7e387481fe266cc10c66326bb44042e1`  
		Last Modified: Thu, 07 Oct 2021 22:30:56 GMT  
		Size: 97.4 MB (97444753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5ebe044929da629f395ac3d5643bcb7beb2c58f2def117f9a5df6753e83178`  
		Last Modified: Thu, 07 Oct 2021 22:30:41 GMT  
		Size: 9.8 MB (9816048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b48ba0d8a8cf35da8f7b8dd3f378d5e1ebbc21d159d911973076129dc676d2`  
		Last Modified: Thu, 07 Oct 2021 22:33:21 GMT  
		Size: 209.2 MB (209182522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26d60349a189af61f2f4097e033ddec413e4c9e2110b6f7df1a0f217d99ee60`  
		Last Modified: Thu, 07 Oct 2021 22:32:43 GMT  
		Size: 17.9 MB (17901225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9`

```console
$ docker pull haskell@sha256:5111a76f526cba0aebfced297906d4d2fdd212460e6cc684d095395d87aaeb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:04aea55b0d6673bfd424046a7ac7e257f065e0994f6ac11e9e4acb6a24ab63ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403286424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0951ada49f823da16cd8656194c3de640a62254efaa610575399308a35e0bb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:15:21 GMT
ARG GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
# Thu, 07 Oct 2021 22:16:33 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:16:48 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:16:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:16:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc823d0e4456ebb1313581b9e813780539baeecb1a833ed9f43ff87221a0fa1`  
		Last Modified: Thu, 07 Oct 2021 22:30:13 GMT  
		Size: 208.1 MB (208145346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8874f4439517d0ae240e42350fbde35359ba7b7ab68ce3927c53403f90b8d27`  
		Last Modified: Thu, 07 Oct 2021 22:29:32 GMT  
		Size: 17.9 MB (17901269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-buster`

```console
$ docker pull haskell@sha256:5111a76f526cba0aebfced297906d4d2fdd212460e6cc684d095395d87aaeb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9-buster` - linux; amd64

```console
$ docker pull haskell@sha256:04aea55b0d6673bfd424046a7ac7e257f065e0994f6ac11e9e4acb6a24ab63ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403286424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0951ada49f823da16cd8656194c3de640a62254efaa610575399308a35e0bb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:15:21 GMT
ARG GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
# Thu, 07 Oct 2021 22:16:33 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:16:48 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:16:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:16:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc823d0e4456ebb1313581b9e813780539baeecb1a833ed9f43ff87221a0fa1`  
		Last Modified: Thu, 07 Oct 2021 22:30:13 GMT  
		Size: 208.1 MB (208145346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8874f4439517d0ae240e42350fbde35359ba7b7ab68ce3927c53403f90b8d27`  
		Last Modified: Thu, 07 Oct 2021 22:29:32 GMT  
		Size: 17.9 MB (17901269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-stretch`

```console
$ docker pull haskell@sha256:5cc255ed1b36aacb7b9a4e3a2890108ed94faef89db981f32bffa911ae6b7208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:f527704397e29c28ad8746a1b39bf3950ceecfb34f9704ef32f4699a73ac1dbb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374107276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4221ee5fbef08a536f6edd4f7cd7863a894baa6e49cc89138ab027f8e871e0`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:17:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:17:30 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:17:30 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:17:31 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:17:31 GMT
ARG GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5
# Thu, 07 Oct 2021 22:18:34 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:18:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:18:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:18:39 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:18:50 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:18:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:18:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297dd1ce1133542b9eca73f903c96abe7e387481fe266cc10c66326bb44042e1`  
		Last Modified: Thu, 07 Oct 2021 22:30:56 GMT  
		Size: 97.4 MB (97444753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5ebe044929da629f395ac3d5643bcb7beb2c58f2def117f9a5df6753e83178`  
		Last Modified: Thu, 07 Oct 2021 22:30:41 GMT  
		Size: 9.8 MB (9816048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae54b6e905a47915c7058ccda98f80db58f6894b54d66a99fc3b97e96062026`  
		Last Modified: Thu, 07 Oct 2021 22:31:22 GMT  
		Size: 203.6 MB (203565573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ef50c8c02fb343040f88b16506ca758420d71a132253240296f5993deaba4e`  
		Last Modified: Thu, 07 Oct 2021 22:30:42 GMT  
		Size: 17.9 MB (17901248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0`

```console
$ docker pull haskell@sha256:5111a76f526cba0aebfced297906d4d2fdd212460e6cc684d095395d87aaeb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0` - linux; amd64

```console
$ docker pull haskell@sha256:04aea55b0d6673bfd424046a7ac7e257f065e0994f6ac11e9e4acb6a24ab63ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403286424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0951ada49f823da16cd8656194c3de640a62254efaa610575399308a35e0bb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:15:21 GMT
ARG GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
# Thu, 07 Oct 2021 22:16:33 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:16:48 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:16:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:16:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc823d0e4456ebb1313581b9e813780539baeecb1a833ed9f43ff87221a0fa1`  
		Last Modified: Thu, 07 Oct 2021 22:30:13 GMT  
		Size: 208.1 MB (208145346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8874f4439517d0ae240e42350fbde35359ba7b7ab68ce3927c53403f90b8d27`  
		Last Modified: Thu, 07 Oct 2021 22:29:32 GMT  
		Size: 17.9 MB (17901269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-buster`

```console
$ docker pull haskell@sha256:5111a76f526cba0aebfced297906d4d2fdd212460e6cc684d095395d87aaeb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0-buster` - linux; amd64

```console
$ docker pull haskell@sha256:04aea55b0d6673bfd424046a7ac7e257f065e0994f6ac11e9e4acb6a24ab63ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403286424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0951ada49f823da16cd8656194c3de640a62254efaa610575399308a35e0bb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:15:21 GMT
ARG GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
# Thu, 07 Oct 2021 22:16:33 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:16:48 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:16:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:16:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc823d0e4456ebb1313581b9e813780539baeecb1a833ed9f43ff87221a0fa1`  
		Last Modified: Thu, 07 Oct 2021 22:30:13 GMT  
		Size: 208.1 MB (208145346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8874f4439517d0ae240e42350fbde35359ba7b7ab68ce3927c53403f90b8d27`  
		Last Modified: Thu, 07 Oct 2021 22:29:32 GMT  
		Size: 17.9 MB (17901269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-stretch`

```console
$ docker pull haskell@sha256:5cc255ed1b36aacb7b9a4e3a2890108ed94faef89db981f32bffa911ae6b7208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:f527704397e29c28ad8746a1b39bf3950ceecfb34f9704ef32f4699a73ac1dbb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374107276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4221ee5fbef08a536f6edd4f7cd7863a894baa6e49cc89138ab027f8e871e0`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:17:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:17:30 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:17:30 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:17:31 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:17:31 GMT
ARG GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5
# Thu, 07 Oct 2021 22:18:34 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:18:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:18:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:18:39 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:18:50 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:18:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:18:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297dd1ce1133542b9eca73f903c96abe7e387481fe266cc10c66326bb44042e1`  
		Last Modified: Thu, 07 Oct 2021 22:30:56 GMT  
		Size: 97.4 MB (97444753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5ebe044929da629f395ac3d5643bcb7beb2c58f2def117f9a5df6753e83178`  
		Last Modified: Thu, 07 Oct 2021 22:30:41 GMT  
		Size: 9.8 MB (9816048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae54b6e905a47915c7058ccda98f80db58f6894b54d66a99fc3b97e96062026`  
		Last Modified: Thu, 07 Oct 2021 22:31:22 GMT  
		Size: 203.6 MB (203565573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ef50c8c02fb343040f88b16506ca758420d71a132253240296f5993deaba4e`  
		Last Modified: Thu, 07 Oct 2021 22:30:42 GMT  
		Size: 17.9 MB (17901248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.1`

```console
$ docker pull haskell@sha256:5111a76f526cba0aebfced297906d4d2fdd212460e6cc684d095395d87aaeb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0.1` - linux; amd64

```console
$ docker pull haskell@sha256:04aea55b0d6673bfd424046a7ac7e257f065e0994f6ac11e9e4acb6a24ab63ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403286424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0951ada49f823da16cd8656194c3de640a62254efaa610575399308a35e0bb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:15:21 GMT
ARG GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
# Thu, 07 Oct 2021 22:16:33 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:16:48 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:16:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:16:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc823d0e4456ebb1313581b9e813780539baeecb1a833ed9f43ff87221a0fa1`  
		Last Modified: Thu, 07 Oct 2021 22:30:13 GMT  
		Size: 208.1 MB (208145346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8874f4439517d0ae240e42350fbde35359ba7b7ab68ce3927c53403f90b8d27`  
		Last Modified: Thu, 07 Oct 2021 22:29:32 GMT  
		Size: 17.9 MB (17901269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.1-buster`

```console
$ docker pull haskell@sha256:5111a76f526cba0aebfced297906d4d2fdd212460e6cc684d095395d87aaeb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0.1-buster` - linux; amd64

```console
$ docker pull haskell@sha256:04aea55b0d6673bfd424046a7ac7e257f065e0994f6ac11e9e4acb6a24ab63ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403286424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0951ada49f823da16cd8656194c3de640a62254efaa610575399308a35e0bb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:15:21 GMT
ARG GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
# Thu, 07 Oct 2021 22:16:33 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:16:48 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:16:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:16:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc823d0e4456ebb1313581b9e813780539baeecb1a833ed9f43ff87221a0fa1`  
		Last Modified: Thu, 07 Oct 2021 22:30:13 GMT  
		Size: 208.1 MB (208145346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8874f4439517d0ae240e42350fbde35359ba7b7ab68ce3927c53403f90b8d27`  
		Last Modified: Thu, 07 Oct 2021 22:29:32 GMT  
		Size: 17.9 MB (17901269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.1-stretch`

```console
$ docker pull haskell@sha256:5cc255ed1b36aacb7b9a4e3a2890108ed94faef89db981f32bffa911ae6b7208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0.1-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:f527704397e29c28ad8746a1b39bf3950ceecfb34f9704ef32f4699a73ac1dbb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374107276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4221ee5fbef08a536f6edd4f7cd7863a894baa6e49cc89138ab027f8e871e0`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:17:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:17:30 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:17:30 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:17:31 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:17:31 GMT
ARG GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5
# Thu, 07 Oct 2021 22:18:34 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:18:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:18:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:18:39 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:18:50 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:18:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:18:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297dd1ce1133542b9eca73f903c96abe7e387481fe266cc10c66326bb44042e1`  
		Last Modified: Thu, 07 Oct 2021 22:30:56 GMT  
		Size: 97.4 MB (97444753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5ebe044929da629f395ac3d5643bcb7beb2c58f2def117f9a5df6753e83178`  
		Last Modified: Thu, 07 Oct 2021 22:30:41 GMT  
		Size: 9.8 MB (9816048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae54b6e905a47915c7058ccda98f80db58f6894b54d66a99fc3b97e96062026`  
		Last Modified: Thu, 07 Oct 2021 22:31:22 GMT  
		Size: 203.6 MB (203565573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ef50c8c02fb343040f88b16506ca758420d71a132253240296f5993deaba4e`  
		Last Modified: Thu, 07 Oct 2021 22:30:42 GMT  
		Size: 17.9 MB (17901248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:buster`

```console
$ docker pull haskell@sha256:5111a76f526cba0aebfced297906d4d2fdd212460e6cc684d095395d87aaeb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:buster` - linux; amd64

```console
$ docker pull haskell@sha256:04aea55b0d6673bfd424046a7ac7e257f065e0994f6ac11e9e4acb6a24ab63ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403286424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0951ada49f823da16cd8656194c3de640a62254efaa610575399308a35e0bb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:15:21 GMT
ARG GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
# Thu, 07 Oct 2021 22:16:33 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:16:48 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:16:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:16:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc823d0e4456ebb1313581b9e813780539baeecb1a833ed9f43ff87221a0fa1`  
		Last Modified: Thu, 07 Oct 2021 22:30:13 GMT  
		Size: 208.1 MB (208145346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8874f4439517d0ae240e42350fbde35359ba7b7ab68ce3927c53403f90b8d27`  
		Last Modified: Thu, 07 Oct 2021 22:29:32 GMT  
		Size: 17.9 MB (17901269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:5111a76f526cba0aebfced297906d4d2fdd212460e6cc684d095395d87aaeb06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:04aea55b0d6673bfd424046a7ac7e257f065e0994f6ac11e9e4acb6a24ab63ca
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403286424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0951ada49f823da16cd8656194c3de640a62254efaa610575399308a35e0bb`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:15:09 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:15:10 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:15:11 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:15:20 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:15:20 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:15:21 GMT
ARG GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
# Thu, 07 Oct 2021 22:16:33 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb10-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:16:38 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:16:48 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=C253E7EB62CC9DA6524C491C85EC8D3727C2CA6035A8653388E636AAA30A2A0F STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:16:49 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:16:49 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a47331340e8310fb5a041a9e2bfe9fa29c876e9b3e13445d38ff241f7bea23`  
		Last Modified: Thu, 07 Oct 2021 22:29:48 GMT  
		Size: 117.0 MB (116987574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c3c7b7f496779fc88f78c67ce6f4027e020e7d27b7f741ce4a704d01ff6ce3`  
		Last Modified: Thu, 07 Oct 2021 22:29:31 GMT  
		Size: 9.8 MB (9816026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbc823d0e4456ebb1313581b9e813780539baeecb1a833ed9f43ff87221a0fa1`  
		Last Modified: Thu, 07 Oct 2021 22:30:13 GMT  
		Size: 208.1 MB (208145346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8874f4439517d0ae240e42350fbde35359ba7b7ab68ce3927c53403f90b8d27`  
		Last Modified: Thu, 07 Oct 2021 22:29:32 GMT  
		Size: 17.9 MB (17901269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:stretch`

```console
$ docker pull haskell@sha256:5cc255ed1b36aacb7b9a4e3a2890108ed94faef89db981f32bffa911ae6b7208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:stretch` - linux; amd64

```console
$ docker pull haskell@sha256:f527704397e29c28ad8746a1b39bf3950ceecfb34f9704ef32f4699a73ac1dbb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.1 MB (374107276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4221ee5fbef08a536f6edd4f7cd7863a894baa6e49cc89138ab027f8e871e0`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Thu, 07 Oct 2021 22:17:20 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         git         gcc         gnupg         g++         libc6-dev         libffi-dev         libgmp-dev         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL=3.6.0.0
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210
# Thu, 07 Oct 2021 22:17:21 GMT
ARG CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
# Thu, 07 Oct 2021 22:17:30 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${CABAL_INSTALL_RELEASE_KEY} &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS &&     curl -fSLO https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/SHA256SUMS.sig &&     gpg --batch --trusted-key B3D9F94B8DCAE210 --verify SHA256SUMS.sig SHA256SUMS &&     curl -fSL https://downloads.haskell.org/~cabal/cabal-install-$CABAL_INSTALL/cabal-install-$CABAL_INSTALL-x86_64-linux.tar.xz -o cabal-install.tar.gz &&     echo "$CABAL_INSTALL_RELEASE_SHA256 cabal-install.tar.gz" | sha256sum --strict --check &&     tar -xf cabal-install.tar.gz -C /usr/local/bin &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:17:30 GMT
ARG GHC=9.0.1
# Thu, 07 Oct 2021 22:17:31 GMT
ARG GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD
# Thu, 07 Oct 2021 22:17:31 GMT
ARG GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5
# Thu, 07 Oct 2021 22:18:34 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5
RUN cd /tmp &&   export GNUPGHOME="$(mktemp -d)" &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz -o ghc.tar.xz &&   curl -sSL https://downloads.haskell.org/~ghc/$GHC/ghc-$GHC-x86_64-deb9-linux.tar.xz.sig -o ghc.tar.xz.sig &&   gpg --batch --keyserver keyserver.ubuntu.com --receive-keys ${GHC_RELEASE_KEY} &&   gpg --batch --trusted-key 2DE04D4E97DB64AD --verify ghc.tar.xz.sig ghc.tar.xz &&   echo "$GHC_RELEASE_SHA256 ghc.tar.xz" | sha256sum --strict --check &&   tar xf ghc.tar.xz &&   cd ghc-$GHC &&   ./configure --prefix /opt/ghc/$GHC &&   make install &&   find /opt/ghc/$GHC/ \( -name "*_p.a" -o -name "*.p_hi" \) -type f -delete &&   rm -rf /opt/ghc/$GHC/share/ &&   rm -rf "$GNUPGHOME" /tmp/*
# Thu, 07 Oct 2021 22:18:38 GMT
ARG STACK=2.7.3
# Thu, 07 Oct 2021 22:18:38 GMT
ARG STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Thu, 07 Oct 2021 22:18:39 GMT
ARG STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
# Thu, 07 Oct 2021 22:18:50 GMT
# ARGS: CABAL_INSTALL=3.6.0.0 CABAL_INSTALL_RELEASE_KEY=A970DF3AC3B9709706D74544B3D9F94B8DCAE210 CABAL_INSTALL_RELEASE_SHA256=BFCB7350966DAFE95051B5FC9FCB989C5708AB9E78191E71FC04647061668A11 GHC=9.0.1 GHC_RELEASE_KEY=FFEB7CE81E16A36B3E2DED6F2DE04D4E97DB64AD GHC_RELEASE_SHA256=4CA6252492F59FE589029FADCA4B6F922D6A9F0FF39D19A2BD9886FDE4E183D5 STACK=2.7.3 STACK_RELEASE_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_SHA256=A6C090555FA1C64AA61C29AA4449765A51D79E870CF759CDE192937CD614E72B
RUN cd /tmp &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     echo "$STACK_RELEASE_SHA256 stack.tar.gz" | sha256sum --strict --check &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 stack-$STACK-linux-x86_64/stack &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /tmp/*
# Thu, 07 Oct 2021 22:18:50 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 22:18:51 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297dd1ce1133542b9eca73f903c96abe7e387481fe266cc10c66326bb44042e1`  
		Last Modified: Thu, 07 Oct 2021 22:30:56 GMT  
		Size: 97.4 MB (97444753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5ebe044929da629f395ac3d5643bcb7beb2c58f2def117f9a5df6753e83178`  
		Last Modified: Thu, 07 Oct 2021 22:30:41 GMT  
		Size: 9.8 MB (9816048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae54b6e905a47915c7058ccda98f80db58f6894b54d66a99fc3b97e96062026`  
		Last Modified: Thu, 07 Oct 2021 22:31:22 GMT  
		Size: 203.6 MB (203565573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ef50c8c02fb343040f88b16506ca758420d71a132253240296f5993deaba4e`  
		Last Modified: Thu, 07 Oct 2021 22:30:42 GMT  
		Size: 17.9 MB (17901248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
