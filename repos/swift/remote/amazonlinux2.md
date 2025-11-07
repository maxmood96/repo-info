## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:f4108b4b3edf025c1072ae64ab7dafbec441ed54648fc4fd02eef2ced8f05d67
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:7f94412582ca19e6a68e9e5031ee8b0c73aec423e2f6802f6a6b549874f32e1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1412102382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c5e653c39dc324158202720f3e4422143a5db50b5d4491f03cc9d283a7d5c78`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:15:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Nov 2025 22:15:13 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Nov 2025 22:15:13 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Thu, 06 Nov 2025 22:15:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 06 Nov 2025 22:15:13 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 06 Nov 2025 22:15:13 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Thu, 06 Nov 2025 22:15:13 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Thu, 06 Nov 2025 22:15:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Nov 2025 22:15:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Nov 2025 22:15:50 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 06 Nov 2025 22:15:50 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5608ad134799b192ebedbf9c7eb465b5318e14446218be0d753a156ca420f6d8`  
		Last Modified: Thu, 06 Nov 2025 23:53:17 GMT  
		Size: 323.8 MB (323776089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff6ffaafbb44a91ca36abf6bc1d8a7a07de0e98991e476045abc8fb9794132a`  
		Last Modified: Tue, 04 Nov 2025 23:52:36 GMT  
		Size: 1.0 GB (1025391985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665ecc4d2ace39c726f354453c1b3604dae4bb93de1a3997cb14392bc131494a`  
		Last Modified: Thu, 06 Nov 2025 22:18:05 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:27935ebae49663564413055fe37341de86126aa79cebdd3bdf6bfc2701f5b730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f08c76bcb5ca71ada034b0560af119de04f9488a7911565213c1d2345be1462`

```dockerfile
```

-	Layers:
	-	`sha256:ddc00d01f8fc855e49f51a63d7a7370a2bd4806fbdb5786e8653082bad8f0e64`  
		Last Modified: Thu, 06 Nov 2025 23:48:42 GMT  
		Size: 12.7 MB (12719991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7ebec5746595d79bd5f405eb31cdd1bb55a6dc00007a53dd2091fc336e586d6`  
		Last Modified: Thu, 06 Nov 2025 23:48:43 GMT  
		Size: 14.8 KB (14847 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:2a213eaa6260b42ca1b3343ab9dc2044f7629386ccf7f74d4137684d6fdda207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1382042551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5673a82ad2607e428a38f8b16bf9415c7912825925f654bb1e7d0e60e3d0780`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:45 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Nov 2025 22:14:45 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Nov 2025 22:14:45 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Thu, 06 Nov 2025 22:14:45 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Thu, 06 Nov 2025 22:14:45 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 06 Nov 2025 22:14:45 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Thu, 06 Nov 2025 22:14:45 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Thu, 06 Nov 2025 22:14:45 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Nov 2025 22:14:45 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Nov 2025 22:15:25 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 06 Nov 2025 22:15:25 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e34f0da9d4c9eef19606afb3a098e3eb923d4187e743ee2ac75c5f5758134d9`  
		Last Modified: Thu, 06 Nov 2025 23:54:24 GMT  
		Size: 295.3 MB (295341047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530e29bfe332d82339a65c057a82781c6f50e73f0e5fb0d5d316eea41f376e45`  
		Last Modified: Tue, 04 Nov 2025 20:52:07 GMT  
		Size: 1.0 GB (1021908034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c039917d80ef6d332ed288ea899fc344c9cc292a79c615dce4c617afa51d69`  
		Last Modified: Thu, 06 Nov 2025 22:17:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:792d437d7191a5938ac4e927fad6ae52ac54d0759e3d8890d9b00d5310d6eb81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953e3bd5533d825957a5784653daaba3dd73929076068913154f6002e6df8de7`

```dockerfile
```

-	Layers:
	-	`sha256:cb6c87a35f567d096455884a54d99f6402cc2990e82ad8eb681d608f27a8753e`  
		Last Modified: Thu, 06 Nov 2025 23:48:54 GMT  
		Size: 12.6 MB (12581628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc372016015908afcfe9b19f5f41bb763cc598cb41646d1048ebb41088ae78b9`  
		Last Modified: Thu, 06 Nov 2025 23:48:55 GMT  
		Size: 15.0 KB (14969 bytes)  
		MIME: application/vnd.in-toto+json
