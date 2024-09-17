## `swift:focal`

```console
$ docker pull swift@sha256:4c8bca3b113e46cdb31c550f77e73b00ec6dc7ce9e2cd6002710f5e04476e0e7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:4396a0f3fd247fc3fb437cb3cf8e63ce4861883dc81b1d14587a34e3ed615efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.4 MB (973435853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f53cbd19f3fdf636aa49ddc145dbdbce73a4be2e3ff9a0a4206a696d81a1f705`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:26:46 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:26:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:26:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:26:48 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Tue, 13 Aug 2024 09:26:48 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830c1a0540854d8c91d8765a6cd99886da76619c80d9874a036039b474b9156b`  
		Last Modified: Tue, 17 Sep 2024 17:01:12 GMT  
		Size: 120.5 MB (120543644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac531c64f1b633b3afc84ff1b53a933d82d914c2bfd25c659149a49b4ae4e91b`  
		Last Modified: Tue, 17 Sep 2024 17:01:27 GMT  
		Size: 825.4 MB (825380266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac7faba1184624209a2574e1645f512818f16c9418127c8f5a5d776ca1ec557`  
		Last Modified: Tue, 17 Sep 2024 17:01:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal` - unknown; unknown

```console
$ docker pull swift@sha256:716cd621893dbfc881fb0e896f29f636e73c86601ec8a8703ba4ba530ccf74bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7682048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b2c606131b29d7911ef908529e475cf25eca4aa590c32e589f31fa8e71c5c6`

```dockerfile
```

-	Layers:
	-	`sha256:5075c9813da4b219bfb91f5e1e67dff4b92edcf9dabeaf6f43cc2a1c103c7ef8`  
		Last Modified: Tue, 17 Sep 2024 17:01:10 GMT  
		Size: 7.7 MB (7666453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:897aff4af7d44b95b00fd731a8e8d328c12d2b80d0aa85574d4d86c1540e6360`  
		Last Modified: Tue, 17 Sep 2024 17:01:09 GMT  
		Size: 15.6 KB (15595 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:focal` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:762a584d9f8a0c9215485b3560a8492bfb0867bd2f6d14f75541a8c9b537941d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **964.7 MB (964703436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45941cbae8712ba4bd0f12ef9269e0ae8dffbf1c12644ada03e8378f1d874454`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 13 Aug 2024 09:27:56 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:27:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:27:56 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:27:58 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Tue, 13 Aug 2024 09:27:58 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:6a1df50fc4815789598fa24d3ecacb70451e506447ab9e45665024b9f3f0233b`  
		Last Modified: Tue, 13 Aug 2024 10:23:55 GMT  
		Size: 26.0 MB (25974217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98149563259ac1700930eb06be2fb02ec2696606f99cc35f2e84e21f002050f1`  
		Last Modified: Tue, 17 Sep 2024 17:12:42 GMT  
		Size: 117.3 MB (117287373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0fdc28eac6c8677522eeef233d5a280960ad465cb982ffc6b4ae17f469cb82`  
		Last Modified: Tue, 17 Sep 2024 17:12:56 GMT  
		Size: 821.4 MB (821441672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27bd0b696c4b48e849fc232635784d9b45d63653ac64b416598501bd7fa5836`  
		Last Modified: Tue, 17 Sep 2024 17:12:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal` - unknown; unknown

```console
$ docker pull swift@sha256:36ec19e30f386ce4f4d37b82cbabd5f3729d89ad86bbb8afe2dff189fad99f67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f3feb6a174859fd71b3d23cccba57505e3e4b429cc1af3239a0220f85d33d5`

```dockerfile
```

-	Layers:
	-	`sha256:76b0591cdfd0d24585f4991e113e1a6b29bea3b1effdac4680117e7f2a3ff7d4`  
		Last Modified: Tue, 17 Sep 2024 17:12:40 GMT  
		Size: 7.7 MB (7670332 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be6576f9828563eeb36ffbd39e04ffcbb3c27e656fb565021ac5a743ed152efd`  
		Last Modified: Tue, 17 Sep 2024 17:12:39 GMT  
		Size: 15.9 KB (15884 bytes)  
		MIME: application/vnd.in-toto+json
