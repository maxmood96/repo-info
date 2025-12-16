## `swift:latest`

```console
$ docker pull swift@sha256:ce273f554d653b0dbf84235bb616aee380eb06bbf53873108312cb695036439f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:0e87e92c8ead7c9ce1e818c7628c0ef6d484ad72eef3ce298f7a288f81ed9d45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1189957127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d56486d996f2f467c7706bee189087ba36ba0e7d6739491d426c9790b6dbe45`
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
# Fri, 12 Dec 2025 22:41:33 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Dec 2025 22:41:33 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Dec 2025 22:41:33 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 12 Dec 2025 22:41:33 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 12 Dec 2025 22:41:33 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Fri, 12 Dec 2025 22:41:33 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Fri, 12 Dec 2025 22:41:33 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Fri, 12 Dec 2025 22:41:33 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:41:33 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:42:22 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Fri, 12 Dec 2025 22:42:22 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Mon, 15 Dec 2025 21:56:21 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011dfe0cc1c92447ace84fd2d7738882ae2a99e1e2ef38263bff287430fb0202`  
		Last Modified: Fri, 12 Dec 2025 22:45:15 GMT  
		Size: 130.4 MB (130384885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202269e06ebc15ed7497dcdec59b084b766be73f5ab738bd14db013c3a01c8b1`  
		Last Modified: Fri, 12 Dec 2025 22:46:22 GMT  
		Size: 1.0 GB (1029847382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3192f5017edd8b85a9df3ac67be0599180d164d9828a7d1c0147e979ec23ff58`  
		Last Modified: Fri, 12 Dec 2025 22:44:59 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:9b9d626b21557f987d34adbe821bf0b9b9bed6b65fe135083a2c6b89fb65c58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7894786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c8b7fa906e1cdf5f987259d213a0d54cdceb1f7b14f23da2a0a71d8d47eb20`

```dockerfile
```

-	Layers:
	-	`sha256:4e59b7d6f093fc4ff61390481540c6a52c23fc8fcb772ae044f312ff840c7b35`  
		Last Modified: Fri, 12 Dec 2025 23:47:50 GMT  
		Size: 7.9 MB (7877987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de114076fc10ffce450c31006d210aede9f637901ce8cd8fb3d5ec8b25bea468`  
		Last Modified: Fri, 12 Dec 2025 23:47:51 GMT  
		Size: 16.8 KB (16799 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:3389205d1d411ae0ee8b81c697880cbf40f379bf62c676fa4de254c818f69fdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1182467599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d813dab1cfd175d358325f2e3c59a7211e148370f91bf16bc9c9e8e46488a7`
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
# Fri, 12 Dec 2025 22:41:36 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Fri, 12 Dec 2025 22:41:36 GMT
LABEL description=Docker Container for the Swift programming language
# Fri, 12 Dec 2025 22:41:36 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Fri, 12 Dec 2025 22:41:36 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Fri, 12 Dec 2025 22:41:36 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Fri, 12 Dec 2025 22:41:36 GMT
ARG SWIFT_BRANCH=swift-6.2.3-release
# Fri, 12 Dec 2025 22:41:36 GMT
ARG SWIFT_VERSION=swift-6.2.3-RELEASE
# Fri, 12 Dec 2025 22:41:36 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:41:36 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Fri, 12 Dec 2025 22:42:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Fri, 12 Dec 2025 22:42:26 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.2.3-release SWIFT_VERSION=swift-6.2.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Mon, 15 Dec 2025 21:56:39 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a26df9403d8577161fa5a21821ebd7569519edaff32bff3d17c75fe97e6ffc`  
		Last Modified: Fri, 12 Dec 2025 22:45:12 GMT  
		Size: 129.5 MB (129484778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c1715ec8336af8b05b6d6d4c99c28932f9bd67f69f534fc8221942d701912c`  
		Last Modified: Fri, 12 Dec 2025 22:45:14 GMT  
		Size: 1.0 GB (1024120690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752e7fbeacf379ec1e02436745dd931272f0c84bafa7cb2633b4eb32b763d229`  
		Last Modified: Fri, 12 Dec 2025 22:44:57 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:5439c56baeda7fab88143c88769d3c3cbcd5378893ff259fda67ebd529a679fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7917430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6808870a9e0f7f08426c3df4021b4dd591db309fbf27700d611929e8c4c3f948`

```dockerfile
```

-	Layers:
	-	`sha256:ec7247e366f9465be80fe508cdf382805f1de12afa49a0ce5ad497d1cb951cba`  
		Last Modified: Fri, 12 Dec 2025 23:47:57 GMT  
		Size: 7.9 MB (7900474 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:607c080a2de17853ac829748ccad672da4e425a0d2ee32b49c4ec8235d2413ac`  
		Last Modified: Fri, 12 Dec 2025 23:47:58 GMT  
		Size: 17.0 KB (16956 bytes)  
		MIME: application/vnd.in-toto+json
