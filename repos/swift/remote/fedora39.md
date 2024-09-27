## `swift:fedora39`

```console
$ docker pull swift@sha256:240a84ddadd905989d701ac1b80c3772638597b89edc91487dc9076fba7cb0d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:fedora39` - linux; amd64

```console
$ docker pull swift@sha256:29c97287ea075bf76087ff5b20d727fc178dd802785b759566e9f9a414743ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1256803010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500ac71fca1f3f08d3f7a563d3e2c965f5aacb79ad3b645c82e13db246a33482`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 10:40:52 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 15 Sep 2024 10:40:52 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Sun, 15 Sep 2024 10:40:52 GMT
ADD fedora-39-x86_64.tar.xz / # buildkit
# Sun, 15 Sep 2024 10:40:52 GMT
CMD ["/bin/bash"]
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
RUN yum -y install   binutils   gcc   git   unzip   libcurl-devel   libedit-devel   libicu-devel   sqlite-devel   libuuid-devel   libxml2-devel   python3-devel # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=fedora39
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:8fbaf22a49eb14a89c9ae872033ffd84bcccd25d4bcd55d33bc936ac30a7efc8`  
		Last Modified: Mon, 16 Sep 2024 18:58:27 GMT  
		Size: 64.9 MB (64890373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d897ab45dbf45e264a7349698dbd04f23c122e0d505d7cdb66d1669d738eb7`  
		Last Modified: Thu, 26 Sep 2024 22:59:58 GMT  
		Size: 360.1 MB (360121473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3285da2e502def12cbe9e9de89548a314db4a084fc8536e8a1a67ca3c79f6f6a`  
		Last Modified: Thu, 26 Sep 2024 23:00:04 GMT  
		Size: 831.8 MB (831790989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dec7ceb03c58adab718e2f06657ba2543075e53f760356d5cab9cb9c35a888`  
		Last Modified: Thu, 26 Sep 2024 22:59:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:fedora39` - unknown; unknown

```console
$ docker pull swift@sha256:6c6ce58a5390c447a6fb10afd768d5fd08dc896b22d6e56ec2bb5cef8964ab2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9400993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:360958589695340daed6c74f2ccd476bf20be1bde287ac61a2a8c0051e9c2fd4`

```dockerfile
```

-	Layers:
	-	`sha256:737abace6bd13cb4bf4b7217d9a9c66874d580e9f65c290483129629fd29039e`  
		Last Modified: Thu, 26 Sep 2024 22:59:52 GMT  
		Size: 9.4 MB (9386493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:568f803474c89b11d81020f42933b2f3b167685d1761de7513e08bf6e5bf4412`  
		Last Modified: Thu, 26 Sep 2024 22:59:52 GMT  
		Size: 14.5 KB (14500 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:fedora39` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:e2db790a7054d20ecb95c21fd5a40e3f6ecad580a043d45cc844500ca83fe3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1219763660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92b302d8cd89f98352456d8313521c5c5ff8328a4c10ae9c5efab9183224f4da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 10:40:52 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 15 Sep 2024 10:40:52 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Sun, 15 Sep 2024 10:40:52 GMT
ADD fedora-39-aarch64.tar.xz / # buildkit
# Sun, 15 Sep 2024 10:40:52 GMT
CMD ["/bin/bash"]
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 25 Sep 2024 05:07:02 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 25 Sep 2024 05:07:02 GMT
RUN yum -y install   binutils   gcc   git   unzip   libcurl-devel   libedit-devel   libicu-devel   sqlite-devel   libuuid-devel   libxml2-devel   python3-devel # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_PLATFORM=fedora39
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_BRANCH=swift-6.0.1-release
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_VERSION=swift-6.0.1-RELEASE
# Wed, 25 Sep 2024 05:07:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 25 Sep 2024 05:07:02 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.1-release SWIFT_VERSION=swift-6.0.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:921ce67e7e51e665859857ab2067fdaea0a4c4d71ebc293d6d7bc9a43f9f9ae7`  
		Last Modified: Mon, 16 Sep 2024 18:58:40 GMT  
		Size: 63.6 MB (63561057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1384341e6d97dc1a8ba4a76362188ea76fc16ad4fd3b9b652bcfb64b566a17c9`  
		Last Modified: Mon, 16 Sep 2024 19:54:15 GMT  
		Size: 326.9 MB (326944428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5396685689a50b915153575e0c3cbbbb51fd35f3078885fcb173c5cf0e239eca`  
		Last Modified: Fri, 27 Sep 2024 09:49:09 GMT  
		Size: 829.3 MB (829258002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8a5005e40931c9d9a2f1963e6252a1acc475d598b97fdad55cd95e70b3aaa4`  
		Last Modified: Fri, 27 Sep 2024 09:48:50 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:fedora39` - unknown; unknown

```console
$ docker pull swift@sha256:b362c3ff341e5decd23eebeec2fcf1b2b148edebcf25e04d22d31dc7f196180b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9298107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b55dac55de2bbbca9ed983ae4176ebb5f5442089a1bf061a1b2f40f465a919`

```dockerfile
```

-	Layers:
	-	`sha256:86f6e36ea964956fcde9b16db82bc86353f6467e585cf6d7c054725bb9fb71ee`  
		Last Modified: Fri, 27 Sep 2024 09:48:51 GMT  
		Size: 9.3 MB (9283234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ef3bf77cb9f420a1ddebe67ccd5d9dd9c54573b54fe94b57490601014d44cb7`  
		Last Modified: Fri, 27 Sep 2024 09:48:50 GMT  
		Size: 14.9 KB (14873 bytes)  
		MIME: application/vnd.in-toto+json
