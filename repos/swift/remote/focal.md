## `swift:focal`

```console
$ docker pull swift@sha256:e44b266a352be836e7800da5c9fd2e8d1ee16f042bd35d5e1204cabd45ee4880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:1e0d1af9323276fe6e189fd806bdaa512330262e681a6d150af19e3bfcba8a06
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.3 MB (720286036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a98915168f97ebe190be0c7fcb3a7a1cd28bd93d588da7b25395d3d31c77e5c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:12:03 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Sat, 16 Oct 2021 02:12:03 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 16 Oct 2021 02:14:42 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     gnupg2     libc6-dev     libcurl4     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:14:43 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 16 Oct 2021 02:14:43 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Sat, 16 Oct 2021 02:14:43 GMT
ARG SWIFT_BRANCH=swift-5.5-release
# Sat, 16 Oct 2021 02:14:44 GMT
ARG SWIFT_VERSION=swift-5.5-RELEASE
# Sat, 16 Oct 2021 02:14:44 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Sat, 16 Oct 2021 02:14:44 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.5-release SWIFT_VERSION=swift-5.5-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Sat, 16 Oct 2021 02:16:42 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Sat, 16 Oct 2021 02:16:47 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6d5ac46cd2e1b6a491e76b54d90ae0d63ca9e4bf899eeafe2232aacab308c0`  
		Last Modified: Sat, 16 Oct 2021 02:37:25 GMT  
		Size: 99.0 MB (99004117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857cf97a4cf6eaa5fec4427507763225e1c7ff59151566e3506bca9e5adb6eb9`  
		Last Modified: Sat, 16 Oct 2021 02:38:38 GMT  
		Size: 592.7 MB (592714588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848d59495421fb22ce67cfa5b874eae0ba53dc5469ef6ee73c64af26e36ad263`  
		Last Modified: Sat, 16 Oct 2021 02:37:08 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
