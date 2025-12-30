## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:ebf0850554e909e42d8a2d2d3ec486a806101b0538edae5e611becf10e120795
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:9b56244e8d46321b74222e84bf6c0e10fb78f2c837b54d5be4febacf2c0a5e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.2 MB (122169532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8556f7777a7e6d2cbd47ef34dc788723031ab6fe8101728005eab578041c931a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:48:47 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Dec 2025 00:48:47 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Dec 2025 00:48:47 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:48:47 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Dec 2025 00:48:47 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 30 Dec 2025 00:48:47 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Tue, 30 Dec 2025 00:48:47 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Tue, 30 Dec 2025 00:48:47 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Dec 2025 00:48:47 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Dec 2025 00:49:18 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:32a5bf163bd75109aaa8d446f1570117432475cbb2df3fb6f89dd243bcedd1f3`  
		Last Modified: Mon, 29 Dec 2025 22:26:43 GMT  
		Size: 48.5 MB (48480796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff29d67efd032bcdf6ad7ac587a8f5679c9caa47cfdc9dbcdbc5dda00d1af63`  
		Last Modified: Tue, 30 Dec 2025 00:49:41 GMT  
		Size: 23.6 MB (23630728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80993fd127f9df0d89b4391bccdffe744091e1a646b5d698033c3d95a22f1304`  
		Last Modified: Tue, 30 Dec 2025 00:49:44 GMT  
		Size: 50.1 MB (50058008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:13069f6015cac651876ba961b4a6c7e94efb1c78d71dff2a4e282ab38f37afc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6918b44f756df719b93e5bd1d0f2a1ea16d657a3d3c11080f6c2c7ad2fbf7264`

```dockerfile
```

-	Layers:
	-	`sha256:e437d4d50b4858a0ee3cda1f7dfd943fe07be2aa266c89881e7c59e47ba3ff30`  
		Last Modified: Tue, 30 Dec 2025 02:48:54 GMT  
		Size: 4.2 MB (4156329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:331058711d8030ba4326b70c8331a9fcacf33b74446b1e21ce3cf20a5960a618`  
		Last Modified: Tue, 30 Dec 2025 02:48:54 GMT  
		Size: 13.9 KB (13926 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:2df0bde32023bd5518257ccd1ae847e8a8c3c3bd1b2e5d553fba96ab088a4c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121271637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958761daf2a61630b2c45679a2a622ad9445267998726942f17ef0c150b50e32`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 00:53:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Dec 2025 00:53:15 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Dec 2025 00:53:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 00:53:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Dec 2025 00:53:15 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 30 Dec 2025 00:53:15 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Tue, 30 Dec 2025 00:53:15 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Tue, 30 Dec 2025 00:53:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Dec 2025 00:53:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Dec 2025 00:53:54 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:bc82f51ad2e6d256131f87c3aebb045333f03c39e64a6b4985cc9e6ea5602d4d`  
		Last Modified: Mon, 29 Dec 2025 22:26:42 GMT  
		Size: 48.4 MB (48359147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30af924462e93a395fc80356dd77a5478e054b8f56bcd964e76a0f0bb061134`  
		Last Modified: Tue, 30 Dec 2025 00:54:16 GMT  
		Size: 23.4 MB (23449899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60f0876f11e3d20b6ee05ba3a8f18266465e7c3ddf4471b9ec1fefbac06efb0`  
		Last Modified: Tue, 30 Dec 2025 00:54:19 GMT  
		Size: 49.5 MB (49462591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:27abfb6d3371d6ec519b9e768bb59e36ec06dc6ea1803348b4c9489cf4efe2fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84273953146bb07c2ac3538018389230af0bbfa18d0109456a85f3b65d9556ac`

```dockerfile
```

-	Layers:
	-	`sha256:575d11d6276953eb35165112179492b38d76727a4e731053ed202f25db5e2c20`  
		Last Modified: Tue, 30 Dec 2025 02:48:59 GMT  
		Size: 4.2 MB (4156606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:490e381e898690c0dced20338da1bf62124a0176239316ab658a46f0f3191b54`  
		Last Modified: Tue, 30 Dec 2025 02:49:00 GMT  
		Size: 14.0 KB (14033 bytes)  
		MIME: application/vnd.in-toto+json
