## `swift:latest`

```console
$ docker pull swift@sha256:b8c1c1b9d9588334dbed935af833269050f12685888df567f37fc4ac8b524547
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:latest` - linux; amd64

```console
$ docker pull swift@sha256:f055ee49c2c3a5ddeaaec4638bdb7fdd808ba8c0643761c48e7e4d305d1a7ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 GB (1252133885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6753403f356cccec8b241fb1013f959d42ec199daa013aceee068bd42b22b41`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:01:08 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 15 Apr 2026 21:01:08 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 15 Apr 2026 21:01:08 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:01:08 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 15 Apr 2026 21:01:08 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Wed, 15 Apr 2026 21:01:08 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 15 Apr 2026 21:01:08 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 15 Apr 2026 21:01:08 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:01:08 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:01:51 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 15 Apr 2026 21:01:51 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec65e3baedeb98e0edf456e6b61caef43dfd6f34c4e0ad22592dfa3fc3237623`  
		Last Modified: Wed, 15 Apr 2026 21:04:16 GMT  
		Size: 130.1 MB (130073048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8264af5094f8505e07547e1088688aa3f47027524bb56c032639c7ac55bbbf06`  
		Last Modified: Wed, 15 Apr 2026 21:04:36 GMT  
		Size: 1.1 GB (1092327687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3579f1408698cd1f21a8e82edf3d52b7e19983d3143fc21cfa6c76ef64185f`  
		Last Modified: Wed, 15 Apr 2026 21:04:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:dcc03925f65d5e1c40c152c85af3c21ec7128f93a64a43e32b9d740096bca37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7894896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8451c81ab4e686ccd30ad84470fb89f202fd43c5dbc268ea6b136f4897fe510e`

```dockerfile
```

-	Layers:
	-	`sha256:6d2c238d617dad00c9d2a2b55c2203f5aecb4125fe582afd43c2fd39e5f6a745`  
		Last Modified: Wed, 15 Apr 2026 21:04:11 GMT  
		Size: 7.9 MB (7878109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db90c0fe952749de7fae50d05900678fd5bd62ceb489eb4e805aa62895b8002c`  
		Last Modified: Wed, 15 Apr 2026 21:04:11 GMT  
		Size: 16.8 KB (16787 bytes)  
		MIME: application/vnd.in-toto+json

### `swift:latest` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:d9682b0c9872d8c1d27afc3cab62795f62eab632b9ea954e32f5418c57a93a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1244917237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1666b5763cb8b9076b25dd33570bb3d75f778b6e23207b32e77503370784cc9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:40:15 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Tue, 07 Apr 2026 02:40:15 GMT
LABEL description=Docker Container for the Swift programming language
# Tue, 07 Apr 2026 02:40:15 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:40:15 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Tue, 07 Apr 2026 02:40:15 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Tue, 07 Apr 2026 02:40:15 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Tue, 07 Apr 2026 02:40:15 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Tue, 07 Apr 2026 02:40:15 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Apr 2026 02:40:15 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Tue, 07 Apr 2026 02:40:58 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Tue, 07 Apr 2026 02:40:58 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46b2096027145c990cd25b951ccf36c5c0fc697a687c5fb0e8ab5b0510f5df9`  
		Last Modified: Tue, 07 Apr 2026 02:43:11 GMT  
		Size: 129.6 MB (129647496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69788f1d601f323cd46a9785ef17181f1ee9ba60f112d35cd63749d5ccb2b10`  
		Last Modified: Tue, 07 Apr 2026 02:43:29 GMT  
		Size: 1.1 GB (1086395493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4f48a8acd5c204bc379f5f213150f5e9631102bc74ffd92765b88bba866117`  
		Last Modified: Tue, 07 Apr 2026 02:43:06 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:latest` - unknown; unknown

```console
$ docker pull swift@sha256:9827f9c3325f92ac68001e8a060a38b2d28a01a5f4b93834e18947ca74ee5081
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7917537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a872c2f54d58aabd5872007f982a058508bfa6db727e68edaa95af721bf69ff1`

```dockerfile
```

-	Layers:
	-	`sha256:d67f0c65cef0a2b781110ee0445991b6ec4209773479d9cc39b75e23e1a6678b`  
		Last Modified: Tue, 07 Apr 2026 02:43:06 GMT  
		Size: 7.9 MB (7900592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8dcf0aae2c5d4d8ef16a2caac3e5da7722f2ae4593c8ce0fe6fae5390e65df`  
		Last Modified: Tue, 07 Apr 2026 02:43:06 GMT  
		Size: 16.9 KB (16945 bytes)  
		MIME: application/vnd.in-toto+json
