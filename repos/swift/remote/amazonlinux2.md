## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:7870e58970d697615b6ae1c6b5e03d4ee05a9cbbf565e90cf9743e9e5d10053f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:73272fccd8198775fdea9664713cb091dbde044f4a60e0c725636bd81f31c670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1637478562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923066467cdd09ede87a68c92ca0be710e2ec64591042a89be545b77e9544d7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:59 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:59 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2026 18:56:44 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Jun 2026 18:56:44 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Jun 2026 18:56:44 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Tue, 30 Jun 2026 18:56:44 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Jun 2026 18:56:44 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 30 Jun 2026 18:56:44 GMT
ARG SWIFT_BRANCH=swift-6.3.3-release
# Tue, 30 Jun 2026 18:56:44 GMT
ARG SWIFT_VERSION=swift-6.3.3-RELEASE
# Tue, 30 Jun 2026 18:56:44 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:56:44 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:57:30 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 30 Jun 2026 18:57:30 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b5a31d0a32c9342b5b53f098c4d8ac4fadeb6cbc6b34b2e4424fd39eb880bf9a`  
		Last Modified: Sat, 13 Jun 2026 04:09:34 GMT  
		Size: 62.9 MB (62942019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e2d4579fca18269a4e7598a367a7316e1a67fd5e4bb3c8f4ed690d3c588fd9`  
		Last Modified: Tue, 30 Jun 2026 19:00:33 GMT  
		Size: 337.7 MB (337685677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33e8aa7d987461f245dc96471d60e0f6128ae368878020718eb933c49dac1c4`  
		Last Modified: Tue, 30 Jun 2026 19:00:52 GMT  
		Size: 1.2 GB (1236850692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d41e45202f666daaa8ee8ab7e929fdfc708c13b2d5f854cf267cc0dc38031061`  
		Last Modified: Tue, 30 Jun 2026 19:00:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:723742ace237808493051a5791d029a5cef9d6f455f8d4c0ebd2ded3a1feb077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41f94fb475005e864096f15253be28b238101bee997053cd55aec9b8d5f5d2f9`

```dockerfile
```

-	Layers:
	-	`sha256:ee0a7d328914d0d1cd86e85239e98f5f0625ad560affebadfe130640c11ffef9`  
		Last Modified: Tue, 30 Jun 2026 19:00:17 GMT  
		Size: 12.7 MB (12720094 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42b250d9e94d8ee5b0eb238004d8a687c9961add735b1303409eaaca304ff3c9`  
		Last Modified: Tue, 30 Jun 2026 19:00:16 GMT  
		Size: 14.8 KB (14847 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:2bb336056af719e4ff64870aa6d9d5b80e991e14fda39f4ea97c6851b9264394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1593020770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93160e233ca269516a2ae461f7869436cfd8149126d61b3c25fb93dedadf7d5e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 22 Jun 2026 18:00:28 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 18:00:28 GMT
CMD ["/bin/bash"]
# Tue, 30 Jun 2026 18:56:24 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 30 Jun 2026 18:56:24 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 30 Jun 2026 18:56:24 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Tue, 30 Jun 2026 18:56:24 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 30 Jun 2026 18:56:24 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Tue, 30 Jun 2026 18:56:24 GMT
ARG SWIFT_BRANCH=swift-6.3.3-release
# Tue, 30 Jun 2026 18:56:24 GMT
ARG SWIFT_VERSION=swift-6.3.3-RELEASE
# Tue, 30 Jun 2026 18:56:24 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:56:24 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 30 Jun 2026 18:57:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Tue, 30 Jun 2026 18:57:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.3.3-release SWIFT_VERSION=swift-6.3.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:4b30ecc040ec91b7e580ef7f93f591eaf80422b110a473c44b4d0dbcb2301395`  
		Last Modified: Wed, 17 Jun 2026 13:06:48 GMT  
		Size: 64.8 MB (64794736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f3e500c8793228adfce4aa328228c32a67de3571a8438f5756a24722d5f634`  
		Last Modified: Tue, 30 Jun 2026 18:59:47 GMT  
		Size: 308.6 MB (308634764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06b78b3b54cf32b7d4aff5b64e08677341fb7d164b390426f2faeccf4920bab`  
		Last Modified: Tue, 30 Jun 2026 19:00:14 GMT  
		Size: 1.2 GB (1219591096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ec1e8dbe48bd67e6602667dfe0335fc4df777d0895118315a5176c6975aecf`  
		Last Modified: Tue, 30 Jun 2026 18:59:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:cfe7c09be4d634d2114c60f645366975d9347da56b3da307ed137676a891fc9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff21d6c67d4332f17b194d9d9e5f1f933fd61fe2a4374a31cccbc46092856d0`

```dockerfile
```

-	Layers:
	-	`sha256:c3436dd1a9ab172b628019180d62f4545274341157a9451415bac3bf82aa9f7e`  
		Last Modified: Tue, 30 Jun 2026 18:59:35 GMT  
		Size: 12.6 MB (12581731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02ef1c560afe66578cd2e09428cef7731bdcd0942eb3b8f92c5d7c48a5f20b6e`  
		Last Modified: Tue, 30 Jun 2026 18:59:34 GMT  
		Size: 15.0 KB (14969 bytes)  
		MIME: application/vnd.in-toto+json
