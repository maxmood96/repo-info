## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:508b1305abde671882867ea2939506a0af2d832e251bac24e072ca26390eacff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:3f36b0e69a000be88396cb37e950a2db5336b77ca1fe12665948c76d698f000e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **734.7 MB (734724286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:270ed71e652a66d930186db705e6a200818e86d55b412c732ff03c9a677ec0d1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 23 Dec 2020 20:20:09 GMT
ADD file:15991ffbefc01e13f134972ce0eabc6b7901ea9ab4d56347bee5057302cf4848 in / 
# Wed, 23 Dec 2020 20:20:09 GMT
CMD ["/bin/bash"]
# Wed, 23 Dec 2020 20:49:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Wed, 23 Dec 2020 20:49:15 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 23 Dec 2020 20:49:47 GMT
RUN yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2   tar   tzdata   zlib-devel
# Wed, 23 Dec 2020 20:49:48 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 23 Dec 2020 20:49:48 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 23 Dec 2020 20:49:48 GMT
ARG SWIFT_BRANCH=swift-5.3.2-release
# Wed, 23 Dec 2020 20:49:48 GMT
ARG SWIFT_VERSION=swift-5.3.2-RELEASE
# Wed, 23 Dec 2020 20:49:48 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Wed, 23 Dec 2020 20:49:49 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.3.2-release SWIFT_VERSION=swift-5.3.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Wed, 23 Dec 2020 20:51:07 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 23 Dec 2020 20:51:11 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:4232b9ee675bb1f9a32337ec3f266a570b75c54c3c3f173b1abb998e9984ad8c`  
		Last Modified: Wed, 23 Dec 2020 20:21:42 GMT  
		Size: 62.0 MB (62007428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9b591b99e45a8a39cff0930ecfa0adf6c5d44c7d1633ed201a5a501fd1353b`  
		Last Modified: Wed, 23 Dec 2020 20:59:18 GMT  
		Size: 248.1 MB (248098951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d677f6bf109989e8072b14c5c084e21bd2ac306bb47cd2c4ddc91843c8fc3b`  
		Last Modified: Wed, 23 Dec 2020 20:59:58 GMT  
		Size: 424.6 MB (424617907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
