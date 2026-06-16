## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:980ef20e3f91509d5819f3f66591f813e83eddd113ce2c049ccccb20bc207457
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:81eb0084d3e0a85fc458db06acb41dab8d2a1fd56e7c38fa889fd7e4d36ae505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294800022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375e6e218efc84ebcf3d41796869961d18d77ddd43f117370479224b84835891`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:40 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:20:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 16 Jun 2026 01:20:15 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 16 Jun 2026 01:20:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 16 Jun 2026 01:20:15 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 16 Jun 2026 01:20:15 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Tue, 16 Jun 2026 01:20:15 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Tue, 16 Jun 2026 01:20:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 16 Jun 2026 01:20:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 16 Jun 2026 01:20:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259f3183f160172426f8640516a7d1ba59f47a6ddf7282532987f7fd79885b6f`  
		Last Modified: Tue, 16 Jun 2026 01:20:48 GMT  
		Size: 231.9 MB (231858072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:8e670103928320b321b9a9690374f1a7c6a697eb09c4fea72cdab25d2dd0c886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03f1e2e0087e787ea291b4f61aaa4177f034ab426c8c7550ce6af46cb24471a`

```dockerfile
```

-	Layers:
	-	`sha256:a5d543341b4f54b0f516b76ac457153d9122230f90d132b38a9552e10a2d2ec9`  
		Last Modified: Tue, 16 Jun 2026 01:20:42 GMT  
		Size: 5.1 MB (5082294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81cfd778d2cdd32a0fb40f27722ab6d79d393e6eeb78a5ce1b318e3afa945f2d`  
		Last Modified: Tue, 16 Jun 2026 01:20:42 GMT  
		Size: 11.9 KB (11854 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:663e683b7417880790dceb52f8ee95efaf46756a8a4d570be07670e8bad724e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271560103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb0d7b891da8a39af82a5c0c502edb8a101a7ba466fecf87ec89f83f87e90c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:21:57 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 16 Jun 2026 01:21:57 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 16 Jun 2026 01:21:57 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 16 Jun 2026 01:21:57 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 16 Jun 2026 01:21:57 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Tue, 16 Jun 2026 01:21:57 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Tue, 16 Jun 2026 01:21:57 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 16 Jun 2026 01:21:57 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 16 Jun 2026 01:21:57 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772f7568174d478ed00d455cf85632d22884f7a9c67b0be19bd48b60d8c73b2d`  
		Last Modified: Tue, 16 Jun 2026 01:22:26 GMT  
		Size: 206.8 MB (206769394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:9371ac8ffa4455002825b0d90ed1e900c818df829ca1e318b9d1f47321a075ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0565e1ac8a0ea93cd7162db2f6bfbb51dda656720b196673f46ba7d95967f82`

```dockerfile
```

-	Layers:
	-	`sha256:3d2289c79ba858500bf9231ffcb520e9c745deb921996dbb8055aef88648378b`  
		Last Modified: Tue, 16 Jun 2026 01:22:23 GMT  
		Size: 5.1 MB (5081728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6a998480dbef739c1375deebd5e0131c0d0b70da3f0bad68c3f8e6d37a6181`  
		Last Modified: Tue, 16 Jun 2026 01:22:22 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.in-toto+json
