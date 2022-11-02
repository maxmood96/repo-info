## `swift:amazonlinux2-slim`

```console
$ docker pull swift@sha256:d7cbc30b7ac44f723fcf2fc987c44a2524661eb8261a04cf8359aa159189a051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2-slim` - linux; amd64

```console
$ docker pull swift@sha256:d9ecb2261603549a7adb78927836e4902115903bcf5ec9416df8431458227217
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.6 MB (288567150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2248a85b8be27e4bd1bea07473c543a68aaeab5dc0f8c2ac0b4d88c560c8ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Oct 2022 00:19:49 GMT
ADD file:33ce740675602f8911c110c617b08d74ebe9c26c82226b4815019d8c2d0a2263 in / 
# Fri, 21 Oct 2022 00:19:50 GMT
CMD ["/bin/bash"]
# Fri, 21 Oct 2022 00:37:44 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 21 Oct 2022 00:37:44 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 21 Oct 2022 00:39:22 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 21 Oct 2022 00:39:22 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 02 Nov 2022 22:55:31 GMT
ARG SWIFT_BRANCH=swift-5.7.1-release
# Wed, 02 Nov 2022 22:55:31 GMT
ARG SWIFT_VERSION=swift-5.7.1-RELEASE
# Wed, 02 Nov 2022 22:55:31 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 02 Nov 2022 22:55:31 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.7.1-release SWIFT_VERSION=swift-5.7.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 02 Nov 2022 22:56:11 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:e3cfe889ce0a44ace07ec174bd2a7e9022e493956fba0069812a53f81a6040e2`  
		Last Modified: Wed, 19 Oct 2022 18:11:43 GMT  
		Size: 62.3 MB (62306642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8345bcf4d30291885028552f9ec088fe00c7fd7b0a5c5e83a11fccbce55a1a7`  
		Last Modified: Wed, 02 Nov 2022 23:13:05 GMT  
		Size: 226.3 MB (226260508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2-slim` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:5707cdcbce61a9dba65c208ad900ade41e79e867c869989e1a86d1ad5cd412b7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252822921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ee61cfbe8c4e3f471e5739670d96c3f23f1737e22ef22eadea5ed9724778c9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 26 Oct 2022 15:27:06 GMT
ADD file:45362bc0bb55d35f704a938eb431f8accb86d1bb8e52b78f3ef34eb141c3ed82 in / 
# Wed, 26 Oct 2022 15:27:06 GMT
CMD ["/bin/bash"]
# Wed, 26 Oct 2022 19:27:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 26 Oct 2022 19:27:42 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 26 Oct 2022 19:29:04 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 26 Oct 2022 19:29:04 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 02 Nov 2022 19:58:58 GMT
ARG SWIFT_BRANCH=swift-5.7.1-release
# Wed, 02 Nov 2022 19:58:58 GMT
ARG SWIFT_VERSION=swift-5.7.1-RELEASE
# Wed, 02 Nov 2022 19:58:59 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 02 Nov 2022 19:58:59 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.7.1-release SWIFT_VERSION=swift-5.7.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 02 Nov 2022 19:59:31 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && yum -y install tar gzip     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && yum autoremove -y tar gzip
```

-	Layers:
	-	`sha256:d900cba9f9f55565485a1181c89317c2718b6232095971d67af440a33db15594`  
		Last Modified: Wed, 19 Oct 2022 18:11:20 GMT  
		Size: 63.9 MB (63919869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd56bcf6ca96be2afd8217153e6d2b700569a16bf33cde408e9f02b0effb84f`  
		Last Modified: Wed, 02 Nov 2022 20:05:09 GMT  
		Size: 188.9 MB (188903052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
