## `swift:amazonlinux2`

```console
$ docker pull swift@sha256:5e601d2ad9b391f3ed4eb9ec598a1af334fb91c9c212fe6476e7fa418e5da3a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:amazonlinux2` - linux; amd64

```console
$ docker pull swift@sha256:a734838f375ed6dea63118b5777ed2432bd765447e81d78ef0cccd26010203d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1416732350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98789ad970cc709395e9c064bc56c9481ce1dbdaa327c6002b5bf515dddacb3c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:22:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:22:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:40:19 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 11 Mar 2026 18:40:19 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 11 Mar 2026 18:40:19 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Wed, 11 Mar 2026 18:40:19 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 11 Mar 2026 18:40:19 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 11 Mar 2026 18:40:19 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Wed, 11 Mar 2026 18:40:19 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Wed, 11 Mar 2026 18:40:19 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 11 Mar 2026 18:40:19 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 11 Mar 2026 18:41:05 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 11 Mar 2026 18:41:06 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:94fc983b0f2661f620fb3c97c279be6e7a6a21ff4a004bf4df15272612aed901`  
		Last Modified: Sat, 07 Mar 2026 04:10:35 GMT  
		Size: 63.0 MB (62956510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0ed6bfe4d64545d45044d3adfc0794ff847ed907e7bfd70ef67fbcbf8753f5`  
		Last Modified: Wed, 11 Mar 2026 18:43:35 GMT  
		Size: 327.9 MB (327859060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d637b393a1538c4e593eba973c98bdb951522eca06321fe08a043c46561525aa`  
		Last Modified: Fri, 27 Feb 2026 22:46:57 GMT  
		Size: 1.0 GB (1025916606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb83e6f9b993acd0b2a6fcf2d9ae24ef6e85a0c429d84ab86cfb8762e55a92b2`  
		Last Modified: Wed, 11 Mar 2026 18:43:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:502ae70adea18339fa9c4d4660bc39b14954c7bc6d72c16eed5afe21cebe20d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12734844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a6652c2d3a9257e1beb900c0664be431f1aae2137d4d98e768b76e06c6bc4d4`

```dockerfile
```

-	Layers:
	-	`sha256:a5a80dcee3d440e01884a77f2e41e85c5efa72ea81a720dc06cc8f2a3c5ad291`  
		Last Modified: Wed, 11 Mar 2026 18:43:25 GMT  
		Size: 12.7 MB (12719997 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:184cad726152bfc088cc92dc683ed84b67b847870c86d116ab9e9a915380c623`  
		Last Modified: Wed, 11 Mar 2026 18:43:24 GMT  
		Size: 14.8 KB (14847 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:amazonlinux2` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:ca425d1dc8db7c3092c4e418b5b8d179c881a04af493d6fd84b50c12f28e9018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.4 GB (1386257041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bef9cd8b36ae66272d2c9d5685ba8f3531e8042405fabc69045774dd7feb1bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:38 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:38:27 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 11 Mar 2026 18:38:27 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 11 Mar 2026 18:38:27 GMT
RUN yum -y install   binutils   gcc   git   unzip   glibc-static   gzip   libbsd   libcurl-devel   libedit   libicu   libsqlite   libstdc++-static   libuuid   libxml2-devel   openssl-devel   tar   tzdata   zlib-devel # buildkit
# Wed, 11 Mar 2026 18:38:27 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 11 Mar 2026 18:38:27 GMT
ARG SWIFT_PLATFORM=amazonlinux2
# Wed, 11 Mar 2026 18:38:27 GMT
ARG SWIFT_BRANCH=swift-6.2.4-release
# Wed, 11 Mar 2026 18:38:27 GMT
ARG SWIFT_VERSION=swift-6.2.4-RELEASE
# Wed, 11 Mar 2026 18:38:27 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 11 Mar 2026 18:38:27 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 11 Mar 2026 18:39:12 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Wed, 11 Mar 2026 18:39:12 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=amazonlinux2 SWIFT_BRANCH=swift-6.2.4-release SWIFT_VERSION=swift-6.2.4-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:1331e22401e9e6f680f618ca7ac295b00616904425c0ac818294801fd11443e3`  
		Last Modified: Mon, 09 Mar 2026 09:10:03 GMT  
		Size: 64.8 MB (64803149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d3a25a77e39ee7b20c9fdedd1e143b25ee3bc783eff266229c30d512ca0a61`  
		Last Modified: Wed, 11 Mar 2026 18:41:26 GMT  
		Size: 299.0 MB (299041491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8d67c513705fd795f8e44bb326acb5b69b27c1bb75ae2486bae7283c715fd3`  
		Last Modified: Fri, 27 Feb 2026 22:46:21 GMT  
		Size: 1.0 GB (1022412227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6005bf311d57f2d6a3181e90311d7fc52a89bab0b31866c220593ab024c9101d`  
		Last Modified: Wed, 11 Mar 2026 18:41:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:amazonlinux2` - unknown; unknown

```console
$ docker pull swift@sha256:ece4561d0e8cc285b02ad55f3473a7c69e000cd871d4595ca665a45976d47ae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12596602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227ead5dc484a862c0aa95b7f73aa218f07f9949d972ca6c284f741e98dd81d`

```dockerfile
```

-	Layers:
	-	`sha256:9b07807d24f6cca75c6ff1b1bb8266ac60f7f56f2e24526078d34ac8276a4648`  
		Last Modified: Wed, 11 Mar 2026 18:41:21 GMT  
		Size: 12.6 MB (12581634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4a6e272ce5fc999ed2df100ec2468993033bb5a58af380039af91ba3ae18a1d`  
		Last Modified: Wed, 11 Mar 2026 18:41:20 GMT  
		Size: 15.0 KB (14968 bytes)  
		MIME: application/vnd.in-toto+json
