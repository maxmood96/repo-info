## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:87721121220aaad9b009a5f1637f64f43401ecf5cd68c05a65894d166c756819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:f6d6dc9357ac5796bc6d9999721b4015818e6b4c6a02b44e1236f14c7667a6bb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **843.8 MB (843840231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972bb95bf804ef4414a664f59985b4127f0d68c59c987150360d6edb203c0788`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Sep 2021 00:19:59 GMT
ADD file:bf148e5e5c33bfe39c321b4ad38c7f1068e1e4f6bfc44f5e33d3bd17f3ea65b0 in / 
# Thu, 09 Sep 2021 00:20:00 GMT
CMD ["/bin/bash"]
# Thu, 09 Sep 2021 00:37:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Thu, 09 Sep 2021 00:37:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 09 Sep 2021 00:38:01 GMT
RUN yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2   tar   tzdata   zlib-devel
# Thu, 09 Sep 2021 00:38:03 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 09 Sep 2021 00:38:03 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 13 Sep 2021 18:43:44 GMT
ARG SWIFT_BRANCH=swift-5.4.3-release
# Mon, 13 Sep 2021 18:43:44 GMT
ARG SWIFT_VERSION=swift-5.4.3-RELEASE
# Mon, 13 Sep 2021 18:43:44 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 13 Sep 2021 18:43:44 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.4.3-release SWIFT_VERSION=swift-5.4.3-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Mon, 13 Sep 2021 18:45:17 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Mon, 13 Sep 2021 18:45:22 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:6b2f67060278d4a8d68cf1aaaba33c5fb108ba15b0d65d3c64c74154adb59e37`  
		Last Modified: Wed, 08 Sep 2021 08:48:25 GMT  
		Size: 62.0 MB (62000303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6a379a0aae5704da973626bfd6571d4563e723230aef1c24e74abe407c9306`  
		Last Modified: Thu, 09 Sep 2021 00:59:53 GMT  
		Size: 262.3 MB (262277989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb3671c018840a2699d246297f4d63c8d12e8dcce74696cb835ee7c7c939b230`  
		Last Modified: Mon, 13 Sep 2021 19:10:01 GMT  
		Size: 519.6 MB (519561939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
