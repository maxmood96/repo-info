## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:78e53f67b149dddc161335583ce98507f1bb35bf03b1c8a2c8062b27eb91e058
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:55f097130d151d0cfbbf2075b1e15f8ab3b3724fcfaed36614abc64deb28e073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1632327561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42761848ede4551e9747a13c8ae9ba053082710fbd2cd9f6a3afd6a49ed24a0b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:13:29 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 30 May 2026 01:13:29 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 30 May 2026 01:13:29 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Sat, 30 May 2026 01:13:29 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 30 May 2026 01:13:29 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Sat, 30 May 2026 01:13:29 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Sat, 30 May 2026 01:13:29 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Sat, 30 May 2026 01:13:29 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 30 May 2026 01:13:29 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 30 May 2026 01:14:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Sat, 30 May 2026 01:14:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e791db80128683b313d542270ed9e3e1f15f5c79fe047f77bf15e736bb6b41d8`  
		Last Modified: Sat, 30 May 2026 01:16:51 GMT  
		Size: 332.6 MB (332576919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b3211f73ed6dab4ae86b6305f4bd1df945dcc072033bbff38184751bac5da2`  
		Last Modified: Wed, 13 May 2026 18:21:34 GMT  
		Size: 1.2 GB (1236808518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e753f93bb0829a22d2c99e09701479294418eca4c0364e6e6addba4e5a6ae4a`  
		Last Modified: Sat, 30 May 2026 01:16:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:b76529289349b64094cf2d175ccc7182d0d44ad2abdfbdbb49279f9d1b844783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd503c8f676a4d06131b56cb7c89e8a98c6c1f7deea4057544e4d07d40356c5`

```dockerfile
```

-	Layers:
	-	`sha256:247d8105392c019ac0fabbbd75494144075b2655762c20b211f4df2aaa49ce86`  
		Last Modified: Sat, 30 May 2026 01:16:45 GMT  
		Size: 12.7 MB (12720094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce226682d684e18fe6aa9bcf01938f67fba13962fec3ccc7050cf06117c21c8`  
		Last Modified: Sat, 30 May 2026 01:16:44 GMT  
		Size: 14.8 KB (14847 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:53038f9183bf24be645f8f7bcee9eb80aedab542445b32a18b6c4fae97b7215b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1588080498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa69cfe8389a8302d8cab170b26498d853590c7f0f111992ae60938ce6c961aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:13:14 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 30 May 2026 01:13:14 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 30 May 2026 01:13:14 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Sat, 30 May 2026 01:13:14 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 30 May 2026 01:13:14 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Sat, 30 May 2026 01:13:14 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Sat, 30 May 2026 01:13:14 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Sat, 30 May 2026 01:13:14 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 30 May 2026 01:13:14 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 30 May 2026 01:13:59 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Sat, 30 May 2026 01:13:59 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4532b060846d025bceb8a57e9267d63548399cb4618365c6971975ac9565aa`  
		Last Modified: Sat, 30 May 2026 01:16:34 GMT  
		Size: 303.7 MB (303698034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d68a9c69fcab24bcd6f286aa786dddc8f06148d2d1aaa2897e551ec726f7608`  
		Last Modified: Wed, 13 May 2026 18:08:41 GMT  
		Size: 1.2 GB (1219591580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b659f215fccae8bbfb8442114aeaa1bf8db73c0f0bff483cc68360fb06fd4200`  
		Last Modified: Sat, 30 May 2026 01:16:27 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:02b5e7d1bb8756718185b675f02b93da56524ae09f719fd21d258113cbc7fd11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eccbbf545fabf6e3241d81f7e6ac28f3f6c423591154bf0761c138301ee1974`

```dockerfile
```

-	Layers:
	-	`sha256:7e99377b5732da472d02f5026e738110a2a759ec9af241295e98ca71d0e88414`  
		Last Modified: Sat, 30 May 2026 01:16:28 GMT  
		Size: 12.6 MB (12581731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc9a7e9f7428643c7921452c422034872d0f22843ffc95526cde6099c993ee1`  
		Last Modified: Sat, 30 May 2026 01:16:27 GMT  
		Size: 15.0 KB (14969 bytes)  
		MIME: application/vnd.in-toto+json
