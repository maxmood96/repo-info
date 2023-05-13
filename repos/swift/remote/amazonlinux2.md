## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:c71f6ce0e7ea51ecb0331af65399b56fe04b06b35d4d11a9821abd25cb8a5d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:a5ba877f8bb5dd1e1ea0b635ccfd1748c16baa078ef56bdc8011f2ae693a521b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.0 MB (913998921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207c4be5968b6e9744ffa4b82ff9eb7684871ecd43dac9695d44a104c9a1fc69`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 13 May 2023 00:19:34 GMT
COPY dir:7a824a76678fb4ef17879dcecd9fac65df3d1efbef31a3b874da9f49f49b6814 in / 
# Sat, 13 May 2023 00:19:34 GMT
CMD ["/bin/bash"]
# Sat, 13 May 2023 01:39:05 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 13 May 2023 01:39:05 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 13 May 2023 01:39:37 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Sat, 13 May 2023 01:39:39 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 13 May 2023 01:39:39 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Sat, 13 May 2023 01:39:39 GMT
ARG SWIFT_BRANCH=swift-5.8-release
# Sat, 13 May 2023 01:39:40 GMT
ARG SWIFT_VERSION=swift-5.8-RELEASE
# Sat, 13 May 2023 01:39:40 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 13 May 2023 01:39:40 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.8-release SWIFT_VERSION=swift-5.8-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 13 May 2023 01:40:21 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Sat, 13 May 2023 01:40:27 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:bf72c394abb748707ec4590d5017f36ad47098c9b92adc1b04c3ea3ba0b395f6`  
		Last Modified: Fri, 12 May 2023 00:07:44 GMT  
		Size: 62.5 MB (62494714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235a18fad11cff4980a3c3f6851c7cb01dc3b301ec7e7e879c79b6d403d72bac`  
		Last Modified: Sat, 13 May 2023 01:55:16 GMT  
		Size: 299.4 MB (299445147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b2cb07c726f635d749294d1c331693e2898355f05a54f31a9c5d01f2d868c3`  
		Last Modified: Sat, 13 May 2023 01:55:58 GMT  
		Size: 552.1 MB (552058834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:586cf5f1cf32e0835015716078766d4e9984e1ea0ab570aa90c8143be1d5e3fd`  
		Last Modified: Sat, 13 May 2023 01:54:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:32e0648198d99259dff4786b123397622cc6bcd3b233502589fe0dc1b78695b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **856.9 MB (856858747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e72d47961b059a573ed899aac1e00fa70e3ee85139775b2b530f3c234f4b87`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 May 2023 20:02:54 GMT
COPY dir:dcba415a4a8d9f29c0f5914e2b9ce92b35bd4109c9cd4a8feba13044e94360bf in / 
# Thu, 04 May 2023 20:02:55 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 21:24:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 04 May 2023 21:24:22 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 04 May 2023 21:24:46 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Thu, 04 May 2023 21:24:51 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 04 May 2023 21:24:51 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 04 May 2023 21:24:51 GMT
ARG SWIFT_BRANCH=swift-5.8-release
# Thu, 04 May 2023 21:24:51 GMT
ARG SWIFT_VERSION=swift-5.8-RELEASE
# Thu, 04 May 2023 21:24:51 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 04 May 2023 21:24:51 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.8-release SWIFT_VERSION=swift-5.8-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 04 May 2023 21:25:30 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 04 May 2023 21:25:39 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:7691241ca28307f278612dad94d3164926fb17e58a2302a47349e0d6e001249e`  
		Last Modified: Tue, 25 Apr 2023 06:49:36 GMT  
		Size: 64.1 MB (64130990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a734c14ff363a5eaee15faed80d13449b354102421e1728cdbea350427f35e9b`  
		Last Modified: Thu, 04 May 2023 21:29:36 GMT  
		Size: 260.1 MB (260079467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a970225cc1655565ef269b9d30351bc6356593ea49d2c3b2853d1cc0e28ce4`  
		Last Modified: Thu, 04 May 2023 21:30:04 GMT  
		Size: 532.6 MB (532648059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd514359e716f5068bf0e7485df4bc635df1b00268530414aa22a7de28008f7d`  
		Last Modified: Thu, 04 May 2023 21:29:13 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
