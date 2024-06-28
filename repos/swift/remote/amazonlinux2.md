## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:1b7b005cc7a7aec777e76611cdcbfc352e6ba7714f7797a693ff01cb48b898a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:12e5f88e33b3c997ad16502fea3c1287c4a00757d63a04fc669e3cac3a9795ce
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **983.4 MB (983396800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e67e3d8019fa22e6793d97a5956560444bdb46337a4cc5d0229cd3948aed5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:55 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Fri, 28 Jun 2024 00:19:56 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 00:37:02 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 28 Jun 2024 00:37:03 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 28 Jun 2024 00:37:34 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel
# Fri, 28 Jun 2024 00:37:36 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 28 Jun 2024 00:37:37 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 28 Jun 2024 00:37:37 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Fri, 28 Jun 2024 00:37:37 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Fri, 28 Jun 2024 00:37:37 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 28 Jun 2024 00:37:37 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 28 Jun 2024 00:38:18 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 28 Jun 2024 00:38:22 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7c038c290ad0c2ed30b23bb2a8dd8940dd1b0445c9265ada82e1b732db87885`  
		Last Modified: Fri, 28 Jun 2024 00:51:37 GMT  
		Size: 296.1 MB (296085154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ffd9c881be391d8fd07eb93b543d95fd7159f2a0884ab8d3d3b24a7f95928af`  
		Last Modified: Fri, 28 Jun 2024 00:52:25 GMT  
		Size: 624.7 MB (624664832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b634b7bdb5829504b6e563c591a40f60578e185ecbc31daeb911ec0705b4379`  
		Last Modified: Fri, 28 Jun 2024 00:51:00 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:610ab11293108b26d87017e3333734a86b15edd9c9b8de055483da265f7170b9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **950.2 MB (950181502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a790a384470e2bd3f798088b93bfc204e6cc7c95d5a9f605634aac69f647f95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:40:02 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Fri, 28 Jun 2024 00:40:03 GMT
CMD ["/bin/bash"]
# Fri, 28 Jun 2024 00:56:13 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 28 Jun 2024 00:56:13 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 28 Jun 2024 00:56:37 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel
# Fri, 28 Jun 2024 00:56:42 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Fri, 28 Jun 2024 00:56:42 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 28 Jun 2024 00:56:42 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Fri, 28 Jun 2024 00:56:42 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Fri, 28 Jun 2024 00:56:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 28 Jun 2024 00:56:42 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 28 Jun 2024 00:57:24 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 28 Jun 2024 00:57:36 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81445cde6fd1fecab392ec8db53e9b4d0bd64102069be6595a3c1e71a21d9399`  
		Last Modified: Fri, 28 Jun 2024 01:06:55 GMT  
		Size: 267.6 MB (267593487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003fa1c4f5f7e4ac8a1db9f48c7a749564809629d75a75944575cab689b11ddd`  
		Last Modified: Fri, 28 Jun 2024 01:07:32 GMT  
		Size: 618.0 MB (618019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e6071ae0c5de7294a1a1c2ac162975253676c2d011df6fda077226d891317cb`  
		Last Modified: Fri, 28 Jun 2024 01:06:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
