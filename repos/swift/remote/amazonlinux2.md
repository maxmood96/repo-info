## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:36f9c9de261c93c48dac83e64b90a8fafd920c0d4382b4f0bd896ff5316d2000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:fa9ded68229e6424ce832d562ac8a99cb082a2e6bef240681e4d3dfd89fa7245
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **962.5 MB (962470123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16531c982c2351c813d911c9a843ea1bf987dee17d55c4f771e2ed9d1717a69c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:21:53 GMT
COPY dir:3e6cf913ede7c7c09de0465c096dad9a8bea883f026db356d68f0e799e2e3847 in / 
# Fri, 03 Nov 2023 22:21:53 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 23:02:08 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 03 Nov 2023 23:02:08 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 03 Nov 2023 23:02:38 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 03 Nov 2023 23:02:41 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 03 Nov 2023 23:02:41 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 03 Nov 2023 23:02:41 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Fri, 03 Nov 2023 23:02:41 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Fri, 03 Nov 2023 23:02:41 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 Nov 2023 23:02:41 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 Nov 2023 23:03:26 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 03 Nov 2023 23:03:32 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:6ebddf7084e9402a3ba6cf1360703e12633f9c49f51772f99c298cd1048d728e`  
		Last Modified: Fri, 03 Nov 2023 11:40:21 GMT  
		Size: 62.6 MB (62646469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4dd8fab03d74e6f6bba61941d975b990ad8aae51068d8da49643d7cde8a6c9`  
		Last Modified: Fri, 03 Nov 2023 23:20:41 GMT  
		Size: 291.6 MB (291561741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187bb5396a31ee151e52a43535438b25b8ee337481806da8312466ac00abdc01`  
		Last Modified: Fri, 03 Nov 2023 23:21:25 GMT  
		Size: 608.3 MB (608261712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50d761c44bdc8ba825154a45f45778a38267fdc523cb7c8e83a802a124a2d0f`  
		Last Modified: Fri, 03 Nov 2023 23:20:04 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3f8c4425a05b0f922723de60244c32fc9fae3b3dbeb11395b978ab48681153dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **924.3 MB (924319583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8574eb9a6c7c4246066e2b22177209ea53b05bb86c7c5822a5dace20841e661`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Nov 2023 22:40:19 GMT
COPY dir:fd6882cfe0ef7631745084a3b6ac01566c46fa528d35361defcd296ca1356d38 in / 
# Fri, 03 Nov 2023 22:40:20 GMT
CMD ["/bin/bash"]
# Fri, 03 Nov 2023 23:14:58 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 03 Nov 2023 23:14:59 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 03 Nov 2023 23:15:22 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Fri, 03 Nov 2023 23:15:27 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 03 Nov 2023 23:15:27 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 03 Nov 2023 23:15:27 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Fri, 03 Nov 2023 23:15:27 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Fri, 03 Nov 2023 23:15:27 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 Nov 2023 23:15:27 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 03 Nov 2023 23:16:05 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 03 Nov 2023 23:16:17 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:615a413db4e82f95ffe4a1cef67468f86d056893cb442e21cb7cea8bc622f9d0`  
		Last Modified: Fri, 03 Nov 2023 17:50:57 GMT  
		Size: 64.4 MB (64380203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663790df51f11b208b4af846c95b8fb4a6d23d3abe7491cce07cb1f4e9c48f95`  
		Last Modified: Fri, 03 Nov 2023 23:22:35 GMT  
		Size: 257.9 MB (257858326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6896cb2a7890efad7f7c0693cd64fdbe4a8c249c138ca6e64560397331591eba`  
		Last Modified: Fri, 03 Nov 2023 23:23:11 GMT  
		Size: 602.1 MB (602080857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082253342c6ecef8f24bb3a5594d0a6fc8a23e95d2b1af98ba00fadbc2367193`  
		Last Modified: Fri, 03 Nov 2023 23:22:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
