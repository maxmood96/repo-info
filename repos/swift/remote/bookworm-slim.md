## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:3ab6fd17bd4812df799cef2f17ab361d7a0363b7e35f99b3198f089ca0f51542
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:dc4a2ebb099dfeaf514b75696ed126bb2810afe76268d199ee1c4583f0af6901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123467007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7554120a47061fec28aa3749f8970d13889ade0102e88f69f7fede647512d62a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:13:18 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 22 Apr 2026 02:13:18 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 22 Apr 2026 02:13:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:13:18 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 22 Apr 2026 02:13:18 GMT
ARG SWIFT_PLATFORM=debian12
# Wed, 22 Apr 2026 02:13:18 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Wed, 22 Apr 2026 02:13:18 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Wed, 22 Apr 2026 02:13:18 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 02:13:18 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 02:13:48 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5f74e81b122d14f2344a3c2cdec252877604719961afcabf596f7789953ed`  
		Last Modified: Wed, 22 Apr 2026 02:14:02 GMT  
		Size: 23.6 MB (23640211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799005bf81f9ab0feb97bb47deedaba92793d32d1149e24a3f80b08ccadf8383`  
		Last Modified: Wed, 22 Apr 2026 02:14:02 GMT  
		Size: 51.3 MB (51338168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:f81c1287c6847d8857c353adf463fce86c0585d9b5759897e097e4c9e9144511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39bc49e0a5e4cc2cf0a7cd8dc8b67c5d409725083ca80df6e11ef974df4da931`

```dockerfile
```

-	Layers:
	-	`sha256:587dc4098a463f2a4df14633507aa0062da626685563501980239794f3c80bca`  
		Last Modified: Wed, 22 Apr 2026 02:14:01 GMT  
		Size: 4.2 MB (4156972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cd75e2b0d770c161409cc10cad32f18004be34cf9314670c9267a91ea35759f`  
		Last Modified: Wed, 22 Apr 2026 02:14:00 GMT  
		Size: 13.9 KB (13926 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f90deebbffaec1c64af12d3c21de1a2a44a5f3e2e485c3ffca3965a0d540b26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122443700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e194380fe4ee00d1abe4ca845beb16b3bcdbfe1015034b006bcbcb4937b39d7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Mon, 20 Apr 2026 21:57:46 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 20 Apr 2026 21:57:46 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 20 Apr 2026 21:57:46 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 21:57:46 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 20 Apr 2026 21:57:46 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 20 Apr 2026 21:57:46 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Mon, 20 Apr 2026 21:57:46 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Mon, 20 Apr 2026 21:57:46 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 21:57:46 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 21:58:22 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:d03e31a3f7ef0d2866d799846c3a18286fab6fcddbd8c523f3cb5ed1bd2f31a3`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.4 MB (48373262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74c6981370d2d971e52417ea905cfb9fad05e95a82f35ceaf564cae9ff969f4`  
		Last Modified: Mon, 20 Apr 2026 21:58:36 GMT  
		Size: 23.5 MB (23456235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad271bc9ed1a51914982ae8b82b7850f33ad5aa5a63294b524de55ff2052859d`  
		Last Modified: Mon, 20 Apr 2026 21:58:37 GMT  
		Size: 50.6 MB (50614203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:33b9a45c9ebb1174d0ba25d3977541f0c0820783da2f4e0d3fc6531d5d342893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd5b1ff7b1ed09c399218eb5a596a080a1a8c45fe87e3017f48fe50eeb37c18d`

```dockerfile
```

-	Layers:
	-	`sha256:ce9ba8fe8f08d89c915c4b19d71d1803cbe0c729effba6d31f2f001cab2d0242`  
		Last Modified: Mon, 20 Apr 2026 21:58:35 GMT  
		Size: 4.2 MB (4157249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03795b1cd1927373eab1b7dc430dcc2581aee4fdd0e41b7bd2b21c9abadcf89a`  
		Last Modified: Mon, 20 Apr 2026 21:58:34 GMT  
		Size: 14.0 KB (14033 bytes)  
		MIME: application/vnd.in-toto+json
