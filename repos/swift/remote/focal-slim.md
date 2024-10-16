## `swift:focal-slim`

```console
$ docker pull swift@sha256:c8b87ed3b8e7b60c243aa6b266f8c3650c6a0632bc564b1445cf6982ee2841c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:focal-slim` - linux; amd64

```console
$ docker pull swift@sha256:52cb5aaa83ed7350caad640a01df9e97455f152df16808ff00a8321aae44b117
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.2 MB (113204319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48cecae8a9dbc34576f3a09f261659be507c553d56133ef90145abb757b32c13`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Sep 2024 05:07:02 GMT
ARG RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Wed, 25 Sep 2024 05:07:02 GMT
CMD ["/bin/bash"]
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb0e08a1cefe4a0ecfdde6fb9f300d138b5a44afea33a2f7a008af060a96ed3`  
		Last Modified: Wed, 16 Oct 2024 16:19:09 GMT  
		Size: 22.3 MB (22296622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c1653e2a4ae213760207d37acf247dccbd4adbb15e9fbf6522ec5cc6fc2259`  
		Last Modified: Wed, 16 Oct 2024 16:19:09 GMT  
		Size: 63.4 MB (63396637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal-slim` - unknown; unknown

```console
$ docker pull swift@sha256:ce083e7f10ceed1f427a78818e8e313184cd7894da56815324d89b96a31a5244
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2931764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb46c124928433b3c70bd17b39a696c89a6fd7af07bbc06a04e3e4a0d4b04b04`

```dockerfile
```

-	Layers:
	-	`sha256:e5de9caaa304b2001ffa193efc2e66fe8cc597523423c814d72430e7760c6ba7`  
		Last Modified: Wed, 16 Oct 2024 16:19:08 GMT  
		Size: 2.9 MB (2917997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcf66f8911b066c8aac4495f82ce5fca9fe5aa10f9561f38a246ccd6274e9a5d`  
		Last Modified: Wed, 16 Oct 2024 16:19:08 GMT  
		Size: 13.8 KB (13767 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:focal-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:60b3c0401ca969a06def111167b190484717d2f759f124015969353ced59f0fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111181414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b9fdaa3b8f32c63c7a8a27d69661f6fe28225d65ab613a72f809225809c5de6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 25 Sep 2024 05:07:02 GMT
ARG RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 25 Sep 2024 05:07:02 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Wed, 25 Sep 2024 05:07:02 GMT
CMD ["/bin/bash"]
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd04771de1da857dee2db42aed26270dd7e6609d700452da7a9dd21710ceced0`  
		Last Modified: Wed, 16 Oct 2024 05:13:03 GMT  
		Size: 22.1 MB (22078071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7f91a293e2f2406e913e9acca01e1b495add2e3473fc88f0b49b3c8d60061e`  
		Last Modified: Wed, 16 Oct 2024 05:13:04 GMT  
		Size: 63.1 MB (63129515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:focal-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d33e148b3ec1a951f441d3af9f67a09331d718fecca65f6e4090877b92527396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2932131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6d8dc3fdae52faa0fa9af28c701b6ead195673570843f595c7e6069c2910218`

```dockerfile
```

-	Layers:
	-	`sha256:b0d51e902dc02ebd6869632ca8d06da01b4720808115a05371fdcbb8060c2b68`  
		Last Modified: Wed, 16 Oct 2024 05:13:03 GMT  
		Size: 2.9 MB (2918263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88ad6fa01314243ab816e42c6f2d15f7636de1f9cf0726f06e24e8d0a5ef658c`  
		Last Modified: Wed, 16 Oct 2024 05:13:02 GMT  
		Size: 13.9 KB (13868 bytes)  
		MIME: application/vnd.in-toto+json
