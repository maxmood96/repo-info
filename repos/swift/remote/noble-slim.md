## `swift:noble-slim`

```console
$ docker pull swift@sha256:4ff2897f61977087b6e1d740a80da5b79fb687821536ee54e62b27d364b5485c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble-slim` - linux; amd64

```console
$ docker pull swift@sha256:cf0a27b8cc76e73b3ddfa8292188458908a4f159a78c4a658384f5a1ff939a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99857859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6dd2359add8e3d1bc3353a9037e5a46f44e9ac3ff64c13c347228aeb24358c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Dec 2025 17:38:34 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Dec 2025 17:38:34 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Dec 2025 17:38:34 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 17:38:34 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Dec 2025 17:38:34 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 09 Dec 2025 17:38:34 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Tue, 09 Dec 2025 17:38:34 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Tue, 09 Dec 2025 17:38:34 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:38:34 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:39:06 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b669a870098d88d5f61ed84f18461bdbe206346e4cfdbc5990e200b8ba8a34da`  
		Last Modified: Tue, 09 Dec 2025 17:39:33 GMT  
		Size: 20.0 MB (20019100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f4d51193570b6f5ac1a6134cf3e13b71d6a84d0e520eb4a11c857c8298562b`  
		Last Modified: Tue, 09 Dec 2025 17:39:37 GMT  
		Size: 50.1 MB (50114071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble-slim` - unknown; unknown

```console
$ docker pull swift@sha256:7d8a06b38ffdac69fac1198ea389cb735658ea7167178c2b54faddc132bc3133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:348de120f962f650a306ea634256d3d0c568b01ef087447b06c640cd2b75c307`

```dockerfile
```

-	Layers:
	-	`sha256:56dd86dae49e2e06fadcfaaffa4a1d4d2ecf6e59d4f6526633610a1787265990`  
		Last Modified: Tue, 09 Dec 2025 20:48:45 GMT  
		Size: 2.5 MB (2497218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3dada3ffbc6122dac97fca8377e5962520bcd28336cb71f4a86e454da5f008d`  
		Last Modified: Tue, 09 Dec 2025 20:48:46 GMT  
		Size: 14.8 KB (14838 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:4811759b10f1e20f570df34b4230d3b490af4ae8fa17ec3eeac2e5117cc7f125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98422380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47823640307f39ade049b7b1ad9d986cbf91803c1bb293aedb6a34ba43c4c230`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Tue, 09 Dec 2025 17:38:03 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Dec 2025 17:38:03 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Dec 2025 17:38:03 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 17:38:03 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Dec 2025 17:38:03 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 09 Dec 2025 17:38:03 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Tue, 09 Dec 2025 17:38:03 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Tue, 09 Dec 2025 17:38:03 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:38:03 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:38:39 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d6cc05ff2e8087db3e973feb0f7e2f1db92e5803b48425666d74cff2645f69`  
		Last Modified: Tue, 09 Dec 2025 17:39:27 GMT  
		Size: 20.0 MB (20029391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0faf2e2bddba4cbb729ef787bed683fd54f2283d89bf0c7865e346a1d3ac0d`  
		Last Modified: Tue, 09 Dec 2025 17:39:29 GMT  
		Size: 49.5 MB (49531032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d4c9c624244a7697b088e349dfd26a706e872e4b77f751ef4687674dd8c5a677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf29fe5b2e13d193f69a07d0ef8947fa8f99616eccc858e9cbeca71061c7a65c`

```dockerfile
```

-	Layers:
	-	`sha256:fdb657644a5bf711d7752cb8850dd908b2b0cbde7b7f04794346317ecdf84b50`  
		Last Modified: Tue, 09 Dec 2025 20:48:50 GMT  
		Size: 2.5 MB (2498334 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7736b28599726b34577befa7078c36c2455a1fe505fc93e80c29853f41fccaff`  
		Last Modified: Tue, 09 Dec 2025 20:48:51 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json
