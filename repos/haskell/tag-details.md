<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:8`](#haskell8)
-	[`haskell:8-buster`](#haskell8-buster)
-	[`haskell:8-stretch`](#haskell8-stretch)
-	[`haskell:8.10`](#haskell810)
-	[`haskell:8.10-buster`](#haskell810-buster)
-	[`haskell:8.10-stretch`](#haskell810-stretch)
-	[`haskell:8.10.4`](#haskell8104)
-	[`haskell:8.10.4-buster`](#haskell8104-buster)
-	[`haskell:8.10.4-stretch`](#haskell8104-stretch)
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
$ docker pull haskell@sha256:5f06c429ab79c806a0c46106c1bbecf8af080b8d1b288e4985df218e05b123c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8` - linux; amd64

```console
$ docker pull haskell@sha256:d39bb456411aeca338c1698115b10c1a86eb5d0829c0d2cf5abf4cd4bab67e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361182905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aed6c1fd11528f7ea450d277c87cc925ab9ad9a29b70c63eb911ee072052847`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:31:42 GMT
ARG GHC=8.10.4
# Mon, 26 Jul 2021 18:31:42 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:31:43 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:32:05 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:32:13 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:32:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:32:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c876ff5ed645ab87400e71ac99ff4db8e021b9bbdfd54761c7c49007efc215`  
		Last Modified: Mon, 26 Jul 2021 18:36:07 GMT  
		Size: 176.6 MB (176593355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f430237bc0f9a14232b6f892a9d08af3ab43519c9ec11d4e9778a801367435`  
		Last Modified: Mon, 26 Jul 2021 18:35:36 GMT  
		Size: 18.1 MB (18103461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-buster`

```console
$ docker pull haskell@sha256:5f06c429ab79c806a0c46106c1bbecf8af080b8d1b288e4985df218e05b123c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8-buster` - linux; amd64

```console
$ docker pull haskell@sha256:d39bb456411aeca338c1698115b10c1a86eb5d0829c0d2cf5abf4cd4bab67e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361182905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aed6c1fd11528f7ea450d277c87cc925ab9ad9a29b70c63eb911ee072052847`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:31:42 GMT
ARG GHC=8.10.4
# Mon, 26 Jul 2021 18:31:42 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:31:43 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:32:05 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:32:13 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:32:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:32:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c876ff5ed645ab87400e71ac99ff4db8e021b9bbdfd54761c7c49007efc215`  
		Last Modified: Mon, 26 Jul 2021 18:36:07 GMT  
		Size: 176.6 MB (176593355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f430237bc0f9a14232b6f892a9d08af3ab43519c9ec11d4e9778a801367435`  
		Last Modified: Mon, 26 Jul 2021 18:35:36 GMT  
		Size: 18.1 MB (18103461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8-stretch`

```console
$ docker pull haskell@sha256:8538f53cf0c3af5757c823cd855d67519703c0a412f78e8ef26b2e3daea71598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:bae91f5b7ebb2534b2d10a72336bd8d268671ea255bea7eb8fa97a47e2106241
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340524848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5bf740d7f4de8ebcbbed624a5d26b8ec17786d1ec957c937d8ca976d05e112`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:19:34 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:30:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:18 GMT
ARG GHC=8.10.4
# Mon, 26 Jul 2021 18:32:18 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:32:18 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:32:43 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:45 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:32:46 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:32:46 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:32:52 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:32:53 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:32:53 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851a104476919e0aac26e73c56cb601a956dd3145679a7ca00eb71c6e8ac5f6`  
		Last Modified: Mon, 26 Jul 2021 18:34:55 GMT  
		Size: 96.5 MB (96502459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e38023b5214caa723512b2a52f27eb8619214cb9d4d9c619a05d883ae5a7430`  
		Last Modified: Mon, 26 Jul 2021 18:37:06 GMT  
		Size: 180.5 MB (180539104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca8952223e9f0ef518038ba48d8816a2f272f7dca242cd655142fe8e3a6a5fe`  
		Last Modified: Mon, 26 Jul 2021 18:36:35 GMT  
		Size: 18.1 MB (18103504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10`

```console
$ docker pull haskell@sha256:5f06c429ab79c806a0c46106c1bbecf8af080b8d1b288e4985df218e05b123c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10` - linux; amd64

```console
$ docker pull haskell@sha256:d39bb456411aeca338c1698115b10c1a86eb5d0829c0d2cf5abf4cd4bab67e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361182905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aed6c1fd11528f7ea450d277c87cc925ab9ad9a29b70c63eb911ee072052847`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:31:42 GMT
ARG GHC=8.10.4
# Mon, 26 Jul 2021 18:31:42 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:31:43 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:32:05 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:32:13 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:32:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:32:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c876ff5ed645ab87400e71ac99ff4db8e021b9bbdfd54761c7c49007efc215`  
		Last Modified: Mon, 26 Jul 2021 18:36:07 GMT  
		Size: 176.6 MB (176593355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f430237bc0f9a14232b6f892a9d08af3ab43519c9ec11d4e9778a801367435`  
		Last Modified: Mon, 26 Jul 2021 18:35:36 GMT  
		Size: 18.1 MB (18103461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-buster`

```console
$ docker pull haskell@sha256:5f06c429ab79c806a0c46106c1bbecf8af080b8d1b288e4985df218e05b123c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10-buster` - linux; amd64

```console
$ docker pull haskell@sha256:d39bb456411aeca338c1698115b10c1a86eb5d0829c0d2cf5abf4cd4bab67e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361182905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aed6c1fd11528f7ea450d277c87cc925ab9ad9a29b70c63eb911ee072052847`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:31:42 GMT
ARG GHC=8.10.4
# Mon, 26 Jul 2021 18:31:42 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:31:43 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:32:05 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:32:13 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:32:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:32:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c876ff5ed645ab87400e71ac99ff4db8e021b9bbdfd54761c7c49007efc215`  
		Last Modified: Mon, 26 Jul 2021 18:36:07 GMT  
		Size: 176.6 MB (176593355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f430237bc0f9a14232b6f892a9d08af3ab43519c9ec11d4e9778a801367435`  
		Last Modified: Mon, 26 Jul 2021 18:35:36 GMT  
		Size: 18.1 MB (18103461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10-stretch`

```console
$ docker pull haskell@sha256:8538f53cf0c3af5757c823cd855d67519703c0a412f78e8ef26b2e3daea71598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:bae91f5b7ebb2534b2d10a72336bd8d268671ea255bea7eb8fa97a47e2106241
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340524848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5bf740d7f4de8ebcbbed624a5d26b8ec17786d1ec957c937d8ca976d05e112`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:19:34 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:30:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:18 GMT
ARG GHC=8.10.4
# Mon, 26 Jul 2021 18:32:18 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:32:18 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:32:43 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:45 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:32:46 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:32:46 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:32:52 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:32:53 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:32:53 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851a104476919e0aac26e73c56cb601a956dd3145679a7ca00eb71c6e8ac5f6`  
		Last Modified: Mon, 26 Jul 2021 18:34:55 GMT  
		Size: 96.5 MB (96502459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e38023b5214caa723512b2a52f27eb8619214cb9d4d9c619a05d883ae5a7430`  
		Last Modified: Mon, 26 Jul 2021 18:37:06 GMT  
		Size: 180.5 MB (180539104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca8952223e9f0ef518038ba48d8816a2f272f7dca242cd655142fe8e3a6a5fe`  
		Last Modified: Mon, 26 Jul 2021 18:36:35 GMT  
		Size: 18.1 MB (18103504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.4`

```console
$ docker pull haskell@sha256:5f06c429ab79c806a0c46106c1bbecf8af080b8d1b288e4985df218e05b123c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10.4` - linux; amd64

```console
$ docker pull haskell@sha256:d39bb456411aeca338c1698115b10c1a86eb5d0829c0d2cf5abf4cd4bab67e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361182905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aed6c1fd11528f7ea450d277c87cc925ab9ad9a29b70c63eb911ee072052847`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:31:42 GMT
ARG GHC=8.10.4
# Mon, 26 Jul 2021 18:31:42 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:31:43 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:32:05 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:32:13 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:32:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:32:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c876ff5ed645ab87400e71ac99ff4db8e021b9bbdfd54761c7c49007efc215`  
		Last Modified: Mon, 26 Jul 2021 18:36:07 GMT  
		Size: 176.6 MB (176593355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f430237bc0f9a14232b6f892a9d08af3ab43519c9ec11d4e9778a801367435`  
		Last Modified: Mon, 26 Jul 2021 18:35:36 GMT  
		Size: 18.1 MB (18103461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.4-buster`

```console
$ docker pull haskell@sha256:5f06c429ab79c806a0c46106c1bbecf8af080b8d1b288e4985df218e05b123c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10.4-buster` - linux; amd64

```console
$ docker pull haskell@sha256:d39bb456411aeca338c1698115b10c1a86eb5d0829c0d2cf5abf4cd4bab67e83
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361182905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aed6c1fd11528f7ea450d277c87cc925ab9ad9a29b70c63eb911ee072052847`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:31:42 GMT
ARG GHC=8.10.4
# Mon, 26 Jul 2021 18:31:42 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:31:43 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:32:05 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:32:09 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:32:13 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:32:13 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:32:13 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c876ff5ed645ab87400e71ac99ff4db8e021b9bbdfd54761c7c49007efc215`  
		Last Modified: Mon, 26 Jul 2021 18:36:07 GMT  
		Size: 176.6 MB (176593355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f430237bc0f9a14232b6f892a9d08af3ab43519c9ec11d4e9778a801367435`  
		Last Modified: Mon, 26 Jul 2021 18:35:36 GMT  
		Size: 18.1 MB (18103461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.10.4-stretch`

```console
$ docker pull haskell@sha256:8538f53cf0c3af5757c823cd855d67519703c0a412f78e8ef26b2e3daea71598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:8.10.4-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:bae91f5b7ebb2534b2d10a72336bd8d268671ea255bea7eb8fa97a47e2106241
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340524848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5bf740d7f4de8ebcbbed624a5d26b8ec17786d1ec957c937d8ca976d05e112`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:19:34 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:30:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:18 GMT
ARG GHC=8.10.4
# Mon, 26 Jul 2021 18:32:18 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:32:18 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:32:43 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:32:45 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:32:46 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:32:46 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:32:52 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=8.10.4 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:32:53 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/8.10.4/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:32:53 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851a104476919e0aac26e73c56cb601a956dd3145679a7ca00eb71c6e8ac5f6`  
		Last Modified: Mon, 26 Jul 2021 18:34:55 GMT  
		Size: 96.5 MB (96502459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e38023b5214caa723512b2a52f27eb8619214cb9d4d9c619a05d883ae5a7430`  
		Last Modified: Mon, 26 Jul 2021 18:37:06 GMT  
		Size: 180.5 MB (180539104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca8952223e9f0ef518038ba48d8816a2f272f7dca242cd655142fe8e3a6a5fe`  
		Last Modified: Mon, 26 Jul 2021 18:36:35 GMT  
		Size: 18.1 MB (18103504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9`

```console
$ docker pull haskell@sha256:09b8c9b0adfb395202937ecacae91452d2552b627da7efd6a5522f34499e8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9` - linux; amd64

```console
$ docker pull haskell@sha256:7eb3cca441344ebfb71dd7b1c03dc46a082b669ef3188016adf02fd4a730d8f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359140164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd58d39e00cdd7fcb9f84d5ec59a2af7af02b6e04119bc9a8fddb8043cafe1`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:29:53 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:29:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:29:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:30:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:30:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:30:26 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:30:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:30:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539fe5d73a5828f158829e757a6e8ece9d7913ff9217ae66890eb8bd4394d775`  
		Last Modified: Mon, 26 Jul 2021 18:34:06 GMT  
		Size: 174.6 MB (174550611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3ea359e5cccee19e88c9f726a142b10adecceaf33d40faaf60a0381617857c`  
		Last Modified: Mon, 26 Jul 2021 18:33:36 GMT  
		Size: 18.1 MB (18103464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-buster`

```console
$ docker pull haskell@sha256:09b8c9b0adfb395202937ecacae91452d2552b627da7efd6a5522f34499e8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9-buster` - linux; amd64

```console
$ docker pull haskell@sha256:7eb3cca441344ebfb71dd7b1c03dc46a082b669ef3188016adf02fd4a730d8f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359140164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd58d39e00cdd7fcb9f84d5ec59a2af7af02b6e04119bc9a8fddb8043cafe1`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:29:53 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:29:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:29:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:30:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:30:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:30:26 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:30:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:30:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539fe5d73a5828f158829e757a6e8ece9d7913ff9217ae66890eb8bd4394d775`  
		Last Modified: Mon, 26 Jul 2021 18:34:06 GMT  
		Size: 174.6 MB (174550611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3ea359e5cccee19e88c9f726a142b10adecceaf33d40faaf60a0381617857c`  
		Last Modified: Mon, 26 Jul 2021 18:33:36 GMT  
		Size: 18.1 MB (18103464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9-stretch`

```console
$ docker pull haskell@sha256:701b69285193fcd27153769fee189ff3cf069e1b89ab73a0ae2e0b8a2a27f090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:01d1bd34ab8a9e423e1ad6f555d95cd569054bacf70f521321c83eb6ab540b9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338504556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838c04ef155f4f10b73e9df15a6ef0cec33aaa020008073a3f5833cf2c74ae89`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:19:34 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:30:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:52 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:30:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:30:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:31:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:31:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:31:22 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:31:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:31:28 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:31:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:31:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851a104476919e0aac26e73c56cb601a956dd3145679a7ca00eb71c6e8ac5f6`  
		Last Modified: Mon, 26 Jul 2021 18:34:55 GMT  
		Size: 96.5 MB (96502459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b012d0b5fc21072b9c8520c0405073ebaaab47689114485caa896d0dc82fa8`  
		Last Modified: Mon, 26 Jul 2021 18:35:16 GMT  
		Size: 178.5 MB (178518844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1526ab89da7a55b797efee943bfeea78e52efbf5ef0cfe7620ee85715aabe0`  
		Last Modified: Mon, 26 Jul 2021 18:34:42 GMT  
		Size: 18.1 MB (18103472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0`

```console
$ docker pull haskell@sha256:09b8c9b0adfb395202937ecacae91452d2552b627da7efd6a5522f34499e8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0` - linux; amd64

```console
$ docker pull haskell@sha256:7eb3cca441344ebfb71dd7b1c03dc46a082b669ef3188016adf02fd4a730d8f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359140164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd58d39e00cdd7fcb9f84d5ec59a2af7af02b6e04119bc9a8fddb8043cafe1`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:29:53 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:29:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:29:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:30:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:30:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:30:26 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:30:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:30:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539fe5d73a5828f158829e757a6e8ece9d7913ff9217ae66890eb8bd4394d775`  
		Last Modified: Mon, 26 Jul 2021 18:34:06 GMT  
		Size: 174.6 MB (174550611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3ea359e5cccee19e88c9f726a142b10adecceaf33d40faaf60a0381617857c`  
		Last Modified: Mon, 26 Jul 2021 18:33:36 GMT  
		Size: 18.1 MB (18103464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-buster`

```console
$ docker pull haskell@sha256:09b8c9b0adfb395202937ecacae91452d2552b627da7efd6a5522f34499e8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0-buster` - linux; amd64

```console
$ docker pull haskell@sha256:7eb3cca441344ebfb71dd7b1c03dc46a082b669ef3188016adf02fd4a730d8f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359140164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd58d39e00cdd7fcb9f84d5ec59a2af7af02b6e04119bc9a8fddb8043cafe1`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:29:53 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:29:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:29:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:30:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:30:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:30:26 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:30:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:30:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539fe5d73a5828f158829e757a6e8ece9d7913ff9217ae66890eb8bd4394d775`  
		Last Modified: Mon, 26 Jul 2021 18:34:06 GMT  
		Size: 174.6 MB (174550611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3ea359e5cccee19e88c9f726a142b10adecceaf33d40faaf60a0381617857c`  
		Last Modified: Mon, 26 Jul 2021 18:33:36 GMT  
		Size: 18.1 MB (18103464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0-stretch`

```console
$ docker pull haskell@sha256:701b69285193fcd27153769fee189ff3cf069e1b89ab73a0ae2e0b8a2a27f090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:01d1bd34ab8a9e423e1ad6f555d95cd569054bacf70f521321c83eb6ab540b9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338504556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838c04ef155f4f10b73e9df15a6ef0cec33aaa020008073a3f5833cf2c74ae89`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:19:34 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:30:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:52 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:30:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:30:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:31:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:31:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:31:22 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:31:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:31:28 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:31:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:31:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851a104476919e0aac26e73c56cb601a956dd3145679a7ca00eb71c6e8ac5f6`  
		Last Modified: Mon, 26 Jul 2021 18:34:55 GMT  
		Size: 96.5 MB (96502459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b012d0b5fc21072b9c8520c0405073ebaaab47689114485caa896d0dc82fa8`  
		Last Modified: Mon, 26 Jul 2021 18:35:16 GMT  
		Size: 178.5 MB (178518844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1526ab89da7a55b797efee943bfeea78e52efbf5ef0cfe7620ee85715aabe0`  
		Last Modified: Mon, 26 Jul 2021 18:34:42 GMT  
		Size: 18.1 MB (18103472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.1`

```console
$ docker pull haskell@sha256:09b8c9b0adfb395202937ecacae91452d2552b627da7efd6a5522f34499e8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0.1` - linux; amd64

```console
$ docker pull haskell@sha256:7eb3cca441344ebfb71dd7b1c03dc46a082b669ef3188016adf02fd4a730d8f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359140164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd58d39e00cdd7fcb9f84d5ec59a2af7af02b6e04119bc9a8fddb8043cafe1`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:29:53 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:29:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:29:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:30:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:30:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:30:26 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:30:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:30:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539fe5d73a5828f158829e757a6e8ece9d7913ff9217ae66890eb8bd4394d775`  
		Last Modified: Mon, 26 Jul 2021 18:34:06 GMT  
		Size: 174.6 MB (174550611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3ea359e5cccee19e88c9f726a142b10adecceaf33d40faaf60a0381617857c`  
		Last Modified: Mon, 26 Jul 2021 18:33:36 GMT  
		Size: 18.1 MB (18103464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.1-buster`

```console
$ docker pull haskell@sha256:09b8c9b0adfb395202937ecacae91452d2552b627da7efd6a5522f34499e8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0.1-buster` - linux; amd64

```console
$ docker pull haskell@sha256:7eb3cca441344ebfb71dd7b1c03dc46a082b669ef3188016adf02fd4a730d8f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359140164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd58d39e00cdd7fcb9f84d5ec59a2af7af02b6e04119bc9a8fddb8043cafe1`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:29:53 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:29:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:29:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:30:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:30:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:30:26 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:30:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:30:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539fe5d73a5828f158829e757a6e8ece9d7913ff9217ae66890eb8bd4394d775`  
		Last Modified: Mon, 26 Jul 2021 18:34:06 GMT  
		Size: 174.6 MB (174550611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3ea359e5cccee19e88c9f726a142b10adecceaf33d40faaf60a0381617857c`  
		Last Modified: Mon, 26 Jul 2021 18:33:36 GMT  
		Size: 18.1 MB (18103464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:9.0.1-stretch`

```console
$ docker pull haskell@sha256:701b69285193fcd27153769fee189ff3cf069e1b89ab73a0ae2e0b8a2a27f090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:9.0.1-stretch` - linux; amd64

```console
$ docker pull haskell@sha256:01d1bd34ab8a9e423e1ad6f555d95cd569054bacf70f521321c83eb6ab540b9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338504556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838c04ef155f4f10b73e9df15a6ef0cec33aaa020008073a3f5833cf2c74ae89`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:19:34 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:30:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:52 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:30:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:30:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:31:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:31:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:31:22 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:31:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:31:28 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:31:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:31:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851a104476919e0aac26e73c56cb601a956dd3145679a7ca00eb71c6e8ac5f6`  
		Last Modified: Mon, 26 Jul 2021 18:34:55 GMT  
		Size: 96.5 MB (96502459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b012d0b5fc21072b9c8520c0405073ebaaab47689114485caa896d0dc82fa8`  
		Last Modified: Mon, 26 Jul 2021 18:35:16 GMT  
		Size: 178.5 MB (178518844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1526ab89da7a55b797efee943bfeea78e52efbf5ef0cfe7620ee85715aabe0`  
		Last Modified: Mon, 26 Jul 2021 18:34:42 GMT  
		Size: 18.1 MB (18103472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:buster`

```console
$ docker pull haskell@sha256:09b8c9b0adfb395202937ecacae91452d2552b627da7efd6a5522f34499e8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:buster` - linux; amd64

```console
$ docker pull haskell@sha256:7eb3cca441344ebfb71dd7b1c03dc46a082b669ef3188016adf02fd4a730d8f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359140164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd58d39e00cdd7fcb9f84d5ec59a2af7af02b6e04119bc9a8fddb8043cafe1`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:29:53 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:29:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:29:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:30:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:30:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:30:26 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:30:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:30:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539fe5d73a5828f158829e757a6e8ece9d7913ff9217ae66890eb8bd4394d775`  
		Last Modified: Mon, 26 Jul 2021 18:34:06 GMT  
		Size: 174.6 MB (174550611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3ea359e5cccee19e88c9f726a142b10adecceaf33d40faaf60a0381617857c`  
		Last Modified: Mon, 26 Jul 2021 18:33:36 GMT  
		Size: 18.1 MB (18103464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:09b8c9b0adfb395202937ecacae91452d2552b627da7efd6a5522f34499e8579
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:7eb3cca441344ebfb71dd7b1c03dc46a082b669ef3188016adf02fd4a730d8f8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.1 MB (359140164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72fd58d39e00cdd7fcb9f84d5ec59a2af7af02b6e04119bc9a8fddb8043cafe1`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:45:30 GMT
ADD file:e952f6979e4b0ead00b6906db1dd70eb9beb564a04e2f02e2e0cff8614920216 in / 
# Thu, 22 Jul 2021 00:45:31 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:18:08 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:29:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:29:53 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:29:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:29:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:30:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian buster main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:30:21 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:30:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:30:26 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:30:26 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:30:27 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:627b765e08d177e63c9a202ca4991b711448905b934435c70b7cbd7d4a9c7959`  
		Last Modified: Thu, 22 Jul 2021 00:50:07 GMT  
		Size: 50.4 MB (50435626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2861ac935da3615d4ff530329225953049fdd0b325d6a1be8d45ccc3ad3ff51`  
		Last Modified: Mon, 26 Jul 2021 18:33:47 GMT  
		Size: 116.1 MB (116050463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539fe5d73a5828f158829e757a6e8ece9d7913ff9217ae66890eb8bd4394d775`  
		Last Modified: Mon, 26 Jul 2021 18:34:06 GMT  
		Size: 174.6 MB (174550611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3ea359e5cccee19e88c9f726a142b10adecceaf33d40faaf60a0381617857c`  
		Last Modified: Mon, 26 Jul 2021 18:33:36 GMT  
		Size: 18.1 MB (18103464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:stretch`

```console
$ docker pull haskell@sha256:701b69285193fcd27153769fee189ff3cf069e1b89ab73a0ae2e0b8a2a27f090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `haskell:stretch` - linux; amd64

```console
$ docker pull haskell@sha256:01d1bd34ab8a9e423e1ad6f555d95cd569054bacf70f521321c83eb6ab540b9c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338504556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838c04ef155f4f10b73e9df15a6ef0cec33aaa020008073a3f5833cf2c74ae89`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:05 GMT
ADD file:fc9409352ad67880b83ccf1ccd1587eb2666715eae04e4dd98fca919f1bb98d7 in / 
# Thu, 22 Jul 2021 00:47:05 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 09:19:34 GMT
ENV LANG=C.UTF-8
# Mon, 26 Jul 2021 18:30:52 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends         ca-certificates         curl         dirmngr         g++         git         gnupg         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:30:52 GMT
ARG GHC=9.0.1
# Mon, 26 Jul 2021 18:30:53 GMT
ARG DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574
# Mon, 26 Jul 2021 18:30:53 GMT
ARG CABAL_INSTALL=3.4
# Mon, 26 Jul 2021 18:31:18 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${DEBIAN_KEY} &&     gpg --batch --armor --export ${DEBIAN_KEY} > /etc/apt/trusted.gpg.d/haskell.org.gpg.asc &&     gpgconf --kill all &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         ghc-${GHC} &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Mon, 26 Jul 2021 18:31:21 GMT
ARG STACK=2.7.3
# Mon, 26 Jul 2021 18:31:22 GMT
ARG STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442
# Mon, 26 Jul 2021 18:31:22 GMT
ARG STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
# Mon, 26 Jul 2021 18:31:28 GMT
# ARGS: CABAL_INSTALL=3.4 DEBIAN_KEY=427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 GHC=9.0.1 STACK=2.7.3 STACK_KEY=C5705533DA4F78D8664B5DC0575159689BEFB442 STACK_RELEASE_KEY=2C6A674E85EE3FB896AFC9B965101FF31C5C154D
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_KEY} &&     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys ${STACK_RELEASE_KEY} &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Mon, 26 Jul 2021 18:31:28 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.4/bin:/opt/ghc/9.0.1/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 26 Jul 2021 18:31:28 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:08224db8ce18b31a78a0a26d1b344d173528e50a7067797c9df4de5d8df353e2`  
		Last Modified: Thu, 22 Jul 2021 00:52:52 GMT  
		Size: 45.4 MB (45379781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6851a104476919e0aac26e73c56cb601a956dd3145679a7ca00eb71c6e8ac5f6`  
		Last Modified: Mon, 26 Jul 2021 18:34:55 GMT  
		Size: 96.5 MB (96502459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b012d0b5fc21072b9c8520c0405073ebaaab47689114485caa896d0dc82fa8`  
		Last Modified: Mon, 26 Jul 2021 18:35:16 GMT  
		Size: 178.5 MB (178518844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1526ab89da7a55b797efee943bfeea78e52efbf5ef0cfe7620ee85715aabe0`  
		Last Modified: Mon, 26 Jul 2021 18:34:42 GMT  
		Size: 18.1 MB (18103472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
