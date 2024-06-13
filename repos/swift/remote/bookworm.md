## `swift:bookworm`

```console
$ docker pull swift@sha256:c61e2c8a1267977ea05de12d81c4268c27d8777594735a700f7c8c0b5d1f1fc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:de6627dc0dc569d7f5a4d1049189fc1e83bf02d8021077cd4e3790a148d4c506
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **963.7 MB (963687279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606190ed0e176a9cd0eaeee44e74c4a23589e64b2dbcd84d67e319e5f25f0f1a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Fri, 07 Jun 2024 04:10:51 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 07 Jun 2024 04:10:51 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 07 Jun 2024 04:11:27 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     && rm -r /var/lib/apt/lists/*
# Fri, 07 Jun 2024 04:11:29 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 07 Jun 2024 04:11:29 GMT
ARG SWIFT_PLATFORM=debian12
# Fri, 07 Jun 2024 04:11:29 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Fri, 07 Jun 2024 04:11:29 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Fri, 07 Jun 2024 04:11:29 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 07 Jun 2024 04:11:29 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 07 Jun 2024 04:12:21 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg
# Fri, 07 Jun 2024 04:12:27 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c17d30b92effa0143cd8c50ed4fea54c9488de98fc11befdbf3779ba04d4fe`  
		Last Modified: Fri, 07 Jun 2024 04:35:41 GMT  
		Size: 194.6 MB (194560127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fa758dcf74ec95035fa6050b64204325b7a8c47fe9963bd9f116d230d5507a`  
		Last Modified: Fri, 07 Jun 2024 04:36:50 GMT  
		Size: 719.6 MB (719550585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92cb1b2d0dd4c7b405b6ebffe11821bf451e3fb01ea92f79ccbfb5ceb6dd21b3`  
		Last Modified: Fri, 07 Jun 2024 04:35:12 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:500e15e093bcd8917f233cf1808408bd413fcf4ab1c6c494d9c2b7c23962b1d1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.1 MB (853079518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df03b765890b27fd7b6d0700d8c1cfcfa231ca5db012477126e48967509fcf20`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:41 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Thu, 13 Jun 2024 00:39:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 07:17:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 13 Jun 2024 07:17:37 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 13 Jun 2024 07:18:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     && rm -r /var/lib/apt/lists/*
# Thu, 13 Jun 2024 07:18:05 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 13 Jun 2024 07:18:05 GMT
ARG SWIFT_PLATFORM=debian12
# Thu, 13 Jun 2024 07:18:05 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 13 Jun 2024 07:18:05 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 13 Jun 2024 07:18:05 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 13 Jun 2024 07:18:05 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 13 Jun 2024 07:18:45 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg
# Thu, 13 Jun 2024 07:18:57 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1c490141db05c38862fb96b5657884aaf9d8eba5b3a836328800489d780619`  
		Last Modified: Thu, 13 Jun 2024 07:21:09 GMT  
		Size: 186.3 MB (186251616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fa539db73d88616d3a24b7c29e504b747efe6f0c329089b79152537e610d8a`  
		Last Modified: Thu, 13 Jun 2024 07:21:52 GMT  
		Size: 617.2 MB (617214325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1e7d5ea66dd9582a1d0a3521a102b852ae92a925d97603b37c6dc899fbcc08`  
		Last Modified: Thu, 13 Jun 2024 07:20:51 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
