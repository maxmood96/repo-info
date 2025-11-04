## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:955272f2f8721e9b1d1510ab68fd200ad54aaa26e62aa04ead8ba6e740290d63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:369feb3cc151bddcac54f775f698ed6a1f96ec6c5f655abd94116cad9a96ea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122169401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b0f898047d8d54937e512292b478caa03943099b75eb357c2eff5a88eec34e5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:49:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 00:49:22 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 00:49:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:49:22 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 00:49:22 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 04 Nov 2025 00:49:22 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Tue, 04 Nov 2025 00:49:22 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Tue, 04 Nov 2025 00:49:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 00:49:22 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 00:50:01 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:5d93aea697980315f27f81c68582d14f63dd3579c2d3a27dc495a588279eda20`  
		Last Modified: Tue, 04 Nov 2025 00:12:20 GMT  
		Size: 48.5 MB (48481056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452546cb79f9d4714a4b1c270c96174e4d7289530236fbe2e9da594bcd9849de`  
		Last Modified: Tue, 04 Nov 2025 00:50:29 GMT  
		Size: 23.6 MB (23630797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a35a00b4c0e28e28d3f0ba9981aaa564fb75192ede4b43c7eba9af14693dfd`  
		Last Modified: Tue, 04 Nov 2025 00:50:35 GMT  
		Size: 50.1 MB (50057548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:a654cbe3b828587eb60c3ec6a7bb80c1f7b14847fc25202aaff0a2f599d2a518
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cb064411841ff90fc68f7440c8b225e986802171b544ed54eaf7dbde07fea9`

```dockerfile
```

-	Layers:
	-	`sha256:ea22e2d805b135bd49702adc3d4a68caf0db57c4b21c1d75379ea3b5b3bb778b`  
		Last Modified: Tue, 04 Nov 2025 11:48:31 GMT  
		Size: 4.2 MB (4156329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17eb3cd4bda5cc5ba1503973b6caf44a9d5a81dce22cded7cc1011c1ef46d9f5`  
		Last Modified: Tue, 04 Nov 2025 11:48:32 GMT  
		Size: 13.9 KB (13917 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:e2fe32990acfa1f04755c8e5df724767f314ee662866a7ee25a970c864407371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121273668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6925b9e56684d6783886e4606ecd7998b1954e0173f8ebb2daaa25ec4351428f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:49:33 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 00:49:33 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 00:49:33 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 00:49:33 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 00:49:33 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 04 Nov 2025 00:49:33 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Tue, 04 Nov 2025 00:49:33 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Tue, 04 Nov 2025 00:49:33 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 00:49:33 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 00:50:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:b81c3047c0240876c5be21e30ab0bb3930d31a1fc064a5cfe3b73eaec871a74c`  
		Last Modified: Tue, 04 Nov 2025 00:12:55 GMT  
		Size: 48.4 MB (48359478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e962d04c1e35ecc35eaa2101c6e98aaa8f5dabca71e3476b918a6f9ca1801a`  
		Last Modified: Tue, 04 Nov 2025 00:50:44 GMT  
		Size: 23.4 MB (23449889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7163240e84d2ad11c0bf6007f83168bcc1b4a5c8b425be6f6533088b7e03539d`  
		Last Modified: Tue, 04 Nov 2025 00:50:35 GMT  
		Size: 49.5 MB (49464301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:3e078b0225101e88647162c67371abf7725bc538c3088d1c2f9014b7d5f78764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39f539eb98827c62a2e4b16f5a3c47ee95ff2ea56e4e5f390e60bcb3e215b55`

```dockerfile
```

-	Layers:
	-	`sha256:df103ce0e9726005cb11521173775695c48b01968258dc9ab8ef476618fd2e4b`  
		Last Modified: Tue, 04 Nov 2025 11:48:42 GMT  
		Size: 4.2 MB (4156606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0f8037cb8808a61e5210dda424bc7fd7d4357bd6ad982f7d88590c2b0631a85`  
		Last Modified: Tue, 04 Nov 2025 11:48:43 GMT  
		Size: 14.0 KB (14025 bytes)  
		MIME: application/vnd.in-toto+json
