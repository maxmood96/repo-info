## `swift:focal`

```console
$ docker pull swift@sha256:a2174c5a2354ce36c697fcecfe1cd6e12dd19de918b9786f51e98faa9541fab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `swift:focal` - linux; amd64

```console
$ docker pull swift@sha256:9bb35e1e8351e41f7a722c559c43eb84226d9ee96e849d94e1b7a5c309e6dd04
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **674.2 MB (674199488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ab4cdbaf2b6581b69afb06fab14d13f91fa0849515ac3b14fbee9cf9aeb407`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:40 GMT
ADD file:1d3b09cf9e041d608a00c2dc25cdf3c388e436c5db607a3d124f2aa0f764fc69 in / 
# Fri, 18 Mar 2022 05:30:40 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 21:25:01 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 19 Mar 2022 21:25:01 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 19 Mar 2022 21:26:57 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Sat, 19 Mar 2022 21:26:58 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 19 Mar 2022 21:26:58 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Sat, 19 Mar 2022 21:26:58 GMT
ARG SWIFT_BRANCH=swift-5.6-release
# Sat, 19 Mar 2022 21:26:58 GMT
ARG SWIFT_VERSION=swift-5.6-RELEASE
# Sat, 19 Mar 2022 21:26:58 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 19 Mar 2022 21:26:59 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.6-release SWIFT_VERSION=swift-5.6-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 19 Mar 2022 21:27:47 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Sat, 19 Mar 2022 21:27:51 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:4d32b49e2995210e8937f0898327f196d3fcc52486f0be920e8b2d65f150a7ab`  
		Last Modified: Thu, 17 Mar 2022 11:55:39 GMT  
		Size: 28.6 MB (28565909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5d5ed404339546c2c2758dcb30d6c81884e7777249e56a88b1696b0a3dbc5b`  
		Last Modified: Sat, 19 Mar 2022 22:05:40 GMT  
		Size: 120.1 MB (120117618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218dda827083dea4410956ed20bb9628eafc69fb4497027ddefb4395da752c76`  
		Last Modified: Sat, 19 Mar 2022 22:06:34 GMT  
		Size: 525.5 MB (525515736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7aefe2fab09c4d12a3252afd9651ac8c64fac64209aa4029fd18acb247e54f`  
		Last Modified: Sat, 19 Mar 2022 22:05:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `swift:focal` - linux; arm64 variant v8

```console
$ docker pull swift@sha256:ed3f8a5b816b31be6825c0a4ba0113c283b99963889fb224d52880e85c3ebf75
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **639.7 MB (639719196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b657f1e5bf9d6ca2b14d1148c5d5939782652eca919ecea1fa4c06b2df0694`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:52 GMT
ADD file:39550cc6d55fc19ba68f94e7b3a21c3206bbd13264f26cf0a32ddd5ed0ad2782 in / 
# Fri, 18 Mar 2022 00:40:53 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 14:51:43 GMT
LABEL maintainer=Swift Infrastructure <swift-infrastructure@forums.swift.org>
# Sat, 19 Mar 2022 14:51:44 GMT
LABEL description=Docker Container for the Swift programming language
# Sat, 19 Mar 2022 14:54:13 GMT
RUN export DEBIAN_FRONTEND=noninteractive DEBCONF_NONINTERACTIVE_SEEN=true && apt-get -q update &&     apt-get -q install -y     binutils     git     gnupg2     libc6-dev     libcurl4-openssl-dev     libedit2     libgcc-9-dev     libpython3.8     libsqlite3-0     libstdc++-9-dev     libxml2-dev     libz3-dev     pkg-config     tzdata     zlib1g-dev     && rm -r /var/lib/apt/lists/*
# Sat, 19 Mar 2022 14:54:14 GMT
ARG SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561
# Sat, 19 Mar 2022 14:54:14 GMT
ARG SWIFT_PLATFORM=ubuntu20.04
# Sat, 19 Mar 2022 14:54:15 GMT
ARG SWIFT_BRANCH=swift-5.6-release
# Sat, 19 Mar 2022 14:54:16 GMT
ARG SWIFT_VERSION=swift-5.6-RELEASE
# Sat, 19 Mar 2022 14:54:17 GMT
ARG SWIFT_WEBROOT=https://download.swift.org
# Sat, 19 Mar 2022 14:54:18 GMT
ENV SWIFT_SIGNING_KEY=A62AE125BBBFBB96A6E042EC925CC1CCED3D1561 SWIFT_PLATFORM=ubuntu20.04 SWIFT_BRANCH=swift-5.6-release SWIFT_VERSION=swift-5.6-RELEASE SWIFT_WEBROOT=https://download.swift.org
# Sat, 19 Mar 2022 14:55:45 GMT
RUN set -e;     ARCH_NAME="$(dpkg --print-architecture)";     url=;     case "${ARCH_NAME##*-}" in         'amd64')             OS_ARCH_SUFFIX='';             ;;         'arm64')             OS_ARCH_SUFFIX='-aarch64';             ;;         *) echo >&2 "error: unsupported architecture: '$ARCH_NAME'"; exit 1 ;;     esac;     SWIFT_WEBDIR="$SWIFT_WEBROOT/$SWIFT_BRANCH/$(echo $SWIFT_PLATFORM | tr -d .)$OS_ARCH_SUFFIX"     && SWIFT_BIN_URL="$SWIFT_WEBDIR/$SWIFT_VERSION/$SWIFT_VERSION-$SWIFT_PLATFORM$OS_ARCH_SUFFIX.tar.gz"     && SWIFT_SIG_URL="$SWIFT_BIN_URL.sig"     && export DEBIAN_FRONTEND=noninteractive     && apt-get -q update && apt-get -q install -y curl && rm -rf /var/lib/apt/lists/*     && export GNUPGHOME="$(mktemp -d)"     && curl -fsSL "$SWIFT_BIN_URL" -o swift.tar.gz "$SWIFT_SIG_URL" -o swift.tar.gz.sig     && gpg --batch --quiet --keyserver keyserver.ubuntu.com --recv-keys "$SWIFT_SIGNING_KEY"     && gpg --batch --verify swift.tar.gz.sig swift.tar.gz     && tar -xzf swift.tar.gz --directory / --strip-components=1     && chmod -R o+r /usr/lib/swift     && rm -rf "$GNUPGHOME" swift.tar.gz.sig swift.tar.gz     && apt-get purge --auto-remove -y curl
# Sat, 19 Mar 2022 14:55:47 GMT
RUN swift --version
```

-	Layers:
	-	`sha256:57d0418fe9dcc5262d8c4fcb06c852ad2d0407b541c64d0f5f2e6ec01fd411ba`  
		Last Modified: Fri, 18 Mar 2022 00:42:36 GMT  
		Size: 27.2 MB (27169617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e85602af6b9b07c2428e384f0c0e66c487d4e2e5f2f26ea9908e2d29f1ed90`  
		Last Modified: Sat, 19 Mar 2022 15:00:26 GMT  
		Size: 116.8 MB (116792469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479c41d2ad6e64b039dd5b8584dfec72b5a01bd97605b2a85691e17db83543f0`  
		Last Modified: Sat, 19 Mar 2022 15:01:18 GMT  
		Size: 495.8 MB (495756906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07d28452570ce50f90dab3a1eced9782520e13521c360fa7cb38a1400a3a5a4e`  
		Last Modified: Sat, 19 Mar 2022 15:00:08 GMT  
		Size: 204.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
