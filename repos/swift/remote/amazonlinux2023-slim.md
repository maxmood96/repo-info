## `swift:amazonlinux2023-slim`

```console
$ docker pull swift@sha256:527295e0cd8b1d0ad4413586eb9013207845021c4c7c99bcdcc8a3e1b4425ae7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2023-slim` - linux; amd64

```console
$ docker pull swift@sha256:c0de34d216dbcd6cb6ef5ff1f9a1f47ca1537f6484165cea65b1606d8cb78372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.8 MB (251824279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f482eadab6526f3e2a056f74a4bb1ca961ec84f58e5bfac1916cec81464ab19`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:17:18 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:17:18 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:17:18 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:17:18 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Wed, 13 May 2026 18:17:18 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:17:18 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:17:18 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:17:18 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:17:18 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Wed, 13 May 2026 18:18:03 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && dnf -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ef8c133a0d13a918fbb031626cadb796e37df2d1ad6f660957e835f4f9f34b`  
		Last Modified: Wed, 13 May 2026 18:18:24 GMT  
		Size: 142.5 MB (142516414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0351f2c873b61e5c91487b9ea357ef05f1409cfe8522e6bb8c42eb8475915cf`  
		Last Modified: Wed, 13 May 2026 18:18:22 GMT  
		Size: 54.7 MB (54731061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023-slim` - unknown; unknown

```console
$ docker pull swift@sha256:c25f5cb070088f7cfabcdc1432850553a3d80d1ec30cfaeaf679ee3c7081c9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4047d240a0f5b0d522c37863f9b497050ddf05acafe0a39adfe3c0030870d8d2`

```dockerfile
```

-	Layers:
	-	`sha256:253a9405ec0db695bbbb54f3a55af47ba53510494ffc532886ddb94e13a66c0c`  
		Last Modified: Wed, 13 May 2026 18:18:20 GMT  
		Size: 6.5 MB (6452556 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f6d06f61cfa584443a77967f5aee4af86f51293ae57e7cf67b3ff727681f494`  
		Last Modified: Wed, 13 May 2026 18:18:20 GMT  
		Size: 13.1 KB (13130 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2023-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:05e3c642f1eadde93c642e7f7ba34c91f598d3cb9ebf218220dffe141fc652a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.8 MB (248802656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc379801a5fe7dec2e893b99abf4c64b238a4f70d440991be8db4ebd931c208`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Wed, 13 May 2026 18:05:00 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 13 May 2026 18:05:00 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 13 May 2026 18:05:00 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 13 May 2026 18:05:00 GMT
ARG SWIFT_PLATFORM=amazonlinux2023
# Wed, 13 May 2026 18:05:00 GMT
ARG SWIFT_BRANCH=swift-6.3.2-release
# Wed, 13 May 2026 18:05:00 GMT
ARG SWIFT_VERSION=swift-6.3.2-RELEASE
# Wed, 13 May 2026 18:05:00 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:05:00 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 13 May 2026 18:05:00 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN dnf -y swap gnupg2-minimal gnupg2-full # buildkit
# Wed, 13 May 2026 18:05:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2023 SWIFT_BRANCH=swift-6.3.2-release SWIFT_VERSION=swift-6.3.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && dnf -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617d8aedf5a2db6dceacd135e845ea4917df6ab16ef4f7769e526c8dc06b7c20`  
		Last Modified: Wed, 13 May 2026 18:06:04 GMT  
		Size: 141.2 MB (141208378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1482734cbf30f1a5dd0fe65f934833ed9a60f4a2a00c4d621e6aa5b51f53b30d`  
		Last Modified: Wed, 13 May 2026 18:06:03 GMT  
		Size: 54.1 MB (54137303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2023-slim` - unknown; unknown

```console
$ docker pull swift@sha256:f76a703c828bcd1595de0a11b6ebfa6590f1026ef4e6502e981586b8068e043f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6465300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c578bc03eaf4e1c449391992534b95da0f17ed0b7a0ec19d302d5a4681ad00c`

```dockerfile
```

-	Layers:
	-	`sha256:9edaabe2fac27fa61a45670c7ba608091bda399a9f3d0d9bb27e64851c521ab6`  
		Last Modified: Wed, 13 May 2026 18:06:01 GMT  
		Size: 6.5 MB (6452063 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa5352ef3ace40f396e6ce180c54dcd13e4b2393511b3ee093f17852bbf9001c`  
		Last Modified: Wed, 13 May 2026 18:06:00 GMT  
		Size: 13.2 KB (13237 bytes)  
		MIME: application/vnd.in-toto+json
