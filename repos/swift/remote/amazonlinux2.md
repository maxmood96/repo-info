## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:3535f738c83c80823aeeed742d7a6d9b908dd1f6cdc91a0ac6846cf9804ca423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:5c6e7dc5cb54c235d150834745978da15b72af307740abf2a08debe8ff7f5f9b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **923.8 MB (923808172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36566b9a3d07c38d4bde43cddb7afc87063c7aa6208661879a8640fb8538773b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jan 2022 02:20:04 GMT
ADD file:618cac8c5b6f6ff56ce221df12002d34997bcc996a0af3200b58db07d68be275 in / 
# Wed, 12 Jan 2022 02:20:04 GMT
CMD ["/bin/bash"]
# Wed, 12 Jan 2022 02:45:30 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 12 Jan 2022 02:45:30 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 12 Jan 2022 02:46:00 GMT
RUN yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2   tar   tzdata   zlib-devel
# Wed, 12 Jan 2022 02:46:02 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 12 Jan 2022 02:46:02 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 12 Jan 2022 02:46:02 GMT
ARG SWIFT_BRANCH=swift-5.5.2-release
# Wed, 12 Jan 2022 02:46:02 GMT
ARG SWIFT_VERSION=swift-5.5.2-RELEASE
# Wed, 12 Jan 2022 02:46:02 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 12 Jan 2022 02:46:03 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.5.2-release SWIFT_VERSION=swift-5.5.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 12 Jan 2022 02:46:54 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 12 Jan 2022 02:46:59 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:3a461b3ae562f8b6cf015b4c480a21b630a874f7fec851457680159226c81632`  
		Last Modified: Mon, 10 Jan 2022 23:29:44 GMT  
		Size: 62.2 MB (62212074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:385b0c42abc526742f96a89046d8471f4f10a0a7741d76d068cbfd27673f4c13`  
		Last Modified: Wed, 12 Jan 2022 02:58:47 GMT  
		Size: 268.5 MB (268546015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5d9194d20fc065e4b884fc48f3c9723fe1bfb3009b58a28bcbfa84ade7669a`  
		Last Modified: Wed, 12 Jan 2022 02:59:39 GMT  
		Size: 593.0 MB (593049858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7220423630b241b9c896b62336a27fb9508b7c5d3613066da4600f39c6e5598d`  
		Last Modified: Wed, 12 Jan 2022 02:58:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
