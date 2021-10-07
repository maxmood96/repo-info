<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:8`](#haskell8)
-	[`haskell:8-buster`](#haskell8-buster)
-	[`haskell:8-stretch`](#haskell8-stretch)
-	[`haskell:8.10`](#haskell810)
-	[`haskell:8.10-buster`](#haskell810-buster)
-	[`haskell:8.10-stretch`](#haskell810-stretch)
-	[`haskell:8.10.5`](#haskell8105)
-	[`haskell:8.10.5-buster`](#haskell8105-buster)
-	[`haskell:8.10.5-stretch`](#haskell8105-stretch)
-	[`haskell:8.10.6`](#haskell8106)
-	[`haskell:8.10.6-buster`](#haskell8106-buster)
-	[`haskell:8.10.6-stretch`](#haskell8106-stretch)
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
$ docker pull haskell@sha256:ab8e9f0ef3bb7f82e44133403fe60abeee01df489a4f04e9ed586f584466fa05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8` - linux; amd64

```console
$ docker pull haskell@sha256:30ecdaee0fd59cdcddf004a68c2d8995ba4212a64106abc3e411742c606e59ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361185226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0242c17ded66809ddd76351363ba7258115b3965c6633962199030ec1906848b`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:37:54 GMT
ARG GHC=8.10.4
# Tue, 28 Sep 2021 07:37:55 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:37:55 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:38:29 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:38:32 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:38:32 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:38:33 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:38:41 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:38:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:38:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb7efacc847fbb50e9246c7e1629b36266cb6989a677cd6de2101a64e86a0fd`  
		Last Modified: Tue, 28 Sep 2021 07:42:54 GMT  
		Size: 176.6 MB (176593498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97d81d43b70c08c2b75f1522a10fe51b9d8b2b12d2a61990c914fe1ffe07e8f`  
		Last Modified: Tue, 28 Sep 2021 07:42:21 GMT  
		Size: 18.1 MB (18103440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-buster`

```console
$ docker pull haskell@sha256:ab8e9f0ef3bb7f82e44133403fe60abeee01df489a4f04e9ed586f584466fa05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:30ecdaee0fd59cdcddf004a68c2d8995ba4212a64106abc3e411742c606e59ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361185226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0242c17ded66809ddd76351363ba7258115b3965c6633962199030ec1906848b`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:37:54 GMT
ARG GHC=8.10.4
# Tue, 28 Sep 2021 07:37:55 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:37:55 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:38:29 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:38:32 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:38:32 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:38:33 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:38:41 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:38:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:38:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb7efacc847fbb50e9246c7e1629b36266cb6989a677cd6de2101a64e86a0fd`  
		Last Modified: Tue, 28 Sep 2021 07:42:54 GMT  
		Size: 176.6 MB (176593498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97d81d43b70c08c2b75f1522a10fe51b9d8b2b12d2a61990c914fe1ffe07e8f`  
		Last Modified: Tue, 28 Sep 2021 07:42:21 GMT  
		Size: 18.1 MB (18103440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-stretch`

```console
$ docker pull haskell@sha256:67b7db57014e3f28401e6458974484099b62666656086ff302bea48f524bc563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:d1a6190ae50aa65f56c8083cc5bfad260d01c811c421201effdca18538082aed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340529078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903b07d280b1424e5934315561a6265e24b2579c7d11448e0adfd5665a90522`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:36:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:38:46 GMT
ARG GHC=8.10.4
# Tue, 28 Sep 2021 07:38:47 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:38:47 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:39:20 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:39:22 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:39:22 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:39:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:39:36 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:39:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:39:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db0b40a788b5dc607b1c57159c10d933482a4d6d133f5dbc25b3ec80f8949d`  
		Last Modified: Tue, 28 Sep 2021 07:41:36 GMT  
		Size: 96.5 MB (96506389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cf440a36860abf18a428055e0711adf525c8b2c6d56b3b2aebb6bf529eab81`  
		Last Modified: Tue, 28 Sep 2021 07:43:57 GMT  
		Size: 180.5 MB (180539558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c357171f0a21f09eb46662c3b5a88ac342fd9b83d6dde9fb81e601fa7f88e9`  
		Last Modified: Tue, 28 Sep 2021 07:43:22 GMT  
		Size: 18.1 MB (18103477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10`

```console
$ docker pull haskell@sha256:ab8e9f0ef3bb7f82e44133403fe60abeee01df489a4f04e9ed586f584466fa05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10` - linux; amd64

```console
$ docker pull haskell@sha256:30ecdaee0fd59cdcddf004a68c2d8995ba4212a64106abc3e411742c606e59ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361185226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0242c17ded66809ddd76351363ba7258115b3965c6633962199030ec1906848b`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:37:54 GMT
ARG GHC=8.10.4
# Tue, 28 Sep 2021 07:37:55 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:37:55 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:38:29 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:38:32 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:38:32 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:38:33 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:38:41 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:38:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:38:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb7efacc847fbb50e9246c7e1629b36266cb6989a677cd6de2101a64e86a0fd`  
		Last Modified: Tue, 28 Sep 2021 07:42:54 GMT  
		Size: 176.6 MB (176593498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97d81d43b70c08c2b75f1522a10fe51b9d8b2b12d2a61990c914fe1ffe07e8f`  
		Last Modified: Tue, 28 Sep 2021 07:42:21 GMT  
		Size: 18.1 MB (18103440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-buster`

```console
$ docker pull haskell@sha256:ab8e9f0ef3bb7f82e44133403fe60abeee01df489a4f04e9ed586f584466fa05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10-buster` - linux; amd64

```console
$ docker pull haskell@sha256:30ecdaee0fd59cdcddf004a68c2d8995ba4212a64106abc3e411742c606e59ac
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361185226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0242c17ded66809ddd76351363ba7258115b3965c6633962199030ec1906848b`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:37:54 GMT
ARG GHC=8.10.4
# Tue, 28 Sep 2021 07:37:55 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:37:55 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:38:29 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:38:32 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:38:32 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:38:33 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:38:41 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:38:42 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:38:42 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb7efacc847fbb50e9246c7e1629b36266cb6989a677cd6de2101a64e86a0fd`  
		Last Modified: Tue, 28 Sep 2021 07:42:54 GMT  
		Size: 176.6 MB (176593498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97d81d43b70c08c2b75f1522a10fe51b9d8b2b12d2a61990c914fe1ffe07e8f`  
		Last Modified: Tue, 28 Sep 2021 07:42:21 GMT  
		Size: 18.1 MB (18103440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-stretch`

```console
$ docker pull haskell@sha256:67b7db57014e3f28401e6458974484099b62666656086ff302bea48f524bc563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:d1a6190ae50aa65f56c8083cc5bfad260d01c811c421201effdca18538082aed
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340529078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9903b07d280b1424e5934315561a6265e24b2579c7d11448e0adfd5665a90522`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:36:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:38:46 GMT
ARG GHC=8.10.4
# Tue, 28 Sep 2021 07:38:47 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:38:47 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:39:20 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:39:22 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:39:22 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:39:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:39:36 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:39:37 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:39:37 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db0b40a788b5dc607b1c57159c10d933482a4d6d133f5dbc25b3ec80f8949d`  
		Last Modified: Tue, 28 Sep 2021 07:41:36 GMT  
		Size: 96.5 MB (96506389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3cf440a36860abf18a428055e0711adf525c8b2c6d56b3b2aebb6bf529eab81`  
		Last Modified: Tue, 28 Sep 2021 07:43:57 GMT  
		Size: 180.5 MB (180539558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c357171f0a21f09eb46662c3b5a88ac342fd9b83d6dde9fb81e601fa7f88e9`  
		Last Modified: Tue, 28 Sep 2021 07:43:22 GMT  
		Size: 18.1 MB (18103477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.5`

```console
$ docker pull haskell@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `haskell:8.10.5-buster`

```console
$ docker pull haskell@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `haskell:8.10.5-stretch`

```console
$ docker pull haskell@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `haskell:8.10.6`

```console
$ docker pull haskell@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `haskell:8.10.6-buster`

```console
$ docker pull haskell@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `haskell:8.10.6-stretch`

```console
$ docker pull haskell@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `haskell:8.10.7`

```console
$ docker pull haskell@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `haskell:8.10.7-buster`

```console
$ docker pull haskell@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `haskell:8.10.7-stretch`

```console
$ docker pull haskell@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 0

## `haskell:9`

```console
$ docker pull haskell@sha256:2085d324b5ec3e3026394b1cc7d984e300490deb71d051658307a8a0846fa80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:d368dfa45ee89f0f988038bd357b8f3580fe9fe18198d0a1df6f70181a30e09b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359141497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ca824c31465096e0a20e8f275fee54bde2eb7b467fbcb85c388007a9d70324`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:35:27 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:35:27 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:35:27 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:36:01 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:04 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:36:15 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:36:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:36:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71751d64b5fca23ceede0931e0f893dcadbe61ae4a2c44c5612d9a7da9230ae`  
		Last Modified: Tue, 28 Sep 2021 07:40:51 GMT  
		Size: 174.5 MB (174549730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39c2ae60255e3f29cce22ade2a5dff3d8794a5fe18aaa82bb35aee593d6ad34`  
		Last Modified: Tue, 28 Sep 2021 07:40:16 GMT  
		Size: 18.1 MB (18103479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-buster`

```console
$ docker pull haskell@sha256:2085d324b5ec3e3026394b1cc7d984e300490deb71d051658307a8a0846fa80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9-buster` - linux; amd64

```console
$ docker pull haskell@sha256:d368dfa45ee89f0f988038bd357b8f3580fe9fe18198d0a1df6f70181a30e09b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359141497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ca824c31465096e0a20e8f275fee54bde2eb7b467fbcb85c388007a9d70324`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:35:27 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:35:27 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:35:27 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:36:01 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:04 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:36:15 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:36:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:36:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71751d64b5fca23ceede0931e0f893dcadbe61ae4a2c44c5612d9a7da9230ae`  
		Last Modified: Tue, 28 Sep 2021 07:40:51 GMT  
		Size: 174.5 MB (174549730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39c2ae60255e3f29cce22ade2a5dff3d8794a5fe18aaa82bb35aee593d6ad34`  
		Last Modified: Tue, 28 Sep 2021 07:40:16 GMT  
		Size: 18.1 MB (18103479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-stretch`

```console
$ docker pull haskell@sha256:f61bee43f1034084e6e6fb8b7592322ca035feb8873d23b9b1bed353a39a1acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:c051b8e82558f0be7aa393bb0b63047ae0a081efdff2721ee9172bd379e54517
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338507856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3059e9838d93bb77fcf74f7c1d1491da505cfc404caad2e17d46f4065e8b130`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:36:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:50 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:36:50 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:36:51 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:37:28 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:37:31 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:37:31 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:37:32 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:37:43 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:37:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:37:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db0b40a788b5dc607b1c57159c10d933482a4d6d133f5dbc25b3ec80f8949d`  
		Last Modified: Tue, 28 Sep 2021 07:41:36 GMT  
		Size: 96.5 MB (96506389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d10d65c8075a3787960d77b4352f8b93fb4f7cc3c71fcdc54e7b6a28e55e73`  
		Last Modified: Tue, 28 Sep 2021 07:41:56 GMT  
		Size: 178.5 MB (178518329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54377016c49e4af1fe6f85ba0d742b3bcaa512bb0425d837c96ef763ce6eca80`  
		Last Modified: Tue, 28 Sep 2021 07:41:20 GMT  
		Size: 18.1 MB (18103484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0`

```console
$ docker pull haskell@sha256:2085d324b5ec3e3026394b1cc7d984e300490deb71d051658307a8a0846fa80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0` - linux; amd64

```console
$ docker pull haskell@sha256:d368dfa45ee89f0f988038bd357b8f3580fe9fe18198d0a1df6f70181a30e09b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359141497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ca824c31465096e0a20e8f275fee54bde2eb7b467fbcb85c388007a9d70324`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:35:27 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:35:27 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:35:27 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:36:01 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:04 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:36:15 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:36:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:36:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71751d64b5fca23ceede0931e0f893dcadbe61ae4a2c44c5612d9a7da9230ae`  
		Last Modified: Tue, 28 Sep 2021 07:40:51 GMT  
		Size: 174.5 MB (174549730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39c2ae60255e3f29cce22ade2a5dff3d8794a5fe18aaa82bb35aee593d6ad34`  
		Last Modified: Tue, 28 Sep 2021 07:40:16 GMT  
		Size: 18.1 MB (18103479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-buster`

```console
$ docker pull haskell@sha256:2085d324b5ec3e3026394b1cc7d984e300490deb71d051658307a8a0846fa80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0-buster` - linux; amd64

```console
$ docker pull haskell@sha256:d368dfa45ee89f0f988038bd357b8f3580fe9fe18198d0a1df6f70181a30e09b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359141497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ca824c31465096e0a20e8f275fee54bde2eb7b467fbcb85c388007a9d70324`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:35:27 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:35:27 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:35:27 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:36:01 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:04 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:36:15 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:36:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:36:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71751d64b5fca23ceede0931e0f893dcadbe61ae4a2c44c5612d9a7da9230ae`  
		Last Modified: Tue, 28 Sep 2021 07:40:51 GMT  
		Size: 174.5 MB (174549730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39c2ae60255e3f29cce22ade2a5dff3d8794a5fe18aaa82bb35aee593d6ad34`  
		Last Modified: Tue, 28 Sep 2021 07:40:16 GMT  
		Size: 18.1 MB (18103479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-stretch`

```console
$ docker pull haskell@sha256:f61bee43f1034084e6e6fb8b7592322ca035feb8873d23b9b1bed353a39a1acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:c051b8e82558f0be7aa393bb0b63047ae0a081efdff2721ee9172bd379e54517
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338507856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3059e9838d93bb77fcf74f7c1d1491da505cfc404caad2e17d46f4065e8b130`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:36:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:50 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:36:50 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:36:51 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:37:28 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:37:31 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:37:31 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:37:32 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:37:43 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:37:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:37:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db0b40a788b5dc607b1c57159c10d933482a4d6d133f5dbc25b3ec80f8949d`  
		Last Modified: Tue, 28 Sep 2021 07:41:36 GMT  
		Size: 96.5 MB (96506389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d10d65c8075a3787960d77b4352f8b93fb4f7cc3c71fcdc54e7b6a28e55e73`  
		Last Modified: Tue, 28 Sep 2021 07:41:56 GMT  
		Size: 178.5 MB (178518329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54377016c49e4af1fe6f85ba0d742b3bcaa512bb0425d837c96ef763ce6eca80`  
		Last Modified: Tue, 28 Sep 2021 07:41:20 GMT  
		Size: 18.1 MB (18103484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.1`

```console
$ docker pull haskell@sha256:2085d324b5ec3e3026394b1cc7d984e300490deb71d051658307a8a0846fa80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0.1` - linux; amd64

```console
$ docker pull haskell@sha256:d368dfa45ee89f0f988038bd357b8f3580fe9fe18198d0a1df6f70181a30e09b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359141497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ca824c31465096e0a20e8f275fee54bde2eb7b467fbcb85c388007a9d70324`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:35:27 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:35:27 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:35:27 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:36:01 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:04 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:36:15 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:36:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:36:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71751d64b5fca23ceede0931e0f893dcadbe61ae4a2c44c5612d9a7da9230ae`  
		Last Modified: Tue, 28 Sep 2021 07:40:51 GMT  
		Size: 174.5 MB (174549730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39c2ae60255e3f29cce22ade2a5dff3d8794a5fe18aaa82bb35aee593d6ad34`  
		Last Modified: Tue, 28 Sep 2021 07:40:16 GMT  
		Size: 18.1 MB (18103479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.1-buster`

```console
$ docker pull haskell@sha256:2085d324b5ec3e3026394b1cc7d984e300490deb71d051658307a8a0846fa80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0.1-buster` - linux; amd64

```console
$ docker pull haskell@sha256:d368dfa45ee89f0f988038bd357b8f3580fe9fe18198d0a1df6f70181a30e09b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359141497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ca824c31465096e0a20e8f275fee54bde2eb7b467fbcb85c388007a9d70324`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:35:27 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:35:27 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:35:27 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:36:01 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:04 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:36:15 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:36:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:36:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71751d64b5fca23ceede0931e0f893dcadbe61ae4a2c44c5612d9a7da9230ae`  
		Last Modified: Tue, 28 Sep 2021 07:40:51 GMT  
		Size: 174.5 MB (174549730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39c2ae60255e3f29cce22ade2a5dff3d8794a5fe18aaa82bb35aee593d6ad34`  
		Last Modified: Tue, 28 Sep 2021 07:40:16 GMT  
		Size: 18.1 MB (18103479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.1-stretch`

```console
$ docker pull haskell@sha256:f61bee43f1034084e6e6fb8b7592322ca035feb8873d23b9b1bed353a39a1acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0.1-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:c051b8e82558f0be7aa393bb0b63047ae0a081efdff2721ee9172bd379e54517
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338507856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3059e9838d93bb77fcf74f7c1d1491da505cfc404caad2e17d46f4065e8b130`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:36:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:50 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:36:50 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:36:51 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:37:28 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:37:31 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:37:31 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:37:32 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:37:43 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:37:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:37:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db0b40a788b5dc607b1c57159c10d933482a4d6d133f5dbc25b3ec80f8949d`  
		Last Modified: Tue, 28 Sep 2021 07:41:36 GMT  
		Size: 96.5 MB (96506389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d10d65c8075a3787960d77b4352f8b93fb4f7cc3c71fcdc54e7b6a28e55e73`  
		Last Modified: Tue, 28 Sep 2021 07:41:56 GMT  
		Size: 178.5 MB (178518329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54377016c49e4af1fe6f85ba0d742b3bcaa512bb0425d837c96ef763ce6eca80`  
		Last Modified: Tue, 28 Sep 2021 07:41:20 GMT  
		Size: 18.1 MB (18103484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:buster`

```console
$ docker pull haskell@sha256:2085d324b5ec3e3026394b1cc7d984e300490deb71d051658307a8a0846fa80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:buster` - linux; amd64

```console
$ docker pull haskell@sha256:d368dfa45ee89f0f988038bd357b8f3580fe9fe18198d0a1df6f70181a30e09b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359141497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ca824c31465096e0a20e8f275fee54bde2eb7b467fbcb85c388007a9d70324`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:35:27 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:35:27 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:35:27 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:36:01 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:04 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:36:15 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:36:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:36:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71751d64b5fca23ceede0931e0f893dcadbe61ae4a2c44c5612d9a7da9230ae`  
		Last Modified: Tue, 28 Sep 2021 07:40:51 GMT  
		Size: 174.5 MB (174549730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39c2ae60255e3f29cce22ade2a5dff3d8794a5fe18aaa82bb35aee593d6ad34`  
		Last Modified: Tue, 28 Sep 2021 07:40:16 GMT  
		Size: 18.1 MB (18103479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:2085d324b5ec3e3026394b1cc7d984e300490deb71d051658307a8a0846fa80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:d368dfa45ee89f0f988038bd357b8f3580fe9fe18198d0a1df6f70181a30e09b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359141497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2ca824c31465096e0a20e8f275fee54bde2eb7b467fbcb85c388007a9d70324`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:22:54 GMT
ADD file:f2a417d653b625cf79b88a517dc7e0ce5ace15a7acbd952daeee3bb4bf6042a1 in / 
# Tue, 28 Sep 2021 01:22:55 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:35:03 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:35:26 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:35:27 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:35:27 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:35:27 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:36:01 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:04 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:36:05 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:36:15 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:36:15 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:36:15 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:5e7b6b7bd506c12399d65977c0ba8dd02824dc5d0e65fc55d7382da889bdac7d`  
		Last Modified: Tue, 28 Sep 2021 01:29:21 GMT  
		Size: 50.4 MB (50436209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be0f49688f0f0724401a9e2a4aa16c818d0826c3dc2c209d4455c643b4f56c8`  
		Last Modified: Tue, 28 Sep 2021 07:40:31 GMT  
		Size: 116.1 MB (116052079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71751d64b5fca23ceede0931e0f893dcadbe61ae4a2c44c5612d9a7da9230ae`  
		Last Modified: Tue, 28 Sep 2021 07:40:51 GMT  
		Size: 174.5 MB (174549730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39c2ae60255e3f29cce22ade2a5dff3d8794a5fe18aaa82bb35aee593d6ad34`  
		Last Modified: Tue, 28 Sep 2021 07:40:16 GMT  
		Size: 18.1 MB (18103479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:stretch`

```console
$ docker pull haskell@sha256:f61bee43f1034084e6e6fb8b7592322ca035feb8873d23b9b1bed353a39a1acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:stretch` - linux; amd64

```console
$ docker pull haskell@sha256:c051b8e82558f0be7aa393bb0b63047ae0a081efdff2721ee9172bd379e54517
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338507856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3059e9838d93bb77fcf74f7c1d1491da505cfc404caad2e17d46f4065e8b130`
-	Default Command: `["ghci"]`

```dockerfile
# Tue, 28 Sep 2021 01:25:15 GMT
ADD file:36e7d2a782d933f47ccfc8692ebf95cacda9f109a51c46514f00b78754070254 in / 
# Tue, 28 Sep 2021 01:25:15 GMT
CMD ["bash"]
# Tue, 28 Sep 2021 07:36:29 GMT
ENV LANG=C.UTF-8
# Tue, 28 Sep 2021 07:36:49 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:36:50 GMT
ARG GHC=9.0.1
# Tue, 28 Sep 2021 07:36:50 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Tue, 28 Sep 2021 07:36:51 GMT
ARG CABAL_INSTALL=3.4
# Tue, 28 Sep 2021 07:37:28 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 28 Sep 2021 07:37:31 GMT
ARG STACK=2.7.3
# Tue, 28 Sep 2021 07:37:31 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Tue, 28 Sep 2021 07:37:32 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Tue, 28 Sep 2021 07:37:43 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Tue, 28 Sep 2021 07:37:43 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Sep 2021 07:37:43 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:af4c2580c6c3e68236ce4f353c045f871e4780b85fdb54c00529426e09bc36ce`  
		Last Modified: Tue, 28 Sep 2021 01:32:26 GMT  
		Size: 45.4 MB (45379654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0db0b40a788b5dc607b1c57159c10d933482a4d6d133f5dbc25b3ec80f8949d`  
		Last Modified: Tue, 28 Sep 2021 07:41:36 GMT  
		Size: 96.5 MB (96506389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d10d65c8075a3787960d77b4352f8b93fb4f7cc3c71fcdc54e7b6a28e55e73`  
		Last Modified: Tue, 28 Sep 2021 07:41:56 GMT  
		Size: 178.5 MB (178518329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54377016c49e4af1fe6f85ba0d742b3bcaa512bb0425d837c96ef763ce6eca80`  
		Last Modified: Tue, 28 Sep 2021 07:41:20 GMT  
		Size: 18.1 MB (18103484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
