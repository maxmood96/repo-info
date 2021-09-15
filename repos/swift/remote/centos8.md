## `swift:centos8`

```console
$ docker pull swift@sha256:f750662588223891c7e90caa438973d11940bf395a7a393ddaedcaf76e48cae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `swift:centos8` - linux; amd64

```console
$ docker pull swift@sha256:5daad3e2674e61372b80aa21d3cfd6fefff00873365469d277d4d358f9dc1e77
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **790.3 MB (790308172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da8ce4056a4a94e682139920c21af8254fcc3490d4a0952bfd3335bdf6fd4ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Sep 2021 18:20:04 GMT
ADD file:805cb5e15fb6e0bb0326ca33fd2942e068863ce2a8491bb71522c652f31fb466 in / 
# Wed, 15 Sep 2021 18:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20210915
# Wed, 15 Sep 2021 18:20:05 GMT
CMD ["/bin/bash"]
# Wed, 15 Sep 2021 19:09:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@swift.org>
# Wed, 15 Sep 2021 19:09:28 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 15 Sep 2021 19:09:36 GMT
RUN yum install -y https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm
# Wed, 15 Sep 2021 19:10:02 GMT
RUN yum install --enablerepo=powertools -y   binutils   gcc   git   glibc-static   libbsd-devel   libedit   libedit-devel   libicu-devel   libstdc++-static   pkg-config   python3   sqlite   zlib-devel
# Wed, 15 Sep 2021 19:10:04 GMT
RUN ln -s /usr/bin/python3 /usr/bin/python
# Wed, 15 Sep 2021 19:10:04 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Wed, 15 Sep 2021 19:10:05 GMT
ARG SWIFT_PLATFORM=centos8
# Wed, 15 Sep 2021 19:10:05 GMT
ARG SWIFT_BRANCH=swift-5.4.3-release
# Wed, 15 Sep 2021 19:10:05 GMT
ARG SWIFT_VERSION=swift-5.4.3-RELEASE
# Wed, 15 Sep 2021 19:10:05 GMT
ARG SWIFT_WEBROOT=https://swift.org/builds/
# Wed, 15 Sep 2021 19:10:05 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=centos8 SWIFT_BRANCH=swift-5.4.3-release SWIFT_VERSION=swift-5.4.3-RELEASE SWIFT_WEBROOT=https://swift.org/builds/
# Wed, 15 Sep 2021 19:11:40 GMT
RUN set -e;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)/"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Wed, 15 Sep 2021 19:11:45 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:a1d0c75327776413fa0db9ed3adcdbadedc95a662eb1d360dad82bb913f8a1d1`  
		Last Modified: Wed, 15 Sep 2021 18:21:25 GMT  
		Size: 83.5 MB (83518086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b868d936c0205e10dd48e7e5ba9d3e75ccd59b2e3438f9a43e0fb4d6a0ed76d`  
		Last Modified: Wed, 15 Sep 2021 19:39:21 GMT  
		Size: 29.0 MB (29003609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db724521fb5dd4ac009a313fb2c61b3c095724e2359d8929b960f87e0f41b55`  
		Last Modified: Wed, 15 Sep 2021 19:39:40 GMT  
		Size: 156.9 MB (156941682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c23df8bd7f93181a64501b14e36f8e0c5d3cbf375993692dacfa504a64a257`  
		Last Modified: Wed, 15 Sep 2021 19:39:18 GMT  
		Size: 151.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce7a1105cd7a3e7d813e4e893f1094b06b13e0fa4b28ce910d50ef6ee8763fe`  
		Last Modified: Wed, 15 Sep 2021 19:40:36 GMT  
		Size: 520.8 MB (520844644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
