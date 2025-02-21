## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:f49ef76d05d237c4ffd75c441de2fccb517d87a6709b3472a6c8dc0b0d014a4a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:dc051794adbe2da9642cf3a3a775baaeb7011114df7c756217aa73ee19d06e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264922710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde7b277c88c427b76ad9bbf1a4051df69a33f8d98cadf505c528cd9db05ebca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:43fdf45428917f1f386fbfe0eba1ccfdadae7696a4cce30a96cca587ab25ab90`  
		Last Modified: Wed, 05 Feb 2025 10:24:14 GMT  
		Size: 62.7 MB (62665244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae9cdcc6eda43ebbfe546eb227a04ad0c0c94aad7eb9460bbcd643d79b0a86f`  
		Last Modified: Mon, 10 Feb 2025 20:09:43 GMT  
		Size: 202.3 MB (202257466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:31a76f4e4a43d423b7699db009cf7914bfefe912bd99b980a76a773bf6ed36c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d736a70ec31bf68f2a7e8caffe4c7c05e0fc9af2703afd2d852ba058f9807f5`

```dockerfile
```

-	Layers:
	-	`sha256:190471ef4de41253f158029278242263779796ddb629f2e348fa62897c5115d4`  
		Last Modified: Mon, 10 Feb 2025 20:09:37 GMT  
		Size: 5.1 MB (5067544 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e70835ac0babac5047cdf82779aed525b42ada02dad611cb7dfbadc93835af94`  
		Last Modified: Mon, 10 Feb 2025 20:09:37 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:4499090e5bf583eb2dfb0e7621181b5e5724b46048c322d17f7f40942da52584
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242612123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7894667e8afe1a45ae04f6b41ea286fade05e832a4ff4f5ea953801b9f42865c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 12 Dec 2024 07:44:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 12 Dec 2024 07:44:15 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 12 Dec 2024 07:44:15 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_BRANCH=swift-6.0.3-release
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_VERSION=swift-6.0.3-RELEASE
# Thu, 12 Dec 2024 07:44:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 12 Dec 2024 07:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.3-release SWIFT_VERSION=swift-6.0.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:e42e49097fe754943ed2309e7c2ac45f6631e5c57fa3daa55479809dc243c87a`  
		Last Modified: Wed, 05 Feb 2025 14:56:54 GMT  
		Size: 64.6 MB (64578222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf2dcaa0f80a47257d02a5ff810ac1c304c29452477d342965d7ee7844edf96`  
		Last Modified: Mon, 10 Feb 2025 20:45:27 GMT  
		Size: 178.0 MB (178033901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:c0001f4880eb98f417756cb4687900d7ad32bf0c590347c445625abe19fa0010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5078967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e1313726c482279933f6633b70ea6e6fd8571c2c6c57936ea004e19b849335`

```dockerfile
```

-	Layers:
	-	`sha256:f2f2da55829db2566e2510740c065c0d10c2109c545398997fcb631f5ba4822a`  
		Last Modified: Mon, 10 Feb 2025 20:45:23 GMT  
		Size: 5.1 MB (5066978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dca186ecd079a560a0bbb7293659eb04283eff6b1a7425b0fcabe05c491015a9`  
		Last Modified: Mon, 10 Feb 2025 20:45:22 GMT  
		Size: 12.0 KB (11989 bytes)  
		MIME: application/vnd.in-toto+json
