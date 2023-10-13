## `swift:focal-slim`

```console
$ docker pull swift@sha256:80e9d1eb86afde449861e6c0adfa4b05906c656f4a1bc3d61e571651a90b1ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:focal-slim` - linux; amd64

```console
$ docker pull swift@sha256:2da3de2ffc75c866c5b462aa0c8d70df769ee066a5fa7f9e4938657774973b27
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88667619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea96d18c237e502f436713aefd923bc4be6cb522ce471e0fb0d9b8c39cd200d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 06:24:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 13 Oct 2023 06:24:42 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 13 Oct 2023 06:24:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 13 Oct 2023 06:24:55 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 13 Oct 2023 06:24:55 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Fri, 13 Oct 2023 06:24:56 GMT
ARG SWIFT_BRANCH=swift-5.9-release
# Fri, 13 Oct 2023 06:24:56 GMT
ARG SWIFT_VERSION=swift-5.9-RELEASE
# Fri, 13 Oct 2023 06:24:56 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 13 Oct 2023 06:24:56 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.9-release SWIFT_VERSION=swift-5.9-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 13 Oct 2023 06:25:55 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cc847ff18a772fbf1961e07e509d4867e128101e4cbb090a169f61a86cfbea`  
		Last Modified: Fri, 13 Oct 2023 06:47:53 GMT  
		Size: 22.3 MB (22272467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee66493f7f5a31da1cccd3c6dd99fbdf9af92ff62b9669dc4edebb43f0f9d7ad`  
		Last Modified: Fri, 13 Oct 2023 06:47:55 GMT  
		Size: 37.8 MB (37814471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:focal-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:5bc46167383f145ce2cf941cac1dd7dffb28aebd7180e000157d9c11e28765ba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.5 MB (86541708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13ce8599f6fd079bc5d2f9e0f2dba063f13c21b68082a10dc2bb266f0d2f5d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 03:14:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 13 Oct 2023 03:14:10 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 13 Oct 2023 03:14:24 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Fri, 13 Oct 2023 03:14:24 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 13 Oct 2023 03:14:24 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Fri, 13 Oct 2023 03:14:24 GMT
ARG SWIFT_BRANCH=swift-5.9-release
# Fri, 13 Oct 2023 03:14:24 GMT
ARG SWIFT_VERSION=swift-5.9-RELEASE
# Fri, 13 Oct 2023 03:14:24 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 13 Oct 2023 03:14:24 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.9-release SWIFT_VERSION=swift-5.9-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 13 Oct 2023 03:15:01 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58948de8374ff3a1caca001c705ae0a34b2aa7ac3e271a23b37be15738a58e46`  
		Last Modified: Fri, 13 Oct 2023 03:27:37 GMT  
		Size: 22.1 MB (22068348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2a7febb7fc6c87a8ad3e495bee425703f9a8ff89dcbb6b7309d13179fd11a4`  
		Last Modified: Fri, 13 Oct 2023 03:27:39 GMT  
		Size: 37.3 MB (37273857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
