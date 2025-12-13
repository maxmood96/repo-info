## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:a19b578c25a2b7b345d33290a76a6a979a2161e36243899d568329d26ddc0fab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:9ecbd0ecc53392e94bf2fd6f45f53a161f7c8157810b5a2af777a3fead028174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1414427523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cff2bd502e70e871f52a1e03e25f88d3d847a617e27ace7aea4c83175091470`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:30 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:30 GMT
CMD ["/bin/bash"]
# Fri, 12 Dec 2025 22:43:36 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Dec 2025 22:43:36 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Dec 2025 22:43:36 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Fri, 12 Dec 2025 22:43:36 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 12 Dec 2025 22:43:36 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 12 Dec 2025 22:43:36 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Fri, 12 Dec 2025 22:43:36 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Fri, 12 Dec 2025 22:43:36 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:43:36 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:44:15 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 12 Dec 2025 22:44:16 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02abe91f61318971fdee1718b89b603f5584e0b77b32aeaf22a19e78586b5366`  
		Last Modified: Fri, 12 Dec 2025 22:47:43 GMT  
		Size: 325.9 MB (325868492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab2201abb0ea65e7852a67d84e018bb8187ec4dae143dee53408da1017be0ff2`  
		Last Modified: Fri, 12 Dec 2025 22:48:01 GMT  
		Size: 1.0 GB (1025617883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788717c0731dcb2f5431e987634202bcac88d83f7c6ad228e5bc7c2637816286`  
		Last Modified: Fri, 12 Dec 2025 22:46:52 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:41cd2630d6b5232d4e8e7f3538beb2c85e1001152ecf1dcb67a3be0279aee6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07df34b6225cdf249fc27d5d8342d9d4ceb74e34e07b8b00599c57ff897e5aa3`

```dockerfile
```

-	Layers:
	-	`sha256:070f6497c431463f852636636b4a8a5f94825b4f4e96f05f67360a4f38576a7c`  
		Last Modified: Fri, 12 Dec 2025 23:47:58 GMT  
		Size: 12.7 MB (12719997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2509353c56c3685322eb3bce5cf0c5bbb06fd7afd6a5ae9587028849200a6ae1`  
		Last Modified: Fri, 12 Dec 2025 23:47:58 GMT  
		Size: 14.8 KB (14847 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:a5c3ca6660d46de8006270693f0dad47ede678b3fd319e3114ec8f805ade5712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1384246721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a352af67d41b96a8889f690919cee069104b68d7714dce277d1e40a932653d88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:28 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:28 GMT
CMD ["/bin/bash"]
# Fri, 12 Dec 2025 22:43:12 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Dec 2025 22:43:12 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Dec 2025 22:43:12 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Fri, 12 Dec 2025 22:43:12 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 12 Dec 2025 22:43:12 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 12 Dec 2025 22:43:12 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Fri, 12 Dec 2025 22:43:12 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Fri, 12 Dec 2025 22:43:12 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:43:12 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:43:59 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Fri, 12 Dec 2025 22:43:59 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc581f92ee3fc9657f41e45972d55368934f7fa59608a088b370c906d7fb2ccf`  
		Last Modified: Fri, 12 Dec 2025 22:47:00 GMT  
		Size: 297.4 MB (297361254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843c07ab810a7daa40e66e42b0ca93d3ed6d3ac0199b778324b24d97ed6feac1`  
		Last Modified: Fri, 12 Dec 2025 22:46:44 GMT  
		Size: 1.0 GB (1022089538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025d2e8aee2edf40f867828123b89eb5fc9107ad0061a7ef4ef9597e9ea1061c`  
		Last Modified: Fri, 12 Dec 2025 22:46:36 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:7ad5feed2a3e77f6b5e6a4a2c8279455d7cc55c292a0f0f4e1963d6555722516
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3a7f77d0ca40ba52675f77240aa406853ce1e32eaf2ebe94072777bd258b7e`

```dockerfile
```

-	Layers:
	-	`sha256:7f4ed3fe6876f882861cdb944b3a25e6011e296214ce318f28562cc945ad609a`  
		Last Modified: Fri, 12 Dec 2025 23:48:11 GMT  
		Size: 12.6 MB (12581634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfdd6d292cd48d1ed150b41c67f77a14820bd17f0a1d3ad3a30dd7fbfcbd241a`  
		Last Modified: Fri, 12 Dec 2025 23:48:12 GMT  
		Size: 15.0 KB (14969 bytes)  
		MIME: application/vnd.in-toto+json
