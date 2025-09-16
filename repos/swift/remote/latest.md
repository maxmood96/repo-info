## `swift:latest`

```console
$ docker pull swift@sha256:a87279d5f9d7e5410643e57ec0d3d61661bb075715c1a5096850bcbf7cccba7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:d544626d7c069cf5e617f79027817140e86923b82727a3d63896547683e8108c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1057676988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d692e34e14b60abd41c5eb63babf1c05efc302fa932aa0dc7bcc6bfcecd5ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 06 Sep 2025 05:03:28 GMT
ARG RELEASE
# Sat, 06 Sep 2025 05:03:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 06 Sep 2025 05:03:28 GMT
ADD file:dafefa97de6dc66a6734ec6f05e58125ce01225cccce3f50662330c252aad518 in / 
# Sat, 06 Sep 2025 05:03:28 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 06 Sep 2025 05:03:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_BRANCH=swift-6.1.3-release
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_VERSION=swift-6.1.3-RELEASE
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:953cdd4133718b72c5d0a78e754c1405c02510fdb5237265f7955863f1757f83`  
		Last Modified: Wed, 10 Sep 2025 09:09:40 GMT  
		Size: 29.7 MB (29723450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16551ccbb23fcd023bdf2a6dcdae809cf4ca57de8c9ffbcd9077e9bad22f54d`  
		Last Modified: Tue, 16 Sep 2025 01:49:46 GMT  
		Size: 130.4 MB (130369159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539f814555b842c503a69477399f3343aa7f30339efd98f7d8c407b99541a2af`  
		Last Modified: Tue, 16 Sep 2025 01:50:25 GMT  
		Size: 897.6 MB (897584205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78749efa3064c6da5eb18bbead6af76bb7605629aca0d6adab8fc057801bcb7e`  
		Last Modified: Mon, 15 Sep 2025 22:31:02 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:68cb06fe465db745e477e91cbb4488d80e41f95072739f0c73e0f9893930884b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7894807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaa9a40561eee99ef2f67b36e44b04c54c146ad8dde5f1546fc0c75a6c93783`

```dockerfile
```

-	Layers:
	-	`sha256:079f42dedf9c1accad4634bc386bf0f2333425b70da07bd0c643147b4fdf41f3`  
		Last Modified: Tue, 16 Sep 2025 01:48:23 GMT  
		Size: 7.9 MB (7877967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99464120ef2b07a6e8f9c6c020e3d00d65b1456270794bff406beb840355192`  
		Last Modified: Tue, 16 Sep 2025 01:48:24 GMT  
		Size: 16.8 KB (16840 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:b566c738207db8a1dcee81c934ed449f8ad2d57b731af30d7b913aa065c54f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 GB (1049962053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c749dc759e1bf02ecd8c8038bc05d18ccbf1f65b20cc3750e0e341422eddd77f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 06 Sep 2025 05:03:28 GMT
ARG RELEASE
# Sat, 06 Sep 2025 05:03:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL org.opencontainers.image.version=24.04
# Sat, 06 Sep 2025 05:03:28 GMT
ADD file:4e55519deacaaab35bcc389ec63f319a61c50e3f8f7d19a0df61fa1571c86c6a in / 
# Sat, 06 Sep 2025 05:03:28 GMT
CMD ["/bin/bash"]
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 06 Sep 2025 05:03:28 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 06 Sep 2025 05:03:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_BRANCH=swift-6.1.3-release
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_VERSION=swift-6.1.3-RELEASE
# Sat, 06 Sep 2025 05:03:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Sat, 06 Sep 2025 05:03:28 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1.3-release SWIFT_VERSION=swift-6.1.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:59a5d47f84c39a2d62d1b5089e60ab67303111f17e1df01dbbcc598246282797`  
		Last Modified: Wed, 10 Sep 2025 09:09:46 GMT  
		Size: 28.9 MB (28861317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b500109373527395d4c1ed19d8bb0f99fe3335d365977b7438005899efd86ac`  
		Last Modified: Tue, 16 Sep 2025 01:55:03 GMT  
		Size: 129.5 MB (129451667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28041e4e161da0002b8eff31fe4660ac6517993022c80e86790ba03250bb5f5d`  
		Last Modified: Tue, 16 Sep 2025 01:55:29 GMT  
		Size: 891.6 MB (891648895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608401333ecf97ea95c879f52f0fb1459af4e56c5fdbd5bafc9f3b984ba50124`  
		Last Modified: Mon, 15 Sep 2025 22:29:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:31424e9893b459eb3a6716149b62de452bea9201396fc31c30a035853da5b574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7917451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73bbbf43b6e4b7b37593315a27419e80ef4129da64528bd41cb9b048ba653471`

```dockerfile
```

-	Layers:
	-	`sha256:9d3d2a8a18d6df0316983405844cf27fadc7cd327f1977f9d7aaecdb28fafcf6`  
		Last Modified: Tue, 16 Sep 2025 01:48:31 GMT  
		Size: 7.9 MB (7900454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc43c639b9dc6b365aa0942edb15f9fe2bd2fcfe1d3a2e519642bca46d5e3d94`  
		Last Modified: Tue, 16 Sep 2025 01:48:32 GMT  
		Size: 17.0 KB (16997 bytes)  
		MIME: application/vnd.in-toto+json
