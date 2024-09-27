## `swift:focal`

```console
$ docker pull swift@sha256:856e087ac8bd0a14ba069792074891cb8d5058885373e512df4a79b1213b2b4b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:fd90e159f132d8f6ebaf05f87c984640ea210869b683830c4497e4e6d726e22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **973.5 MB (973480683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:094167fb29e74dc9f3a33dddfb37aa07c01f5d86a91f55f8d0cc096e183273a9`
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
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:602d8ad51b8130f3fcd71cb936dea612ebc799666136abf2e5914585b3178a4a`  
		Last Modified: Tue, 13 Aug 2024 10:23:50 GMT  
		Size: 27.5 MB (27511769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0e842a0e4bc243ae338c9da147e7faf57e4e62ecb5a5c8931824cf4a3b6bd8`  
		Last Modified: Thu, 26 Sep 2024 22:59:22 GMT  
		Size: 120.6 MB (120555107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b73c31a0c2704331f004f055c5c611fa9845968a9d5309cda5479affd7519bd`  
		Last Modified: Thu, 26 Sep 2024 22:59:31 GMT  
		Size: 825.4 MB (825413634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b41c9034aa0fb0b2c4abfe226e15328af6a9398f4d61747f49c1eef312f07fb`  
		Last Modified: Thu, 26 Sep 2024 22:59:20 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal` - unknown; unknown

```console
$ docker pull swift@sha256:4ce71fd4329af8ec37ec0381ac8f4949abe913e5abf967670c4b82574768c49c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7687970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd7e9c6f8fc4ec82ea265dada19ac07003e070d61a9bd68f207562b7bebe2fb`

```dockerfile
```

-	Layers:
	-	`sha256:2801a5da3bc1127153dbae7e13ebcd9294acf8ad35477a2ae94ed8a1480a7c8a`  
		Last Modified: Thu, 26 Sep 2024 22:59:20 GMT  
		Size: 7.7 MB (7672360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d55c80fcc26666c303d68002999367594c5143157e75918980bf295c90bc282d`  
		Last Modified: Thu, 26 Sep 2024 22:59:20 GMT  
		Size: 15.6 KB (15610 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:focal` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:dd64eaf2a93c057b9f60b3e50cc3bdb6e04bddada8a5eb47fd2717b38989ffa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **964.7 MB (964709345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07ebfd860a428c78cf282d56424fdaf9af44ecbaa005194583f82a21bf6d9132`
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
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
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
	-	`sha256:399e1b2248c640260102deed99977f6068e5d969b04ad7cb93392cde1c14dfdf`  
		Last Modified: Fri, 27 Sep 2024 07:44:21 GMT  
		Size: 821.4 MB (821447581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ba637b9ceb995290edca64da84358b968f2d998b5e720d1292a3b27fed80b1`  
		Last Modified: Fri, 27 Sep 2024 07:43:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal` - unknown; unknown

```console
$ docker pull swift@sha256:d804c26d63b2bb43fea98eea702b201e20af5634c97489d1dffa325b4ce772d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7686249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44b7afe2658eb79ec01498f5bb7b6824db8d719e55a91ec84d784705194700c8`

```dockerfile
```

-	Layers:
	-	`sha256:3f4e0e61b2eb42fe91a365e0912743b08f022da06dc96e128684b3b79497a2ff`  
		Last Modified: Fri, 27 Sep 2024 07:43:58 GMT  
		Size: 7.7 MB (7670349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ef4e0a955a2a673cb1de08d891a2b377f663dcbde213452fefcc84162ce27e`  
		Last Modified: Fri, 27 Sep 2024 07:43:57 GMT  
		Size: 15.9 KB (15900 bytes)  
		MIME: application/vnd.in-toto+json
