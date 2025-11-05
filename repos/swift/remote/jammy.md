## `swift:jammy`

```console
$ docker pull swift@sha256:94bee3f0448fe19ad0f5fd6ded227f2b4a927ad635e0e1043bfc8b2eda58e42f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:jammy` - linux; amd64

```console
$ docker pull swift@sha256:4dcd8b670f8d2ce1b4525a92b154d8cc770f0f17ad0194f4731b0ef1fc3e75d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1233375516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb50e7ed388a626571126469cd45b1daa7fc28281830334a00e0aed645df022b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 22:26:22 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 22:26:22 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 22:26:22 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 22:26:22 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 22:26:22 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 04 Nov 2025 22:26:22 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 22:26:22 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 22:26:22 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 22:26:22 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 22:27:04 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 04 Nov 2025 22:27:04 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8d46ac236d99c0c5d85b9f3a4a7e229d6b64577d0252dee0a9c97ba2cb2283`  
		Last Modified: Tue, 04 Nov 2025 23:50:46 GMT  
		Size: 175.5 MB (175451432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01decbba744e405e9307882a3e6b7cd819f611d4c38003a81021c91cd8037e6`  
		Last Modified: Tue, 04 Nov 2025 23:50:49 GMT  
		Size: 1.0 GB (1028387092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7fcdbd91e3126012905c46daf54af71250bf7fd706bc708e4b7fc78e7d44a6`  
		Last Modified: Tue, 04 Nov 2025 22:29:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:9e9a27a74979d8c6a14d25a4b156f45852447c979915e1735cba6716ae9a9400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8493390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65024dcfbfe60b1ac537dfa2d64c67c070e91268d003b0eeebabcbfdec1ad5fe`

```dockerfile
```

-	Layers:
	-	`sha256:a8ad45e1d92452325312364d80d9270b3844c16cec9605d99ad07868e4ab7759`  
		Last Modified: Tue, 04 Nov 2025 23:48:11 GMT  
		Size: 8.5 MB (8477471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12dbc014315ab51e05fd74f77759578f1e9c5165d05138fd541e848e982b8bb8`  
		Last Modified: Tue, 04 Nov 2025 23:48:12 GMT  
		Size: 15.9 KB (15919 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:jammy` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:4d135738df2d17a0fa302c9887f506e2b199ce9be2ba79049d3c5e30f93ba2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1222005818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b00b61163b9acbad862e6a2f8160a02655867eb32dd91f9a590c98cf7cc174`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 19:24:18 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 04 Nov 2025 19:24:18 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 04 Nov 2025 19:24:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-11-dev     libpython3-dev     libsqlite3-0     libstdc++-11-dev     libxml2-dev     libz3-dev     pkg-config     python3-lldb-13     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 04 Nov 2025 19:24:18 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 04 Nov 2025 19:24:18 GMT
ARG SWIFT_PLATFORM=ubuntu22.04
# Tue, 04 Nov 2025 19:24:18 GMT
ARG SWIFT_BRANCH=swift-6.2.1-release
# Tue, 04 Nov 2025 19:24:18 GMT
ARG SWIFT_VERSION=swift-6.2.1-RELEASE
# Tue, 04 Nov 2025 19:24:18 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:24:18 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 04 Nov 2025 19:25:06 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 04 Nov 2025 19:25:06 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu22.04 SWIFT_BRANCH=swift-6.2.1-release SWIFT_VERSION=swift-6.2.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cab1225cd71b55f46a76d8f5019964bbfae364128f1d971aa4828ff0100af3`  
		Last Modified: Tue, 04 Nov 2025 20:54:04 GMT  
		Size: 171.8 MB (171762958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9575d0f489d1e021ac4ca8e1ff210f37f312ac8899908c6d7d9c3d22879d8bd8`  
		Last Modified: Tue, 04 Nov 2025 20:54:53 GMT  
		Size: 1.0 GB (1022859579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a770e8585cbb3aa050835b4635f589121091f307dcd3bbe7eaf64194c501ac`  
		Last Modified: Tue, 04 Nov 2025 19:27:41 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:jammy` - unknown; unknown

```console
$ docker pull swift@sha256:63c6cb580baec60529de74a9a4b43df5748c6e45a909242d650d75b6c51d2a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8489198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a644c2e41afcbf1dedb3677e2872c281b24f1b8c53344ad3180c6ff445be9ce5`

```dockerfile
```

-	Layers:
	-	`sha256:4364d577590258e05280eb74af65253198ed4abc228e39cd9010d76fa3521ae1`  
		Last Modified: Tue, 04 Nov 2025 20:48:19 GMT  
		Size: 8.5 MB (8473157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15e7c8fafdfa81d25e51968dd777f418d83dff81da68b0205fa44fca1af9fd0`  
		Last Modified: Tue, 04 Nov 2025 20:48:21 GMT  
		Size: 16.0 KB (16041 bytes)  
		MIME: application/vnd.in-toto+json
