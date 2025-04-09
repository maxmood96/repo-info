## `swift:noble`

```console
$ docker pull swift@sha256:4e7920a34695dbf2c7ae3020fb806a6c86e8d91b3fc494b3610a9e17a38e3299
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble` - linux; amd64

```console
$ docker pull swift@sha256:e0ce72c88f5f446d5e0c149d34c7b6d29a33d6410b228d55b575988f9e02e15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1058910047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e9108b4c1e152b0d654e8f1d10e09d1ac6e46b6b8dd4e02fef17904467fc3d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
ARG RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Apr 2025 00:12:10 GMT
ADD file:1d7c45546e94b90e941c5bf5c7a5d415d7b868581ad96171d4beb76caa8ab683 in / 
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:2726e237d1a374379e783053d93d0345c8a3bf3c57b5d35b099de1ad777486ee`  
		Last Modified: Tue, 08 Apr 2025 11:53:40 GMT  
		Size: 29.7 MB (29717652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb5e775a274dd9e1bfdc9cd23c27f223163f371d270b7dd506318097a00ab6fd`  
		Last Modified: Wed, 09 Apr 2025 01:24:42 GMT  
		Size: 130.2 MB (130243817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8880b4617c55924f3abed83211bf1ddbdf5a3ec376a5c097a9c9d5ed3170e85`  
		Last Modified: Wed, 09 Apr 2025 01:24:56 GMT  
		Size: 898.9 MB (898948405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04eb92e59209b22430a39c96624aa392ea151705cb47f42cf74396128abc5b0f`  
		Last Modified: Wed, 09 Apr 2025 01:24:40 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:49ff957fcd3856ce3e9e653770ed727f55e2f593fe51bfe299fcab158f06956d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7678123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fb3e58114103083207de885653806adb0141d541dce5f59a053837c8962503`

```dockerfile
```

-	Layers:
	-	`sha256:b0ab1f1b2f73fd526ec213bec0941b9838b6f2f25843a93a47396b62f41ebacc`  
		Last Modified: Wed, 09 Apr 2025 01:24:41 GMT  
		Size: 7.7 MB (7661295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32f1dfca6a662e3386ec875ac385169e50c37cf842b6a781a8be789c214ef54e`  
		Last Modified: Wed, 09 Apr 2025 01:24:40 GMT  
		Size: 16.8 KB (16828 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:noble` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:7010024899d6ca114493ead216440361c81c0fbd17ab65880cd50ec1f574a390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1051912283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775ca2668c03cc4b42be25e05e622c75afd368dce7b5d97aaac825de44581c36`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 00:12:10 GMT
ARG RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 01 Apr 2025 00:12:10 GMT
ADD file:918b7712da52a62e47b028978dd5fc952b2f7f7f0507ea2362c4ccd14120133c in / 
# Tue, 01 Apr 2025 00:12:10 GMT
CMD ["/bin/bash"]
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 01 Apr 2025 00:12:10 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 01 Apr 2025 00:12:10 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_BRANCH=swift-6.1-release
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_VERSION=swift-6.1-RELEASE
# Tue, 01 Apr 2025 00:12:10 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 01 Apr 2025 00:12:10 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.1-release SWIFT_VERSION=swift-6.1-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:49b96e96358d7aed127d4f4cd2294d77d497c683123bbad89fa80a83d8ef64aa`  
		Last Modified: Tue, 08 Apr 2025 11:53:46 GMT  
		Size: 28.8 MB (28846958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fce81d413cb026d51579643018a120cdd0e4937a24032d21753682826a7f0ea`  
		Last Modified: Wed, 09 Apr 2025 13:10:19 GMT  
		Size: 129.3 MB (129346733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708fc817245ad91dbd1952d943c60ad0b282b40eb6d4dce19b8d91e2e6fcb211`  
		Last Modified: Wed, 09 Apr 2025 18:04:21 GMT  
		Size: 893.7 MB (893718418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1e615347884ae47e2e756a8e80d367f4bc21a1bdbd22a379aef965dea7c31f`  
		Last Modified: Wed, 09 Apr 2025 18:04:03 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:6c2c79b08e2b14d983bd016fc85b41968288a454f4bdc8c102d2841068b23e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7701057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58944bf47f15649e640ef9881184721bc9b2f9193bfaa91c8bf683f5af83a388`

```dockerfile
```

-	Layers:
	-	`sha256:faeae76d369adff165a955d5f8ab5827e03494b05e11174b647d7e8189925eb2`  
		Last Modified: Wed, 09 Apr 2025 18:04:04 GMT  
		Size: 7.7 MB (7684071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b5995b14d558753012f860b0f14b393dd3ea0db4cb4caff9a5b0023f0e35ecd`  
		Last Modified: Wed, 09 Apr 2025 18:04:03 GMT  
		Size: 17.0 KB (16986 bytes)  
		MIME: application/vnd.in-toto+json
