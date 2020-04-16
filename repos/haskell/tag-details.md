<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `haskell`

-	[`haskell:8`](#haskell8)
-	[`haskell:8.6`](#haskell86)
-	[`haskell:8.6.5`](#haskell865)
-	[`haskell:8.8`](#haskell88)
-	[`haskell:8.8.3`](#haskell883)
-	[`haskell:latest`](#haskelllatest)

## `haskell:8`

```console
$ docker pull haskell@sha256:474ee67ea389cd07a799fd78ee072c663f2ab7f9f68ffecdc4e95bcd9801beda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `haskell:8` - linux; amd64

```console
$ docker pull haskell@sha256:2311f03c85a897b0b9e711a386372d1af01bdc88d340d72a2317b1daf722868a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334109878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095b182d90778dce00f58059b7e82546ef6b6af7e892d3e3af3a4604016cf9ca`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:22 GMT
ADD file:9f6f0c8b90de3204ad5db95d10d8aa76b42454def6ac811c888ad4e274292c9c in / 
# Thu, 16 Apr 2020 03:27:22 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:50:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates dirmngr &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:50:18 GMT
ARG GHC=8.8.3
# Thu, 16 Apr 2020 09:50:18 GMT
ARG STACK=2.1.3
# Thu, 16 Apr 2020 09:50:18 GMT
ARG CABAL_INSTALL=3.0
# Thu, 16 Apr 2020 09:51:02 GMT
# ARGS: CABAL_INSTALL=3.0 GHC=8.8.3 STACK=2.1.3
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         curl         g++         ghc-${GHC}         git         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:51:12 GMT
# ARGS: CABAL_INSTALL=3.0 GHC=8.8.3 STACK=2.1.3
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 2C6A674E85EE3FB896AFC9B965101FF31C5C154D &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Thu, 16 Apr 2020 09:51:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.0/bin:/opt/ghc/8.8.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 09:51:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7568c21980bd8003ca9d23a218302c6386aac91e069cc0c0be6bedf45476f056`  
		Last Modified: Thu, 16 Apr 2020 03:34:47 GMT  
		Size: 45.4 MB (45375910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd22a5396b8f86e624a8a9849e375a3ffdfe580864a38133bb9e6f29db2c4b78`  
		Last Modified: Thu, 16 Apr 2020 09:53:04 GMT  
		Size: 9.6 MB (9613334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7825e2c7f267267f985315f9e462923778dc64bd36eba406029406bb6e8bc88a`  
		Last Modified: Thu, 16 Apr 2020 09:54:27 GMT  
		Size: 264.6 MB (264553244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7282a0304815b8416219c22048ffea0ff34261432f65f51481ba79bdd6099be0`  
		Last Modified: Thu, 16 Apr 2020 09:53:06 GMT  
		Size: 14.6 MB (14567390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.6`

```console
$ docker pull haskell@sha256:ce90adb0e2dc9ae907fac9c20418ad9aae42418d23e8beb90d7f0da9a2fc6ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `haskell:8.6` - linux; amd64

```console
$ docker pull haskell@sha256:581872392b460b0f3293e85e63c502058c0634526ca028e2fa9a96cb4c780c63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304132309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e8d436152d34534e49fecfc40bd349272196cbb424ccccee5d5f193b9bf841`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:22 GMT
ADD file:9f6f0c8b90de3204ad5db95d10d8aa76b42454def6ac811c888ad4e274292c9c in / 
# Thu, 16 Apr 2020 03:27:22 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:50:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates dirmngr &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:51:25 GMT
ARG GHC=8.6.5
# Thu, 16 Apr 2020 09:51:25 GMT
ARG STACK=1.9.3
# Thu, 16 Apr 2020 09:51:25 GMT
ARG CABAL_INSTALL=2.4
# Thu, 16 Apr 2020 09:52:32 GMT
# ARGS: CABAL_INSTALL=2.4 GHC=8.6.5 STACK=1.9.3
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         curl         g++         ghc-${GHC}         git         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:52:39 GMT
# ARGS: CABAL_INSTALL=2.4 GHC=8.6.5 STACK=1.9.3
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Thu, 16 Apr 2020 09:52:40 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/2.4/bin:/opt/ghc/8.6.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 09:52:40 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7568c21980bd8003ca9d23a218302c6386aac91e069cc0c0be6bedf45476f056`  
		Last Modified: Thu, 16 Apr 2020 03:34:47 GMT  
		Size: 45.4 MB (45375910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd22a5396b8f86e624a8a9849e375a3ffdfe580864a38133bb9e6f29db2c4b78`  
		Last Modified: Thu, 16 Apr 2020 09:53:04 GMT  
		Size: 9.6 MB (9613334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f02a855f53f344aaad78db58c565b1f6b01b39dc3182b8ea922b3cd50ae3bf`  
		Last Modified: Thu, 16 Apr 2020 09:55:46 GMT  
		Size: 234.9 MB (234906724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34d4939d7b7e63525dc989fe6a664356489af01a1b6b2e976e1ab14f69973ec`  
		Last Modified: Thu, 16 Apr 2020 09:54:40 GMT  
		Size: 14.2 MB (14236341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.6.5`

```console
$ docker pull haskell@sha256:ce90adb0e2dc9ae907fac9c20418ad9aae42418d23e8beb90d7f0da9a2fc6ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `haskell:8.6.5` - linux; amd64

```console
$ docker pull haskell@sha256:581872392b460b0f3293e85e63c502058c0634526ca028e2fa9a96cb4c780c63
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304132309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9e8d436152d34534e49fecfc40bd349272196cbb424ccccee5d5f193b9bf841`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:22 GMT
ADD file:9f6f0c8b90de3204ad5db95d10d8aa76b42454def6ac811c888ad4e274292c9c in / 
# Thu, 16 Apr 2020 03:27:22 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:50:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates dirmngr &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:51:25 GMT
ARG GHC=8.6.5
# Thu, 16 Apr 2020 09:51:25 GMT
ARG STACK=1.9.3
# Thu, 16 Apr 2020 09:51:25 GMT
ARG CABAL_INSTALL=2.4
# Thu, 16 Apr 2020 09:52:32 GMT
# ARGS: CABAL_INSTALL=2.4 GHC=8.6.5 STACK=1.9.3
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         curl         g++         ghc-${GHC}         git         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:52:39 GMT
# ARGS: CABAL_INSTALL=2.4 GHC=8.6.5 STACK=1.9.3
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Thu, 16 Apr 2020 09:52:40 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/2.4/bin:/opt/ghc/8.6.5/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 09:52:40 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7568c21980bd8003ca9d23a218302c6386aac91e069cc0c0be6bedf45476f056`  
		Last Modified: Thu, 16 Apr 2020 03:34:47 GMT  
		Size: 45.4 MB (45375910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd22a5396b8f86e624a8a9849e375a3ffdfe580864a38133bb9e6f29db2c4b78`  
		Last Modified: Thu, 16 Apr 2020 09:53:04 GMT  
		Size: 9.6 MB (9613334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f02a855f53f344aaad78db58c565b1f6b01b39dc3182b8ea922b3cd50ae3bf`  
		Last Modified: Thu, 16 Apr 2020 09:55:46 GMT  
		Size: 234.9 MB (234906724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34d4939d7b7e63525dc989fe6a664356489af01a1b6b2e976e1ab14f69973ec`  
		Last Modified: Thu, 16 Apr 2020 09:54:40 GMT  
		Size: 14.2 MB (14236341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.8`

```console
$ docker pull haskell@sha256:474ee67ea389cd07a799fd78ee072c663f2ab7f9f68ffecdc4e95bcd9801beda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `haskell:8.8` - linux; amd64

```console
$ docker pull haskell@sha256:2311f03c85a897b0b9e711a386372d1af01bdc88d340d72a2317b1daf722868a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334109878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095b182d90778dce00f58059b7e82546ef6b6af7e892d3e3af3a4604016cf9ca`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:22 GMT
ADD file:9f6f0c8b90de3204ad5db95d10d8aa76b42454def6ac811c888ad4e274292c9c in / 
# Thu, 16 Apr 2020 03:27:22 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:50:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates dirmngr &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:50:18 GMT
ARG GHC=8.8.3
# Thu, 16 Apr 2020 09:50:18 GMT
ARG STACK=2.1.3
# Thu, 16 Apr 2020 09:50:18 GMT
ARG CABAL_INSTALL=3.0
# Thu, 16 Apr 2020 09:51:02 GMT
# ARGS: CABAL_INSTALL=3.0 GHC=8.8.3 STACK=2.1.3
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         curl         g++         ghc-${GHC}         git         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:51:12 GMT
# ARGS: CABAL_INSTALL=3.0 GHC=8.8.3 STACK=2.1.3
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 2C6A674E85EE3FB896AFC9B965101FF31C5C154D &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Thu, 16 Apr 2020 09:51:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.0/bin:/opt/ghc/8.8.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 09:51:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7568c21980bd8003ca9d23a218302c6386aac91e069cc0c0be6bedf45476f056`  
		Last Modified: Thu, 16 Apr 2020 03:34:47 GMT  
		Size: 45.4 MB (45375910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd22a5396b8f86e624a8a9849e375a3ffdfe580864a38133bb9e6f29db2c4b78`  
		Last Modified: Thu, 16 Apr 2020 09:53:04 GMT  
		Size: 9.6 MB (9613334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7825e2c7f267267f985315f9e462923778dc64bd36eba406029406bb6e8bc88a`  
		Last Modified: Thu, 16 Apr 2020 09:54:27 GMT  
		Size: 264.6 MB (264553244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7282a0304815b8416219c22048ffea0ff34261432f65f51481ba79bdd6099be0`  
		Last Modified: Thu, 16 Apr 2020 09:53:06 GMT  
		Size: 14.6 MB (14567390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:8.8.3`

```console
$ docker pull haskell@sha256:474ee67ea389cd07a799fd78ee072c663f2ab7f9f68ffecdc4e95bcd9801beda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `haskell:8.8.3` - linux; amd64

```console
$ docker pull haskell@sha256:2311f03c85a897b0b9e711a386372d1af01bdc88d340d72a2317b1daf722868a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334109878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095b182d90778dce00f58059b7e82546ef6b6af7e892d3e3af3a4604016cf9ca`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:22 GMT
ADD file:9f6f0c8b90de3204ad5db95d10d8aa76b42454def6ac811c888ad4e274292c9c in / 
# Thu, 16 Apr 2020 03:27:22 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:50:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates dirmngr &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:50:18 GMT
ARG GHC=8.8.3
# Thu, 16 Apr 2020 09:50:18 GMT
ARG STACK=2.1.3
# Thu, 16 Apr 2020 09:50:18 GMT
ARG CABAL_INSTALL=3.0
# Thu, 16 Apr 2020 09:51:02 GMT
# ARGS: CABAL_INSTALL=3.0 GHC=8.8.3 STACK=2.1.3
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         curl         g++         ghc-${GHC}         git         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:51:12 GMT
# ARGS: CABAL_INSTALL=3.0 GHC=8.8.3 STACK=2.1.3
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 2C6A674E85EE3FB896AFC9B965101FF31C5C154D &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Thu, 16 Apr 2020 09:51:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.0/bin:/opt/ghc/8.8.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 09:51:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7568c21980bd8003ca9d23a218302c6386aac91e069cc0c0be6bedf45476f056`  
		Last Modified: Thu, 16 Apr 2020 03:34:47 GMT  
		Size: 45.4 MB (45375910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd22a5396b8f86e624a8a9849e375a3ffdfe580864a38133bb9e6f29db2c4b78`  
		Last Modified: Thu, 16 Apr 2020 09:53:04 GMT  
		Size: 9.6 MB (9613334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7825e2c7f267267f985315f9e462923778dc64bd36eba406029406bb6e8bc88a`  
		Last Modified: Thu, 16 Apr 2020 09:54:27 GMT  
		Size: 264.6 MB (264553244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7282a0304815b8416219c22048ffea0ff34261432f65f51481ba79bdd6099be0`  
		Last Modified: Thu, 16 Apr 2020 09:53:06 GMT  
		Size: 14.6 MB (14567390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `haskell:latest`

```console
$ docker pull haskell@sha256:474ee67ea389cd07a799fd78ee072c663f2ab7f9f68ffecdc4e95bcd9801beda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `haskell:latest` - linux; amd64

```console
$ docker pull haskell@sha256:2311f03c85a897b0b9e711a386372d1af01bdc88d340d72a2317b1daf722868a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.1 MB (334109878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095b182d90778dce00f58059b7e82546ef6b6af7e892d3e3af3a4604016cf9ca`
-	Default Command: `["ghci"]`

```dockerfile
# Thu, 16 Apr 2020 03:27:22 GMT
ADD file:9f6f0c8b90de3204ad5db95d10d8aa76b42454def6ac811c888ad4e274292c9c in / 
# Thu, 16 Apr 2020 03:27:22 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:50:17 GMT
RUN apt-get update &&     apt-get install -y --no-install-recommends gnupg ca-certificates dirmngr &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:50:18 GMT
ARG GHC=8.8.3
# Thu, 16 Apr 2020 09:50:18 GMT
ARG STACK=2.1.3
# Thu, 16 Apr 2020 09:50:18 GMT
ARG CABAL_INSTALL=3.0
# Thu, 16 Apr 2020 09:51:02 GMT
# ARGS: CABAL_INSTALL=3.0 GHC=8.8.3 STACK=2.1.3
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 427CB69AAC9D00F2A43CAF1CBA3CBA3FFE22B574 &&     echo 'deb http://downloads.haskell.org/debian stretch main' > /etc/apt/sources.list.d/ghc.list &&     apt-get update &&     apt-get install -y --no-install-recommends         cabal-install-${CABAL_INSTALL}         curl         g++         ghc-${GHC}         git         libsqlite3-dev         libtinfo-dev         make         netbase         openssh-client         xz-utils         zlib1g-dev &&     rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:51:12 GMT
# ARGS: CABAL_INSTALL=3.0 GHC=8.8.3 STACK=2.1.3
RUN export GNUPGHOME="$(mktemp -d)" &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys C5705533DA4F78D8664B5DC0575159689BEFB442 &&     gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys 2C6A674E85EE3FB896AFC9B965101FF31C5C154D &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz -o stack.tar.gz &&     curl -fSL https://github.com/commercialhaskell/stack/releases/download/v${STACK}/stack-${STACK}-linux-x86_64.tar.gz.asc -o stack.tar.gz.asc &&     gpg --batch --trusted-key 0x575159689BEFB442 --verify stack.tar.gz.asc stack.tar.gz &&     tar -xf stack.tar.gz -C /usr/local/bin --strip-components=1 &&     /usr/local/bin/stack config set system-ghc --global true &&     /usr/local/bin/stack config set install-ghc --global false &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* /stack.tar.gz.asc /stack.tar.gz
# Thu, 16 Apr 2020 09:51:14 GMT
ENV PATH=/root/.cabal/bin:/root/.local/bin:/opt/cabal/3.0/bin:/opt/ghc/8.8.3/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 09:51:16 GMT
CMD ["ghci"]
```

-	Layers:
	-	`sha256:7568c21980bd8003ca9d23a218302c6386aac91e069cc0c0be6bedf45476f056`  
		Last Modified: Thu, 16 Apr 2020 03:34:47 GMT  
		Size: 45.4 MB (45375910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd22a5396b8f86e624a8a9849e375a3ffdfe580864a38133bb9e6f29db2c4b78`  
		Last Modified: Thu, 16 Apr 2020 09:53:04 GMT  
		Size: 9.6 MB (9613334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7825e2c7f267267f985315f9e462923778dc64bd36eba406029406bb6e8bc88a`  
		Last Modified: Thu, 16 Apr 2020 09:54:27 GMT  
		Size: 264.6 MB (264553244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7282a0304815b8416219c22048ffea0ff34261432f65f51481ba79bdd6099be0`  
		Last Modified: Thu, 16 Apr 2020 09:53:06 GMT  
		Size: 14.6 MB (14567390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
