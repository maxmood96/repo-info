## `swift:focal-slim`

```console
$ docker pull swift@sha256:b35f69bf97517f5c0b5fcdeb594c2414b253be807481049232181a5eef00e18a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:focal-slim` - linux; amd64

```console
$ docker pull swift@sha256:ab2bccdd83934f5e972e96894b8b782911999ba92593c89aae130ca920a0e090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98704802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7404e7841afd933cb5f4a957b11c38181256135e7b7afa40d662897110b7b576`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
ARG RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Apr 2025 00:12:10 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c149ff17a351b40697b27e1f71f8183dc29241c753a689fa0b300ae2c73e0c16`  
		Last Modified: Wed, 09 Apr 2025 01:23:07 GMT  
		Size: 22.3 MB (22292879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373fbae24e5a0b3753b316ad62520b8aaa8144012e95f36ad2839aa349dfbb57`  
		Last Modified: Wed, 09 Apr 2025 01:23:07 GMT  
		Size: 48.9 MB (48901529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal-slim` - unknown; unknown

```console
$ docker pull swift@sha256:fd5b103db6b3e37684a437725d888944174dab4007c95001d7f5d10c6aa21f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2946315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e4174ecfd8946e7bf9c56fea199543cea82cdf5f04228a25775a8a9a93ed7b`

```dockerfile
```

-	Layers:
	-	`sha256:f13decf983cc6dba31a9a556417728d6e899d235e82d789a0d848530b56b2e1c`  
		Last Modified: Wed, 09 Apr 2025 01:23:06 GMT  
		Size: 2.9 MB (2932345 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4505337f9b9bfdbc040dca9503c8bf5b028b36b32c0a726b8637244aa7f8f551`  
		Last Modified: Wed, 09 Apr 2025 01:23:06 GMT  
		Size: 14.0 KB (13970 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:focal-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:b7b3ae883141050a27168f85f21e2c6390cc3eb90a897fc23231b9ad07c1422e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96537463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507326c60879b8dae6cc3e6ae4c234b133ebeff4f55d19f874ffca6369dba1b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bcc1fe662d5e3c01874c14b7b5f75930ae1bc8d50b459e1172bf6efae54d1d`  
		Last Modified: Tue, 01 Apr 2025 17:30:59 GMT  
		Size: 22.1 MB (22069759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc26a46705f880bbfcd03b1b57d9a05905a992b9ae0f85c27c9197d4a8e078f`  
		Last Modified: Tue, 01 Apr 2025 17:30:59 GMT  
		Size: 48.5 MB (48493876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d6e6bbc542e405ffacde56f9edc2cbe5468cbe2055605491d2250b6b373ac36b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2944794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9ed610f1eb2b64322a15c0673e8e07d89361dd7f614911767c52b01666d39e`

```dockerfile
```

-	Layers:
	-	`sha256:38fc0dc099441246f383261442911af83cfb8cd9e7cfa1e14bb82849cdf598e5`  
		Last Modified: Tue, 01 Apr 2025 17:30:58 GMT  
		Size: 2.9 MB (2930716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db9615a1532a76fc6be35b9699128dcc10d1ef3b08f002bf10985f730d884406`  
		Last Modified: Tue, 01 Apr 2025 17:30:58 GMT  
		Size: 14.1 KB (14078 bytes)  
		MIME: application/vnd.in-toto+json
