## `swift:latest`

```console
$ docker pull swift@sha256:6e314ee8116fa91778ff6db82a2acaaa3793e367be2b600a5cc43cdebd737319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:97be70c34cf32520dcb52bf88e50983085c686be2794f45f203639e1cb7bfe4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **812.8 MB (812806096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68853f9721a2a198ec169f5c504b74d6e8e3fff9fe5255851f6d00b3e6f436d0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:54:38 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:54:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:54:38 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:54:40 GMT
ADD file:99224b1f237763b3053ca27ea5641f9a801c21154c7ccbff2c099654cc6db942 in / 
# Thu, 25 Jan 2024 17:54:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:57:30 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 02 Feb 2024 00:57:31 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 02 Feb 2024 00:59:23 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:59:25 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 02 Feb 2024 00:59:25 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 02 Feb 2024 00:59:25 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Fri, 02 Feb 2024 00:59:25 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Fri, 02 Feb 2024 00:59:25 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 02 Feb 2024 00:59:25 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 02 Feb 2024 01:00:08 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 02 Feb 2024 01:00:15 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:31bd5f451a847d651a0996256753a9b22a6ea8c65fefb010e77ea9c839fe2fac`  
		Last Modified: Thu, 25 Jan 2024 22:24:23 GMT  
		Size: 30.4 MB (30447882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f7ff0e45bf30b711238f010baadc5f6e12fc46d49041bdf8cc3449aac897773`  
		Last Modified: Fri, 02 Feb 2024 01:37:51 GMT  
		Size: 175.4 MB (175407099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187e13ff38c91fbad536934511df9e5f3438674f1308ca0492696232361cc6d7`  
		Last Modified: Fri, 02 Feb 2024 01:38:45 GMT  
		Size: 607.0 MB (606950915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d82e8c3cd64884821bb4f27f69674d6ef63202687eeac5680e0ee961fe32a51`  
		Last Modified: Fri, 02 Feb 2024 01:37:22 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:c7145325dc62d7ca001eef9a912ed08a47a099970a54e75feaedc3ae61c00e6f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **801.9 MB (801867655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f21227a95fabd8e639730466b140b3df3dd85c4d9f5e33b4c691877878a31fe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 25 Jan 2024 17:52:41 GMT
ARG RELEASE
# Thu, 25 Jan 2024 17:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Jan 2024 17:52:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Jan 2024 17:52:47 GMT
ADD file:1bffdeb50a8b94d632a24e4dfa455cbba1b09f8640572cd4111f0ad9747b4500 in / 
# Thu, 25 Jan 2024 17:52:47 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:05:45 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 02 Feb 2024 00:05:45 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 02 Feb 2024 00:08:16 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 02 Feb 2024 00:08:19 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 02 Feb 2024 00:08:19 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Fri, 02 Feb 2024 00:08:19 GMT
ARG SWIFT_BRANCH=swift-5.9.2-release
# Fri, 02 Feb 2024 00:08:19 GMT
ARG SWIFT_VERSION=swift-5.9.2-RELEASE
# Fri, 02 Feb 2024 00:08:19 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 02 Feb 2024 00:08:20 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-5.9.2-release SWIFT_VERSION=swift-5.9.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 02 Feb 2024 00:09:00 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 02 Feb 2024 00:09:12 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:b90a30ba7a05123de8a1e1661ed0ddb6563ad55ca11133e21e3d19f7e6bce76a`  
		Last Modified: Fri, 26 Jan 2024 01:55:46 GMT  
		Size: 28.4 MB (28400102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c29aeed4f429de40e97187bb307cc0798e0cbf6ec0a5c868ad662c02092d0a3`  
		Last Modified: Fri, 02 Feb 2024 00:30:17 GMT  
		Size: 171.7 MB (171666695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfb878180d9fc0a04420fc63e257748ec076e4872d55646ef72b8ff2f02167e`  
		Last Modified: Fri, 02 Feb 2024 00:30:56 GMT  
		Size: 601.8 MB (601800660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ab1a5e2fc8d7abe57629b41180b4e54eaa25982a15e11a2d0689a1bab4d8a2`  
		Last Modified: Fri, 02 Feb 2024 00:29:55 GMT  
		Size: 198.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
