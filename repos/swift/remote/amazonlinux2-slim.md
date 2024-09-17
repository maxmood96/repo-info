## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:0c6879febd171801bb6b03f6fa905cd2643f05b1fefdbb8b954c1fa36ef1dfe7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:c446aa0bd46ec66f0035fa7d43fad16fd3130dc992dbeb1b07997dcf091383f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272515618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8e4de5626d09e0a7c4fd4183f136a3c139cba6d1fffec8cfbb1855c131c6890`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 06 Sep 2024 17:28:31 GMT
COPY /rootfs/ / # buildkit
# Fri, 06 Sep 2024 17:28:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf670d7facc6c1bf68782c33b01074c43893554a278c9f3ac4803466bde5a020`  
		Last Modified: Tue, 17 Sep 2024 16:59:10 GMT  
		Size: 209.8 MB (209820071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:a85b56ebdf8adc38f6d90ce453b0da7dcaf004e9cccd83484a923877e1bb3370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b28d6dac2219b7ab00f1d1627f1353961f52d4fbb86a86e73ef012d6a092cef`

```dockerfile
```

-	Layers:
	-	`sha256:716aef2bdaa294d6bf83b4e06d8ebf76e3a0955edccc6bbf087dc797ee897566`  
		Last Modified: Tue, 17 Sep 2024 16:59:07 GMT  
		Size: 5.1 MB (5077144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2126c93389a910d52588a946cb13b4bb29a9b0a770545bed3caf6f3002ad051b`  
		Last Modified: Tue, 17 Sep 2024 16:59:07 GMT  
		Size: 11.9 KB (11851 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f5efb47b63d9dc51d444e258e2b1af03b77d248c7dc0b3e913a2ebd83774136f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.1 MB (250148898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb9c93c196d7b46ebfdab7f86f0ab3518cdd2aab202b27a0b620192db90a132c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 06 Sep 2024 17:28:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 06 Sep 2024 17:28:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:0f0968c920788bb8a898446e0bbe8ea6b11fcbf7f55810ef51044775a045d6c9`  
		Last Modified: Fri, 06 Sep 2024 18:59:50 GMT  
		Size: 64.6 MB (64586343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1128c4213e835f3f6280a719115a8a28986cb1071b061edee8204a52772646e1`  
		Last Modified: Tue, 17 Sep 2024 17:26:15 GMT  
		Size: 185.6 MB (185562555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:82601a01e7d45d70370031e365e23bf13931cfc6f5a666735832d5c2a9e18d36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5088801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f898245bbab20f4ef0f8717e86175a0ca296d49eea7f22ab16f236f271c7eab7`

```dockerfile
```

-	Layers:
	-	`sha256:120eb2d954abc5d69c24d28b3c4525e0415f89b384a42fee846176d16eafa839`  
		Last Modified: Tue, 17 Sep 2024 17:26:11 GMT  
		Size: 5.1 MB (5076577 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:986bf85bbee64ba6290e7b9a45aad16fbbc9b036873a5fd21870d58ffd1b7e47`  
		Last Modified: Tue, 17 Sep 2024 17:26:10 GMT  
		Size: 12.2 KB (12224 bytes)  
		MIME: application/vnd.in-toto+json
