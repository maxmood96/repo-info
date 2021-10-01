## `swift:focal`

```console
$ docker pull swift@sha256:1e91360e2a484eeb1813d3bc44e97b3c2caadc9d08c7f30f7e465f8a9704c435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:e9c8a7a07a6a042209b53f2c644b9ff989f842896678c26893f47b3cd90d3027
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **720.3 MB (720286794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e75ac7d55c0152c4a398c5eb8c55f481e010e6dee050acc29bbbec2168080f3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:40 GMT
ADD file:8d2f4a45a58b3f5426c89e2ef57164824fbf0e4d17b8a90fffa0d5ff3b4e5114 in / 
# Fri, 01 Oct 2021 02:23:40 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:48:26 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 01 Oct 2021 03:48:26 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 01 Oct 2021 03:51:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     gnupg2     libc6-dev     libcurl4     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:51:11 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 01 Oct 2021 03:51:11 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Fri, 01 Oct 2021 03:51:11 GMT
ARG SWIFT_BRANCH=swift-5.5-release
# Fri, 01 Oct 2021 03:51:12 GMT
ARG SWIFT_VERSION=swift-5.5-RELEASE
# Fri, 01 Oct 2021 03:51:12 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 01 Oct 2021 03:51:12 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.5-release SWIFT_VERSION=swift-5.5-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Fri, 01 Oct 2021 03:53:07 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Fri, 01 Oct 2021 03:53:12 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:f3ef4ff62e0da0ef761ec1c8a578f3035bef51043e53ae1b13a20b3e03726d17`  
		Last Modified: Thu, 23 Sep 2021 03:03:26 GMT  
		Size: 28.6 MB (28568914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eaf17b35fdbdeb0065fa6e4438b59cd39f00e3f4f873316c95bb1463da8ae9`  
		Last Modified: Fri, 01 Oct 2021 04:33:09 GMT  
		Size: 99.0 MB (99002901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e86d1f28aaf2733575aeefcc1a90fdeda420665dd5561b1e3ba9518f9183663`  
		Last Modified: Fri, 01 Oct 2021 04:34:15 GMT  
		Size: 592.7 MB (592714749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19a0ca99b188200ce95b2320358b1b24a1317f673bb737404c8c4ae36ae60a`  
		Last Modified: Fri, 01 Oct 2021 04:32:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
