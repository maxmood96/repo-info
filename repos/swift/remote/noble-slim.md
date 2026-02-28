## `swift:noble-slim`

```console
$ docker pull swift@sha256:c264d87484a75761c5740c249844d53d0b62ce007cc4f37a40b96380dd69ae65
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble-slim` - linux; amd64

```console
$ docker pull swift@sha256:fb5dbc2b8e0102bfb484cf3fb192c9b6fedd4f2bd28004220c1af9829abd406d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99879307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e3362295f890900eb83fa9a58e3b9e05947fe6ac89f399d29e53f114847983`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:49:54 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:49:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:49:54 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:49:56 GMT
ADD file:1ae27d2ef4369361104b699712f3897141e394785df5d193d67b44626f57eb87 in / 
# Tue, 10 Feb 2026 16:49:57 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:43:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 27 Feb 2026 22:43:06 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 27 Feb 2026 22:43:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 27 Feb 2026 22:43:06 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 27 Feb 2026 22:43:06 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Fri, 27 Feb 2026 22:43:06 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Fri, 27 Feb 2026 22:43:06 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Fri, 27 Feb 2026 22:43:06 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:43:06 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:43:38 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:01d7766a2e4a62b74e0bebf2cd12c47e675e9221174f6570854203e84ffe68b0`  
		Last Modified: Tue, 10 Feb 2026 17:41:34 GMT  
		Size: 29.7 MB (29727611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4b8671d7b412015619cbfb159d191c38c5ec6ac317aa7a3079593828a4088e`  
		Last Modified: Fri, 27 Feb 2026 22:43:51 GMT  
		Size: 20.0 MB (20023969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8a98d65d74ad30ab25689c098d29e299a35fb9840b82c76911adf7e4969035`  
		Last Modified: Fri, 27 Feb 2026 22:43:52 GMT  
		Size: 50.1 MB (50127727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble-slim` - unknown; unknown

```console
$ docker pull swift@sha256:09e40796fc42f07779067ec18ed6249973b315b52f51e67e33115e582b1939a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2512068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7dbdd36de5e67d5bd3a51a0a732d0e85b19db21b987433aba301a7aeeeed3d4`

```dockerfile
```

-	Layers:
	-	`sha256:55ab5bb27cd7683692e279fa74b6c403caaa238f330d0e4c81485ab2bde70f86`  
		Last Modified: Fri, 27 Feb 2026 22:43:50 GMT  
		Size: 2.5 MB (2497230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:656a3a05c7cc6e7246b76d308bdd13985e8eabb2d1057bc67d2d90692f4f78e1`  
		Last Modified: Fri, 27 Feb 2026 22:43:50 GMT  
		Size: 14.8 KB (14838 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:e6fd6732cb27c0435ed85d5bbfb099c286c77eb2e7c35e9121304fd91602fbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98434839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2b0a5c0965a30d11ad2d80a8ade8927374ab395a7fa86997b40cccbac163b2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 16:52:26 GMT
ARG RELEASE
# Tue, 10 Feb 2026 16:52:26 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 16:52:27 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 10 Feb 2026 16:52:29 GMT
ADD file:25d708bf0b30ddee20c0b2764034e065aca922cafd48eb9c662e35ba02ccf1de in / 
# Tue, 10 Feb 2026 16:52:29 GMT
CMD ["/bin/bash"]
# Fri, 27 Feb 2026 22:42:01 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 27 Feb 2026 22:42:01 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 27 Feb 2026 22:42:01 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 27 Feb 2026 22:42:01 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 27 Feb 2026 22:42:01 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Fri, 27 Feb 2026 22:42:01 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Fri, 27 Feb 2026 22:42:01 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Fri, 27 Feb 2026 22:42:01 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:42:01 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 27 Feb 2026 22:42:39 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:66a4bbbfab887561d75f1fdb3c6221c974346f82c9229f5ef99f96b7e6c25704`  
		Last Modified: Tue, 10 Feb 2026 17:41:42 GMT  
		Size: 28.9 MB (28865120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066393625a098823322331f3f76cc6b21703c39186edbec06c2693187f16683c`  
		Last Modified: Fri, 27 Feb 2026 22:42:52 GMT  
		Size: 20.0 MB (20036834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad1f7f5f5e49fea539e328747e65a0bc1aae07de03486c153fddf4d0ae60029`  
		Last Modified: Fri, 27 Feb 2026 22:42:52 GMT  
		Size: 49.5 MB (49532885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble-slim` - unknown; unknown

```console
$ docker pull swift@sha256:9284623f8fc5925eaa519212525f27d0666386b8aaf92b62b9446268ee56ce2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2513327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2050e6214010653959afe2ff1c55fa1370db51504fa537e89ea255bea3eb76`

```dockerfile
```

-	Layers:
	-	`sha256:84280d1a2a8919feb474d75526497eca710d0a6f37f0d581855b3e5871711d16`  
		Last Modified: Fri, 27 Feb 2026 22:42:51 GMT  
		Size: 2.5 MB (2498346 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34b0337a6dabbb97e16e4a2087533871e05bcb15fd023d552b49b2a12c0cdc47`  
		Last Modified: Fri, 27 Feb 2026 22:42:51 GMT  
		Size: 15.0 KB (14981 bytes)  
		MIME: application/vnd.in-toto+json
