## `swift:noble`

```console
$ docker pull swift@sha256:9949aac363e63fe96c44d08e3d00878fecbad7f50cb5450067c702012d6990e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `swift:noble` - linux; amd64

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

### `swift:noble` - unknown; unknown

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

### `swift:noble` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:2ff0db2ce993cd16cf512e5dff91c103986b6335c632a7085d5f8616cb5867a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 GB (1244410232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a347162bcd244b9384d34cdf60f7130f035da25a9fd28362740a85d1ad9272b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:11:28 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Wed, 15 Apr 2026 21:11:28 GMT
LABEL description=Docker Container for the Swift programming language
# Wed, 15 Apr 2026 21:11:28 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     unzip     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-13-dev     libpython3-dev     libsqlite3-0     libstdc++-13-dev     libxml2-dev     libncurses-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/* # buildkit
# Wed, 15 Apr 2026 21:11:28 GMT
ARG SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F
# Wed, 15 Apr 2026 21:11:28 GMT
ARG SWIFT_PLATFORM=ubuntu24.04
# Wed, 15 Apr 2026 21:11:28 GMT
ARG SWIFT_BRANCH=swift-6.3-release
# Wed, 15 Apr 2026 21:11:28 GMT
ARG SWIFT_VERSION=swift-6.3-RELEASE
# Wed, 15 Apr 2026 21:11:28 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:11:28 GMT
ENV SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Wed, 15 Apr 2026 21:12:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl # buildkit
# Wed, 15 Apr 2026 21:12:13 GMT
# ARGS: SWIFT_SIGNING_KEY=52BB7E3DE28A71BE22EC05FFEF80A866B47A981F SWIFT_PLATFORM=ubuntu24.04 SWIFT_BRANCH=swift-6.3-release SWIFT_VERSION=swift-6.3-RELEASE SWIFT_WEBROOT=https://download.swift.org
RUN swift --version # buildkit
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fadb1547d89964638f086119c9d00d7551a4e49038b449f60c05ca94cf4158`  
		Last Modified: Wed, 15 Apr 2026 21:14:34 GMT  
		Size: 129.1 MB (129138707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352d30d93ea76b047498567f8405748c50fa84349a6f0004928bfe924200696a`  
		Last Modified: Wed, 15 Apr 2026 21:14:58 GMT  
		Size: 1.1 GB (1086395568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317de55d677c142f8182ca0ab34be6392250ceea2c0484a6f363c86ad11ed975`  
		Last Modified: Wed, 15 Apr 2026 21:14:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `swift:noble` - unknown; unknown

```console
$ docker pull swift@sha256:020e8235a4fa064053e56b63449febd8f15e2f0e960289d743f36496cffcc1e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7917537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8088a99d4a267d04e2a4073a0e5220be6d693b05f9193d9ff8383b9b3f5062cc`

```dockerfile
```

-	Layers:
	-	`sha256:869b912fceb18b23f17190f3f1ebb5b53731126674207b3819db0568b4ed5069`  
		Last Modified: Wed, 15 Apr 2026 21:14:27 GMT  
		Size: 7.9 MB (7900592 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7b49e3b642d3c50bbd143e67529c6ca65b8a9618c0750ce064f55301266e46d`  
		Last Modified: Wed, 15 Apr 2026 21:14:26 GMT  
		Size: 16.9 KB (16945 bytes)  
		MIME: application/vnd.in-toto+json
