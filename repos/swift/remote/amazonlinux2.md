## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:9d9cb12621fd333940cfe0b8e0ed3f460109944525af6b52b09be965d966ee3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:9b6ca21b4c6c032db9d3fce511f78d473a515cc40903635211bcd5cf059c2832
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **893.4 MB (893392215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a270ff7cb494876e12f38ad3b080318d7c65cd6379f6cfdb404454e1caf5bf63`
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
# Fri, 21 Oct 2022 00:38:17 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 21 Oct 2022 00:38:19 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 21 Oct 2022 00:38:19 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 21 Oct 2022 00:38:19 GMT
ARG SWIFT_BRANCH=swift-5.7-release
# Fri, 21 Oct 2022 00:38:19 GMT
ARG SWIFT_VERSION=swift-5.7-RELEASE
# Fri, 21 Oct 2022 00:38:20 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 21 Oct 2022 00:38:20 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.7-release SWIFT_VERSION=swift-5.7-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 21 Oct 2022 00:39:07 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 21 Oct 2022 00:39:14 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:e3cfe889ce0a44ace07ec174bd2a7e9022e493956fba0069812a53f81a6040e2`  
		Last Modified: Wed, 19 Oct 2022 18:11:43 GMT  
		Size: 62.3 MB (62306642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8119baad8662ccc1804fb041deb0a70d7ca75d0c1b689f7e9f834d4fe4985a21`  
		Last Modified: Fri, 21 Oct 2022 00:57:13 GMT  
		Size: 285.8 MB (285799595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7df220c2b29c0c320d13faf81deaed3a30164317d790c1e9b48417ca680faa`  
		Last Modified: Fri, 21 Oct 2022 00:57:57 GMT  
		Size: 545.3 MB (545285753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1a23d0bdb4b006237f8d5df3750bbf1befaf6bd29d7d9c78377cd52eea1ce3`  
		Last Modified: Fri, 21 Oct 2022 00:56:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:47e0d1ee0d285a9a2c7bc0255ee31ebae6b99724dc3f1a99ece52a2b575ca8cf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **844.6 MB (844618979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4594dc860d75212c978c95d314932a66a6947af0cf454a3124fb393303755272`
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
# Wed, 26 Oct 2022 19:28:05 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Wed, 26 Oct 2022 19:28:10 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 26 Oct 2022 19:28:10 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 26 Oct 2022 19:28:10 GMT
ARG SWIFT_BRANCH=swift-5.7-release
# Wed, 26 Oct 2022 19:28:10 GMT
ARG SWIFT_VERSION=swift-5.7-RELEASE
# Wed, 26 Oct 2022 19:28:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 26 Oct 2022 19:28:10 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.7-release SWIFT_VERSION=swift-5.7-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 26 Oct 2022 19:28:43 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 26 Oct 2022 19:28:54 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:d900cba9f9f55565485a1181c89317c2718b6232095971d67af440a33db15594`  
		Last Modified: Wed, 19 Oct 2022 18:11:20 GMT  
		Size: 63.9 MB (63919869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abacb6dbc9c45bd9abb9e6f56b356431af997e90321686944b8ef52bbf684035`  
		Last Modified: Wed, 26 Oct 2022 19:32:18 GMT  
		Size: 255.3 MB (255300549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d623deda6d9a92b04a8f7ae2d96ea768edef1748f73db4a55d0ebf736fedb83a`  
		Last Modified: Wed, 26 Oct 2022 19:32:52 GMT  
		Size: 525.4 MB (525398334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc750e016a377077b7b86f75ca18e9ae4958c6c31d8f398a32f47cb2ad5f6f1d`  
		Last Modified: Wed, 26 Oct 2022 19:31:56 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
