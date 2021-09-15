## `swift:centos7`

```console
$ docker pull swift@sha256:66c7f3edac163e1cebd58f49d73fcd88c95f819d0fcbfb6263ade2dbd3841b10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:centos7` - linux; amd64

```console
$ docker pull swift@sha256:8217e4139a3bd97b09a348856751b639c8832566aa6273c2ca439dbb6d60b48e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **722.1 MB (722105913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dcefb290efcda976689045af8481b3e1d9e3733dd756c8493d05f7f3d441b88`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:13:20 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Wed, 15 Sep 2021 19:13:20 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 15 Sep 2021 19:14:17 GMT
RUN yum install shadow-utils.x86_64 -y   binutils   gcc   git   glibc-static   libbsd-devel   libedit   libedit-devel   libicu-devel   libstdc++-static   pkg-config   python3   sqlite   zlib-devel
# Wed, 15 Sep 2021 19:14:19 GMT
RUN sed -i -e 's/\*__block/\*__libc_block/g' /usr/include/unistd.h
# Wed, 15 Sep 2021 19:14:19 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 15 Sep 2021 19:14:19 GMT
ARG SWIFT_PLATFORM=centos7
# Wed, 15 Sep 2021 19:14:19 GMT
ARG SWIFT_BRANCH=swift-5.4.3-release
# Wed, 15 Sep 2021 19:14:19 GMT
ARG SWIFT_VERSION=swift-5.4.3-RELEASE
# Wed, 15 Sep 2021 19:14:20 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Wed, 15 Sep 2021 19:14:20 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=centos7 SWIFT_BRANCH=swift-5.4.3-release SWIFT_VERSION=swift-5.4.3-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Wed, 15 Sep 2021 19:16:19 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 15 Sep 2021 19:16:24 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c87cf883aa1886eeeb3e713ce2f8966670e8c4ffa9f894cf8051d09e977ee0`  
		Last Modified: Wed, 15 Sep 2021 19:41:30 GMT  
		Size: 130.3 MB (130265237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889af7860b387692c19620b50022b64a4e1cd4f348818809e900284ec653990c`  
		Last Modified: Wed, 15 Sep 2021 19:41:09 GMT  
		Size: 11.5 KB (11501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5212617f4cee32fd1d637fae6c8dbab26b07c6ea1d14ed668b62b1638e120c0b`  
		Last Modified: Wed, 15 Sep 2021 19:42:24 GMT  
		Size: 515.7 MB (515732018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
