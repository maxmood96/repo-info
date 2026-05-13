## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:3c7aeadc4fffb920cec2855c070ce354fe22158eca009da8c1a22da63eae1910
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:5c77b8fdddc54c79501a19380b6bdec433870ec8518c70ed7654e573e620ccdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123467044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e55128fe3a90bde18ea926d9f41523f6add1b681739b526731f41fd71931a9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:12:17 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 08 May 2026 20:12:17 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 08 May 2026 20:12:17 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:12:17 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 08 May 2026 20:12:17 GMT
ARG SWIFT_PLATFORM=debian12
# Fri, 08 May 2026 20:12:17 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Fri, 08 May 2026 20:12:17 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Fri, 08 May 2026 20:12:17 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 08 May 2026 20:12:17 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 08 May 2026 20:12:59 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:9104793a826a01456b0ba567a92064e85a029816661fbb4524da7913f0123ab5`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 48.5 MB (48488676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4f12ae4779377c2c479bf41af06ef4e1c15a302027b1a9d16aee8f2a37cedc`  
		Last Modified: Fri, 08 May 2026 20:13:14 GMT  
		Size: 23.6 MB (23640172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f809d9113f5d131dabad61076109454feb420af5b8ad6deb2298209763749d`  
		Last Modified: Fri, 08 May 2026 20:13:14 GMT  
		Size: 51.3 MB (51338196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:953e33362ffc2f617d27e2f96b2b8f7cbf983436fbd6e3aaf76815e3135b65e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7670eafbe880970af29984c51051e15a743aa50bd1eb0bf432dedc60260282f4`

```dockerfile
```

-	Layers:
	-	`sha256:21385be506f029998141178cf3f0319a63dfe78e510fa8b3c0f833740dc49e9a`  
		Last Modified: Fri, 08 May 2026 20:13:13 GMT  
		Size: 4.2 MB (4156972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35485cac29b6fdafa903c0129733d85f2f2e19f9eb72235dfbf606b02a3b515e`  
		Last Modified: Fri, 08 May 2026 20:13:12 GMT  
		Size: 13.9 KB (13925 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:62f89a3b257c8b6da1431a2c9fe8ea13d8f541f5a143cd855c7b0d8b626c7117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.4 MB (122375842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a1fc8e201f10d43d201dd83ba87b2e4ccf6c74cdf61e79f9ebdea36b350673`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Wed, 13 May 2026 18:04:36 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:04:36 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:04:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 13 May 2026 18:04:36 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:04:36 GMT
ARG SWIFT_PLATFORM=debian12
# Wed, 13 May 2026 18:04:36 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:04:36 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:04:36 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:04:36 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:05:12 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878fe85b8c1e5ac023ebe0cf7e57d45c02e0799f5c2b7f4b9624cc0515b13248`  
		Last Modified: Wed, 13 May 2026 18:05:26 GMT  
		Size: 23.5 MB (23456193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0860a9aa939e05daf7877ded15cef7c8a98d47a7d91d49e8eccf1727bfcacda`  
		Last Modified: Wed, 13 May 2026 18:05:27 GMT  
		Size: 50.5 MB (50546499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:ee303b8697bd4e3609c688e5f644c4a6cf307de0fd9707c05253d86e968d3988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4171282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52941ab76d3195d2e537689b12c42d01b38efdfb77105c0b58e8f36ac9abdd58`

```dockerfile
```

-	Layers:
	-	`sha256:37b53d5881ba1ec0d4841ed82642773d4be27a87ef5d3a6efb286c058f88b574`  
		Last Modified: Wed, 13 May 2026 18:05:25 GMT  
		Size: 4.2 MB (4157249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:525c7dd6966846d7ed68188f377edca78700f7dbf57f1bc7a26906c2893cc95e`  
		Last Modified: Wed, 13 May 2026 18:05:25 GMT  
		Size: 14.0 KB (14033 bytes)  
		MIME: application/vnd.in-toto+json
