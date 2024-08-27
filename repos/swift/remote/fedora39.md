## `swift:fedora39`

```console
$ docker pull swift@sha256:f0dc779d8afa2019e86f36554448d29132255610ebbd03af4599dbc8810445f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:fedora39` - linux; amd64

```console
$ docker pull swift@sha256:c5588d6b0db9e31c5786c5deec1d95bd8c6e18df29cca12b18e88b67627782ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1129603622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbf8b86e493b0d8873e62d467e7a0aabfd7ee3a744fdf56a686c78adf516eee`
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
	-	`sha256:8aabb11ccd002f37ec0b66ffe7f545f4c0260cb243b797c02717210d666a17a6`  
		Last Modified: Mon, 26 Aug 2024 22:56:16 GMT  
		Size: 64.9 MB (64868871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1b9714f852bd2cc485b7c32cd8af3c63b5a715f68e3a31cf0680a21989a49c`  
		Last Modified: Tue, 27 Aug 2024 00:01:03 GMT  
		Size: 344.0 MB (344041604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b118e171f98f1f49374e76002c2b09139462a7a236ef17bfed95be56699d6ad3`  
		Last Modified: Mon, 22 Jul 2024 22:11:00 GMT  
		Size: 720.7 MB (720692973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40102ccb4a1ecdee28f7a1f05174cb6732aac638cd3d150c8ef0b494bd346f26`  
		Last Modified: Tue, 27 Aug 2024 00:00:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:fedora39` - unknown; unknown

```console
$ docker pull swift@sha256:84385a34a8db5338795664742ea16b1770718050a4111ae54605214b7f1b5cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9400140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26542ff0a286e2179e2b530e78a527a9f41e15cc16259dc04e7b77f42592c639`

```dockerfile
```

-	Layers:
	-	`sha256:9a7d8d70fd80a55e237b2137839bdb0772e84a377af85690a0d7cfcc5dac0664`  
		Last Modified: Tue, 27 Aug 2024 00:01:01 GMT  
		Size: 9.4 MB (9385594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5586ea7d64b07a94bb665df93454490576c8dad359b5aa5272c125d4f1a9bc87`  
		Last Modified: Tue, 27 Aug 2024 00:00:59 GMT  
		Size: 14.5 KB (14546 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:fedora39` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:46d5ca4be39f54c093426619a500d1265a9fb43d2675832847b269bfd35f26f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1007394259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd991a593f8196bf52f83682958d666bd517c5292b89326e44c975e2850eb696`
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
	-	`sha256:83453e252cce33981ff26614452fce537bbd274f8fe42bec49ea908d277cdc3d`  
		Last Modified: Mon, 26 Aug 2024 22:55:58 GMT  
		Size: 63.5 MB (63540830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b940a1633ae4b5b6390447072dde0e59eda52e37725e156a2c74bf7c069d331`  
		Last Modified: Tue, 27 Aug 2024 00:00:39 GMT  
		Size: 326.4 MB (326407975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb176a5540e18374515e5906c9cbf7cbe9f45de62440272a66663e2aec258a0`  
		Last Modified: Wed, 24 Jul 2024 17:58:42 GMT  
		Size: 617.4 MB (617445280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e37c8ffc864cd23d00da1459e8998986f3814fe4a3d7548910296167566fe07`  
		Last Modified: Tue, 27 Aug 2024 00:00:32 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:fedora39` - unknown; unknown

```console
$ docker pull swift@sha256:7a913c7c797ee921e754763c0ed27a434aefd8163e2ad9ebe3dbc143607ed294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9298147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c664a15a461b2207003407659151aae4b5e1245595299fb95b0ba9831141e852`

```dockerfile
```

-	Layers:
	-	`sha256:bf36916d9de7a8b53a1fb75e990390dee1c40dc96956f24012893d21465df26e`  
		Last Modified: Tue, 27 Aug 2024 00:00:33 GMT  
		Size: 9.3 MB (9283229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc63cd976ef106ae218980cd6ebd6c9d47142bed21d98c473f963a6fbd3d188`  
		Last Modified: Tue, 27 Aug 2024 00:00:32 GMT  
		Size: 14.9 KB (14918 bytes)  
		MIME: application/vnd.in-toto+json
