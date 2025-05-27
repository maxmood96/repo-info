## `swift:focal-slim`

```console
$ docker pull swift@sha256:faeb897c1f372870263aecc05a41fdd513e13307ebf5274cbb1c06f83e2ac575
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:focal-slim` - linux; amd64

```console
$ docker pull swift@sha256:c70a945d9d0610124a5c775d7d212099cb60fceec03063987fbdbd78b268e89f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.7 MB (98703896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f04f9c7492f35bdda5eb8e1eb579d10610ce754f7d67803ea126f3c0da2ed0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 08 Apr 2025 10:42:46 GMT
ARG RELEASE
# Tue, 08 Apr 2025 10:42:46 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 08 Apr 2025 10:42:46 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 08 Apr 2025 10:42:48 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Tue, 08 Apr 2025 10:42:48 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 22:39:21 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 26 May 2025 22:39:21 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 26 May 2025 22:39:21 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_BRANCH=swift-6.1.1-release
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_VERSION=swift-6.1.1-RELEASE
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 May 2025 22:39:21 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 May 2025 22:39:21 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84b798a4050a113414b602896848994a51d6b8779de035022c5995f1feb0a2d`  
		Last Modified: Tue, 27 May 2025 18:56:28 GMT  
		Size: 22.3 MB (22292630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d96a28718be4f1b14bd75440d3e9990e0dc85079e812bcd2e05f51ea2480df`  
		Last Modified: Tue, 27 May 2025 18:56:28 GMT  
		Size: 48.9 MB (48900872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d49b40f80c78a206e6cdc2b06477170a7a130b3b1870d2409ef4196ca3b5ec6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71bc57273120d47d55036dbe3640932089be465104f226fd43734ebe3edc82ac`

```dockerfile
```

-	Layers:
	-	`sha256:79072a3da9ab04633e1fa4aee30a4b62623d7861b1358b835d41d6549a9526d0`  
		Last Modified: Tue, 27 May 2025 18:56:27 GMT  
		Size: 3.0 MB (2958259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0654b1b176d9bf9916b82c25f6c84f6dd793cb44f68dea6bd364fb9eef2d3416`  
		Last Modified: Tue, 27 May 2025 18:56:27 GMT  
		Size: 14.0 KB (13983 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:focal-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:cbd35d6a262f1d3940c2724c22a75f725c2cb593e9c120abd7affccb67b5413c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96547367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea2d84010e1c597f04fbc69635e580ba386fcc6d22528286dd9e5ccbf11805fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
ARG RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 01 Apr 2025 00:12:10 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903f3f45a36b4341896a6a860422e767ce8d6b963de01bd17e75cbfe9e4092eb`  
		Last Modified: Wed, 09 Apr 2025 13:01:36 GMT  
		Size: 22.1 MB (22075783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a56846d20e62e5944c01d5a4c47076e6fe895f8a804905d758f0a26638f5a6e`  
		Last Modified: Wed, 09 Apr 2025 13:01:36 GMT  
		Size: 48.5 MB (48493923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal-slim` - unknown; unknown

```console
$ docker pull swift@sha256:80f7634a8b2098bece42865fda8609bda0c04f10fd31161f4e2cb3183074b1a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2946690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e58a4bb23b9cc8647c7a0be1da5e455ad08948b309cc8e2a45b627c71cfb3b5`

```dockerfile
```

-	Layers:
	-	`sha256:af90950747a7e09b2e0d9e41d9bd24f7eda52d842d1e01eab8321d64481013da`  
		Last Modified: Wed, 09 Apr 2025 13:01:35 GMT  
		Size: 2.9 MB (2932612 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4f88d2b7a8d425c319198ad269bb21e84241720b9ff10f11d80cbfc3f52d66`  
		Last Modified: Wed, 09 Apr 2025 13:01:35 GMT  
		Size: 14.1 KB (14078 bytes)  
		MIME: application/vnd.in-toto+json
