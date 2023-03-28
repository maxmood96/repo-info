## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:dcde52239e24dd428a59ca65d5dd2d126541c50cc550061c416a44aec116760a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:a60b26e4481b8d838c1c42a7910d91773bbe5377a28e1937dd8f52ec2d903270
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **903.5 MB (903501848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc59cbf8a447d62b4ace2e788de9e285f03ecbc3d0d229620facb87f27f5e28`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Mar 2023 18:20:51 GMT
COPY dir:d74df4759bcd6e2619baa3ec354d8703c77c836345c6a887554df76aaf1d9965 in / 
# Tue, 28 Mar 2023 18:20:52 GMT
CMD ["/bin/bash"]
# Tue, 28 Mar 2023 18:42:14 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 28 Mar 2023 18:42:14 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 28 Mar 2023 18:42:45 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Tue, 28 Mar 2023 18:42:47 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 28 Mar 2023 18:42:47 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 28 Mar 2023 18:42:47 GMT
ARG SWIFT_BRANCH=swift-5.7.3-release
# Tue, 28 Mar 2023 18:42:47 GMT
ARG SWIFT_VERSION=swift-5.7.3-RELEASE
# Tue, 28 Mar 2023 18:42:47 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 28 Mar 2023 18:42:47 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.7.3-release SWIFT_VERSION=swift-5.7.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 28 Mar 2023 18:43:21 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Tue, 28 Mar 2023 18:43:26 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:128d54f2c9b134270b406c5f3a41296da7c1111d3a6927f0b4451131d636151e`  
		Last Modified: Thu, 23 Mar 2023 21:24:22 GMT  
		Size: 62.5 MB (62483466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29875483ca1b4b8aafce40091a05d899a62adf713dc9d71c10e2c59f122bcbee`  
		Last Modified: Tue, 28 Mar 2023 18:58:17 GMT  
		Size: 296.9 MB (296859574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba5d8f964e793dd66b19d4654b5b93f42e6dec904b5dc6e2c6d79b7479dd909`  
		Last Modified: Tue, 28 Mar 2023 18:59:00 GMT  
		Size: 544.2 MB (544158581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120f8386b8094a41daa997311b8d3bb6b59cfe0318cf53c4bc58e5fc78b9cb84`  
		Last Modified: Tue, 28 Mar 2023 18:57:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:16107d957cb806e692018cc5a0a561719c881e0b727a703b6d0141cd2fa3a21f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.2 MB (845244386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719aeb26c7201fb2ed57aa227271ff5165fa305cbeb580caadf6117537f3ca7b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Mar 2023 18:40:10 GMT
COPY dir:1d0df99dbb2a961dca382ec30c27f40e06635a9186a0715c0d2a629262a04288 in / 
# Tue, 28 Mar 2023 18:40:10 GMT
CMD ["/bin/bash"]
# Tue, 28 Mar 2023 19:13:47 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 28 Mar 2023 19:13:47 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 28 Mar 2023 19:14:11 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Tue, 28 Mar 2023 19:14:15 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 28 Mar 2023 19:14:15 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 28 Mar 2023 19:14:15 GMT
ARG SWIFT_BRANCH=swift-5.7.3-release
# Tue, 28 Mar 2023 19:14:15 GMT
ARG SWIFT_VERSION=swift-5.7.3-RELEASE
# Tue, 28 Mar 2023 19:14:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 28 Mar 2023 19:14:16 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.7.3-release SWIFT_VERSION=swift-5.7.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 28 Mar 2023 19:14:52 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Tue, 28 Mar 2023 19:15:03 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:949542da27c3c0ab979766d37f455344960f838d9f661b9db50bec634ca7149e`  
		Last Modified: Thu, 23 Mar 2023 21:25:53 GMT  
		Size: 64.1 MB (64126936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a41c593a52c8c8062b0208f08a00d64f7058cfb3924100c0829e49a90d9fe9e`  
		Last Modified: Tue, 28 Mar 2023 19:18:00 GMT  
		Size: 256.8 MB (256755589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566041017ea928eacccbc5e9cbec83dad83c745964447d524455c5e438b58c4c`  
		Last Modified: Tue, 28 Mar 2023 19:18:31 GMT  
		Size: 524.4 MB (524361633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb93d04fa56dcde7ea008fe73a691f965970ff0ccb459855f27ac152f6f36d34`  
		Last Modified: Tue, 28 Mar 2023 19:17:39 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
