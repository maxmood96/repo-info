## `swift:latest`

```console
$ docker pull swift@sha256:047ec90b87375d655e0b4165d78274f572edef684123bbdfdaccec19d630ba42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:latest` - linux; amd64

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

### `swift:latest` - unknown; unknown

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

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:71b6e584fb4fdf5bc6349c0d0fb04499ee43a696246dd0c96ee2b1c181418a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1062403089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90bca605aefdfae8c677a1e334baeb171d2b6c9aed2a5d42361f6107c7e531d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
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
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79970ef4e95025d87384f9f11f5640e6fecb0427c5db354c27743c573b438b40`  
		Last Modified: Tue, 01 Apr 2025 17:21:02 GMT  
		Size: 139.8 MB (139791248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f24a8b3ab490b83ea37e35846454f213187580f53fe55138d01f3bfa92cc2e4`  
		Last Modified: Tue, 01 Apr 2025 17:21:19 GMT  
		Size: 893.7 MB (893718071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bdce0fc5b799913fcdaf67a4bbc5df2620e4229df3d1bf5c3a58f8fc9e720d`  
		Last Modified: Tue, 01 Apr 2025 17:20:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:cea72787c8e7fbcbe4c4380b10438ba30c533aa448d0dc46673223e4877e01f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7700297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4223d396da6d26b87f651d4b776852aa7b929837a8738a5121903680486932d7`

```dockerfile
```

-	Layers:
	-	`sha256:3c9e34f81c1cf556c03a3915c036c986220cfbb4f7119332a9cec939a7fe960c`  
		Last Modified: Tue, 01 Apr 2025 17:20:59 GMT  
		Size: 7.7 MB (7683311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d504fee8d6ea7b37e559180aee05f2ff37fba587be664daf0d584bbf6e020250`  
		Last Modified: Tue, 01 Apr 2025 17:20:58 GMT  
		Size: 17.0 KB (16986 bytes)  
		MIME: application/vnd.in-toto+json
