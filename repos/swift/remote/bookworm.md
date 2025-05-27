## `swift:bookworm`

```console
$ docker pull swift@sha256:4e09caf5e2d54d9e79ea2082c8e6dc47b6027a96c757a44469fda74f5efa30ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:43ad0cd202dacc32b3300e8bf782d05f94037455169ee51c5c2c291f0b8d0f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1145601475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4f9b740e5c2d63dd7373156655ef86f5ce507bc80ddd3e14626d0d29313116`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Mon, 26 May 2025 22:39:21 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 26 May 2025 22:39:21 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 26 May 2025 22:39:21 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_PLATFORM=debian12
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_BRANCH=swift-6.1.1-release
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_VERSION=swift-6.1.1-RELEASE
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 May 2025 22:39:21 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 May 2025 22:39:21 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Mon, 26 May 2025 22:39:21 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe823326448c5d7994d90cfbe01267a277b8364914bd93b37764b605dc423c7`  
		Last Modified: Tue, 27 May 2025 18:58:38 GMT  
		Size: 198.3 MB (198318479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01763e53285f6afb7a837660e45e84f26402e6ae005a7f94fb3ba4e5f3c3220e`  
		Last Modified: Tue, 27 May 2025 18:58:48 GMT  
		Size: 898.8 MB (898794577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc5c086b312dc60e85816aa2d1dab75456fc47163ed8099415e15673b4766ec6`  
		Last Modified: Tue, 27 May 2025 18:58:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:279e0b6a94475e25bc473d7fdcf4c29b910bca887b4c48f0b7e6a7434bd09a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11173239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3948f6d6b5f626cbf4d63630cb07e788db7950527fd5b09a304a5255b0e3977`

```dockerfile
```

-	Layers:
	-	`sha256:64f75327424522aa32ca3a9cf86886e31ccfb680c92d98c333d3ca47172e41fd`  
		Last Modified: Tue, 27 May 2025 18:58:35 GMT  
		Size: 11.2 MB (11157475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a339c132593b2e1593841e1dbaea15eb33d7978100664f8eba7f3f168535fa`  
		Last Modified: Tue, 27 May 2025 18:58:35 GMT  
		Size: 15.8 KB (15764 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c37b80886d150591b81cfcfd64aaded51749873df356767432b6e264c709c338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1132092469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:044e389d07e036acf614a6fb8a0751b8c8c5dc60d427a6e7118a45ae645d47f5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=debian12
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdbdefeec6ff982cd11a443a39e7937c406e09ebe28f5ebc0b1cf5d3d8158c3`  
		Last Modified: Thu, 22 May 2025 07:40:59 GMT  
		Size: 190.2 MB (190159697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b2dadbf084d5a6e7138c92d20c24b138059b433be9d13b3860040bda85311af`  
		Last Modified: Thu, 22 May 2025 07:41:14 GMT  
		Size: 893.6 MB (893605416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a514ddddcf9268e77fed07016f73fd0f458093be778b294e357a1eed763d0b43`  
		Last Modified: Thu, 22 May 2025 07:40:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:31f0bf0e230dd780024c41e48e5395c66396d0bc19a5eac98b17748625b5e99f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11201349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6371da222d0f2f448baad95a928a3712f25ec8af32f0025b00e9c300f788dca4`

```dockerfile
```

-	Layers:
	-	`sha256:6cfe3a413c62797db83be88bdda1cc26de1c668bb04aff24a6b1cbf08d6e4f97`  
		Last Modified: Thu, 22 May 2025 07:40:55 GMT  
		Size: 11.2 MB (11185475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a349d5327a3901f84ff19ad4b217df30915e28dc5caae2989c4bcc30f872009`  
		Last Modified: Thu, 22 May 2025 07:40:54 GMT  
		Size: 15.9 KB (15874 bytes)  
		MIME: application/vnd.in-toto+json
