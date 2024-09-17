## `swift:bookworm`

```console
$ docker pull swift@sha256:a2bf416cc01d0a4fc813027004f70dc2e627bb793b5204728cb450ab15a97f2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:0bc79616cad9d7239c27287252cf7954631db9feefe6adc1663bc80964857542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1073134476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b360e8968c174df55b07bb545093e769957dfcc31f925f8425bc586c17ac2dae`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:36 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 04 Sep 2024 22:30:36 GMT
CMD ["bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34eb0e6b783c72321307cad1bfc771a2e534786786f58e4fa227348566d65886`  
		Last Modified: Tue, 17 Sep 2024 17:01:01 GMT  
		Size: 194.9 MB (194863662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe168342459ada4b0eba50889fc4f9be5b0682b85e7d7066784eec2d205e49a`  
		Last Modified: Tue, 17 Sep 2024 17:01:15 GMT  
		Size: 828.7 MB (828713938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e5fad1a7025a5a76ecbbacae6ccff33197c3f935d1ed7541a934243fb29c2e`  
		Last Modified: Tue, 17 Sep 2024 17:00:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:9238ad768e5651b76d40ef8ab4db1d716e505ee62a4b2110c41f6c0d35fc8330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10455947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6e7afc63b5f8b7e4af5106732c820d3daa3549facdda00542425a13a163895`

```dockerfile
```

-	Layers:
	-	`sha256:2fd9f4e29bb06ea48c40cb86105cc22a9b2355d3f8d6f5993d5672465230811a`  
		Last Modified: Tue, 17 Sep 2024 17:00:58 GMT  
		Size: 10.4 MB (10440514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4887bc2d4abc864aa0e80f0c7c1094a778ddd6205fc60c4f703e1f7d86dd8003`  
		Last Modified: Tue, 17 Sep 2024 17:00:58 GMT  
		Size: 15.4 KB (15433 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:ce0351c8c1e5f290b76f1aace4b4c73ae8d219d86c01ad3934eea8e2a7dc619b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1062501370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b839596600d0697c5445ae5e6838409b0086b870f2f39075e8696391eb521a2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:42 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 04 Sep 2024 21:39:43 GMT
CMD ["bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023c5dab8d9eeda9af3786ded05fdbd33fdb0a5919f7e4e045e2c0fa9284f6cd`  
		Last Modified: Tue, 17 Sep 2024 17:16:30 GMT  
		Size: 186.6 MB (186644951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bab3582b922cf8c917690781542baad6244e3baac66109db2109a5d7a24609`  
		Last Modified: Tue, 17 Sep 2024 17:16:43 GMT  
		Size: 826.3 MB (826270622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11868fb1642834b874f9fdbdd3845b91d8cbfcc6e243d9837f9fcaac88c0862c`  
		Last Modified: Tue, 17 Sep 2024 17:16:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:c8e2254def5067838c493d25d6d44424e141376a9e0721940177c31bab517855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10484242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b3bd6099dd2ca9069c0538e3b123a84b3429aedf7fe5c323dcd5326f0e8d26`

```dockerfile
```

-	Layers:
	-	`sha256:daa356983703b31108e39ae1da6901d84b0919506138bcb7819f9dca13233d5c`  
		Last Modified: Tue, 17 Sep 2024 17:16:26 GMT  
		Size: 10.5 MB (10468523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9633fde3e3ff0635348f4d8e7a1f5605ae6ad0c570f202d22daf6ca01a91149`  
		Last Modified: Tue, 17 Sep 2024 17:16:25 GMT  
		Size: 15.7 KB (15719 bytes)  
		MIME: application/vnd.in-toto+json
