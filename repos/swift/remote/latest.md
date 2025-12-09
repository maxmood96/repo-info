## `swift:latest`

```console
$ docker pull swift@sha256:512d27e81ca465e627034efb141516e5945517625de1a523550a9d33539c56a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:bada6fc75729af7e2933d874f1bcab75d58a4c2ce42445dbca7522e7a2027464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1189791742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0c7f87d726c2e3963cf584e37d1860063de5d08b32b110f8186dc45f309baf1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Tue, 09 Dec 2025 17:37:45 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Dec 2025 17:37:45 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Dec 2025 17:37:45 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 17:37:45 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Dec 2025 17:37:45 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 09 Dec 2025 17:37:45 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Tue, 09 Dec 2025 17:37:45 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Tue, 09 Dec 2025 17:37:45 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:37:45 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:38:36 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 09 Dec 2025 17:38:36 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0615e8e066a83358516779f867347f949a36b5fdb070662fa0d6961749bba234`  
		Last Modified: Tue, 09 Dec 2025 17:42:16 GMT  
		Size: 130.4 MB (130384646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81677296a4655209f3167a0657783a9246358022759dfdf5be6a59ef8d7efec`  
		Last Modified: Tue, 09 Dec 2025 17:42:39 GMT  
		Size: 1.0 GB (1029682234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c60a632cf805e1afff83190d56df44fd61c92c03bc810706f0a7e64811b4147`  
		Last Modified: Tue, 09 Dec 2025 17:41:18 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:2e540431517b81fd23ffbfcf6df94c697ffb544646a39b8033827b69a9b133ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7894774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f2e17ad53f18527538882c670bbf64465bd8705c829567fe91110d931f4325`

```dockerfile
```

-	Layers:
	-	`sha256:ddb8a7968f307c6461b859eb9ff83d00089944cb60391270729565944488149b`  
		Last Modified: Tue, 09 Dec 2025 20:47:54 GMT  
		Size: 7.9 MB (7877975 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32014ef7a5c6d9430776de36ba79af881a9659f3cc565822bc16e3888f2010ea`  
		Last Modified: Tue, 09 Dec 2025 20:47:56 GMT  
		Size: 16.8 KB (16799 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:45fdf623b3774f3c4186a5ce9f2d3be9d3de21738b7b21f3a4dd8af5b9f5ff3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1182297258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6d2e066581510ca961442e0ff235a626424f3570f5b1ed2e0ca8b1b169e59d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Tue, 09 Dec 2025 17:37:39 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 09 Dec 2025 17:37:39 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 09 Dec 2025 17:37:39 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 17:37:39 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 09 Dec 2025 17:37:39 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 09 Dec 2025 17:37:39 GMT
ARG SWIFT_BRANCH=swift-6.2.2-release
# Tue, 09 Dec 2025 17:37:39 GMT
ARG SWIFT_VERSION=swift-6.2.2-RELEASE
# Tue, 09 Dec 2025 17:37:39 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:37:39 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 09 Dec 2025 17:38:31 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 09 Dec 2025 17:38:31 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.2-release SWIFT_VERSION=swift-6.2.2-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d039832d03e634132f341a1e4db5c5d7550dc8b430abe60bc3d9c15ca233e312`  
		Last Modified: Tue, 09 Dec 2025 17:41:18 GMT  
		Size: 129.5 MB (129485385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473c40e77530d13f91245a26938a2525e3f87f5a3cb9e23d82b9c13bd1628589`  
		Last Modified: Tue, 09 Dec 2025 17:41:37 GMT  
		Size: 1.0 GB (1023949741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fef7feb307c782d54f4d7e69daa32b2334e13f4a22334b2f3d04e7c51002472b`  
		Last Modified: Tue, 09 Dec 2025 17:41:04 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:2979784984c63aa00f82274e16676075c16443cd4c73be7dbaa0c618cb3f0502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7917419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a1bda70023b704d28f7ee4f954ef82d116f5954f962b1f5dff96777cb65b3b4`

```dockerfile
```

-	Layers:
	-	`sha256:f59c991e423a524e3abb55ec5f302aab697b6b37881bff40004b7483d095d22f`  
		Last Modified: Tue, 09 Dec 2025 20:48:02 GMT  
		Size: 7.9 MB (7900462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca519eadce40d7f5c69199d244c188657c903c7bb58085859bb3911a90d19d2b`  
		Last Modified: Tue, 09 Dec 2025 20:48:05 GMT  
		Size: 17.0 KB (16957 bytes)  
		MIME: application/vnd.in-toto+json
