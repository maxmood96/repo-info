## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:d8c46ed86e26b4b69f6ea961f27b28a54faaad3b2f2052732dd31c4603e0047c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:2d18d8fc721dde8cd7ec27d1a02009d74662185e259e5a7d0e6a7db3a2df8748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294783382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cc4558dc9e6aa624cf6a07080af6fec34acb5958a11f37fbe1cb3681b43253`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:26 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:13:51 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Jun 2026 21:13:51 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Jun 2026 21:13:51 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Jun 2026 21:13:51 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 09 Jun 2026 21:13:51 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Tue, 09 Jun 2026 21:13:51 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Tue, 09 Jun 2026 21:13:51 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Jun 2026 21:13:51 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Jun 2026 21:13:51 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a9c23e02236f863af4c1f764b0170f6bdfa89d06cfac7ff2b2fe56e3017414`  
		Last Modified: Tue, 09 Jun 2026 21:14:23 GMT  
		Size: 231.8 MB (231841432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:e267df06fa1c4e2995dc22d996009bc97172d683062e5ec69130c2637980b897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c580c6d013210790a022fdb2a134777518506ff6d97e5440d60dc33171b7ecb6`

```dockerfile
```

-	Layers:
	-	`sha256:6075c3b12fec4e7c0a277840613d3eb3e152b45affd03d6917faf374f0aaa815`  
		Last Modified: Tue, 09 Jun 2026 21:14:18 GMT  
		Size: 5.1 MB (5082294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:755b75e2ccf42fe755736eee5298e016262a23930f2b45fee6ac7cf9c23dc20c`  
		Last Modified: Tue, 09 Jun 2026 21:14:17 GMT  
		Size: 11.9 KB (11854 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3157345521196a2253fa2e7d10daf2efa34db57c58a4ae1568b88a28631af182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271553051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296fa374e040f843bb4288268d61047a31826705b4cf12234fc5a5e8ca6b8082`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:22 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:13:41 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Jun 2026 21:13:41 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Jun 2026 21:13:41 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Jun 2026 21:13:41 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 09 Jun 2026 21:13:41 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Tue, 09 Jun 2026 21:13:41 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Tue, 09 Jun 2026 21:13:41 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Jun 2026 21:13:41 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Jun 2026 21:13:41 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb79947a4cda3657794f1f1f7e4c82b07a0d1c29c1a72ed392e206d369dc53c`  
		Last Modified: Tue, 09 Jun 2026 21:14:10 GMT  
		Size: 206.8 MB (206762342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:b412c9aba2e4fcd6309d72bdf302caf9f27e95bb138246015e52db00d437097d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:866e1f378d39df1967bb7e81bb9ef3b06cb2242647f5a60f3e9e1bd0be0ea404`

```dockerfile
```

-	Layers:
	-	`sha256:90e264e4f097714e5a254b586122616210960ab8912a4dc749ecdb71a90df540`  
		Last Modified: Tue, 09 Jun 2026 21:14:06 GMT  
		Size: 5.1 MB (5081728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20e282fb46e1910ddbd87a04c2c49d67d1d3ebba41fd9f5d4fc4f7bb06edd241`  
		Last Modified: Tue, 09 Jun 2026 21:14:05 GMT  
		Size: 11.9 KB (11945 bytes)  
		MIME: application/vnd.in-toto+json
