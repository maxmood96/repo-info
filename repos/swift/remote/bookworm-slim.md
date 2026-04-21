## `swift:bookworm-slim`

```console
$ docker pull swift@sha256:dbbd75cfbdcd24927793afa1791e602cbd49900db9fe72c129518ed3ae9cdd42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm-slim` - linux; amd64

```console
$ docker pull swift@sha256:cec87222f26cd2bd3902cf9cf7eb011210867ab28eae7a628521c4b9173c2f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.5 MB (123467215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500b2b3edfddd8602f776b8cc879c700e899e626e149504d8cd4ae1b6d996842`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Mon, 20 Apr 2026 21:52:30 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 20 Apr 2026 21:52:30 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 20 Apr 2026 21:52:30 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 20 Apr 2026 21:52:30 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 20 Apr 2026 21:52:30 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 20 Apr 2026 21:52:30 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Mon, 20 Apr 2026 21:52:30 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Mon, 20 Apr 2026 21:52:30 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 21:52:30 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 20 Apr 2026 21:53:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
```

-	Layers:
	-	`sha256:c150dd3f5fc91eabd1818cc30298a4a956782621583cadfd369c4d327584008e`  
		Last Modified: Tue, 07 Apr 2026 00:10:26 GMT  
		Size: 48.5 MB (48488823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c126aadc59260a61294a64384430f380daa742e732f5ef59ccf8874ad621f6`  
		Last Modified: Mon, 20 Apr 2026 21:53:29 GMT  
		Size: 23.6 MB (23640168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04e5e1c86c0d1cbfd1cb3525f86c3c1cd3ec699ad1d9202931dda160008ae82`  
		Last Modified: Mon, 20 Apr 2026 21:53:30 GMT  
		Size: 51.3 MB (51338224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm-slim` - unknown; unknown

```console
$ docker pull swift@sha256:ec0ef4bd0f3715ea404348567c7ac649e136f174d04ef19411256f0bbbe26f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4170898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c12396fa17364fe75773d388365f8e6a5361bb67ec3dc2c4d388f796535332c`

```dockerfile
```

-	Layers:
	-	`sha256:321275b419a697e0182a9425f75d96632a95f7c2a61c75afff24c63c88406ce7`  
		Last Modified: Mon, 20 Apr 2026 21:53:28 GMT  
		Size: 4.2 MB (4156972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea291558c1d5370c2effd79cd079f4a4112f79e92d27b56fa19eb64c14cbd7d8`  
		Last Modified: Mon, 20 Apr 2026 21:53:28 GMT  
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
