## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:af5650f39f726917714263ecf107664a9cfafd5d2f445ceecdbe817aac182065
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
$ docker pull swift@sha256:7ff2157455bdf1eda6e4581eec6a94fb532d5ab9d3736e1fbaa9e4cf97060603
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122443493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a45088b8ab2501e4ccd8ec038abfa99a15e4218690c7786cc7c585c411f7d2f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:16:51 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 22 Apr 2026 02:16:51 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 22 Apr 2026 02:16:51 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:16:51 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 22 Apr 2026 02:16:51 GMT
ARG SWIFT_PLATFORM=debian12
# Wed, 22 Apr 2026 02:16:51 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Wed, 22 Apr 2026 02:16:51 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Wed, 22 Apr 2026 02:16:51 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 02:16:51 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 02:17:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77bdcda23f8c7a54b81c1e567a2355452a01e7806e755ece91f784037ca2d724`  
		Last Modified: Wed, 22 Apr 2026 02:17:46 GMT  
		Size: 23.5 MB (23456203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc15fda02a38bdcd713b84dc20c60e2b44ab0054cc7f563254cc67ed007e736c`  
		Last Modified: Wed, 22 Apr 2026 02:17:48 GMT  
		Size: 50.6 MB (50614219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:0be18a9b6a57e3564daa620e298a01345d4c7413265548d9e041405a1bc9d5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d271c96eb4e849861962f8f0f88de5d7fb2d10787279edae2e5911214b64b970`

```dockerfile
```

-	Layers:
	-	`sha256:6d960c35738b9b97b4042bc4765370b4a5716b4d6bccb2c7e00ddab7a1d54ce1`  
		Last Modified: Wed, 22 Apr 2026 02:17:45 GMT  
		Size: 4.2 MB (4157249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d245b8e5fc68c44278675ec5a4ae098fea172d99a56596db290c3edbedbcf9ca`  
		Last Modified: Wed, 22 Apr 2026 02:17:45 GMT  
		Size: 14.0 KB (14033 bytes)  
		MIME: application/vnd.in-toto+json
