## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:91406f7eeea48344622a4251da42859d7833349ad4dc39e2c95bbaa88e33cf35
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:5d686f2f8cc38166d6cdde88d23c27dbdfb9613690b38c6427496b4bb4151ce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.7 MB (289666903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47af86fd77b3ff29677f3db9dfe7110665d15668c5ffa2e01177157bd14b5e43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:03:09 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:03:09 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:14:39 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 24 Apr 2026 00:14:39 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 24 Apr 2026 00:14:39 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 24 Apr 2026 00:14:39 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 24 Apr 2026 00:14:39 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Fri, 24 Apr 2026 00:14:39 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Fri, 24 Apr 2026 00:14:39 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 24 Apr 2026 00:14:39 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 24 Apr 2026 00:14:39 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:e31bc602eae80620b93a07bcadec78ad83d112fa08abc35008da53ebf7ca3693`  
		Last Modified: Wed, 15 Apr 2026 10:04:45 GMT  
		Size: 63.0 MB (62952183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192d6e11c326e650f7bcd344149580d39cb03b4d871c56b9ed08a9a2bc351cbe`  
		Last Modified: Fri, 24 Apr 2026 00:15:10 GMT  
		Size: 226.7 MB (226714720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:096a237be5e0528ca789135259b1e12f227355fa2a271afbb6e95eb21c6374c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5094148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48fa942311233c167ed56c5437ff6aad578e7afeed870a4a8792277023c2b477`

```dockerfile
```

-	Layers:
	-	`sha256:ef79b115713ce2fb2b401e4560793b0de43411f40eaa03e38c5adc7d32bd17c6`  
		Last Modified: Fri, 24 Apr 2026 00:15:05 GMT  
		Size: 5.1 MB (5082294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e68b89ee9df8c3b3edb97ee250bdc826d0d5b38535d1c4184218ae4ffdbc68d`  
		Last Modified: Fri, 24 Apr 2026 00:15:05 GMT  
		Size: 11.9 KB (11854 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:76b257aa82393cfc321cc5920819287238939f8eaa49e9c5289915d60544dbc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266403604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808382b8fc5f5aa509a4cf1e75a9c0eb6eba9727d9be2689659b3184b457aecb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:35 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:14:53 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 24 Apr 2026 00:14:53 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 24 Apr 2026 00:14:53 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 24 Apr 2026 00:14:53 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 24 Apr 2026 00:14:53 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Fri, 24 Apr 2026 00:14:53 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Fri, 24 Apr 2026 00:14:53 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 24 Apr 2026 00:14:53 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 24 Apr 2026 00:14:53 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip # buildkit
```

-	Layers:
	-	`sha256:0089d862b3b6e84c40891727df0dc5639dc509aa2f4dc6079056a5a3f8b526e1`  
		Last Modified: Wed, 15 Apr 2026 10:04:56 GMT  
		Size: 64.8 MB (64798783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda2f8bc1d9d8311b96548287e0a37c5d2ec94ac6098a76c8ab7946ab5bd34b7`  
		Last Modified: Fri, 24 Apr 2026 00:15:23 GMT  
		Size: 201.6 MB (201604821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2-slim` - unknown; unknown

```console
$ docker pull swift@sha256:9ae2fa32a61c211e03e0632722b70effd62d94e26961a31bef23fd420a33068d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5093674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd74356ef2d1962b08fedf429754f15831378ede224e882a2531be4a8ae470a9`

```dockerfile
```

-	Layers:
	-	`sha256:791b3045621eb476557e78f18558c09545c57d34b4848a95afa0bd77e3caa409`  
		Last Modified: Fri, 24 Apr 2026 00:15:19 GMT  
		Size: 5.1 MB (5081728 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554dc1502ec5325e6bbf80af2d8fb8067546a52845e389d22ef8c0da4f70db06`  
		Last Modified: Fri, 24 Apr 2026 00:15:18 GMT  
		Size: 11.9 KB (11946 bytes)  
		MIME: application/vnd.in-toto+json
