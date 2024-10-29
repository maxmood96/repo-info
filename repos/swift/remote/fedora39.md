## `swift:fedora39`

```console
$ docker pull swift@sha256:0e062cf3f25e1994b69dfdf2b93fb6287e6bde349bfccf8adcbcde3611e769a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:fedora39` - linux; amd64

```console
$ docker pull swift@sha256:d6384dc5ea61eebf9587be130fbc365115a4f4ee0f83f6bd3d439d74721dabc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1262518538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fce05a257db16d7111e6dccfc2662c622702ffcb2a55be2b1eb2dcab5b071bf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 10:40:52 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 15 Sep 2024 10:40:52 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Sun, 15 Sep 2024 10:40:52 GMT
ADD fedora-39-x86_64.tar.xz / # buildkit
# Sun, 15 Sep 2024 10:40:52 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN yum -y install   binutils   gcc   git   unzip   libcurl-devel   libedit-devel   libicu-devel   sqlite-devel   libuuid-devel   libxml2-devel   python3-devel # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=fedora39
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:8fbaf22a49eb14a89c9ae872033ffd84bcccd25d4bcd55d33bc936ac30a7efc8`  
		Last Modified: Mon, 16 Sep 2024 18:58:27 GMT  
		Size: 64.9 MB (64890373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf48283daf7eb88eb75aceec4e9c155fc9334b1935b8a60aa4f58de5cda3c5ae`  
		Last Modified: Mon, 28 Oct 2024 21:01:21 GMT  
		Size: 365.1 MB (365078935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68532d6938be037de8d4426e3e8ad3b0ad8893c74f5bc6912a170fd55f713b0`  
		Last Modified: Mon, 28 Oct 2024 21:01:30 GMT  
		Size: 832.5 MB (832549056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2a9c27b588698d22d369e8791cf71208d106b5493e1238143ae8d103557bd3`  
		Last Modified: Mon, 28 Oct 2024 21:01:16 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:fedora39` - unknown; unknown

```console
$ docker pull swift@sha256:9cebb2b29c4190fe11f5108a7694e4d578102bade5ef6f9b0f2ee98bd10c2059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 MB (9403806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dcd2c43812a1df627b63629414ab34edd0cac46d2ee042dae5aadf27449bd68`

```dockerfile
```

-	Layers:
	-	`sha256:60a8ce63a0842769eabc902ca50d9e4b6716534f3c6a4dfc68433d13393af57a`  
		Last Modified: Mon, 28 Oct 2024 21:01:16 GMT  
		Size: 9.4 MB (9389274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27aadab9170084fa52410d6deb9fa5e71fdbd991c4a4e00dec74a7598184828`  
		Last Modified: Mon, 28 Oct 2024 21:01:16 GMT  
		Size: 14.5 KB (14532 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:fedora39` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d2ddd7e124aa7f288393e60f9d6a330371e591879c7e0b7c1f19351d45f1b3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1239931995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43437ff1095c59c13b03e3d3aa8944ad07f48c95ec725bb3420c1a492f8718e9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 15 Sep 2024 10:40:52 GMT
LABEL maintainer=Clement Verna <cverna@fedoraproject.org>
# Sun, 15 Sep 2024 10:40:52 GMT
ENV DISTTAG=f39container FGC=f39 FBR=f39
# Sun, 15 Sep 2024 10:40:52 GMT
ADD fedora-39-aarch64.tar.xz / # buildkit
# Sun, 15 Sep 2024 10:40:52 GMT
CMD ["/bin/bash"]
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Mon, 28 Oct 2024 18:01:55 GMT
LABEL description=Docker Container for the Swift programming language
# Mon, 28 Oct 2024 18:01:55 GMT
RUN yum -y install   binutils   gcc   git   unzip   libcurl-devel   libedit-devel   libicu-devel   sqlite-devel   libuuid-devel   libxml2-devel   python3-devel # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_PLATFORM=fedora39
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_BRANCH=swift-6.0.2-release
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_VERSION=swift-6.0.2-RELEASE
# Mon, 28 Oct 2024 18:01:55 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(rpm --eval '%{_arch}')";     url=;     case "${ARCH_NAME##*-}" in         'x86_64')             OS_ARCH_SUFFIX='';             ;;         'aarch64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && echo $SWIFT_BIN_URL     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz # buildkit
# Mon, 28 Oct 2024 18:01:55 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=fedora39 SWIFT_BRANCH=swift-6.0.2-release SWIFT_VERSION=swift-6.0.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:921ce67e7e51e665859857ab2067fdaea0a4c4d71ebc293d6d7bc9a43f9f9ae7`  
		Last Modified: Mon, 16 Sep 2024 18:58:40 GMT  
		Size: 63.6 MB (63561057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8987a7ffe9c0c7e51d6f1df37c3eb72ffc81f0e56ec0958456c49a98f232ea`  
		Last Modified: Mon, 28 Oct 2024 21:24:15 GMT  
		Size: 346.3 MB (346334693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda5e1e4249f2668b72ff29effe7666e3c8f13dafa333019596b0ac8e36cd584`  
		Last Modified: Mon, 28 Oct 2024 21:24:28 GMT  
		Size: 830.0 MB (830036074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2392f0461e6d7a6132324e06d28048ae1ad26301b3dc247b30184a0d6eec63`  
		Last Modified: Mon, 28 Oct 2024 21:24:08 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:fedora39` - unknown; unknown

```console
$ docker pull swift@sha256:64d0dfb132412e48733a1e87bbf0d0c07b7d23e2a09b389a2789de3b47ba3ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 MB (9302179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f9f9ca063e9628538872e5ed18ab6c1e0abed29f8e275ba7fde17fa137fe79`

```dockerfile
```

-	Layers:
	-	`sha256:c85cc73872e7b9f98dcc4ef52177beab9e50a148e0e7060e67d85a31c669802f`  
		Last Modified: Mon, 28 Oct 2024 21:24:09 GMT  
		Size: 9.3 MB (9287523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a31b977c8b677b6dc1ca5ae2202f251974c8466a61becbc8576d7dc056eb7210`  
		Last Modified: Mon, 28 Oct 2024 21:24:08 GMT  
		Size: 14.7 KB (14656 bytes)  
		MIME: application/vnd.in-toto+json
