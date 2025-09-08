## `swift:noble`

```console
$ docker pull swift@sha256:c8e7c8e1c6f06c13bc51645dd03abe47e1092be9ce49dbfd8883943d9410b755
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble` - linux; amd64

```console
$ docker pull swift@sha256:cfc65db666a63ddfe6ddda9311486e80301c7754350ccdb0cebba271ed0134df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1057675386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e83850a808df0a226cc4246fe548a673dd4d9953d81e899f7f695ff4567e145`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 06 Sep 2025 05:03:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_BRANCH=swift-6.1.3-release
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_VERSION=swift-6.1.3-RELEASE
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1add8bb65c40e82da9ab7f9f6c0aea1677d3c5e75c6162db1fad4d6af6fa6cf2`  
		Last Modified: Mon, 08 Sep 2025 19:49:45 GMT  
		Size: 130.4 MB (130367983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfa0e7d2a807ff0a06df9a6f516a6f0979dff0276d615863b361ae70a236c6`  
		Last Modified: Mon, 08 Sep 2025 19:51:34 GMT  
		Size: 897.6 MB (897584165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be56e946a18e7d0985944418ab2d1fd5e570947882efdc86e855df48460d8c5a`  
		Last Modified: Mon, 08 Sep 2025 16:50:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:85ccaa666c19afdd71318cb383d943d7a0ff2181a349988c0d65b50ed982393d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7894803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55108ceb912de3accdeae0205cd46cd1669c0c096bf4615926d06c408c51d370`

```dockerfile
```

-	Layers:
	-	`sha256:0795161558bb956551c704fe453806b7897c1d999dd3429443c4d1718366aca8`  
		Last Modified: Mon, 08 Sep 2025 19:47:50 GMT  
		Size: 7.9 MB (7877963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:259bb1153bba4a45dc0d477f43f898695f1be0b2d2bfe6833ca6a48add61255e`  
		Last Modified: Mon, 08 Sep 2025 19:47:51 GMT  
		Size: 16.8 KB (16840 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:97dbb3a769f081cc19313f97a866625fb3d937cbca107b6985f8a04375cf012e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1049963229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5746e278d307835b559131df582dd1e9082c4678590417b136e915949965c583`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 06 Sep 2025 05:03:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_BRANCH=swift-6.1.3-release
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_VERSION=swift-6.1.3-RELEASE
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06267e17355a8003944c6ad7ce9c33cd63c6f4372c5fb607e41f1e20019ce3cb`  
		Last Modified: Mon, 08 Sep 2025 16:50:17 GMT  
		Size: 129.5 MB (129453904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ef4156babe7664abee45a7fd9318c2cf71894ac4d7ff52e7dbe9743bac6fb4`  
		Last Modified: Mon, 08 Sep 2025 16:50:32 GMT  
		Size: 891.6 MB (891648911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7a7a45a0faa5895de4f4b12f54e6a55ef290791fc1b7ce9596b3e7b9ad11e6`  
		Last Modified: Mon, 08 Sep 2025 16:51:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:6509e0622666966c15b1d00912e77f07ac0407bcbf9d0f71e75d492cbf20e2d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7917448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8d1ac040c08c26629765d29867cd503c6664775b301a5ffb1bb44562a342903`

```dockerfile
```

-	Layers:
	-	`sha256:7bb114506324f76d121a1b2acb4c1f81ee9097b1599faf7905730072679843d5`  
		Last Modified: Mon, 08 Sep 2025 19:48:16 GMT  
		Size: 7.9 MB (7900450 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e473a1046828ced555d733a255ad1bce002c4f89746f3aa239a4a8423d3e8e6`  
		Last Modified: Mon, 08 Sep 2025 19:48:17 GMT  
		Size: 17.0 KB (16998 bytes)  
		MIME: application/vnd.in-toto+json
