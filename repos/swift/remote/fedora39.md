## `swift:fedora39`

```console
$ docker pull swift@sha256:b3f441afc0e8f2c07774528eb52f51a074b4d8fdbd2d9bcb1b871f5f95ea0f09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:fedora39` - linux; amd64

```console
$ docker pull swift@sha256:8d8fde13a003a088a2efa90d98e68d85a21226118ee046e534d371502196146c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1128510542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95479a5729717813a36900e3e936d967ef9537b279d82ddf6e027bdc68db973c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 06 Jun 2024 15:11:32 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Thu, 06 Jun 2024 15:11:32 GMT
ADD fedora-39-x86_64.tar.xz / # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
RUN yum -y install   binutils   gcc   git   unzip   libcurl-devel   libedit-devel   libicu-devel   sqlite-devel   libuuid-devel   libxml2-devel   python3-devel # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=fedora39
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:71b76c4c0078fa6f40daca5688b6d78622acedbc7b366c9d80acc8efb0aef476`  
		Last Modified: Mon, 29 Jul 2024 18:56:25 GMT  
		Size: 64.9 MB (64886785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486df570fe720a953cb6230f17b2bf82e185bb76117e843716458d4aa60157b2`  
		Last Modified: Mon, 29 Jul 2024 19:52:34 GMT  
		Size: 342.9 MB (342930610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118e171f98f1f49374e76002c2b09139462a7a236ef17bfed95be56699d6ad3`  
		Last Modified: Mon, 22 Jul 2024 22:11:00 GMT  
		Size: 720.7 MB (720692973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed5093f8c1207ca468ce25e3f6cef0e0f0042de12ddb86ce9a9b6a48f52290f`  
		Last Modified: Mon, 29 Jul 2024 19:52:28 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:fedora39` - unknown; unknown

```console
$ docker pull swift@sha256:f4c1a881a4ce41c81df6443c179f685be3c5eacddbe6d180c70977fbc6992628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9397431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6066dd21504e2ba3eb916d0563bbc7a52917905ab4a749ff913d372bfd3b958a`

```dockerfile
```

-	Layers:
	-	`sha256:0af1aaeacb42c6ea78f9808f360a4e11ec899b01ee86abc55353433c48335f45`  
		Last Modified: Mon, 29 Jul 2024 19:52:28 GMT  
		Size: 9.4 MB (9382886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19963c5b30ffa31bac95a04160b3b65b106891d4c9ed301ec94599f7ff778226`  
		Last Modified: Mon, 29 Jul 2024 19:52:28 GMT  
		Size: 14.5 KB (14545 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:fedora39` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d3a6c4868d59590957e9c84de3a97a685653760465e9f34d19b29fc2ba72cca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1006426440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7794e2c383b50195e98fe7c9ccce77a094d0bd0edb335872da24c3d1931b4637`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Thu, 06 Jun 2024 15:11:32 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Thu, 06 Jun 2024 15:11:32 GMT
ADD fedora-39-aarch64.tar.xz / # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
RUN yum -y install   binutils   gcc   git   unzip   libcurl-devel   libedit-devel   libicu-devel   sqlite-devel   libuuid-devel   libxml2-devel   python3-devel # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=fedora39
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:895dcefed1d2120c414413619ca21832169e3831080a849f6e3e8072a8e8b8d2`  
		Last Modified: Mon, 29 Jul 2024 18:58:06 GMT  
		Size: 63.5 MB (63545888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105734de2dd5c9079c1917fd0cd7afe403b28315d4f2a11843430fb1f4bb3c44`  
		Last Modified: Mon, 29 Jul 2024 19:52:02 GMT  
		Size: 325.4 MB (325435097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb176a5540e18374515e5906c9cbf7cbe9f45de62440272a66663e2aec258a0`  
		Last Modified: Wed, 24 Jul 2024 17:58:42 GMT  
		Size: 617.4 MB (617445280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:636e33be76d3341eac6386cc2ca97048d636e349dadb9c9c2b4a51147c0bfae4`  
		Last Modified: Mon, 29 Jul 2024 19:51:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:fedora39` - unknown; unknown

```console
$ docker pull swift@sha256:6c1646a6639df0279eba9bcaae4b5cd398bfcb2747aa5537d7d345b8c2a04e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9295440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627cf3c61029e4a095dddf83316e24af0f386f200042f48b3a4da3e61b2ea94e`

```dockerfile
```

-	Layers:
	-	`sha256:e100e4250471540706b8a1df1bba7a14091dfb62d15152304e81dbfeb3c415c6`  
		Last Modified: Mon, 29 Jul 2024 19:51:55 GMT  
		Size: 9.3 MB (9280521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f07804a9dabb71162fdd915386fa1639721e5a2737793bebc8a2c597052c4604`  
		Last Modified: Mon, 29 Jul 2024 19:51:54 GMT  
		Size: 14.9 KB (14919 bytes)  
		MIME: application/vnd.in-toto+json
