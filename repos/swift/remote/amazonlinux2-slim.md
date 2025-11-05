## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:1e2124d2f17aeb97a19959445114b795076cdae736dcd5c0e1b6d7000e83ad2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:ae5f45f323d1ed202eb32d5d7367b85adc80f80e7d508ff20b57f62a3fe15139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.3 MB (282317012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:829ec5d9aca5a9a7028b1f92b419c58d806eab2744ac3062fec5a1763ae630b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 22:26:51 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 22:26:51 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 22:26:51 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 22:26:51 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 04 Nov 2025 22:26:51 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 22:26:51 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 22:26:51 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 22:26:51 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 22:26:51 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71322800563e74611a6e394e5da4187de223fcb8e760d564eb627341aebf0130`  
		Last Modified: Tue, 04 Nov 2025 23:56:33 GMT  
		Size: 219.4 MB (219382944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d866e76af695a23c5bb091709ab5f454789d5ebb948f12c1176ac0f8aa786319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3485fac4b2440869a712da15d4a802e90250d1d7cdf25062636d7987835d9db8`

```dockerfile
```

-	Layers:
	-	`sha256:eacfb45cd612763e80d5b5daa84fc8bca9277d6b51eff11b81a31a85a8a057bf`  
		Last Modified: Tue, 04 Nov 2025 23:47:57 GMT  
		Size: 5.1 MB (5082193 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5df07e76970ef7ee42a4324ce36951453627ad54ea05209ad8709838b87dba82`  
		Last Modified: Tue, 04 Nov 2025 23:47:58 GMT  
		Size: 11.9 KB (11854 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:64db2dc04e5313cc59a5f2dbe1f462f4dda7110f0143d5ab0380fbf734150643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259664520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0cada5603c017f882ba14f7207a83da5fca228c9641550caf28240e0c8bd0cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 19:24:44 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 19:24:44 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 19:24:44 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 19:24:44 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 04 Nov 2025 19:24:44 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 19:24:44 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 19:24:44 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:24:44 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:24:44 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d63759090ee91753b949528918ca6e8e81ae41445d0ebf73d3dd7f439f49a8`  
		Last Modified: Tue, 04 Nov 2025 22:22:54 GMT  
		Size: 194.9 MB (194871062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:69a8c1cb104fc3706b11fcc821515344e13c6bc81d6c96df94d905599c0942b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8c1e006eb6645773a5a9d6b6c55341e736b53cd812b5220b94bfeb53180997d`

```dockerfile
```

-	Layers:
	-	`sha256:5031f915670d25e7d8c673bac2a091f20178668649c11e5a9926e0ca0a22606e`  
		Last Modified: Tue, 04 Nov 2025 20:48:00 GMT  
		Size: 5.1 MB (5081627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c9238e95516523ad8427eb9968909f7d473db1d2dd144009038a1908b3f2bcb`  
		Last Modified: Tue, 04 Nov 2025 20:48:01 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.in-toto+json
