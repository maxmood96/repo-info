## `swift:focal`

```console
$ docker pull swift@sha256:22959d40da12e4803712271d627a30e5634e962313d6bdf736859a3379bacbea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:ab1fff90f995e802333b72524dba0a0dee6062dda4b8b8596ec923f0648acdd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.0 MB (752026671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee992bf350d99a53e7fef1d4411e92da82e5f16b4a91c1f7c162a393f8ff0c38`
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
# Fri, 13 Oct 2023 06:27:24 GMT
ARG SWIFT_BRANCH=swift-5.9-release
# Fri, 13 Oct 2023 06:27:24 GMT
ARG SWIFT_VERSION=swift-5.9-RELEASE
# Fri, 13 Oct 2023 06:27:24 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 13 Oct 2023 06:27:24 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.9-release SWIFT_VERSION=swift-5.9-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 13 Oct 2023 06:28:04 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 13 Oct 2023 06:28:11 GMT
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
	-	`sha256:45238969dc2424dc2823a05911b64148d33574a19e10bbc4d4263dcb8de0d1d8`  
		Last Modified: Fri, 13 Oct 2023 06:49:27 GMT  
		Size: 602.9 MB (602948455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d905ffadd234a520aaf8c773806c99efb5a8b3fcea07b1b24d5009ac7861335b`  
		Last Modified: Fri, 13 Oct 2023 06:48:05 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:focal` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:2424dad10bb6ad3f1cea22e867850a94f704ff3d6b1e17c0225333741bc12761
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **742.0 MB (742007962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13ef5adc64d167649eb6690ad1463cdcee6211f09ede7f61c07336ae4d9a437e`
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
# Fri, 13 Oct 2023 03:15:40 GMT
ARG SWIFT_BRANCH=swift-5.9-release
# Fri, 13 Oct 2023 03:15:40 GMT
ARG SWIFT_VERSION=swift-5.9-RELEASE
# Fri, 13 Oct 2023 03:15:40 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 13 Oct 2023 03:15:41 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.9-release SWIFT_VERSION=swift-5.9-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 13 Oct 2023 03:16:22 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 13 Oct 2023 03:16:34 GMT
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
	-	`sha256:b2ab5c71eb219cf2e0e8895c5c8dc5f6bbfa14c6b37120da4828db9c9ca82132`  
		Last Modified: Fri, 13 Oct 2023 03:28:51 GMT  
		Size: 597.5 MB (597539913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025b10fde024520e76ae444d1a63551ab889e7b8beed49547401a3a714861b41`  
		Last Modified: Fri, 13 Oct 2023 03:27:50 GMT  
		Size: 200.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
