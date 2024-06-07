## `swift:centos7`

```console
$ docker pull swift@sha256:a274f403cfdf4cec44b22874b876da09b528ff5cf9e1483c930e1d1775fc7873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:centos7` - linux; amd64

```console
$ docker pull swift@sha256:e35058c7961e868a604783b3f41d005bd5eb3e57a2057be87eeddf67deb0cbd4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1242426571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:110f16c369cc6b267febb9328f5162d2daf5f8d9a9a533862c5d9f245c01b597`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Fri, 07 Jun 2024 04:16:52 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 07 Jun 2024 04:16:52 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 07 Jun 2024 04:17:43 GMT
RUN yum install shadow-utils.x86_64 -y   binutils   gcc   git   unzip   glibc-static   libbsd-devel   libcurl-devel   libedit   libedit-devel   libicu-devel   libstdc++-static   libxml2-devel   pkg-config   python3   sqlite   zlib-devel
# Fri, 07 Jun 2024 04:17:46 GMT
RUN sed -i -e 's/\*__block/\*__libc_block/g' /usr/include/unistd.h
# Fri, 07 Jun 2024 04:17:46 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 07 Jun 2024 04:17:46 GMT
ARG SWIFT_PLATFORM=centos7
# Fri, 07 Jun 2024 04:17:47 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Fri, 07 Jun 2024 04:17:47 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Fri, 07 Jun 2024 04:17:47 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 07 Jun 2024 04:17:47 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=centos7 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 07 Jun 2024 04:18:30 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 07 Jun 2024 04:18:40 GMT
RUN yum install -y centos-release-scl
# Fri, 07 Jun 2024 04:19:30 GMT
RUN yum install -y devtoolset-8
# Fri, 07 Jun 2024 04:19:32 GMT
RUN ln -s /opt/rh/devtoolset-8/root/usr/lib/gcc/x86_64-redhat-linux/8/libstdc++_nonshared.a /usr/lib/swift_static/linux &&     ln -s /opt/rh/devtoolset-8/root/usr/lib/gcc/x86_64-redhat-linux/8/libstdc++.so /usr/lib/swift_static/linux
# Fri, 07 Jun 2024 04:19:33 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e392c0a8dc8edc659ef9c63cfdd2879338cfeabb7b73ab1df1e8f8f7f0b9dcfe`  
		Last Modified: Fri, 07 Jun 2024 04:41:28 GMT  
		Size: 237.0 MB (236973174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4fb80ffccdcad5ffe5aa7ce7bfc77f8d348820d14e36cee3020b883e603adb`  
		Last Modified: Fri, 07 Jun 2024 04:40:54 GMT  
		Size: 11.5 KB (11502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a164afc004b188f1ab9947e42faf6d64c10d3c5f702d07e7c7246925ddba2e79`  
		Last Modified: Fri, 07 Jun 2024 04:42:19 GMT  
		Size: 628.5 MB (628478197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e394ef541e539fb88a09034f543466d3b1e85cbe24088c1cb524bacdb400487`  
		Last Modified: Fri, 07 Jun 2024 04:41:03 GMT  
		Size: 88.9 MB (88901704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4615f97fda34479792b7c03ca37b331637e1cc5af69949d9b23eb28abf8bd980`  
		Last Modified: Fri, 07 Jun 2024 04:41:24 GMT  
		Size: 212.0 MB (211964390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048220b6e5e58ba4af3835a4b83fdc713d066f1a697b3048574627211dec65b4`  
		Last Modified: Fri, 07 Jun 2024 04:40:52 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2454f244ffb3db07073b8ef82f0da0205a5c32e6e4c4ef25a2dc3c41b8b173a8`  
		Last Modified: Fri, 07 Jun 2024 04:40:53 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
