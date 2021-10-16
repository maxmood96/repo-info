## `swift:focal-slim`

```console
$ docker pull swift@sha256:89140fe08a824afd327d6b187fcb24e8a321101ad2f059d98fa664148fdb8a53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:focal-slim` - linux; amd64

```console
$ docker pull swift@sha256:2a20ab1024998a2f689e6f32347978012be50dd7be99a966e74d94563a7e1d63
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142980007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed3b8ad15b6c59f891817d72fd6954b5c9ae4b597f85fb45f483b796f08ca5c5`
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
# Sat, 16 Oct 2021 02:12:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     libcurl4     libxml2     tzdata     && rm -r /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:12:13 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 16 Oct 2021 02:12:13 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Sat, 16 Oct 2021 02:12:13 GMT
ARG SWIFT_BRANCH=swift-5.5-release
# Sat, 16 Oct 2021 02:12:14 GMT
ARG SWIFT_VERSION=swift-5.5-RELEASE
# Sat, 16 Oct 2021 02:12:14 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Sat, 16 Oct 2021 02:12:14 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.5-release SWIFT_VERSION=swift-5.5-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Sat, 16 Oct 2021 02:14:00 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl gnupg && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1 $SWIFT_VERSION-$SWIFT_PLATFORM/usr/lib/swift/linux     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl gnupg
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2818be884de634b3b543f240a970102b8c1682ef2243d2042182d85c9a8e06f5`  
		Last Modified: Sat, 16 Oct 2021 02:36:47 GMT  
		Size: 22.3 MB (22254677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cc4aeb0010e648b355eee5cb20b124205b3a40ad720ef23f0d3346c25a70b9`  
		Last Modified: Sat, 16 Oct 2021 02:36:57 GMT  
		Size: 92.2 MB (92158229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
