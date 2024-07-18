## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:6381df32ba30e8ab368a4dccbc8a658932d3db4fce04fe46afd527f655b1ce74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:b07d07a43841dcd1769832b088ab32ea55f3b92a3d6cc414b33bdbac7afcf7ae
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **984.2 MB (984238404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30dcbe627e55ececd6a8030d1bda558620697a70d6c5b32b503bfa5c768f9d95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Jul 2024 21:19:52 GMT
COPY dir:15f372c0d55f5152b222fa508a1a8c382d0621d72fdef0d2b746557a14bc0dd9 in / 
# Thu, 18 Jul 2024 21:19:52 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 21:36:25 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 18 Jul 2024 21:36:26 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 18 Jul 2024 21:36:58 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel
# Thu, 18 Jul 2024 21:37:00 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 18 Jul 2024 21:37:00 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 18 Jul 2024 21:37:00 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 18 Jul 2024 21:37:00 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 18 Jul 2024 21:37:01 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 18 Jul 2024 21:37:01 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 18 Jul 2024 21:37:42 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 18 Jul 2024 21:37:49 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:1e5e0347739e5468c65eed56d50fba90128674d8aae6fa196a8c01eeea145da9`  
		Last Modified: Thu, 18 Jul 2024 21:20:18 GMT  
		Size: 62.6 MB (62647926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98285b9fad024e2fefd98e785a6cafa759ae64473ce411f15ec4f7d2747843d8`  
		Last Modified: Thu, 18 Jul 2024 21:50:53 GMT  
		Size: 296.9 MB (296925455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faa71d6c35bc9718bd436eca3add31e1ab7159af90e14c3a4e18aa343160b1a2`  
		Last Modified: Thu, 18 Jul 2024 21:51:40 GMT  
		Size: 624.7 MB (624664848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550e707da9fd7143c8ea42e5cc28d80497fe66adca253a72e1dbed21fb5e3624`  
		Last Modified: Thu, 18 Jul 2024 21:50:16 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:18b5f81ea8280897827b64f0a546170036fcd47780cc4f8a021a3d20e2b58f69
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **951.1 MB (951058082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ffa6b73b2439f61020ec6fabbd8139df8a97b3fd6a70c1e13d92f5dbdebd05`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Jul 2024 21:39:44 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Thu, 18 Jul 2024 21:39:45 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 21:55:41 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 18 Jul 2024 21:55:41 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 18 Jul 2024 21:56:07 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel
# Thu, 18 Jul 2024 21:56:12 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 18 Jul 2024 21:56:12 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 18 Jul 2024 21:56:12 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 18 Jul 2024 21:56:12 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 18 Jul 2024 21:56:12 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 18 Jul 2024 21:56:12 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 18 Jul 2024 21:56:57 GMT
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz
# Thu, 18 Jul 2024 21:57:11 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05525f95f91140c5f3dc41fd83efe6f8d20c7af636a5061ca350efab21c43cfa`  
		Last Modified: Thu, 18 Jul 2024 22:06:39 GMT  
		Size: 268.5 MB (268463461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f038016a5c5528c56fd51f486d77abb24bfa058e2769527ffaa5026cbf141ace`  
		Last Modified: Thu, 18 Jul 2024 22:07:15 GMT  
		Size: 618.0 MB (618019135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42732af9e6c5b1b6b38ce971f9aa9e9a39aa8e6206adfc783bc7fececb8106b6`  
		Last Modified: Thu, 18 Jul 2024 22:06:13 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
