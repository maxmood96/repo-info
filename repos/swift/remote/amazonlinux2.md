## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:7158974920eda3f7f9545f0b8a6611258843ff47143789d3a87aa9c9404fdea7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:8cc532f8b03baa3f5e29604e97f0bcf0e2fe7603557886dcfd564d9cc095acec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1191659701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca15eddb177c7da808b8c9ad8fb78e68188c2dde2f2801db8850f54a196f30c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 06 Sep 2024 17:28:31 GMT
COPY /rootfs/ / # buildkit
# Fri, 06 Sep 2024 17:28:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea56c9462585b80f66d2aa1493ea9108fe474eb06c6e836e476ba883ccac0e8e`  
		Last Modified: Tue, 17 Sep 2024 17:00:50 GMT  
		Size: 299.8 MB (299840642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190cd9deaa728393132bf086e85b85e61db35ae2290b65f7a00245bb22c842b6`  
		Last Modified: Tue, 17 Sep 2024 17:00:58 GMT  
		Size: 829.1 MB (829123338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b862d0088c45c4583f930b398cc40d5c10bac4d0fd1f1c6bee69e2c12050f300`  
		Last Modified: Tue, 17 Sep 2024 17:00:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:e7a19dbb93013d6481ed63c8ca78a64f9a131280497cd13fa8d085709c0843a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12660129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1bd7e34ae24041b68934337aaeb4866c2db68f766225728a809ed3e31ca5026`

```dockerfile
```

-	Layers:
	-	`sha256:f6e545cd0f1b49c331c248b47854e28b9d1aedeace9a722205e248f0a2a4c3b7`  
		Last Modified: Tue, 17 Sep 2024 17:00:46 GMT  
		Size: 12.6 MB (12645287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf5d6f4ddcff9ce664271720109997e41f2146ac0e88a96572ba7502ac6b3ae`  
		Last Modified: Tue, 17 Sep 2024 17:00:46 GMT  
		Size: 14.8 KB (14842 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:77c6fe65be0b78f0b9d5bb05259a841f6d5b78f659bc3ad4601ffb1a6fea36b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1160618157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316d27e1125fdabaa35242d6b8fe5ed4a28cfef657a4515c7d4ca6a8cdd9d97c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 06 Sep 2024 17:28:35 GMT
COPY /rootfs/ / # buildkit
# Fri, 06 Sep 2024 17:28:35 GMT
CMD ["/bin/bash"]
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 17 Sep 2024 00:51:42 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 17 Sep 2024 00:51:42 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_BRANCH=swift-6.0-release
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_VERSION=swift-6.0-RELEASE
# Tue, 17 Sep 2024 00:51:42 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 17 Sep 2024 00:51:42 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.0-release SWIFT_VERSION=swift-6.0-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:0f0968c920788bb8a898446e0bbe8ea6b11fcbf7f55810ef51044775a045d6c9`  
		Last Modified: Fri, 06 Sep 2024 18:59:50 GMT  
		Size: 64.6 MB (64586343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b2bab80d098f889b2017ed5eccffa02bf567ffd7e435a9f93bd557b80675ca`  
		Last Modified: Tue, 17 Sep 2024 17:23:59 GMT  
		Size: 271.4 MB (271377422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb415d318fa28058edc4d03a9136ae49d0ff9a1d5eb235b8f44491025645f059`  
		Last Modified: Tue, 17 Sep 2024 17:24:05 GMT  
		Size: 824.7 MB (824654219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16d3053b663b2f86df84f9cc916e9362a91d5586498ebb51a42a75baa58fc43d`  
		Last Modified: Tue, 17 Sep 2024 17:23:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:8a6e3f5e0b60236bf670b2d72cfe72fadccdd4a1ec86d214167a694fdcfc6bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.5 MB (12522214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:621238dec3eac28a89398168dcbf69d2819b7dd845e80be16c71cffbf1fa929e`

```dockerfile
```

-	Layers:
	-	`sha256:bcfc3bc407bd894216c8c98052b1c9236d868741adccc5df7f587de64647e573`  
		Last Modified: Tue, 17 Sep 2024 17:23:50 GMT  
		Size: 12.5 MB (12506999 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:597d2f33d7be681d77c28c7cc7335b64e27f9fd0bc3afb1d2f2a5923536ee876`  
		Last Modified: Tue, 17 Sep 2024 17:23:49 GMT  
		Size: 15.2 KB (15215 bytes)  
		MIME: application/vnd.in-toto+json
