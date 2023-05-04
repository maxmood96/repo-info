## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:6050af41669fc0769111a3caef2bbf098759ec074617ce3533b0cddea8059c5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:e954f3b0663860e8cbecb88f233180b41ae05d1bad564a1f4904cfda97ec0a2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **914.8 MB (914813248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afca19520b7d0c6725007dc8489250bde6b6bfd363e5435dad145c6b67041084`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 04 May 2023 19:20:10 GMT
COPY dir:e8a4b2d0bb4f52911c2b1115b27842bc606a63bd56c8563ded4e6b898fe187d1 in / 
# Thu, 04 May 2023 19:20:10 GMT
CMD ["/bin/bash"]
# Thu, 04 May 2023 19:48:59 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 04 May 2023 19:48:59 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 04 May 2023 19:49:29 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Thu, 04 May 2023 19:49:31 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 04 May 2023 19:49:31 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 04 May 2023 19:49:31 GMT
ARG SWIFT_BRANCH=swift-5.8-release
# Thu, 04 May 2023 19:49:31 GMT
ARG SWIFT_VERSION=swift-5.8-RELEASE
# Thu, 04 May 2023 19:49:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 04 May 2023 19:49:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.8-release SWIFT_VERSION=swift-5.8-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 04 May 2023 19:50:05 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 04 May 2023 19:50:10 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:7cbd40bc2978b9c91c4cf0a5064302062d07242909f83ad9d8d7e2a2d379cf03`  
		Last Modified: Tue, 25 Apr 2023 00:08:27 GMT  
		Size: 62.5 MB (62512332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98224af4ac8f01c56f6a4d4c3091211617c707e3c1e57fae196be1b460823e72`  
		Last Modified: Thu, 04 May 2023 20:04:41 GMT  
		Size: 300.2 MB (300241867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f4ba8cb189ffe65c70b091b05f19442e5b827d5166d6e5bec8f2ea3383ee962`  
		Last Modified: Thu, 04 May 2023 20:05:24 GMT  
		Size: 552.1 MB (552058821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e712f0d0915215247a77b253670d5258e6682eca4b4dd4f97d775e150394fa`  
		Last Modified: Thu, 04 May 2023 20:04:10 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3a14f97259c10cd493960916e20498836593e00515ab3a7800a324bf94966b1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **853.5 MB (853530737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd94e74c50ada006926f929501307013e9af240c5412f7a5b27af5a8cfd71ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Mar 2023 18:40:10 GMT
COPY dir:1d0df99dbb2a961dca382ec30c27f40e06635a9186a0715c0d2a629262a04288 in / 
# Tue, 28 Mar 2023 18:40:10 GMT
CMD ["/bin/bash"]
# Tue, 28 Mar 2023 19:13:47 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 28 Mar 2023 19:13:47 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 28 Mar 2023 19:14:11 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   tar   tzdata   zlib-devel
# Tue, 28 Mar 2023 19:14:15 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Tue, 28 Mar 2023 19:14:15 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Fri, 31 Mar 2023 21:54:33 GMT
ARG SWIFT_BRANCH=swift-5.8-release
# Fri, 31 Mar 2023 21:54:33 GMT
ARG SWIFT_VERSION=swift-5.8-RELEASE
# Fri, 31 Mar 2023 21:54:34 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Mar 2023 21:54:34 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.8-release SWIFT_VERSION=swift-5.8-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 31 Mar 2023 21:55:06 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Fri, 31 Mar 2023 21:55:18 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:949542da27c3c0ab979766d37f455344960f838d9f661b9db50bec634ca7149e`  
		Last Modified: Thu, 23 Mar 2023 21:25:53 GMT  
		Size: 64.1 MB (64126936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a41c593a52c8c8062b0208f08a00d64f7058cfb3924100c0829e49a90d9fe9e`  
		Last Modified: Tue, 28 Mar 2023 19:18:00 GMT  
		Size: 256.8 MB (256755589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bad36b98e2ae098864718e1d3c559045551948ca05c5f945788ca80aa89056f`  
		Last Modified: Fri, 31 Mar 2023 22:02:12 GMT  
		Size: 532.6 MB (532647986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7f23a485ef34507db1492ad295c149dde0c0391aa0e1f9d2a924ee50ea13b7`  
		Last Modified: Fri, 31 Mar 2023 22:01:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
