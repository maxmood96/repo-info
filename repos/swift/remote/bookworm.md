## `swift:bookworm`

```console
$ docker pull swift@sha256:ac35e9d326a3d4c176f4f1a43a5e6019de372fb0fe91dc9e4844e53b99df2148
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:cfc620422f0c78c6090ff5e46ffd12fb8ef3c17593b946f7683fee4cf9778efc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1338868895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49c91f87f7cb8802808369b2bf0ab2f6fd0aeac65aaac32e56f3af6a2d3732c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:13:06 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 22 Apr 2026 02:13:06 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 22 Apr 2026 02:13:06 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:13:06 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 22 Apr 2026 02:13:06 GMT
ARG SWIFT_PLATFORM=debian12
# Wed, 22 Apr 2026 02:13:06 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Wed, 22 Apr 2026 02:13:06 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Wed, 22 Apr 2026 02:13:06 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 02:13:06 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 22 Apr 2026 02:13:47 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Wed, 22 Apr 2026 02:13:47 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f733b41c4c0517b8114e19a27cdc43b6e9796114930f4f9daec642b4fddf80`  
		Last Modified: Wed, 22 Apr 2026 02:16:02 GMT  
		Size: 198.4 MB (198446254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc228cd5ee9bb8167f4f0ee5357e8e7f8772ba39085cbe0a11d4fdc3252e58b2`  
		Last Modified: Wed, 22 Apr 2026 02:16:19 GMT  
		Size: 1.1 GB (1091933840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f9976ec65bb1e43e37ef8ad4e175980800de4f9372372215d6bec12393ccfb`  
		Last Modified: Wed, 22 Apr 2026 02:15:55 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:aa59b52b1331d8f5eeceb684358878f8ecbb130bef5067644f68a72b50b9998b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.3 MB (11330724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9cf9212c9af42ce25725cb69666e050184229cef74aa211f3056f0e06f6769`

```dockerfile
```

-	Layers:
	-	`sha256:63668f38ae8dda0e0c0e3919f35189918a4d2cc84dc60a89361c5a8fe60051e7`  
		Last Modified: Wed, 22 Apr 2026 02:15:56 GMT  
		Size: 11.3 MB (11315001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8098072a85cf635204302ff234334e3ec5222ed6b3e2bf4af58a112808104832`  
		Last Modified: Wed, 22 Apr 2026 02:15:55 GMT  
		Size: 15.7 KB (15723 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:bookworm` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f0008d780af4cafa9a2da324b00ded63bfa6e3af9b975a0bf3bbf358e3bad5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1325031722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1e39cd0dc45d3530a6768492af1dfa147c9553c5a52fef327aeebff7f2f04a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:16:29 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 08 May 2026 20:16:29 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 08 May 2026 20:16:29 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     libicu-dev     libcurl4-openssl-dev     libedit-dev     libsqlite3-dev     libncurses-dev     libpython3-dev     libxml2-dev     pkg-config     uuid-dev     tzdata     git     gcc     libstdc++-12-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 20:16:29 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 08 May 2026 20:16:29 GMT
ARG SWIFT_PLATFORM=debian12
# Fri, 08 May 2026 20:16:29 GMT
ARG SWIFT_BRANCH=swift-6.3.1-release
# Fri, 08 May 2026 20:16:29 GMT
ARG SWIFT_VERSION=swift-6.3.1-RELEASE
# Fri, 08 May 2026 20:16:29 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 08 May 2026 20:16:29 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 08 May 2026 20:17:16 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gpg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gpg # buildkit
# Fri, 08 May 2026 20:17:16 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=debian12 SWIFT_BRANCH=swift-6.3.1-release SWIFT_VERSION=swift-6.3.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:8eda28c6ece628fdff982fd6c7c1cd1f5eeccc51cfd0a3ee9155b2ccbdcc68a3`  
		Last Modified: Fri, 08 May 2026 18:24:51 GMT  
		Size: 48.4 MB (48373150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c8cb6286a109a2cfe3cda71ddbc4c9bece7e4088c0483e4d557f2a0997c119f`  
		Last Modified: Fri, 08 May 2026 20:19:38 GMT  
		Size: 190.5 MB (190508662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edb429276e8dbb30047df13dd855c042d9f259714922d2baeb0a67004915d43`  
		Last Modified: Fri, 08 May 2026 20:19:59 GMT  
		Size: 1.1 GB (1086149735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830de082f42bb66889de5072cb0493f98b10fd8bf31eecca28d355085d6a1106`  
		Last Modified: Fri, 08 May 2026 20:19:30 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:0260e08036c2aaf0c9cc46ad1ddd091c734a5fba7bb09b54f5142fcd7e914028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.4 MB (11358851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b201eb1ebfd723396b4c9e3753f6e188ad05a5b1536961d47e0170b54910ed21`

```dockerfile
```

-	Layers:
	-	`sha256:d51b1fa292459330c2c8f86ecfacbf59ddbc5a54a509d6f9e04bfe1a476e26fd`  
		Last Modified: Fri, 08 May 2026 20:19:31 GMT  
		Size: 11.3 MB (11343006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e66edc30e12e23ea1f5e2f585ff8670807bbae399cbfaec27afc9fcd95fb005`  
		Last Modified: Fri, 08 May 2026 20:19:30 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json
