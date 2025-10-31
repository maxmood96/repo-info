## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:2ec5e3570c6ef7c3a6ebb7f281489630a1b813d0ab94a4be224df4c959421582
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:8428fcc36467f71f558d36b96ae0702d1fba1ec7004882c9f1933bd4f5da7720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282343943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1171b6bbeaec67e306b4003c2f6d31a5cbbf89e11fe9d5e3edfb15d689398c4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:13:29 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 31 Oct 2025 00:13:29 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 31 Oct 2025 00:13:29 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 31 Oct 2025 00:13:29 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 31 Oct 2025 00:13:29 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Fri, 31 Oct 2025 00:13:29 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Fri, 31 Oct 2025 00:13:29 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Oct 2025 00:13:29 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Oct 2025 00:13:29 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f221d78810acf36e0724b6a5034da40459992670ab220e53518cd4c7fc2688`  
		Last Modified: Fri, 31 Oct 2025 01:51:39 GMT  
		Size: 219.4 MB (219409875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d54f011337c87af422fe4fa6abcda60227c134c5590db696a69cb99511c0da14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130366e2cf199073e5ea2a2f414f581756abb632e29506b820b05a1a0fd19cd0`

```dockerfile
```

-	Layers:
	-	`sha256:1cc02f17f0b734c85ce199aa92717c8e4417d3640cde54d85323d3f6c7520919`  
		Last Modified: Fri, 31 Oct 2025 01:48:44 GMT  
		Size: 5.1 MB (5082193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:739f277c0a329bb5873f128828ac9b670003adbed4586f49629239014fe05c30`  
		Last Modified: Fri, 31 Oct 2025 01:48:45 GMT  
		Size: 11.8 KB (11842 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:8f8c5b8e75ba7a80ef92120295a842a5596b80fd34b3eadec9165be43d87bc4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259683369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760d945b9b47c1b968f605541d097dce9569ffe027502ad0ca3cd404282274d5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:13:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 31 Oct 2025 00:13:42 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 31 Oct 2025 00:13:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 31 Oct 2025 00:13:42 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 31 Oct 2025 00:13:42 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Fri, 31 Oct 2025 00:13:42 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Fri, 31 Oct 2025 00:13:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Oct 2025 00:13:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Oct 2025 00:13:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c51e434d6344a78d3f313869cc9e6b52c4fa434026550cba81fda5c7f7a93a`  
		Last Modified: Fri, 31 Oct 2025 01:51:58 GMT  
		Size: 194.9 MB (194889911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:2293cfab839a2486121eb702bc18ec31a013a8c1e2f2e8bb710019bea49470b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12c2e716def0d479158bbae1a215fe6eba7f62b14dbf6bbba2aa21f06343fd5`

```dockerfile
```

-	Layers:
	-	`sha256:602fb3200dfe972cd67ae225f943ba18d725ef691b3a1ac37820a1a2c7e9ca91`  
		Last Modified: Fri, 31 Oct 2025 01:48:49 GMT  
		Size: 5.1 MB (5081627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbe1ab47c0a319f3b2c7c22c0e69bc7ff28a54d330e1b434632bccd1cbedd669`  
		Last Modified: Fri, 31 Oct 2025 01:48:50 GMT  
		Size: 11.9 KB (11934 bytes)  
		MIME: application/vnd.in-toto+json
