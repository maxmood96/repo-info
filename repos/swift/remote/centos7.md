## `swift:centos7`

```console
$ docker pull swift@sha256:0ac842b27deb817cd483962ca109c0f49f44dde2bfba7db59214b06fcfa8d4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:centos7` - linux; amd64

```console
$ docker pull swift@sha256:bb8f9208640598c61fc73b24f0553cdeebc8cedafab75fe802a0f714b6cd3836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1174786028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9a38525fb7b99781b5b6d1e2e2ccf811333a7e36d5a7f671d8eb0ccdcf8e7e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:23 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Wed, 15 Sep 2021 18:20:23 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Wed, 15 Sep 2021 18:20:23 GMT
CMD ["/bin/bash"]
# Thu, 28 Oct 2021 23:56:50 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 28 Oct 2021 23:56:50 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 12 Sep 2022 18:29:45 GMT
RUN yum install shadow-utils.x86_64 -y   binutils   gcc   git   unzip   glibc-static   libbsd-devel   libcurl-devel   libedit   libedit-devel   libicu-devel   libstdc++-static   libxml2-devel   pkg-config   python3   sqlite   zlib-devel
# Mon, 12 Sep 2022 18:29:47 GMT
RUN sed -i -e 's/\*__block/\*__libc_block/g' /usr/include/unistd.h
# Mon, 12 Sep 2022 18:29:47 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Mon, 12 Sep 2022 18:29:47 GMT
ARG SWIFT_PLATFORM=centos7
# Thu, 19 Oct 2023 19:42:44 GMT
ARG SWIFT_BRANCH=swift-5.9.1-release
# Thu, 19 Oct 2023 19:42:44 GMT
ARG SWIFT_VERSION=swift-5.9.1-RELEASE
# Thu, 19 Oct 2023 19:42:44 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 19:42:44 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=centos7 SWIFT_BRANCH=swift-5.9.1-release SWIFT_VERSION=swift-5.9.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 19 Oct 2023 19:43:33 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 19 Oct 2023 19:43:47 GMT
RUN yum install -y centos-release-scl
# Thu, 19 Oct 2023 19:44:37 GMT
RUN yum install -y devtoolset-8
# Thu, 19 Oct 2023 19:44:40 GMT
RUN ln -s /opt/rh/devtoolset-8/root/usr/lib/gcc/x86_64-redhat-linux/8/libstdc++_nonshared.a /usr/lib/swift_static/linux &&     ln -s /opt/rh/devtoolset-8/root/usr/lib/gcc/x86_64-redhat-linux/8/libstdc++.so /usr/lib/swift_static/linux
# Thu, 19 Oct 2023 19:44:40 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cf153ce065ef54d83d11b3352a6545dfd22f9957115fb02b8bc021c67daada`  
		Last Modified: Mon, 12 Sep 2022 18:44:30 GMT  
		Size: 197.0 MB (197029788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f65e7a10ed0a06abeb8a0152eedaf1e823e22aab9e7ed0fa711649a48de7974`  
		Last Modified: Mon, 12 Sep 2022 18:44:03 GMT  
		Size: 11.5 KB (11502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c76bf2c6f2a0af2d422679d764423926756304b926f150ea3699354d124182`  
		Last Modified: Thu, 19 Oct 2023 20:09:20 GMT  
		Size: 612.0 MB (611969114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1768153b8f734a1f9b88d5adf387b587c1e72cad776926da656b95513733254f`  
		Last Modified: Thu, 19 Oct 2023 20:08:09 GMT  
		Size: 87.1 MB (87084080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a01fb7a1efb1c0a718f734a8cb63fd95fb67c86d14f6af4497f6e9b39e2d2e8`  
		Last Modified: Thu, 19 Oct 2023 20:08:28 GMT  
		Size: 202.6 MB (202593914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a5178c44d583bbe75032169efa7cc35ff731657014f1cc45851b5ed7e9aeea`  
		Last Modified: Thu, 19 Oct 2023 20:07:59 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de509095f8bc9728286269f063c63644a6e2f62a0f96a79a4dcc47d89c176998`  
		Last Modified: Thu, 19 Oct 2023 20:07:59 GMT  
		Size: 199.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
