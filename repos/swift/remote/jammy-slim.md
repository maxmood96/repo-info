## `swift:jammy-slim`

```console
$ docker pull swift@sha256:40578a1c71f5533edff6cf176c14cab8617ae4dd5079012a5923285c82f12cc9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy-slim` - linux; amd64

```console
$ docker pull swift@sha256:16a133fb85db4c818410c5e37fb1fd1eb36d8e697f5aeb8c43a2897616d0b01f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97724275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b43fffed9bed5224a45c02ae752ff1470dbf3a25f33a933002ded01dec124c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
ARG RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 17:53:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 17:53:13 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 17:53:13 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3650628a66b5d822a25d9c24826ec83fa7be2ad9949f0ec4c34bfa554333b04`  
		Last Modified: Tue, 02 Sep 2025 00:19:08 GMT  
		Size: 19.2 MB (19224169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b876a25aefff8ffbca3064a1f932fd9a8741a355010fd96459d0bdd94a4bcf50`  
		Last Modified: Tue, 02 Sep 2025 00:19:11 GMT  
		Size: 49.0 MB (48963171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:d537b1e1cd5853d0be3f9111d33fd557f1a89cbf1503b0eac6b3745886a2e496
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45a2e69a63452b47d7ccc3c501c7cfe4fb49d397597389bc24354057dc2d870c`

```dockerfile
```

-	Layers:
	-	`sha256:d3e1d32f55591ecc51a24127715bace97eea043b85b0622aad9c35e4ed1bde71`  
		Last Modified: Tue, 02 Sep 2025 01:48:53 GMT  
		Size: 3.1 MB (3055479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14646fb701f121a2486936542550256530932ee7076eba90fcd314aaffd54a68`  
		Last Modified: Tue, 02 Sep 2025 01:48:54 GMT  
		Size: 14.0 KB (13983 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3eb43b8227791aca889381438b757f1a65218060de77b19110a060722b1310f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94841695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f03a72c8fb2bf50a975ef8875b2397994c9ab4b778b01a61768180669c624153`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 May 2025 17:53:13 GMT
ARG RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 May 2025 17:53:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 May 2025 17:53:13 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 May 2025 17:53:13 GMT
ADD file:5f2c65daac761cc691b34ee3e3e2ba42ec520d71fc59aef131d38058a7891ab8 in / 
# Wed, 28 May 2025 17:53:13 GMT
CMD ["/bin/bash"]
# Wed, 28 May 2025 17:53:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 28 May 2025 17:53:13 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 May 2025 17:53:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_BRANCH=swift-6.1.2-release
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_VERSION=swift-6.1.2-RELEASE
# Wed, 28 May 2025 17:53:13 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 28 May 2025 17:53:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.1.2-release SWIFT_VERSION=swift-6.1.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux         $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/libexec/swift/linux     && chmod -R o+r /usr/lib/swift /usr/libexec/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg # buildkit
```

-	Layers:
	-	`sha256:fdf67ba0bcdcbe417cffb2808175ef408d653d78cb464d1917e84ba0f40ef5de`  
		Last Modified: Tue, 19 Aug 2025 19:22:54 GMT  
		Size: 27.4 MB (27361469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbd3b82b4af8b10040b54d52097c9f4c1a2b4e4975985e298a7866dc236f38b`  
		Last Modified: Tue, 02 Sep 2025 03:28:01 GMT  
		Size: 19.1 MB (19088955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29e7c56e64c6fef12bd98b9a7e637849e2f513ccfc6c75e1edb4e2d0a731ea0`  
		Last Modified: Tue, 02 Sep 2025 03:28:04 GMT  
		Size: 48.4 MB (48391271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy-slim` - unknown; unknown

```console
$ docker pull swift@sha256:520736e916e427c143d026658ecafe970ee0bc0f540f1e023018bcf8a675ccaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3069856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed552683237816ec9da3d59d24c24be8242368b2150ede689fc4a9b1b623dc57`

```dockerfile
```

-	Layers:
	-	`sha256:26a93443a07c96759f1b5f6fe033cc12b8af7c5e57efaeb760f06d3a7bc11cff`  
		Last Modified: Tue, 02 Sep 2025 04:49:08 GMT  
		Size: 3.1 MB (3055766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a58f0e4e99505acb88f47d2f77c2b71b9ce821cdd148c23652c7e0562e15e9d`  
		Last Modified: Tue, 02 Sep 2025 04:49:09 GMT  
		Size: 14.1 KB (14090 bytes)  
		MIME: application/vnd.in-toto+json
