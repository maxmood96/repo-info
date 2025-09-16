## `swift:jammy-slim`

```console
$ docker pull swift@sha256:b0275aa860063505c8fa689ffef68c09b20b760d896d2b3b88a47c4d8a4b8bcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy-slim` - linux; amd64

```console
$ docker pull swift@sha256:cba56cb54534b32f853f95a58b292ef019b62eec77a604fb36a52d2d28996d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.8 MB (98830521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c9c74b1ac282f960c40dadb6618b6e56625a3e06136dc95b431cd09862c899`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 15 Sep 2025 22:15:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea5e5a85e9fccb039bd622ad2b017134a3c1c529a8caacb244e03795ab6513e`  
		Last Modified: Tue, 16 Sep 2025 16:52:49 GMT  
		Size: 19.2 MB (19224009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d12e77209153d53715d64d3eacd8ca7ecde1e24febbac4cf452d9d9e6a8e48`  
		Last Modified: Tue, 16 Sep 2025 16:53:02 GMT  
		Size: 50.1 MB (50069577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:6e9c6ef06af0789b413e60434a504e7f624122dee54d544f03bf0f46e7f4bb43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81058e9a6033a8e22ca66dc65f569c604afe67bbd07f7d27b6f93e8f263225a2`

```dockerfile
```

-	Layers:
	-	`sha256:82ff0886df8155387e6b33e74ff1d5aa1e1fafb9912e57f929a6d544e317d91c`  
		Last Modified: Tue, 16 Sep 2025 19:49:18 GMT  
		Size: 3.1 MB (3055479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:128f84117c0323aaa938e79d1fb78879d9010274b2e7eca6d5df29aa74fac32a`  
		Last Modified: Tue, 16 Sep 2025 19:49:18 GMT  
		Size: 14.0 KB (13970 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:05895093e4e75312e0eeed0e78d2f50b0da37e64112ba874d7bbcf02e784836c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95932532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b96d564699ff94148e0cbec95835168a88761489a91ab31214e2052033e9a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 17:21:17 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:21:17 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:21:17 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:21:19 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Tue, 19 Aug 2025 17:21:19 GMT
CMD ["/bin/bash"]
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 15 Sep 2025 22:15:37 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 15 Sep 2025 22:15:37 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_BRANCH=swift-6.2-release
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_VERSION=swift-6.2-RELEASE
# Mon, 15 Sep 2025 22:15:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eec4eafcd73801d0c1f3e2f59c85026393634f70fd02e3ca025624205f715a1`  
		Last Modified: Tue, 16 Sep 2025 16:53:42 GMT  
		Size: 19.1 MB (19093009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b202afd270735af20099c8d95fb9dcd4b2a09e4da33140dfcbea482ba4f87274`  
		Last Modified: Tue, 16 Sep 2025 16:53:44 GMT  
		Size: 49.5 MB (49478054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:86ab0585ac260eb3187ade847743156afec635c46047c40481c4f8d2b9413e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8724ab6c56c8c6d29072a9a9b9f673b2836c4e87cfe15acf055f76eb53dfc1b`

```dockerfile
```

-	Layers:
	-	`sha256:7e3ab7e25558329e5076e2bf8f19ead72a3694d6435b597d514b24687775e890`  
		Last Modified: Tue, 16 Sep 2025 19:49:23 GMT  
		Size: 3.1 MB (3055766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:535dcee8e13f7c52989ee6cb5818d847ee1e459f2472b69d389fae0a61c70b8d`  
		Last Modified: Tue, 16 Sep 2025 19:49:25 GMT  
		Size: 14.1 KB (14078 bytes)  
		MIME: application/vnd.in-toto+json
