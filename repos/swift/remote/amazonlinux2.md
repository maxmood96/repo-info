## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:b71a0f63fe276337befe835005e0821da2f8c59a9df476bc2d7563f5b64a9423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:bd76f19b80617a6b8f9181d06a54d44ef817e2001f734a1d3233c0231da1dc94
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **841.3 MB (841322745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb6787342ec6f16e3229e75f4eb80bf536c2d5b8a65349baec99eb83cd7f6b9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 25 Jun 2021 17:19:49 GMT
ADD file:dc851f79dbfc66e08196951041e8c856c41a3cc24b8bc27e66722210d51e87cf in / 
# Fri, 25 Jun 2021 17:19:50 GMT
CMD ["/bin/bash"]
# Fri, 25 Jun 2021 17:37:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Fri, 25 Jun 2021 17:37:15 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 25 Jun 2021 17:37:44 GMT
RUN yum -y install   binutils   gcc   git   glibc-static   gzip   libbsd   libcurl   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2   tar   tzdata   zlib-devel
# Fri, 25 Jun 2021 17:37:46 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 25 Jun 2021 17:37:46 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 29 Jun 2021 22:52:01 GMT
ARG SWIFT_BRANCH=swift-5.4.2-release
# Tue, 29 Jun 2021 22:52:01 GMT
ARG SWIFT_VERSION=swift-5.4.2-RELEASE
# Tue, 29 Jun 2021 22:52:02 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 29 Jun 2021 22:52:02 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.4.2-release SWIFT_VERSION=swift-5.4.2-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Tue, 29 Jun 2021 22:53:33 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver ha.pool.sks-keyservers.net --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Tue, 29 Jun 2021 22:53:38 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:85ee02fe1a09b50ffaacc1e7482fdbb3e80c577256420503196fc549b9e4ef29`  
		Last Modified: Fri, 25 Jun 2021 00:50:03 GMT  
		Size: 61.9 MB (61940054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336e6c251388942add459a8dcf167cf14c7b39798f6d4ec9638409f144ad166e`  
		Last Modified: Fri, 25 Jun 2021 17:56:55 GMT  
		Size: 259.8 MB (259827241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0be80560775ade7c08566cdd64d495e76a5872923f1e8aae67fef0ce4f0a04`  
		Last Modified: Tue, 29 Jun 2021 23:19:42 GMT  
		Size: 519.6 MB (519555450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
