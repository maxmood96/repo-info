## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:4dbf9e8bbabdd4a1918c6dbd5cab5f690acc3b3574bddde2bf5a56b6ad33bcd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:b7512dd9972c5bf037f187811d1b145706c1d5b7e3c95600e2daf65a50b31018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1271925046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:704ab2fa377a4a1b65032b4559b423d6ca14e70ffe63985308bc66b1fe18941a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 14 May 2025 20:17:09 GMT
COPY /rootfs/ / # buildkit
# Wed, 14 May 2025 20:17:09 GMT
CMD ["/bin/bash"]
# Mon, 26 May 2025 22:39:21 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 26 May 2025 22:39:21 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 26 May 2025 22:39:21 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_BRANCH=swift-6.1.1-release
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_VERSION=swift-6.1.1-RELEASE
# Mon, 26 May 2025 22:39:21 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 May 2025 22:39:21 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 26 May 2025 22:39:21 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 26 May 2025 22:39:21 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.1.1-release SWIFT_VERSION=swift-6.1.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Wed, 14 May 2025 22:47:15 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4cbafb894b3eda271e4357f1f7765b32e566f92b7e29b615437fd416e79429`  
		Last Modified: Tue, 27 May 2025 18:58:38 GMT  
		Size: 313.7 MB (313682695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32dcf357d52cbe9ffc5e7a581c2a2a3d68b4c5f908ddfdddfa0596bb78b97725`  
		Last Modified: Tue, 27 May 2025 18:58:46 GMT  
		Size: 895.5 MB (895482192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a6df20640330cf3ea551ffc480586823e2635dfe4d0da568f816217ae739dc`  
		Last Modified: Tue, 27 May 2025 18:58:33 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:b936c95de6dc080e727944a426980e4d569bf4d1b217f2c0bd140d92b80cb811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12720865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a8c8b68a5e7d6ae6c5903cb49b1e4e6ecd328d146212dd291ddc451f0a97050`

```dockerfile
```

-	Layers:
	-	`sha256:273edbc409cfef015a8ee66530b4e7f85a36f73cf7889fe499763b850f6f0f3c`  
		Last Modified: Tue, 27 May 2025 18:58:33 GMT  
		Size: 12.7 MB (12705977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab615ab35904fe0721709be3cf1cf475c378659536f397cb26b7133da075162e`  
		Last Modified: Tue, 27 May 2025 18:58:33 GMT  
		Size: 14.9 KB (14888 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:05042e9933e91ab05b9addd7b04ca8e86540540ac6f8a310a0347324db9855c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1242244802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5835e8384cce9a89a51037b7f12d49899a09228c7beedf5104bcb4c2f5f32052`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Wed, 14 May 2025 22:47:33 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f75f12160f665a34ce0a513832787727a04972d5e22b85cfe102ec846df3867`  
		Last Modified: Tue, 20 May 2025 00:10:36 GMT  
		Size: 285.2 MB (285223339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947165e1775bf7f9f8eea790d688fc4e199d4fd4d95625e3ca73023b18e791a2`  
		Last Modified: Tue, 01 Apr 2025 17:43:47 GMT  
		Size: 892.4 MB (892413807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534a8a182c9dca38a60daaea0ffdb99e70eb58824ead0323c598076fede5f94d`  
		Last Modified: Tue, 20 May 2025 00:10:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:0f7338be4864d77852a9edfa780231fdb2084f186509ebbfa6f480221e382018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12582608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e979e4250848eea64c9a3f21141cf39d5586218ff4a32313ecf27afb11db71e2`

```dockerfile
```

-	Layers:
	-	`sha256:7c70481e4a1cb6a2a86e6b154fbfa9be1eb2daa8a37c5c45958570b7b7c69f15`  
		Last Modified: Tue, 20 May 2025 00:10:30 GMT  
		Size: 12.6 MB (12567610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e82ec131072626786ddca2dcbf7b7004acbeefc9342dfdc2f976f6b40b143c79`  
		Last Modified: Tue, 20 May 2025 00:10:29 GMT  
		Size: 15.0 KB (14998 bytes)  
		MIME: application/vnd.in-toto+json
