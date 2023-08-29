## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:2c1bcdb7455ad180f48ceec9e5142719cb8ff50dce9f9a4cdad85c20fbbe140e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:16981215a8bed5eb5bd72312ff42c954a39c198f9d6bd046651318570dbde623
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.2 MB (304191595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29c444cc3a9e4e5d1e8da4a09b5e1cd2eb8d6f0e01ee9a7ba3bdbadd8c93026f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:29:22 GMT
COPY dir:591ada5c2fb65633b614a3ff732e6d83dcd91fe9ae925844fe9ba3323311bf74 in / 
# Tue, 29 Aug 2023 18:29:23 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 19:08:21 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 29 Aug 2023 19:08:21 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 29 Aug 2023 19:09:45 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 29 Aug 2023 19:09:45 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 29 Aug 2023 19:09:45 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Tue, 29 Aug 2023 19:09:45 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Tue, 29 Aug 2023 19:09:45 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Aug 2023 19:09:45 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Aug 2023 19:10:25 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:8be3d01330d7e2e197495d440aa60d14ac366aad5e8d105d86e384876aefec18`  
		Last Modified: Fri, 25 Aug 2023 08:53:43 GMT  
		Size: 62.5 MB (62477278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e2a8a224777ca4b3b6753fc926fe4758710092d6ff1aeef7b706b7e4cba1f`  
		Last Modified: Tue, 29 Aug 2023 19:27:05 GMT  
		Size: 241.7 MB (241714317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:974b7a485ca5138cca49b5f7876c2f4136d14d97b691aabd469bc5b5a93b37e7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.7 MB (267689088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ff9efb12b6cc08a5ec0073012d101b62dd53ada7616c9e3ca1a4a9417edd2c2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 29 Aug 2023 18:41:03 GMT
COPY dir:6fcca547a5a58ffe09e9507247c1ba371889e20efec9c9e016fb6276715fb958 in / 
# Tue, 29 Aug 2023 18:41:04 GMT
CMD ["/bin/bash"]
# Tue, 29 Aug 2023 18:57:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 29 Aug 2023 18:57:02 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 29 Aug 2023 18:58:25 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 29 Aug 2023 18:58:25 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 29 Aug 2023 18:58:25 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Tue, 29 Aug 2023 18:58:25 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Tue, 29 Aug 2023 18:58:25 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Aug 2023 18:58:25 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 29 Aug 2023 18:59:00 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:aa4ff431ef8289088d3cf576f166a7c73e7a5dabe3fae46528dbdd9d7194e9e4`  
		Last Modified: Fri, 25 Aug 2023 18:25:09 GMT  
		Size: 64.1 MB (64129994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b3a33e153d72d59ff22b3fb41330047c6036ed097d4d83506c006a9c453fd1`  
		Last Modified: Tue, 29 Aug 2023 19:03:36 GMT  
		Size: 203.6 MB (203559094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
