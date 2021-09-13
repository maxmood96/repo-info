## `swift:centos7`

```console
$ docker pull swift@sha256:7514e7ac72c0cf4bd818bc6181b8c45d8f70af9839192ef82cc944d62b775874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:centos7` - linux; amd64

```console
$ docker pull swift@sha256:7bcd5128e5babf671680964a0463d06d89a408a5c407d51f0bd271f164e9c168
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **712.6 MB (712580762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5044e996d1b227c37866642366235b5958626f29b512db236ffad348eb6f188e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:08:35 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 26 Mar 2021 14:08:35 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 28 Apr 2021 19:50:13 GMT
RUN yum install shadow-utils.x86_64 -y   binutils   gcc   git   glibc-static   libbsd-devel   libedit   libedit-devel   libicu-devel   libstdc++-static   pkg-config   python3   sqlite   zlib-devel
# Wed, 28 Apr 2021 19:50:15 GMT
RUN sed -i -e 's/\*__block/\*__libc_block/g' /usr/include/unistd.h
# Wed, 28 Apr 2021 19:50:15 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 28 Apr 2021 19:50:15 GMT
ARG SWIFT_PLATFORM=centos7
# Mon, 13 Sep 2021 18:50:42 GMT
ARG SWIFT_BRANCH=swift-5.4.3-release
# Mon, 13 Sep 2021 18:50:42 GMT
ARG SWIFT_VERSION=swift-5.4.3-RELEASE
# Mon, 13 Sep 2021 18:50:42 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 13 Sep 2021 18:50:42 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=centos7 SWIFT_BRANCH=swift-5.4.3-release SWIFT_VERSION=swift-5.4.3-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 13 Sep 2021 18:52:12 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Mon, 13 Sep 2021 18:52:17 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98dccb7d5309b1c240e55098b6640f598479ab3f80af9d7e85d77ec21c4ebec`  
		Last Modified: Wed, 28 Apr 2021 20:14:02 GMT  
		Size: 120.7 MB (120739184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31543fee229d5f9ad56c07859fefb30b10fd117d87e84334248ee3ceda9bace`  
		Last Modified: Wed, 28 Apr 2021 20:13:38 GMT  
		Size: 11.5 KB (11500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c9a3e731dc1c2630b0281b4879dd6f3b32b3ac703ca298a3f85ff7e730e44c4`  
		Last Modified: Mon, 13 Sep 2021 19:13:45 GMT  
		Size: 515.7 MB (515732921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
