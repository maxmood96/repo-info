## `swift:bookworm`

```console
$ docker pull swift@sha256:81217e6ebc390e0201210cf46c9a787c7f5fcaff902730880ee5e464a1c9a3de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:5ada4fd51acddbeac573d35c59a83325b1899ef1b4061e6918f1191317751ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1276375779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1fd2df737dd0daf3fffa29cdb6530a40ea018f247067dfe838504a05626411`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 22:26:18 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 22:26:18 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 22:26:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 22:26:18 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 22:26:18 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 04 Nov 2025 22:26:18 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 22:26:18 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 22:26:18 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 22:26:18 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 22:27:01 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 04 Nov 2025 22:27:01 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5276a1db9970f471126d61538a6a7dff31d34b66a92167dc8d201afb78016d`  
		Last Modified: Tue, 04 Nov 2025 23:54:47 GMT  
		Size: 198.4 MB (198400387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2d7caec2027ec60f4a38f86f3621a8b65394bd890bcecc41645505add2ceb8`  
		Last Modified: Tue, 04 Nov 2025 23:56:04 GMT  
		Size: 1.0 GB (1029494162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0922b4b42f781ac524c0d2139ce13572903715c900650b8dd941941689f4cee1`  
		Last Modified: Tue, 04 Nov 2025 22:29:50 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:dcca8b807f74214f3d30db662b0430470af9340b8180972c0576a69ef54aaafc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11330045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1a9912ba3ef170441ac5e4e971e7bc5aaae3ab2334fd3aa9f56aae85323b53`

```dockerfile
```

-	Layers:
	-	`sha256:a55a7672e120a2f6f49b2e3c22607dc7c47e870a9621babafa436e65832caa20`  
		Last Modified: Tue, 04 Nov 2025 23:48:02 GMT  
		Size: 11.3 MB (11314322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:907f296b4c8ecc88fa8a586537051802c0ff8e1bbddbee10e168b4cca4dd4689`  
		Last Modified: Tue, 04 Nov 2025 23:48:03 GMT  
		Size: 15.7 KB (15723 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:57e91be08a9f18c29e9f46dbb1a591eaed5fd7f83e1039eda82c08b616b10e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1262467563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb67b8d237bf1a30c2092fa22534b7c2ca9a5dc22916725e876a69f2513f063`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 19:24:16 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 19:24:16 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 19:24:16 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 19:24:16 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 19:24:16 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 04 Nov 2025 19:24:16 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 19:24:16 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 19:24:16 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:24:16 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:24:59 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 04 Nov 2025 19:24:59 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5ff700e50189a7194c8f8d910f3054007f279a4dad57eeb91047bbb035dd8c`  
		Last Modified: Tue, 04 Nov 2025 22:17:52 GMT  
		Size: 190.3 MB (190312730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5188938cda76c1731d839edcab379ceb755a5b0c047f1c7d37d0db5bcbabd514`  
		Last Modified: Tue, 04 Nov 2025 22:18:11 GMT  
		Size: 1.0 GB (1023795181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7a9e49b6ab3547cdd91629399f0ae11a4d51fb3332023dced88906b8f59d88`  
		Last Modified: Tue, 04 Nov 2025 19:27:32 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:882fec6dbace6eb9d22d9d994dc52e74288d76949dcf1496fd23ea04cfd73b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d7d5503cba9dabd90210d2b8c034d7cc1b5552ee4b4fe3ade3f9eee2410151`

```dockerfile
```

-	Layers:
	-	`sha256:41d4c6a9a4dd84b5ada4d7d1dd7ec455546b2ca59cbdd7be6510966b9517b7fd`  
		Last Modified: Tue, 04 Nov 2025 20:48:10 GMT  
		Size: 11.3 MB (11342327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa458a81fdcd29de289914298e45901bfd4e49aa7de1e990481abb26f7877182`  
		Last Modified: Tue, 04 Nov 2025 20:48:11 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json
