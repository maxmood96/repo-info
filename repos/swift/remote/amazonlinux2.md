## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:306b06bc3dece6e6f256d0d5ed2335045b49e5339141d7e75de56142a5ae26ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:cca45695cf53142d72504ba18c3984313b98e92fb7d152fe7ef1c027a55667cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1628950541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d90358657b539a0c0562622eac8f194bc519eb248b346af143540024c05de102`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:52:43 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 15 Apr 2026 21:52:43 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 15 Apr 2026 21:52:43 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Wed, 15 Apr 2026 21:52:43 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 15 Apr 2026 21:52:43 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 15 Apr 2026 21:52:43 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 15 Apr 2026 21:52:43 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 15 Apr 2026 21:52:43 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:52:43 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:53:27 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 15 Apr 2026 21:53:27 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310ed73748145cc7db7c52b4514d226e8d227d030325ee062a9cd6fd5f8232b`  
		Last Modified: Wed, 15 Apr 2026 21:56:04 GMT  
		Size: 329.3 MB (329269653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d485e6f5ee595e37591b0b5a6f3f94b126c0815137d055ab1ebf6192bb829988`  
		Last Modified: Tue, 24 Mar 2026 22:17:17 GMT  
		Size: 1.2 GB (1236725448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7141829cffa6d261d514b60cdc81edc094d3336587b7677842dc0cf43dbe2c93`  
		Last Modified: Wed, 15 Apr 2026 21:55:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:3b0d5b67309f269feeb5be8263babe0fb0da8fa482b8ed1514ea5ec4a673cf29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c65e8f4553627e653da32c1ca42fe4fcdc096363eaed35eee54289a5bb375a9`

```dockerfile
```

-	Layers:
	-	`sha256:a1e868445b6fb3c3012fbf75fff14284906db4917db322ab8b2133fea69cb613`  
		Last Modified: Wed, 15 Apr 2026 21:55:57 GMT  
		Size: 12.7 MB (12720090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a565392883da10fae2f0955f545d12b485e76dd4674b412cb87bbe86876dfcfe`  
		Last Modified: Wed, 15 Apr 2026 21:55:56 GMT  
		Size: 14.8 KB (14835 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:f30af9e2996d98376b1f40a4369ac2513f3476674a2f2d3cfa52c99ac9489334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1584703475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0336c4231635f18633ffc011cb03f39f3fd6003e1c96b6dbf2a355ba9e8cfd5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 22:04:45 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 15 Apr 2026 22:04:45 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 15 Apr 2026 22:04:45 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Wed, 15 Apr 2026 22:04:45 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 15 Apr 2026 22:04:45 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 15 Apr 2026 22:04:45 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 15 Apr 2026 22:04:45 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 15 Apr 2026 22:04:45 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 22:04:45 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 22:05:32 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 15 Apr 2026 22:05:32 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9d66f34a41cd5eab6d9a1feaf2ffd4c043ea47a57c0c192df0596bf9f0754d`  
		Last Modified: Wed, 15 Apr 2026 22:08:08 GMT  
		Size: 300.4 MB (300350493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da830afe4a48477f4e79981e0b1d301531bb8386eefecddcf8ed80ae66f6d107`  
		Last Modified: Tue, 24 Mar 2026 22:17:05 GMT  
		Size: 1.2 GB (1219549834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2237fc5b8127c5043f0a0ed714c665af1188a2d5ab2ea346310faa825be8dc58`  
		Last Modified: Wed, 15 Apr 2026 22:08:01 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:1472966a9ead80dd9e831a7536d5619e42b06c665faea304f725b45eb7b70b3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c18fc19b42cf70a6bbb71e2d76505af8a0e4a67dfbe41ecbe91137bd7136917f`

```dockerfile
```

-	Layers:
	-	`sha256:35b8d63a92e405be53e0ea90fd13ee452a247875ca2a1a97c2957a99d4acca7c`  
		Last Modified: Wed, 15 Apr 2026 22:08:02 GMT  
		Size: 12.6 MB (12581727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c50abf8780482a0dff6af3b8baa88b5b0057bc775ccfef4e44887ba314f422aa`  
		Last Modified: Wed, 15 Apr 2026 22:08:01 GMT  
		Size: 15.0 KB (14957 bytes)  
		MIME: application/vnd.in-toto+json
