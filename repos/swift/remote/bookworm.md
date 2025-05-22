## `swift:bookworm`

```console
$ docker pull swift@sha256:61488fcef1cf56623b6f96d7e44e48c2a399de90420c0876bde61cdd879f86b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:bookworm` - linux; amd64

```console
$ docker pull swift@sha256:f7d0b3639fdeb032f1531f8a881dd7e3ed5761403a7684f201c5587d85adcef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1145577010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6c3ca35568c4cf990ece7b316cf7d39b907a3ffd5ee3e1d1cb0f4fbccdf425d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Wed, 21 May 2025 22:27:42 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210cab727a632a06158162d8f3a89a6a22b9addfa157c250e389ed1aac58c0ad`  
		Last Modified: Wed, 21 May 2025 23:32:53 GMT  
		Size: 198.3 MB (198314472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8633a1ca7cf5e260198f4b1d3173d6e725acaa176c35061777eeeb8929dc5bab`  
		Last Modified: Wed, 21 May 2025 23:33:05 GMT  
		Size: 898.8 MB (898774119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55f9be9eed61f73eee3dfe63bb885aba9ea56c0aee7b5003a97bb59e12ed8b5`  
		Last Modified: Wed, 21 May 2025 23:32:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:bookworm` - unknown; unknown

```console
$ docker pull swift@sha256:0f5439ef456418ac1d1b7cd9c6a424d770698b4a606c56d8a021953f1b8b91fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.2 MB (11173223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d9ad0e0c93a3894aea2ab3b2c276070871d24d88a807aa68f59f7192e7b77dd`

```dockerfile
```

-	Layers:
	-	`sha256:b5397bf5e12046ee2a2e33da3ca3cbe874e5125126b0fd1c93a02148be368570`  
		Last Modified: Wed, 21 May 2025 23:32:51 GMT  
		Size: 11.2 MB (11157471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df080cb0ce6a27265218758c5100072a2d9c2915e9fe53c1ad638e2efac7f6c9`  
		Last Modified: Wed, 21 May 2025 23:32:50 GMT  
		Size: 15.8 KB (15752 bytes)  
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
