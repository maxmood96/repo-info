## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:7e0b0d9546e5d6de16529d29e18a6da532cff51c8bd13b5310e595a2302fcae4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 3
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:e74d5962b62889bea0e8c83ff5ec5752d971e1969c8b1a223f0a8dd0bd69f0f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **985.3 MB (985272264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebaf0b48db9f76beca9441f45b58aa548cc5969c9d0c7e05b06b89790ffb1ada`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Jun 2024 15:11:32 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
CMD ["/bin/bash"]
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Thu, 06 Jun 2024 15:11:32 GMT
LABEL description=Docker Container for the Swift programming language
# Thu, 06 Jun 2024 15:11:32 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_BRANCH=swift-5.10.1-release
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_VERSION=swift-5.10.1-RELEASE
# Thu, 06 Jun 2024 15:11:32 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Thu, 06 Jun 2024 15:11:32 GMT
# ARGS: SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-5.10.1-release SWIFT_VERSION=swift-5.10.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:37766f9d8ddf179208313163dc89d8d39dc16ba3be3bc46534855c244565cdd4`  
		Last Modified: Fri, 12 Jul 2024 13:12:20 GMT  
		Size: 62.6 MB (62649406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba019b501051aefda89bf6130cacf9372789ed564e2a6c1d859ee7aca8bbdb3f`  
		Last Modified: Tue, 23 Jul 2024 00:09:29 GMT  
		Size: 298.0 MB (297957399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:841dcdb309f55330a0e26507d229166475e9395cb361ff48c26df7266209bba1`  
		Last Modified: Tue, 23 Jul 2024 00:09:38 GMT  
		Size: 624.7 MB (624665285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f98b5793e449c65edd6d0579e732fb3f81d99cdd474eb77dfde9c66b4c6c0c0`  
		Last Modified: Tue, 23 Jul 2024 00:09:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:0d71ce2665d83dbfd6325abd9640864c1f8ebf359ca075b0bf3db7c3e6ad5463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12660183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdde01325092c9f9da547c101a3ee55d875b9d6eb7c127a35ad43c7f03f1a89`

```dockerfile
```

-	Layers:
	-	`sha256:3372097eebcbe183076bf5094ba29ce459169f8fca86883ce1dc1875799d1e60`  
		Last Modified: Tue, 23 Jul 2024 00:09:23 GMT  
		Size: 12.6 MB (12645283 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b93222c11d7d38be57d16581fdd35e17355c165dc697e1c4c188ab17bd64e26`  
		Last Modified: Tue, 23 Jul 2024 00:09:23 GMT  
		Size: 14.9 KB (14900 bytes)  
		MIME: application/vnd.in-toto+json

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
