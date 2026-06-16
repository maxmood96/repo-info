## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:0875ad0db464bfcb8bbc366f0b461c958dfad0ef9ae861f3483e6d3e2ad802d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:99dde538989ef53b3e02e94b91811d1e5f4ae819eaa6a3058e3c8025c0043a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1634251649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75ad005685d59009966d3d9674cffd06e2677a1d566bd277f710d2161b56f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:40 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:20:00 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 16 Jun 2026 01:20:00 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 16 Jun 2026 01:20:00 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Tue, 16 Jun 2026 01:20:00 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 16 Jun 2026 01:20:00 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 16 Jun 2026 01:20:00 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Tue, 16 Jun 2026 01:20:00 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Tue, 16 Jun 2026 01:20:00 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 16 Jun 2026 01:20:00 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 16 Jun 2026 01:20:45 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 16 Jun 2026 01:20:45 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f840903d8067c372be99d2c17736eb6cae8a2c1f781caa7b990c77c242cc08a7`  
		Last Modified: Tue, 16 Jun 2026 01:23:36 GMT  
		Size: 334.5 MB (334501009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b3211f73ed6dab4ae86b6305f4bd1df945dcc072033bbff38184751bac5da2`  
		Last Modified: Wed, 13 May 2026 18:21:34 GMT  
		Size: 1.2 GB (1236808518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0356167b138e4149e3036105b75466cfcab1ad9ba1d8e0c9f52350a98e3ea00c`  
		Last Modified: Tue, 16 Jun 2026 01:23:29 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:6bedd6dab779d98f26e49d0ace73b3268ea67622eba476d27fffb201426b980d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe8e918a71acaa025a00a90e9e0866813897aa45cb177d38382d1ff24507ff3`

```dockerfile
```

-	Layers:
	-	`sha256:df2a5804a4c34b31fc67abe7f3325fa6f1bf79d5e3230929ae99c97d6a491d8c`  
		Last Modified: Tue, 16 Jun 2026 01:23:30 GMT  
		Size: 12.7 MB (12720094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e1bb4a2fed39cae274e847e6ab370263fa9724d1a2d4c3c5371a8539212e25a`  
		Last Modified: Tue, 16 Jun 2026 01:23:29 GMT  
		Size: 14.8 KB (14847 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d24023aba68fdf9adc4839d176dd79fc157229085dd4005ff4f5fee0ace2ee31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1589975822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924d2b03874d6d49d8cdbf8b0ea47d80353b0c305728637a0a38cce193c6c90f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:21:29 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 16 Jun 2026 01:21:29 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 16 Jun 2026 01:21:29 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Tue, 16 Jun 2026 01:21:29 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 16 Jun 2026 01:21:29 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 16 Jun 2026 01:21:29 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Tue, 16 Jun 2026 01:21:29 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Tue, 16 Jun 2026 01:21:29 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 16 Jun 2026 01:21:29 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 16 Jun 2026 01:22:14 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 16 Jun 2026 01:22:14 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d30852e9a5de87af026ebc9eceba5ed6e3825980700ed55f22f2df6c38cb7d`  
		Last Modified: Tue, 16 Jun 2026 01:24:49 GMT  
		Size: 305.6 MB (305593359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d68a9c69fcab24bcd6f286aa786dddc8f06148d2d1aaa2897e551ec726f7608`  
		Last Modified: Wed, 13 May 2026 18:08:41 GMT  
		Size: 1.2 GB (1219591580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b0c154c4b2a165e5c7df8824ba09b4b355076d45b5438bd26ac9a6981df1e7`  
		Last Modified: Tue, 16 Jun 2026 01:24:41 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:57d8684967ca2cbdf4025f3b20f6fc11b465d8c3fa6e6f124b7d8a4ef124169a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7989bddcf0f73d8506532a81c88285e23d337512815841648cf8b33fbfb427e4`

```dockerfile
```

-	Layers:
	-	`sha256:109d66b0a39a78b11497a2e2367804a311246009d41156e21732e05452c362c7`  
		Last Modified: Tue, 16 Jun 2026 01:24:42 GMT  
		Size: 12.6 MB (12581731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eeb110c3b9efc66385a00a2699220063dc50affeb80b3f6a938d3881646c5a9`  
		Last Modified: Tue, 16 Jun 2026 01:24:41 GMT  
		Size: 15.0 KB (14969 bytes)  
		MIME: application/vnd.in-toto+json
