## `swift:focal`

```console
$ docker pull swift@sha256:f3240d599f42d42eb7ed6214c205c021bf73fd30941e9034cf877f06c6df79b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:20b02c340a980fd11cc962149ba00aa96d0bf4aa152bebeebca4bf9a857c8ed8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **755.0 MB (754993452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65aacc2371af7d1cf1040982e9a611ea84a4bc727d046fa2d8111a58710a6cd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 10:45:50 GMT
ARG RELEASE
# Tue, 03 Oct 2023 10:45:50 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 10:45:50 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 10:45:51 GMT
ADD file:4809da414c2d478b4d991cbdaa2df457f2b3d07d0ff6cf673f09a66f90833e81 in / 
# Tue, 03 Oct 2023 10:45:52 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 06:24:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 13 Oct 2023 06:24:42 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 13 Oct 2023 06:27:23 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 13 Oct 2023 06:27:24 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 13 Oct 2023 06:27:24 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Thu, 19 Oct 2023 19:39:25 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Thu, 19 Oct 2023 19:39:25 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Thu, 19 Oct 2023 19:39:25 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 19:39:25 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 19:40:09 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Thu, 19 Oct 2023 19:40:16 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:7a2c559011895d255fce249c00396abff5ae7e0c0a92931d0ed493e71de78e3a`  
		Last Modified: Tue, 03 Oct 2023 17:02:08 GMT  
		Size: 28.6 MB (28580681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747b3af13a4c166931ffc068585f19a9daea071f67dd661fd74f644a9cbc2ff8`  
		Last Modified: Fri, 13 Oct 2023 06:48:24 GMT  
		Size: 120.5 MB (120497335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f059b5c017216758e8253b2847a41642dbc83957e2f7173767439e39ac1c0ef6`  
		Last Modified: Thu, 19 Oct 2023 20:05:37 GMT  
		Size: 605.9 MB (605915238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e008997aeafd5e154283e6b9c1fbf6c3a67bbfb42ed5d8a4e659ec68a31287`  
		Last Modified: Thu, 19 Oct 2023 20:04:18 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:focal` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:2ed8b067c83e315af85f000a56c3bd19abb64fdc3f647d53783d3ac217a6a7c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.9 MB (744859780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bf4af79702151aa21f300bca32bdc1acfbb166b1814827310aa9c5354d6cf8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 03 Oct 2023 11:04:09 GMT
ARG RELEASE
# Tue, 03 Oct 2023 11:04:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 03 Oct 2023 11:04:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 03 Oct 2023 11:04:10 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 03 Oct 2023 11:04:16 GMT
ADD file:f70cc2610ea8fcd25e6e9ae727eb9345d5b7198102f6a6d8e458ab8f99efefc3 in / 
# Tue, 03 Oct 2023 11:04:17 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 03:14:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 13 Oct 2023 03:14:10 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 13 Oct 2023 03:15:38 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 13 Oct 2023 03:15:40 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 13 Oct 2023 03:15:40 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Thu, 19 Oct 2023 20:07:04 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Thu, 19 Oct 2023 20:07:04 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Thu, 19 Oct 2023 20:07:04 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 20:07:04 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 20:07:54 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Thu, 19 Oct 2023 20:08:06 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:6cba4020c0a193cd551ed8edf368670967e3546345b52c4ec66cb0931436e9b9`  
		Last Modified: Thu, 05 Oct 2023 12:12:17 GMT  
		Size: 27.2 MB (27199503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e321598e082c6270002b18e6fda8cc6252aa1ee55a7e41d85efabee44a0536`  
		Last Modified: Fri, 13 Oct 2023 03:28:06 GMT  
		Size: 117.3 MB (117268346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e28f1a1ccd3195de1cb941ee2c7ba2311f911a2a5ef49c67d024c35be7f8e4f5`  
		Last Modified: Thu, 19 Oct 2023 20:20:23 GMT  
		Size: 600.4 MB (600391730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ccaa708c0f89e44e01f1c020a6d1c32a5e1e185ca09ed979a9f720be018168`  
		Last Modified: Thu, 19 Oct 2023 20:19:20 GMT  
		Size: 201.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
