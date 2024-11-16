## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:3e31607ec52d1d21d48c2d15bbe4ead5a5544451576ade803c223dcf193bc923
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:08238b7e122838479c807aae3706d43a236461710ecc6104dbfc5d47182e075c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1196310728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78da0c96932414120c49678a8b62d1daa792e395019ee80900b4cc4c5642ae9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9164afa634804f357356ebb252286d5fc42e5763bc912fd973f7e196c6c161e`  
		Last Modified: Sat, 16 Nov 2024 00:50:34 GMT  
		Size: 303.7 MB (303668133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099b241a4b7d02098d8ccf898e66c08ccb242b84e7ec8f5ec675c597b11a5f13`  
		Last Modified: Mon, 28 Oct 2024 21:00:49 GMT  
		Size: 830.0 MB (829964983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c8d4483035f04fb905aee0ce17ce866084e5def8e706d6a0864caaab96acf12`  
		Last Modified: Sat, 16 Nov 2024 00:50:29 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:50c6b4c2c8d1cff9381b736411a297ffda95de92eb144007149e5c342bd14014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12660285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c0549d93462f3426264fe43bb049e0395e729d7310b74cc191c4a79737daa9`

```dockerfile
```

-	Layers:
	-	`sha256:f528733e8789018ae0af31579db5b53ab0f2d0f737b5f3aa14502abd083eb08c`  
		Last Modified: Sat, 16 Nov 2024 00:50:30 GMT  
		Size: 12.6 MB (12645397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09a4663c9dd59ffd98e05ee5f18c069ed5d6c362c30ed1b98668223d48489f2d`  
		Last Modified: Sat, 16 Nov 2024 00:50:29 GMT  
		Size: 14.9 KB (14888 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:01a86f94cb4f2a6fc07c277e878b2635efd20e18a80b6783f27b1c756a02d2b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1165227655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55ddc1adbd11b38152e38e50a1a96279c7913ca7fc7e3889c481443dbb86876`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 28 Oct 2024 18:01:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0e9ee956c0e72f50f9c0f291d2fab9d6e5bafb446c3c99bf8fa63542e5b090d`  
		Last Modified: Sat, 16 Nov 2024 01:16:33 GMT  
		Size: 275.2 MB (275166563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b179166cb3aed929bcd4e15e7b352b7dc59473b69c9e8774d3a3cacf55a053e`  
		Last Modified: Mon, 28 Oct 2024 21:29:25 GMT  
		Size: 825.5 MB (825479031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:addb4853f8d92398b85e2374dc5f6a78427fa14df62550915f54447f7efb66a3`  
		Last Modified: Sat, 16 Nov 2024 01:16:27 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:4dd22bbd473f668db7c7ce5aa69c21202360151ffceccff98b7e392478e7a97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12522119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f106dea738d01fcc6a620b5a9ec08cc729009ed0fa99b1a6dc714c7414810130`

```dockerfile
```

-	Layers:
	-	`sha256:6122cbb37c0c602e6fe4e19556ab32ce9b5dcd9d27a4f4fe4cc16c800897a538`  
		Last Modified: Sat, 16 Nov 2024 01:16:28 GMT  
		Size: 12.5 MB (12507109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce30a8dc3363e34e45faa4b79ab5f5135744c49db90ccf60a233e12daa7c3af9`  
		Last Modified: Sat, 16 Nov 2024 01:16:27 GMT  
		Size: 15.0 KB (15010 bytes)  
		MIME: application/vnd.in-toto+json
