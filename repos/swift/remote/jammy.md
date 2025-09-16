## `swift:jammy`

```console
$ docker pull swift@sha256:5635772543306e129257de8b65d1ef05832215334803ef792039e51b14d84ea3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:25160ffbcc1c8d716580c492267b269981d720fc6c79f6f7a9dda611ffd686f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1232669993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c73fcc98234d4716120247517c016c384ee9dff258cf6b5efc78ee2bf694aab1`
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
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
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
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba82835be63042f274bc388c8acbfa9386078e0e82a53521c6ccfa3eeeb030c8`  
		Last Modified: Tue, 16 Sep 2025 16:55:08 GMT  
		Size: 175.5 MB (175466692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b92c96fac7b6d78b3cdd4f358f369aa192ccb0fe81e4d10877290422c28452f`  
		Last Modified: Tue, 16 Sep 2025 16:55:39 GMT  
		Size: 1.0 GB (1027666192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e7151ab008c5eff9a52e62c90bf5e3b94465372c42e9215de7e40dd0d358e5`  
		Last Modified: Tue, 16 Sep 2025 16:55:49 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:e22aa06c107083c0b237f3d5ded0cb134ed51861cce1275657678dc6d039d62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9d97f1915d116afb7e86444c05d0b22cd2ddc553693b08ce3855ef49d16ddc`

```dockerfile
```

-	Layers:
	-	`sha256:d982824b86d5ac87ba49c08de155a739c633681473a41e3fbbb3936b24edfbf8`  
		Last Modified: Tue, 16 Sep 2025 19:49:14 GMT  
		Size: 8.5 MB (8477451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8514e39ffa190df79d00b1b23f05987e8838a24635aa54a0eac981b17b25d95`  
		Last Modified: Tue, 16 Sep 2025 19:49:14 GMT  
		Size: 16.0 KB (15951 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:37951b5d61a29676b09e4b1ebbead84897e666c15b899a3eda50bbf2b2f5faf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1221259302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8effee568d3352cf05537192c2d403bd34cf071805ec72c1b63bfb13eae1b9af`
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
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
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
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Mon, 15 Sep 2025 22:15:37 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2-release SWIFT_VERSION=swift-6.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91f3f7173c498e65044579d3fbaca8f940067e95c5de7735f8b82156a441de2`  
		Last Modified: Tue, 16 Sep 2025 16:55:26 GMT  
		Size: 171.7 MB (171718903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1692e4bf3b42701ba0672f428f3930c5490493e0583dd54ce3a3a1c46b8ddc`  
		Last Modified: Tue, 16 Sep 2025 16:55:49 GMT  
		Size: 1.0 GB (1022178756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf428c6a7c86ecb83102dbb18a20f0477874c1cfd07c7155b17ecfca3810842`  
		Last Modified: Tue, 16 Sep 2025 16:55:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:6e6c088b62ccc17293128906cc2a5391018944d40b05021db3c86aaa0a29108d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8489210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8f81cd422b403d8ebe9b7d3ab5bc4e9ea9eceaf669a17bee6b149f3f4df3ed`

```dockerfile
```

-	Layers:
	-	`sha256:8a437315a061922f1c8652a198808fd797ce799216c249a175b6248ac6c82d17`  
		Last Modified: Tue, 16 Sep 2025 19:49:27 GMT  
		Size: 8.5 MB (8473137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49f7495da2911879e86dfdc2ea9c6a7e26e9c8ec6b9e59bb46b785f5a843717`  
		Last Modified: Tue, 16 Sep 2025 19:49:28 GMT  
		Size: 16.1 KB (16073 bytes)  
		MIME: application/vnd.in-toto+json
