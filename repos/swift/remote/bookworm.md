## `swift:bookworm`

```console
$ docker pull swift@sha256:39ec7ecb016c51219e8dbacda6cee941afeb512fe7fe90af551167b127a2da00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:e21dde60a31669aa58a2979efba6cc1619d986b0144a6b25ceb9ce79f94821be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1072936955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198676751473abd6be500ba73e545645e5fdd9e2e4bedcd2e9f13115403aa0f9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1212991382127db001c7aab5f3e4a69a53749426911b2f3c793118cb0c5ba2b6`  
		Last Modified: Tue, 03 Dec 2024 02:39:39 GMT  
		Size: 194.9 MB (194906479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88c92986e7e3921aa3c8494eec3ceb9655abb828f3e899fbccdf7796e03bf64`  
		Last Modified: Tue, 03 Dec 2024 02:39:50 GMT  
		Size: 829.5 MB (829533092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743f6b0994fb9b2227535942f917f8a7d8e60844518beba933022953390ccb92`  
		Last Modified: Tue, 03 Dec 2024 02:39:37 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:87f752f713888ab0df38cfa76180ff955eeedc5f9009cb63917d939842959293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10483082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6371f27cb732064f48707b414b12488c3518fc0927798980477067d6f185f616`

```dockerfile
```

-	Layers:
	-	`sha256:c4f0d5482844d6d292cd25b4029fcb252640347c212997e54430a44a3d049ee3`  
		Last Modified: Tue, 03 Dec 2024 02:39:37 GMT  
		Size: 10.5 MB (10467398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89c6790ef463e970ffe966e8f6d8a5eae3ac0706a83fde349460805f265d0199`  
		Last Modified: Tue, 03 Dec 2024 02:39:37 GMT  
		Size: 15.7 KB (15684 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:78e05e14c8e63964475553a7c652cdd020e6e4a7ab66bc091b4ce8f42bca08b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1062115998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb6b3a3c8399923e96ee738fa7dc1049779a287eb72325e301f447d45816038`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils-gold     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246313fa97ca40c97d7ff266ce52143eaa84a0b0b8a31ee95befc247c6adeb74`  
		Last Modified: Tue, 03 Dec 2024 11:06:24 GMT  
		Size: 186.7 MB (186721749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a21807e4eb3182ee9c5809166a7117d09d66384c00c27b626e260479b8f616`  
		Last Modified: Tue, 03 Dec 2024 11:06:37 GMT  
		Size: 827.1 MB (827068395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81a21106aea6cece25fdf0ec40b56bcb64903204e2825679e417b0783f1d3230`  
		Last Modified: Tue, 03 Dec 2024 11:06:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:7c0d84c2a9680ff5e0f97d2aa5a5296e3391723e9ff77227d441e5b4f28eac1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10511213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2f8aeb759188d6f2b4f2024389b0df74b3fdf69187adcb552e02f4f36ddd67`

```dockerfile
```

-	Layers:
	-	`sha256:777d602af0bf640096b9d753b6e0fcebbda6995336e701762ba9bec02f2ec2d7`  
		Last Modified: Tue, 03 Dec 2024 11:06:20 GMT  
		Size: 10.5 MB (10495407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e560b10a3b078ada6ca8994305edc9a4c9bc904a0022865d02e4ab6c5b43ec4`  
		Last Modified: Tue, 03 Dec 2024 11:06:20 GMT  
		Size: 15.8 KB (15806 bytes)  
		MIME: application/vnd.in-toto+json
