## `swift:bookworm`

```console
$ docker pull swift@sha256:3d61981cc7a82ec3b8f17f942d71adfbcc2c41d7c57c93ed3f9902c005ff0c4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:f64c88d73df967daea8ebb6e9585a31126d0e40a37d6867dcb821c3658af62c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276432390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bd314686e3956c6d455fc435dad474d61575492aca2bb8035f124bb829aea4`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 17:38:57 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Dec 2025 17:38:57 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Dec 2025 17:38:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 17:38:57 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Dec 2025 17:38:57 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 09 Dec 2025 17:38:57 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Tue, 09 Dec 2025 17:38:57 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Tue, 09 Dec 2025 17:38:57 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:38:57 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:39:46 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 09 Dec 2025 17:39:46 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9172659e84c8a69fe26af9d683bc183c452eb9fbe690af4b1920d5ce63f91142`  
		Last Modified: Tue, 09 Dec 2025 20:53:36 GMT  
		Size: 198.4 MB (198408999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb015bd6c38503a1728065c36ffac19456ffee3ee3803b6b756a3eac8ee29cd7`  
		Last Modified: Tue, 09 Dec 2025 17:43:16 GMT  
		Size: 1.0 GB (1029542481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ad935de85f3ce920856b08298eb25ea9259d0e2d11af78298ca813c751a920f`  
		Last Modified: Tue, 09 Dec 2025 17:42:37 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:4d026ab416f8c267f52166f1071ae38cc87e634a91df1acc6f84ff92417002a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11330045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02e40384e2d04c6bc3934902d8118f63fc01a9b326fe96b3a1ae218d07634b5`

```dockerfile
```

-	Layers:
	-	`sha256:b90a153ebc22530b121139bc0582c9424bde2bda2e35b3e1d012e51bbea8dff6`  
		Last Modified: Tue, 09 Dec 2025 20:48:17 GMT  
		Size: 11.3 MB (11314322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8ba84b04cab3a4f7d7a083835e179178e312d46e6d50eb139ba1380639a67f`  
		Last Modified: Tue, 09 Dec 2025 20:48:18 GMT  
		Size: 15.7 KB (15723 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:a07c113f23bf3430468bedd6d068bc08d548da3d48858c264d4dba70933cedc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1262501041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ecd0af661613083f28a6a730f96e35f9ea4b17bdc1bb9e388b7be155b04130`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 17:38:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Dec 2025 17:38:37 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Dec 2025 17:38:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 17:38:37 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Dec 2025 17:38:37 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 09 Dec 2025 17:38:37 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Tue, 09 Dec 2025 17:38:37 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Tue, 09 Dec 2025 17:38:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:38:37 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:39:27 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 09 Dec 2025 17:39:27 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cc2af345c0592febb07e6f21f2e54a7d3c0772fef7416f3e538283b9c27079`  
		Last Modified: Tue, 09 Dec 2025 17:42:17 GMT  
		Size: 190.3 MB (190315194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fee291a53188757c8b1c6f368114f95c43094f48b8b6ca9b1edd2f9dd11f79b`  
		Last Modified: Tue, 09 Dec 2025 17:42:16 GMT  
		Size: 1.0 GB (1023826604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1d2c4d4b11ec40a3392546e6c6949b400b8d59782900b3600e54279affa11e`  
		Last Modified: Tue, 09 Dec 2025 17:42:06 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:4d1d73624f9737aefe3b98f83571b2b9d46199fd1b292d309c7ef20c70a7d612
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a050eac2f3ebfbe6550a02c8b2ce682396b066591fa1c7ec3a360ed43b195d04`

```dockerfile
```

-	Layers:
	-	`sha256:3d91bdcf96e0cfbbeb2eca095523c1d4b41a346743d1143c92bd6c17108be230`  
		Last Modified: Tue, 09 Dec 2025 20:48:27 GMT  
		Size: 11.3 MB (11342327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c19968c3cff18b912fd9785341c2bb6c55e6093a1c83a0114d8e374f0d31a03`  
		Last Modified: Tue, 09 Dec 2025 20:48:28 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json
