## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:3491df44fd98843b9dd174e09104d386f641d28c395b0653a24882ea767fd33a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:1aaa132be42ae9c0fcd295a3012a2523bace6cc16deb2820df19318b58b6dfce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **924.5 MB (924530024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7fe61601ca6ed0f1e674f52b8f40811b781c1711ca9fb822a98d63755809372`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 19:59:12 GMT
COPY dir:a1cfeec8f9b5a4b857222f4bbc7f5fb80ef351168a5f48841d4545523a0a3e1c in / 
# Mon, 07 Aug 2023 19:59:13 GMT
CMD ["/bin/bash"]
# Mon, 07 Aug 2023 21:14:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 07 Aug 2023 21:14:22 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 07 Aug 2023 21:14:51 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Mon, 07 Aug 2023 21:14:54 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Mon, 07 Aug 2023 21:14:54 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 07 Aug 2023 21:14:54 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Mon, 07 Aug 2023 21:14:54 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Mon, 07 Aug 2023 21:14:54 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 07 Aug 2023 21:14:54 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 07 Aug 2023 21:15:34 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Mon, 07 Aug 2023 21:15:40 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:c0184eb4a5d5dddba3605f9adcde7e4af58050e9e4ed44751e74957c2ad0f1b4`  
		Last Modified: Tue, 01 Aug 2023 21:03:56 GMT  
		Size: 62.5 MB (62467383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c6cbeb7d8e47e79f738590a8229ccdd7fbbda6357d5aeb3d46feb883c98d07`  
		Last Modified: Mon, 07 Aug 2023 21:46:13 GMT  
		Size: 307.1 MB (307087052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdd2928e5211ab9317f5b11b118c27e56e15eea6b16ce207f054b40096b9ab8`  
		Last Modified: Mon, 07 Aug 2023 21:46:47 GMT  
		Size: 555.0 MB (554975363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667e9aa5bd1f22ac42e8a0d0c69548c6841a4dc944b3c7898fd4e08b507c8b21`  
		Last Modified: Mon, 07 Aug 2023 21:45:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d0516eaee15646315729cd183781a50ffe66d9d89010f6fc21ac7dd05ffba0f9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **866.0 MB (865972863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5b85fef05807878825cdafaa39c4791853d41b1ecf0fe7a40e7356947db9f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 07 Aug 2023 19:40:56 GMT
COPY dir:95dabd7a234aac70a826a1e3c0eafa3928b0be72717af1dea469f66b7db891d5 in / 
# Mon, 07 Aug 2023 19:40:57 GMT
CMD ["/bin/bash"]
# Mon, 07 Aug 2023 21:12:53 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 07 Aug 2023 21:12:53 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 07 Aug 2023 21:13:17 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Mon, 07 Aug 2023 21:13:21 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Mon, 07 Aug 2023 21:13:21 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 07 Aug 2023 21:13:21 GMT
ARG SWIFT_BRANCH=swift-5.8.1-release
# Mon, 07 Aug 2023 21:13:21 GMT
ARG SWIFT_VERSION=swift-5.8.1-RELEASE
# Mon, 07 Aug 2023 21:13:21 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 07 Aug 2023 21:13:21 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.8.1-release SWIFT_VERSION=swift-5.8.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 07 Aug 2023 21:13:56 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Mon, 07 Aug 2023 21:14:06 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:c3b5a1e75067e9d540ad8d844cad5a291a8cce89e1a3ed8e0f362a5736d3030c`  
		Last Modified: Wed, 02 Aug 2023 19:26:38 GMT  
		Size: 64.1 MB (64129548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48cfc064a3f09fa2b3360eb899e138d59201ae82ea47a1f081a1eedd54c6968`  
		Last Modified: Mon, 07 Aug 2023 21:22:51 GMT  
		Size: 266.4 MB (266365084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fdd01cdd9f8c68949dab1d40fce64edbaad162b2b5ae98bafec6174cd1a1be`  
		Last Modified: Mon, 07 Aug 2023 21:23:20 GMT  
		Size: 535.5 MB (535478004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1190aa0df3660a43eedbd023d0f665494edbba2c6830d52a990417fd5734e2c2`  
		Last Modified: Mon, 07 Aug 2023 21:22:28 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
